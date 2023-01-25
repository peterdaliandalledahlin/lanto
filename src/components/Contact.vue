<template>
    <v-container id="contact">
        <v-form
          ref="form"
          v-model="valid"
          lazy-validation
        >
          <v-text-field
            aria-label="namn"
            v-model="name"
            :counter="20"
            :rules="nameRules"
            label="Namn"
            name="namn"
            required
          ></v-text-field>
      
          <v-text-field
            aria-label="epost"
            v-model="email"
            :rules="emailRules"
            label="E-post"
            name="email"
            required
          ></v-text-field>

          <v-text-field
            aria-label="telfonnummer"
            v-model="phone"
            label="Telefonnummer"
            name="phone"
          ></v-text-field>
      
          <v-select
            aria-label="välj ett ärende"
            v-model="select"
            :items="items"
            :rules="[v => !!v || 'Ni måste välja ett ämne']"
            label="Välj ett ärende"
            name="select"
            required
          ></v-select>
      
          <!-- <v-checkbox
            v-model="checkbox"
            :rules="[v => !!v || 'Du måste godkänna villkoren för att kunna fortsätta!']"
            label="Godkänn villkoren?"
            required
          ></v-checkbox> -->
      
          <v-btn
            aria-label="skicka förfrågan från formulär"
            :disabled="!valid"
            color="#D7B46A"
            class="mr-4"
            type="submit"
            @click.prevent="submit"
          >
          <v-progress-circular
            aria-label="spinner"
            v-if="spinner"
            indeterminate
            color="#D7B46A"
          ></v-progress-circular>
            Skicka
          </v-btn>
      
          <v-btn
          aria-label="rensa formuläret"
            variant="outlined"
            color="#D7B46A"
            class="mr-4"
            @click="reset"
          >
            Rensa formuläret
          </v-btn>

        </v-form>
        <v-snackbar
      v-model="snackbar"
    >
      {{ text }}

      <template v-slot:actions>
        <v-btn
          aria-label="stäng popup meddelande"
          color="pink"
          variant="text"
          @click="snackbar = false"
        >
          Stäng
        </v-btn>
      </template>
    </v-snackbar>
    </v-container>
</template>


<script>
import axios from 'axios'
export default {
  data: () => ({
    spinner: false,
    valid: true,
    name: '',
    nameRules: [
      v => !!v || 'Name is required',
      v => (v && v.length <= 20) || 'Name must be less than 20 characters',
    ],
    email: '',
    emailRules: [
      v => !!v || 'E-mail is required',
      v => /.+@.+\..+/.test(v) || 'Ange en giltig e-postadress',
    ],
    phone: '',
    select: null,
    items: [
      'Boka ett möte',
      'Kostnadsförslag',
      'Rådgivning',
      'Jag vill bli kontaktad',
    ],
    checkbox: false,
    snackbar: false,
    text: `Meddelandet är skickat!`,
  }),

  methods: {
    submit () {
      this.spinner = true
      this.$refs.form.validate()
      axios.defaults.headers.post['Content-Type'] = 'application/json';
      axios.post('https://formsubmit.co/ajax/info@kok-bygg.se', {
          name: this.name,
          email: this.email,
          phone: this.phone,
          select: this.select
      })
      .then((response) => {
          console.log(response)
          if(response.status === 200){
            this.snackbar = true
            this.$refs.form.reset()
            this.checkbox = false
            this.spinner = false
          }
      })
      .catch(error => console.log(error));
    },
    reset () {
        this.$refs.form.reset()
      },
    resetValidation () {
      this.$refs.form.resetValidation()
    },
  },
}
</script>

<style scoped>
button:disabled {
  cursor: not-allowed;
  pointer-events: all !important;
}
</style>