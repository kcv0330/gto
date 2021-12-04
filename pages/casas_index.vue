<script>
  export default {
    async asyncData({ $content }) {
      const houses = await $content('character-predictions').fetch()
      return {
        houses
      }
    }
  }
</script>

<template>
  <div class="container">
   <HeaderView />
   <h3 style="margin-top: 15px">Fortalezas de Games of Thrones</h3>
     <p>Descubre cuáles son las mejores locaciones de grabación de la serie éxito del momento Game Of Thrones</p>
   <ul class="lis_prin">
     <li v-for="house in houses" :key="house.slug">
       <NuxtLink :to="{ name: 'casas-slug', params: {slug: house.slug}}">{{house.name}}</NuxtLink>
     </li>
   </ul>
   <FooterView />
 </div>
</template>