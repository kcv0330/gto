<script>
  export default {
    async asyncData({ $content }) {
      const battles = await $content('batallas').fetch()
      return {
        battles
      }
    }
  }
</script>

<template>
  <div class="container">
   <HeaderView />
   <h3 style="margin-top: 15px">Batallas Games of Thrones</h3>
     <p>Games of Thrones</p>
   <ul class="lis_prin">
     <li v-for="battle in battles" :key="battle.slug">
       <NuxtLink :to="{ name: 'batallas-slug', params: {slug: battle.slug}}">{{battle.name}}</NuxtLink>
     </li>
   </ul>
   <FooterView />
 </div>
</template>