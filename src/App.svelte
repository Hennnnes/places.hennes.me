<script>
	import Card from './Card.svelte';

	const fetchData = (async () => {
		const response = await fetch('./data.json')
    	return await response.json()
	})()
</script>

<main>
	<h1>Places</h1>
	{#await fetchData then data}
		{#each data as { city, country, img, places}}
			<Card {city} {country} {img} {places}/>
		{/each}
	{/await}
</main>

<style>
</style>