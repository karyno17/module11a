<template>
  <div>
    <h1>Here are Some Random Facts</h1>
    <button @click="getJoke">Tell Me a Joke!</button>
    <p v-if="joke">{{ joke }}</p>
    <p v-else>Click the button to get a joke!</p>
    <GoBackButton />
  </div>
</template>

<script>
import GoBackButton from './GoBackButton.vue'

export default {
  name: 'RandomFacts',
  data() {
    return {
      joke: ''
    }
  },
  methods: {
    async getJoke() {
      try {
        const response = await fetch('https://jokes-by-api-ninjas.p.rapidapi.com/v1/jokes', {
          method: 'GET',
          headers: {
            'X-RapidAPI-Key': 'def8a62c73msh4fd32cc4ffe9745p1c60ffjsn7b6eaad8e540', // 🔐 replace with your real key
            'X-RapidAPI-Host': 'jokes-by-api-ninjas.p.rapidapi.com'
          }
        })
        const data = await response.json()
        this.joke = data[0].joke
      } catch (error) {
        this.joke = 'Oops! No joke for now...'
        console.error(error)
      }
    }
  },
  components: {
    GoBackButton
  }
}
</script>
