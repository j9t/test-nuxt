<template>
  <div class="container">
    <Head>
      <Title>Contact</Title>
    </Head>
    <Navigation />
    <h1>Contact Us</h1>
    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="name">Name</label>
        <input type="text" id="name" v-model="form.name" required />
      </div>
      <div class="form-group">
        <label for="email">Email</label>
        <input type="email" id="email" v-model="form.email" required />
      </div>
      <div class="form-group">
        <label for="message">Message</label>
        <textarea id="message" v-model="form.message" required></textarea>
      </div>
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script>
import '~/pages/contact.css';

export default {
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: ''
      }
    };
  },
  methods: {
    async submitForm() {
      try {
        const response = await fetch('/api/contact', {
          method: 'POST',
          headers: {
            'Content-Type': 'application/json'
          },
          body: JSON.stringify(this.form)
        });
        if (response.ok) {
          alert('Message sent successfully!');
          this.form.name = '';
          this.form.email = '';
          this.form.message = '';
        } else {
          alert('Failed to send message.');
        }
      } catch (error) {
        alert('An error occurred.');
      }
    }
  }
};
</script>