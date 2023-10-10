<template>
  <form ref="form" @submit.prevent="sendEmail">
    <div class="name-input">
      <div class="field">
        <label class="sans">Name</label>
        <input required class="input" type="text" name="user_name" />
      </div>
      <div class="field">
        <label class="sans">Email</label>
        <input required class="input" type="email" name="user_email" />
      </div>
    </div>
    <div class="field">
      <label class="sans">Message</label>
      <textarea class="input" name="message"></textarea>
    </div>
    <input required class="btn" type="submit" value="SHOOOOOT" />
  </form>
</template>
  
  <script>
import emailjs from "@emailjs/browser";

export default {
  methods: {
    sendEmail() {
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

    outline: 0
    border: 0

    cursor: pointer
    overflow: hidden

    transition: 0.3s
</style>