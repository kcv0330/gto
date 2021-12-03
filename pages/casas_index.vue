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
   <h3 style="margin-top: 15px">Amazon Top 50 Bestselling Books 2009 - 2019</h3>
     <p>Dataset on Amazon's Top 50 bestselling books from 2009 to 2019. Contains 550 books, data has been categorized into fiction and non-fiction using Goodreads</p>
   <ul class="lis_prin">
     <li v-for="house in houses" :key="house.slug">
       <NuxtLink :to="{ name: 'casas-slug', params: {slug: house.slug}}">{{house.name}}</NuxtLink>
     </li>
   </ul>
   <FooterView />
 </div>
</template>