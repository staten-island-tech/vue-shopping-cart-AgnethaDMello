<template>
  <div class="home">
    <HelloWorld msg="cart for shopping" />
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
};
</script>
<style>
h1 {
  color: rgb(0, 98, 255);
}
</style>