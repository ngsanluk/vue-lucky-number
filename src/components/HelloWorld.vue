<template>
  <div class="hello">
    <h2>{{ msg }}</h2>
    <h1 class="luckyNumber">
      {{ luckyNumber == 0 ? "?" : luckyNumber }}
    </h1>
    <button v-on:click="play">Play</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {luckyNumber: 0}
  },
  props: {
    msg: String
  },
  methods: {
    play: function() {
      console.log("play() function called");
      var luckyNumber = Math.floor((Math.random() * 100) + 1);
      this.luckyNumber = luckyNumber;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.luckyNumber {
  font-size: 800%;
  color: #CC0000;
}
</style>
