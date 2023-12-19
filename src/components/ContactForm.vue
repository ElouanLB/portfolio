<template>
  <section class="contact-form">
    <h2>Contact</h2>
      <form ref="form" @submit.prevent="envoyerEmail">
        <label>Nom-Prénom</label>
        <input type="text" name="firstName" v-model="firstName">
        <label>Email</label>
        <input type="email" name="user_email" id="email_id" v-model="lastName">
        <label>Message</label>
        <textarea name="message" v-model="message"></textarea>
        <input class="send" type="submit" value="Envoyer">
      </form>
    </section>
  </template>
  

<script>
import emailjs from '@emailjs/browser';

export default {
  data() {
    return {
      firstName: '',
      lastName: '',
      message: '',
    };
  },
  methods: {
    envoyerEmail() {
      // Vérifiez si tous les champs sont remplis
      if (this.firstName === '' || this.lastName === '' || this.message === '') {
        alert('Veuillez remplir tous les champs du formulaire avant d\'envoyer le message.');
      } else {
        emailjs
          .sendForm(
            'service_6yavw7c',
            'template_eta70ee',
            this.$refs.form,
            'e5A4BElpNIED5w4XH'
          )
          .then(
            (result) => {
              alert('Message envoyé par email !', result.text);
            },
            (error) => {
              alert('Message non-envoyé par email.', error.text);
            }
          );
      }
    },
  },
};
</script>

<style scoped>
.contact-form {
  display: flex;
  justify-content: center;
  margin: 0;
  padding: 50px;
  box-sizing: border-box;
}

h2 {
  display: flex;
  padding-right: 200px;
  align-items: center;
}

form {
  display: flex;
  flex-direction: column;
  width: 300px;
  padding: 15px;
  border: 1px solid lightskyblue;
  border-radius: 5px;
}

input {
  margin: 5px 0px;
  height: 35px;
  padding: 7px;
}

textarea {
  width: 280px;
  height: 150px;
  resize: none;
}

.send {
  height: 35px;
  margin: 5px 0px;
  background-color: skyblue;
  border: none;
  border-radius: 5px;
  color: #333;
}

.send:hover {
  background-color: black;
  color: lightskyblue;
}
</style>