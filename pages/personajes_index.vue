<script>
  export default {
    async asyncData({ $content }) {
      const characters = await $content('character-deaths').fetch()
      return {
        characters
      }
    }
  }
</script>

<template>
  <div class="container">
   <HeaderView />
   <h3 style="margin-top: 15px">Personajes de Games of Thrones</h3>
     <p>El elenco de Game of Thrones</p>
   <ul class="lis_prin">
     <li v-for="character in characters" :key="character.slug">
       <NuxtLink :to="{ name: 'personajes-slug', params: {slug: character.slug}}">{{character.Name}}</NuxtLink>
     </li>
   </ul>
   <FooterView />
 </div>
</template>