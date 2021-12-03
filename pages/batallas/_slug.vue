<script>
  export default {
    async asyncData({ $content, params }) {
      const batalla = await $content('batallas', params.slug).fetch()
      return { batalla }
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
       <h4>{{batalla.name}}</h4></br>
	   <label>Attacker king</label>{{batalla.attacker_king}} number of attackers <span>{{batalla.attacker_size}}</span></br>
     <label>Defender king</label>{{batalla.defender_king}} number of defenders <span>{{batalla.defender_size}}</span></br>
     <label>Year</label>{{batalla.year}}</br>
     <label>Location</label>{{batalla.location}}</br>
     <label>Region</label>{{batalla.region}}</br>

	 </div>
	 <div class="two columns"></div>
   </div>
   <FooterView />
 </div>
</template>