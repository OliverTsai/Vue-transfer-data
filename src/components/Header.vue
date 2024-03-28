<template>
  <h1>Hello Component</h1>
  <p>{{ myname }}</p>
</template>

<script>
export default {
  name: 'App-header',
  props: {
    myname: {
      type: String,
      default: 'Allen', // 這個將會是 myname 的默認值，如果沒有從父組件傳入值的話
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
