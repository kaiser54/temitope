<template>
  <form ref="form" @submit.prevent="sendEmail">
    <div class="name-input">
      <div class="field" :class="{ 'has-error': nameError }">
        <label class="sans">Name</label>
        <input
          required
          class="input"
          type="text"
          name="user_name"
          v-model="name"
        />
        <span class="error-message" v-if="nameError">
          <span class="material-symbols-sharp"> error </span>
          {{ nameError }}
        </span>
      </div>
      <div class="field" :class="{ 'has-error': emailError }">
        <label class="sans">Email</label>
        <input
          required
          class="input"
          type="email"
          name="user_email"
          v-model="email"
        />
        <span class="error-message" v-if="emailError">
          <span class="material-symbols-sharp"> error </span>
          {{ emailError }}
        </span>
      </div>
    </div>
    <div class="field" :class="{ 'has-error': messageError }">
      <label class="sans">Message</label>
      <textarea class="input" name="message" v-model="message"></textarea>
      <span class="error-message" v-if="messageError">
        <span class="material-symbols-sharp"> error </span>
        {{ messageError }}
      </span>
    </div>
    <input required class="btn" type="submit" value="SHOOOOOT" />
  </form>
</template>

<script>
import emailjs from "@emailjs/browser";

export default {
  data() {
    return {
      name: "",
      email: "",
      message: "",
      nameError: "",
      emailError: "",
      messageError: "",
    };
  },
  methods: {
    sendEmail() {
      // Validation
      this.nameError = !this.name ? "Name is required." : "";
      this.emailError = !this.email ? "Email is required." : "";
      this.messageError = !this.message ? "Message is required." : "";

      if (!this.name || !this.email || !this.message) {
        return; // Stop submission if there are errors
      }

      emailjs
        .sendForm(
          "service_r1w6gfe",
          "template_bzjs34g",
          this.$refs.form,
          "hVEBAMgTltF486Eor"
        )
        .then(
          (result) => {
            console.log("SUCCESS!", result);
          },
          (error) => {
            console.log("FAILED...", error);
          }
        );
    },
  },
  watch: {
    name() {
      this.nameError = "";
    },
    email() {
      this.emailError = "";
    },
    message() {
      this.messageError = "";
    },
  },
};
</script>


<style lang="sass" scoped>
form
  display: flex
  flex-direction: column
  gap: 32px
  width: 100%
.name-input
  display: flex
  gap: 32px
  width: 100%
.sans
  font-family: "DM Sans"

label
  color: white
textarea
  padding: 10px
  width: 100%
  height: 150px
  resize: none
.btn
  display: flex
  flex-direction: row
  justify-content: center
  align-items: center

  border-radius: 10px

  width: 100%
  padding: 10px
  color: black !important
  outline: 0
  border: 0

  cursor: pointer
  overflow: hidden

  transition: 0.3s

.error-message,
.material-symbols-sharp
  display: flex
  align-items: center
  color: red
  font-weight: 100
input
  color: white
</style>