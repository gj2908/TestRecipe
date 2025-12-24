<script setup>
import Footer from './components/Footer.vue'
import Header from './components/Header.vue'
import RecipeCard from './components/RecipeCard.vue'
import recipes from './assets/data.js'
</script>

<template>

<Header/>
<section id="banner">
  <p>🚨 <strong>NEW RECIPE:</strong> Triple Chocolate Chip Cookies! 🚨</p>
</section>
<main>

<RecipeCard v-for="recipe in recipes" :recipe/>
  
</main>
<Footer/>
</template>

<style scoped>





/* BANNER STYLES */
#banner{
  width:100%;
  background:#ffe97b;
  padding:10px;
  text-align:center;
}
/* ----------------- */



/* BUTTON STYLES */
button{
  cursor:pointer;
  background: #D17862;
  color:white;
  font-weight:bold;
  border: 0;
  border-radius:5px;
  padding:5px 15px;
  font-size:1rem;
  transition: transform 0.2s;
  margin: 10px 0;
}
button:hover{
  transform:scale(1.05);
}
/* ----------------- */



/* RECIPE LIST STYLES */
main{
  padding:10px;
  display:grid;
  grid-template-columns: 1fr;
  gap:10px;
  background:white;
}

@media (min-width:414px){
  main{
    grid-template-columns: 1fr 1fr;
  }
}

@media (min-width:768px){
  main{
    grid-template-columns: 1fr 1fr 1fr;
  }
}

@media (min-width:1200px){
  main{
    grid-template-columns: 1fr 1fr 1fr 1fr;
  }
}
/* ----------------- */

</style>
