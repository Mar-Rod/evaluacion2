<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h3>Daniela Heredia Tolumes</h3>
    <br>
    <p>Perdon profe no pude acabar, esta semana tuve algunos problemas y no he tenido tiempo de ponerme al día con las clases, pero por lo menos añadi alo con lo que me pueda calificar.</p>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
  color: rgb(244, 189, 233);
}

h3 {
  font-size: 1.7rem;
  color: bisque;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
