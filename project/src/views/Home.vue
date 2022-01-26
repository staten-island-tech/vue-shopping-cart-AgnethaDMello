<template>
  <div class="home">
    <HelloWorld msg="cart for shopping" />
    <p v-if="alive">{{ pet }}</p>
    <p v-else>rest in pieces</p>
    <ul>
      <li c-for="feature in features" :key="feature"></li>
    </ul>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
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
};
</script>
<style>
h1 {
  color: rgb(0, 98, 255);
}
</style>