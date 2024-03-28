<template>
<button @click="show('tab1')">Input</button>
<button @click="show('tab2')">View</button>
<button @click="show('tab3')">Header</button>

<Input v-if="tab === 'tab1'" v-model="name" />
<p v-if="tab === 'tab1'">{{ name }}</p>
<View v-if="tab === 'tab2'" @viewText="getViewText" />
<p v-if="tab === 'tab2'">{{ text }}</p>
<Header v-if="tab === 'tab3'" myname="Jahn" />
</template>

<script>
import Input from './components/Input.vue';
import View from './components/View.vue';
import Header from './components/Header.vue';


export default {
name: 'App',
components: {
  Input,
  View,
  Header,
},
data() {
  return {
    name: '',
    tab: 'tab1',
    text: '',
  };
},
methods: {
  show(index) {
    this.tab = index;
  },
  getViewText(text) {
    this.text = text;
  }
},
};
</script>

<style>
#app {
font-family: Avenir, Helvetica, Arial, sans-serif;
-webkit-font-smoothing: antialiased;
-moz-osx-font-smoothing: grayscale;
text-align: center;
color: #2c3e50;
margin-top: 90px;
}
</style>
