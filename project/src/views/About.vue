<template>
  <div class="cart">
    <h1>when they always say "yeehaw" but never ask "haw yee" :(</h1>
    <p>so sad, heart broken</p>
    <input type="text" placeholder="type sumn :D" v-model="message" />
    <p>{{ message }}</p>
    <input type="checkbox" id="dog" value="dog" v-model="check" />
    <label for="dog">dog</label>
    <input type="checkbox" id="cat" value="cat" v-model="check" />
    <label for="cat">cat</label>
    <input type="checkbox" id="bird" value="bird" v-model="check" />
    <label for="bird">bird</label>
    <br />
    <span>Checked Animals: {{ check }}</span>
    <div>
      <select v-model="selected">
        <option>annie</option>
        <option>yinglin</option>
        <option>iris</option>
        <option>elizabeth</option>
      </select>
      <span>{{ selected }}</span>
    </div>
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
      selected: "",
    };
  },
};
</script>
<style>