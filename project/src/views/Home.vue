<template>
  <div class="home">
    <h2>{{ now }}</h2>
    <HelloWorld msg="cart for shopping" />
    <p v-if="alive">{{ pet }}</p>
    <p v-else>rest in pieces</p>
    <ul>
      <li v-for="feature in features" :key="feature">{{ feature }}</li>
    </ul>
    <Card class="card" title="oo la la" />
    <Card class="card" title="00 la la" />
    <Card class="card" title="oo l@ l@" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import Card from "@/components/Card.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
    Card,
  },
  data() {
    return {
      pet: "rogi the dogi",
      alive: true,
      features: [
        "white fur",
        "golden brown features",
        "black whiskers/eyelashes",
        "white whiskers/eyelashes",
      ],
    };
  },
  computed: {
    now: function () {
      const time = new Date();
      return `${time.getHours()}:${time.getMinutes()}`;
    },
  },
};
</script>
<style>
h1 {
  color: rgb(0, 98, 255);
}
.card {
  width: 10rem;
  height: 10rem;
  background-color: magenta;
}
</style>