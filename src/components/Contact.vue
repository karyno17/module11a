<template>
  <div>
    <h1>Contact Information</h1>
    <p>Name: Karyn O'Neill</p>
    <p>Email: kaoneill@my.waketech.edu</p>
    <GoBackButton />
  </div>
</template>

<script>
import GoBackButton from './GoBackButton.vue'

export default {
  name: 'ContactPage',
  components: {
    GoBackButton
  }
}

</script>

<style scoped>
.about-container {
  background-color: #2e003e; /* Dark purple background */
  color: #f0e6ff; /* Light text for contrast */
  padding: 20px;
  border-radius: 10px;
  width: 80%;
  margin: 0 auto;
  max-width: 600px;
  text-align: center;
}

h1 {
  color: #d8b4f8; /* Soft lavender for the heading */
  font-size: 2rem;
}

p {
  font-size: 1.2rem;
  margin: 10px 0;
}

button {
  margin-top: 20px;
  padding: 10px 20px;
  background-color: #d8b4f8;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #f0e6ff;
  color: #2e003e;
}
</style>
