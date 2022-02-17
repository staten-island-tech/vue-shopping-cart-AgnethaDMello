<template>
  <div v-bind:class="id">
    <h2>{{ title }}</h2>
    <img v-bind:src="image" class="image" alt="" />
    <p>${{ price }}</p>
    <button @click="add(index)">Add to Cart!</button>
    <button @click="remove(index)">Remove from Cart!</button>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    title: String,
    price: Number,
    image: String,
    id: Number,
    index: Number,
    add: Function,
    remove: Function,
  },
};
</script>
