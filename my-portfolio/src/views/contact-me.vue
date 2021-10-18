<template>
  <div
    style=" background-image:linear-gradient(to right, #e6e6fa, white); height:100vh"
  >
    <section>
      <v-row style="width:100%; height:100%" class="mx-auto">
        <v-snackbar
          :timeout="5000"
          style=" text-align:center"
          class="mt-10"
          :value="true"
          center
          elevation="0"
          top
          v-model="snackbar"
          color="#FDF5E6"
        >
          <h4 class="mt-4" style="color:black; text-align:center">
            Email Sent!
          </h4>
        </v-snackbar>
        <v-card
          style="width:60%; height:65%; margin-top:150px; background-image: linear-gradient(to right, #e6e6fa, white); box-shadow: 12px 12px 2px 1px rgba(0, 0, 255, .2); border-radius:30px"
          class="mx-auto card"
        >
          <v-card-title style=" width:100%; height:20%; justify-content:center">
            <h2 class="mt-5" style="text-align:center">Contact Me</h2>
          </v-card-title>

          <v-card-text style="width:80%" class="mx-auto card-text">
            <form @submit.prevent="sendEmail">
              <v-text-field
                v-model="name"
                :error-messages="nameErrors"
                label="Name"
                name="name"
                required
                solo
                elevation="0"
                @input="$v.name.$touch()"
                @blur="$v.name.$touch()"
              ></v-text-field>
              <v-text-field
                v-model="email"
                :error-messages="emailErrors"
                label="E-mail"
                name="email"
                required
                solo
                elevation="0"
                @input="$v.email.$touch()"
                @blur="$v.email.$touch()"
              ></v-text-field>
              <v-textarea
                v-model="message"
                :error-messages="messageErrors"
                label="Message"
                maxlength="500"
                full-width
                counter
                name="message"
                single-line
                required
                solo
                elevation="0"
                @input="$v.message.$touch()"
                @blur="$v.message.$touch()"
              ></v-textarea>

              <v-row class="mx-auto " style=" width:50%">
                <v-btn
                  :disabled="!isValid"
                  rounded
                  style="background:	#C71585"
                  class="mx-auto mt-2 mb-2 "
                  @click="sendEmail"
                >
                  <input type="submit" value="Send" />
                </v-btn>
              </v-row>
            </form>
          </v-card-text>
        </v-card>
      </v-row>
    </section>

    <section class="footer" style="height:10vh"></section>
  </div>
</template>
<script>
import { validationMixin } from 'vuelidate'
import { required, maxLength, email, minLength } from 'vuelidate/lib/validators'
import emailjs from 'emailjs-com'

export default {
  name: 'Contact-Me',
  mixins: [validationMixin],

  validations: {
    name: { required, minLength: minLength(5), maxLength: maxLength(25) },
    email: { required, email },
    message: { required, minLength: minLength(20) },
  },

  data: () => ({
    name: '',
    email: '',
    message: '',
    snackbar: false,
    isValid: false,
  }),

  computed: {
    nameErrors() {
      const errors = []
      if (!this.$v.name.$dirty) return errors
      !this.$v.name.maxLength &&
        errors.push('Name must be at most 25 characters long')
      !this.$v.name.minLength &&
        errors.push('Name must be at least 5 characters long')
      !this.$v.name.required && errors.push('Name is required.')
      return errors
    },
    emailErrors() {
      const errors = []
      if (!this.$v.email.$dirty) return errors
      !this.$v.email.email && errors.push('Must be valid e-mail')
      !this.$v.email.required && errors.push('E-mail is required')
      return errors
    },
    messageErrors() {
      const errors = []
      if (!this.$v.name.$dirty) return errors
      !this.$v.name.minLength &&
        errors.push('Message must be at least 20 characters long')
      !this.$v.name.required && errors.push('Message is required.')
      return errors
    },
  },

  methods: {
    clear() {
      this.$v.$reset()
      this.name = ''
      this.email = ''
      this.message = ''
    },
    sendEmail(e) {
      try {
        emailjs
          .sendForm(
            process.env.VUE_APP_SERVICE_ID,
            process.env.VUE_APP_TEMPLATE_ID,
            e.target,
            process.env.VUE_APP_USER_ID,
            {
              name: this.name,
              email: this.email,
              message: this.message,
            },
          )
          .then(() => {
            this.name = ''
            this.email = ''
            this.message = ''
            this.snackbar = true
          })
      } catch (error) {
        throw new Error(error)
      }
    },
  },
}
</script>
<style scoped>
/* phones */
@media screen and (max-device-width: 640px) {
  .card,
  .card-text {
    width: 95% !important;
  }
}
</style>
