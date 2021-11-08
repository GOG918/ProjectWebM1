<template>

    <div class="li" >
       <h3> {{article.name}}</h3>
       <p class="price"> {{article.price.toFixed(2)}}</p>
      <div><img v-bind:src=article.picture1 alt="picture" /></div>
      <button class="article-btn" @click="$emit('view-article',article)">view</button>
    </div>

</template>

<script>
export default {
  name: 'Products',
  props: ['article']
}
</script>

<style lang="scss">
.li {
        margin: 20px;
        padding: 20px;
        width: 400px;
        height: 400px;
        border-radius: 5px;
        display: inline-block;
      justify-content: space-between;
        button {
          padding: 10px;
      cursor: pointer;
      font-weight :bold;
      font-size: 1.15rem;
      background-color:#ebc8b2;
      color:black;
      margin: 20px;
    }
    }
</style>
