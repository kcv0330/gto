<script>
  export default {
    async asyncData({ $content, params }) {
      const casa = await $content('character-predictions', params.slug).fetch()
      return { casa }
    }
  }
</script>

<template>
  <div class="container">
   <HeaderView />
   <div class="row">
     <div class="three columns">
     </div>
     <div class="six columns">
       <h4>{{casa.house}}</h4></br>
     <label>Owner</label>{{casa.title}} {{casa.name}}<br> 
     <label>Age</label> <span>{{casa.age}}</span></br>
    <label>Spouse</label>{{casa.spouse}}<br> 
    <label>Mother</label>{{casa.mother}}<br> 
    <label>Father</label>{{casa.father}}<br> 


   </div>
   <div class="two columns"></div>
   </div>
   <FooterView />
 </div>
</template>