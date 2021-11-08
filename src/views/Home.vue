<template>
  <div class="home">
    <Header></Header>
       
    <div class=container>
       <Products v-for="article of articles" :key="article.id" :article="article" 
       v-on:view-article="viewArticle($event)"/>
    </div>

    <Footer></Footer>
  </div>
</template>

<script>
// @ is an alias to /src
import articles  from "../data/Articles.js"
import Header from './header.vue'
import Footer from './footer.vue'
import Products from './products.vue'

export default {
  name: 'Home',
  components: {
    Header,
    Footer,
    Products
  },
  data () {
    return {
      articles: articles,
      article: null
    }
  },
  methods:{
   viewArticle(article) {
     this.article = article
     console.log(this.article)
   }
  }
}
</script>

<style>
    .home{
      margin: auto;
    }
    .container{
      
    }

    img {
        width: 60%;
        height: 60%;
        cursor: pointer;
    }

    #div1 {
        padding: 0;
        justify-content: space-between;
    }
    
    </style>
