<script lang="ts">
	import type { Snippet } from "svelte";
    import "../app.css"
	import { Button } from "$lib";
	import { slide } from "svelte/transition";
	import Menu from "$lib/components/Menu.svelte";
    interface Props {
        children?: Snippet
    }
    let { children }: Props = $props()

    let showSide = $state(true)
    function toggleSide() {
        showSide = !showSide
    }
</script>

<!-- <div class="layout" class:collapsed={!showSide}>
    {#if showSide}
        <aside transition:slide>
            <div class="logo">
                <h1>Hello There</h1>
            </div>
            <div class="nav">
                <a href="/">Home</a>
                <a href="/about">About</a>
                <a href="/contact">Contact</a>
            </div>
        </aside>
    {/if}
    
    
    <main>
        <Button type="button" color="yellow" onclick={toggleSide}>Hide Side</Button>
        {@render children?.()}
    </main>

</div> -->

<main>
	<Menu />
	<section class="content">
		{@render children?.()}
	</section> 
</main>



<style>
    main {
        margin: 0.5rem;
        border-radius: 0.2rem;
        border: var(--blue-dark) 1px solid;
		display: grid;
		grid-template:
			"nav content" min-content
            / auto 1fr; /* 2 columns, first auto, second 1fr */
            overflow: hidden;           /* Clipping for child overflow */
            isolation: isolate;         /* Ensures stacking context for transitions, z-index, etc. */
            background: white;          /* Optional: so border-radius looks good */
            box-shadow: 0 0 8px rgba(0,0,0,0.05);  /* Optional: add depth */
        
	}
	.content {
        padding: 0 1rem;
		grid-area: content;
	}


    div.layout {
        display: grid;
        grid-template-columns: auto 1fr;
        min-height: 100vh;

        &.collapsed {
            grid-template-columns: 1fr;
        }
    }
    aside {
        height: 100%;
        background-color: white;
        overflow: auto;
        padding: 1rem;
        border-right: var(--blue-bright) 1px solid;

        width: 200px;
        /* transition: all 0.3s ease; */
        /* transform: translateX(0);
        opacity: 1;
        transition: transform 0.3s ease, opacity 0.3s ease;
        width: 200px;


        &.hide {
            transform: translateX(-100%);
            opacity: 0;
        } */

        & .nav {
            display: flex;
            flex-direction: column;
            gap: 0.2rem;
            margin-top: 2rem;
            & a {
                text-decoration: none;
                color: var(--purple-dark);
                font-size: 1rem;
                font-weight: bold;
                padding: 0.5rem 1rem;
                border-radius: 0.2rem;
                transition: background-color 0.3s ease, color 0.3s ease;
                outline: none;

                &:hover {
                    background-color: var(--purple-dark);
                    color: white;
                }
            }
        }
    }
</style>