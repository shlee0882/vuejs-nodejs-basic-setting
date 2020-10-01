<template>
  <div class="hello">
    <h1>{{ name }}</h1>
    <h1>{{ age }}</h1>
    <h1>{{ livingArea }}</h1>
    <button v-on:click="changeAddress">자식에서 부모로 주소변경</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    name: String,
    age: Number,
    livingArea: String,
  },
  methods: {
    changeAddress() {
      const newAddress = '강원도 속초시';
      this.$emit('change-address', newAddress);
    },
  },
};
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
</style>
