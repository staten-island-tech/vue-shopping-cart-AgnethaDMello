<template>
  <div v-bind:id="id">
    <h2>{{ title }}</h2>
    <img v-bind:src="image" class="image" alt="" />
    <p>${{ price }}</p>
    <button @click="$emit('add-click')">Add to Cart!</button>
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
  },
  /*   data() {
    return {
      total: null,
      cart: [],
    };
  },
   methods: {
    caart: function () {
      this.total += this.price;
      document.querySelector("#totalprice").textContent = this.total;
      document
        .querySelector(".list")
        .insertAdjacentHTML(
          `afterbegin`,
          `<p class="yo">${this.title}  ~  $${this.price}</p>`
        );
    },
  }, */
};
</script>
