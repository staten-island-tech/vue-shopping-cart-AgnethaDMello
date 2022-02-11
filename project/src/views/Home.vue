<template>
  <div class="home">
    <h2>{{ now }}</h2>
    <HelloWorld msg="cart for shopping" />
    <p v-if="alive">{{ pet }}</p>
    <p v-else>rest in pieces</p>
    <ul>
      <li v-for="feature in features" :key="feature">{{ feature }}</li>
    </ul>
    <Card
      class="card"
      title="oo la la"
      description="hehe"
      image="https://bit.ly/3uFl6K5"
    />
    <Card
      class="card"
      title="00 la la"
      description="haha"
      image="https://bit.ly/3uKF5qU"
    />
    <Card
      class="card"
      title="oo l@ l@"
      description="hoho"
      image="https://bit.ly/3HMNRIi"
    />
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
  background-color: rgb(79, 146, 197);
}
.image {
  width: 3rem;
  height: 3rem;
}
</style>