<script>
	import Place from './Place.svelte'

	export let city = '';
	export let country = '';
	export let img = '';
	export let places = [];
</script>

<div class="card">
	<div class="card__image-container">
		<img src={ img } alt="{ city }, { country }" class="card__image">    
	</div>
	<div class="card__content">
		<h2 class="card__title"><strong>{ city }</strong>, { country }</h2>

		{#each places as { src, title }}
			<Place {src} {title} />
		{/each}
	</div>
  </div>


<style>
.card {
  max-width: 400px;
  margin: 0 auto;
  box-shadow: 0 0 10px 0 rgba(100, 100, 100, 0.2);
  border-radius: 30px;
  font-family: sans-serif;
}

.card__image-container {
	height: 400px;
  	border-radius: 30px;
  	overflow: hidden;
}

.card__image {
	width: 100%;
  	height: 100%;
  	object-fit: cover;
}

.card__content {
  padding: 20px;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-column-gap: 15px;
  grid-row-gap: 15px;
}

.card__title {
  font-weight: normal;
  color: #b1a290;
  grid-column: span 2;
  margin: 0;
}

.card__title strong {
  color: #453e37;
}
</style>