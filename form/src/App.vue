<script setup>
  import { ref } from 'vue'

  const text = ref('Your Name')
  const checked = ref(true)
  const checkedNames = ref(['Emma'])
  const picked = ref('One')
  const selected = ref('A')
  const multiSelected = ref(['A'])
</script>

<template>
   <h2>Text Input</h2>
  <input v-model="text"> {{ text }}

  <h2>Checkbox</h2>
  <input type="checkbox" id="checkbox" v-model="checked">
  <label for="checkbox">Checked: {{ checked }}</label>

  
  <h2>Multi Checkbox</h2>
  <input type="checkbox" id="Emma" value="Emma" v-model="checkedNames">
  <label for="Emma">Emma</label>
  <input type="checkbox" id="Eliora" value="Eliora" v-model="checkedNames">
  <label for="Eliora">Eliora</label>
  <input type="checkbox" id="Eliakim" value="Eliakim" v-model="checkedNames">
  <label for="Eliakim">Eliakim</label>
  <p>Checked names: <pre>{{ checkedNames }}</pre></p>

  <h2>Radio</h2>
  <input type="radio" id="one" value="One" v-model="picked">
  <label for="one">One</label>
  <br>
  <input type="radio" id="two" value="Two" v-model="picked">
  <label for="two">Two</label>
  <br>
  <span>Picked: {{ picked }}</span>

  <h2>Select</h2>
  <select v-model="selected">
    <option disabled value="">Please select one</option>
    <option>A</option>
    <option>B</option>
    <option>C</option>
  </select>
  <span>Selected: {{ selected }}</span>

</template>

<style scoped>
header {
  
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
