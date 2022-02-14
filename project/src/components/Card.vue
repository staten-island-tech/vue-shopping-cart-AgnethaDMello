<template>
  <div v-bind:id="id">
    <h2>{{ title }}</h2>
    <img v-bind:src="image" class="image" alt="" />
    <p>${{ price }}</p>
    <div>
      <button v-on:click="caart">Add to Cart!</button>
      <button class="remove" v-on:click="nocaart">Remove!</button>
    </div>
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
  data() {
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
        .querySelector(".arts")
        .insertAdjacentHTML(
          `afterbegin`,
          `<p class="yo">${this.title}  ~  $${this.price}</p>`
        );
    },
    nocaart: function () {
      const el = document.querySelector(".yo");
      el.remove();
      this.total -= this.price;
      document.querySelector("#totalprice").textContent = this.total;
    },
  },
};
</script>
