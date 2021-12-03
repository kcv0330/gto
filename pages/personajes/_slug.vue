<script>
  export default {
    async asyncData({ $content, params }) {
      const personaje = await $content('character-deaths', params.slug).fetch()
      return { personaje }
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
       <h4>{{personaje.Name}}</h4></br>
     <label>Allegiances</label>{{personaje.Allegiances}}<br> 
     <label>Death Year</label> <span>{{personaje.death_year}}</span></br>
    <label>Book of Death</label>{{personaje.Book_of_Death}}<br> 
    <label>Death Chapter</label>{{personaje.Death_Chapter}}<br> 
    <label>Book Intro Chapter</label>{{personaje.Book_Intro_Chapter}}<br> 


   </div>
   <div class="two columns"></div>
   </div>
   <FooterView />
 </div>
</template>