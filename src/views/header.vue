<template>
    <header>
        <h1> FASHION MIRAI</h1>
            <nav>
                <ul>
                    <il><router-link to="/">Home</router-link></il>
                    <il><router-link to="/panier">Panier</router-link></il>
                    <il><router-link to="/about">About us</router-link></il>
                    
                </ul>
            </nav>
    </header>
    <router-view/>
</template>

<script>
  export default {
      name: 'Header',
  data () {
      return {

    }

  }
}
</script>

<style scoped>
    header {
        background-color: #F2D2BD;
        padding: 10px;
    }
  h1 {
    font-family:'Times New Roman', Times, serif;
    text-align: center;
    color:black;
  }
    .navbar {
        display: flex;
        align-items: center;
    }

    nav {
        flex: 1;
        text-align: right;
    }

        nav ul il {
            display: inline-block;
            padding: 10px;
        }
</style>


