<template>
  <div class="cart">
    <h1>when they always say "yeehaw" but never ask "haw yee" :(</h1>
    <p>so sad, heart broken</p>
    <input type="text" placeholder="type sumn :D" v-model="message" />
    <p>{{ message }}</p>
    <input type="checkbox" id="dog" value="dog" V-model="checkedNames" />
    <label for="dog">dog</label>
    <input type="checkbox" id="cat" value="cat" V-model="checkedNames" />
    <label for="cat">cat</label>
    <input type="checkbox" id="bird" value="bird" v-model="checkedNames" />
    <label for="bird">bird</label>
    <br />
    <span>Checked names: {{ check }}</span>
  </div>
</template>

<script>
export default {
  name: "Home",
  components: {},
  data() {
    return {
      message: "",
      check: [],
    };
  },
};
</script>
<style>