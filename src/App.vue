<template>
  <Header @close="closeButton"/>
  <Article :names="names"/>
  <Footer/>
  <h5 v-if="isTrue">I have got a happy family!</h5>
  <button @click="openButton">Open</button>
</template>

<script>
import Header from "./components/HeaderComponent.vue";
import Article from "./components/ArticleComponent.vue";
import Footer from "./components/FooterComponent.vue";
export default {
  name: "App",
  components: {
    Header,
    Article,
    Footer
  } ,
  data (){
    return{
      names:['Shohruh', 'Ismoil', 'Nazarbek', 'Faxriddin'],
      isTrue:false
    }
  },
  methods:{
    openButton(){
      this.isTrue = true
    },
    closeButton(){
      this.isTrue = false
    }
  }
}
</script>

<style scoped>
h5{
  font-size: 40px;
}

</style>
