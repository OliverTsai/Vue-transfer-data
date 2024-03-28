<template>
  <div>
    <input type="text" v-model="text" />
    <button @click="$emit('viewText', text)">發送</button>
    <p>View</p>
  </div>
</template>

<script>
export default {
  name: 'app-View',
  emits: ['viewText'],
  data() {
    return {
      text: '',
    };
  },
};
</script>
