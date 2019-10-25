<template>
  <div id="main">
    <header class="bg-primary">
      <h1 class="text-white text-center p-3">Cat card app</h1>
    </header>
    <section class="container">
      <h2>Cat card list</h2>
      <hr />
      <div class="card-group">
        <card-view 
          v-for="cat in cardList"
          :item="cat"
          :key="cat.id"
          :catUrl="cat.imageUrl"
          :catName="cat.title"
          :catDescription="cat.description"/>
      </div>
      <button class="btn btn-lg btn-danger circle add"><i class="fas fa-plus"></i></button>
    </section>
    <Footer :year="currentY" universityName="Lille" footerMessage="No cat has been hurt during the development of this app."/>
  </div>
</template>

<script>
  import Footer from './components/Footer.vue'
  import CardView from './components/CardView.vue'
  import { getAllCards } from "@/data-service";

  export default {
    name: 'app',
    components: {
      Footer,
      CardView
    },
    data: () => ({
      currentY : (new Date()).getFullYear(),   
      cardList : []
    }),
    created : () => {
      getAllCards().then(cards => {
        this.cardList = cards;
      })
    }
  }
</script>

<style src=".//css/main.css"></style>
