<script lang="ts">
	import { fade } from 'svelte/transition';
	
	const fadeIn = {
		delay: 100,
		duration: 200
	}
	
	const fadeOut = {
		delay: 0,
		duration: 100
	}
	
	let isExpanded = $state(false);
</script>


<nav class:expanded={isExpanded}>

</nav>


<style>

</style>