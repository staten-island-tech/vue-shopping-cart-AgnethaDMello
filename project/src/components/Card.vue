<template>
  <div>
    <h2>{{ title }}</h2>
    <img v-bind:src="image" class="image" alt="" />
    <p>${{ price }}</p>
    <p>{{ index }}</p>
    <button>Add to Cart!</button>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    title: String,
    price: Number,
    image: String,
  },
};
</script>
