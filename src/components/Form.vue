<template>
  <div class="container my-3 py-4 d-flex justify-content-center" id="form">
    <div>
      <div v-if="result.type != 'alert-success'">
        <h3 class="text-red mb-4">Зарегистрируйтесь на вебинар</h3>
        <form @submit.prevent="sendForm">
          <div class="form-group text-center">
            <input
              id="name"
              v-model="name"
              :class="{'is-invalid': $v.name.$dirty && !$v.name.required}"
              class="form-control mb-3"
              type="text"
              placeholder="Ваше имя"
            />
            <input
              id="email"
              v-model="email"
              :class="{
                'is-invalid':
                  ($v.email.$dirty && !$v.email.required) ||
                  ($v.email.$dirty && !$v.email.email)
              }"
              class="form-control mb-3"
              type="text"
              placeholder="Email"
            />
            <input
              v-mask="'+7 (###) ###-##-##'"
              v-model="phone"
              class="form-control mb-3"
              type="text"
              placeholder="Телефон"
            />
            <button class="btn btn-lg btn-red my-4" type="submit">
              Зарегистрироваться
            </button>
          </div>
        </form>
      </div>
      <div
        class="alert"
        v-if="result.type === ('alert-success' || 'alert-danger')"
        :class="result.type"
      >
        {{ result.message }}
      </div>
    </div>
  </div>
</template>

<script>
  import {email, required} from 'vuelidate/lib/validators'
  import {mask} from 'vue-the-mask'
  import axios from 'axios'
  export default {
    name: 'Form',
    directives: {mask},
    data: () => ({
      email: '',
      phone: '',
      name: '',
      result: ''
    }),
    validations: {
      email: {email, required},
      name: {required}
    },
    methods: {
      sendForm() {
        if (this.$v.$invalid) {
          this.$v.$touch()
          return
        }
        try {
          axios
            .post('https://api.bblk.ga/feedback/aurora', {
              name: this.name,
              email: this.email,
              phone: this.phone
            })
            .then((result) => (this.result = result.data))
          axios
            .post('https://mail.bblk.ga/aurora/landing', {
              email: this.email
            })
            .then((result) => console.log(result))
        } catch (err) {
          console.log(err)
        }
      }
    }
  }
</script>

<style scoped></style>
