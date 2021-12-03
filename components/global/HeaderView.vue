<template>
  <header>
	  <div class="title">Games of Thrones</div>
	  <nav>
		  <nuxt-link to="/">Inicio</nuxt-link>
		  <nuxt-link to="/batallas_index">Batallas</nuxt-link>
		  <nuxt-link to="/casas_index">Casas</nuxt-link>
		  <nuxt-link to="/personajes_index">Personajes</nuxt-link>
	  </nav>
  </header>
</template>
<style>
header {
	padding: 15px 30px;
	background-color: #FFF;
	display: flex;
	justify-content: space-between;
	align-items: center;
	box-shadow: 0px 3px 6px rgba(0, 0, 0, 0.1);
}

header .title {
	color: #212121;
	font-size: 24px;
	font-weight: 900;
	text-transform: uppercase;
}

nav {
	display: flex;
	align-items: center;
	margin: 0 -15px;
}

nav a {
	display: block;
	margin: 0 15px;
	color: #9f25cf;
}
</style>