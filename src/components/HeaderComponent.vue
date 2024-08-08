<template>
  <h1>Header Component</h1>
  <button @click="closeButton">Close</button>
</template>

<script>
export default {
  components: {
  },
  name: "Header",
  data(){
    return{
      title:'Header Component'
    }
  },
  methods:{
    closeButton(){
      this.$emit('close');
    }
  }
}
</script>


<style scoped>
  h1{
    color: blue;
  }
</style>