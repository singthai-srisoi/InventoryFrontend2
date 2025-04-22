<script>
	import { fade } from 'svelte/transition';
	
	const fadeIn = {
		delay: 100,
		duration: 200
	}
	
	const fadeOut = {
		delay: 0,
		duration: 100
	}
	
	let isExpanded = false;
</script>

<nav class:expanded={isExpanded}>
	<button on:click={() => isExpanded = !isExpanded}>
		{#if isExpanded}
			Close
		{:else}
			Open
		{/if}
	</button>
	<ul>
		<li>
			<div class="logo">🚀</div>
			{#if isExpanded}
			<span in:fade="{fadeIn}" out:fade="{fadeOut}">Inbox</span>
			{/if}
		</li>
		<li>
			<div class="logo">⭐️</div>
			{#if isExpanded}
			<span in:fade="{fadeIn}" out:fade="{fadeOut}">Starred</span>
			{/if}
		</li>
		<li>
			<div class="logo">🗑</div>
			{#if isExpanded} 
			<span in:fade="{fadeIn}" out:fade="{fadeOut}">Trashed</span>
			{/if}
		</li>
	</ul>
	{#if isExpanded}
	<section in:fade="{fadeIn}" out:fade="{fadeOut}" >
		<hr />
		<ul>
			<h3>
				Folders
			</h3>
			<li><div class="logo">🧾</div> Receipts</li>
			<li><div class="logo">🤖</div> Autofilter</li>
		</ul>
	</section>
	{/if}
</nav>

<style>
	nav {
		grid-area: nav;
		min-height: 100vh;
		background-color: #324754;
		color: #A2B7C4;
		transition: ease-out 200ms;
		width: 60px;
		overflow: hidden;
	}

	.expanded {
		transition: ease-out 200ms;
		width: 200px;
	}
	
	ul {
		list-style: none;
		padding: 20px;
		margin: 0;
	}
	
	li {
		width: 200px;
	}
	
	h3 {
		text-transform: uppercase;
		margin: 0;
		padding: 10px 0;
	}
	
	hr {
	  color: white;
		width: 100%;
	}
	.logo {
		width: 20px;
		height: 20px;
		display: inline-block;
		margin-right: 10px;
		text-align: center;
	}
	button {
		border: none;
		background: none;
		color: #A2B7C4;
		text-transform: uppercase;
		padding: 0.5rem 1rem;
	}
</style>