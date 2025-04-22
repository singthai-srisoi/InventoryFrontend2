<script lang="ts">
	import type { Snippet } from "svelte";
    import "../app.css"
    interface Props {
        children?: Snippet
    }
    let { children }: Props = $props()
</script>

<main>
	<nav>
        <h1 class="logo">Hi</h1>
        <div class="menu">
            <ul class="menu-list">
                <li>
                    <button type="button">
                        <h1 aria-label="Hello">
                            <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
                            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12c0 4.9706-4.0294 9-9 9m9-9c0-4.97056-4.0294-9-9-9m9 9h-5m-4 9c-4.97056 0-9-4.0294-9-9m9 9v-5m-9-4c0-4.97056 4.02944-9 9-9m-9 9h5m4-9v5M8 3.93552V8m0 0v4m0-4H3.93552M8 8h4m-4 4v4m0-4h4m-4 4v4.0645M8 16H3.93552M8 16h4m0-8v4m0-4h4m-4 4v4m0-4h4m-4 4h4m0-12.06448V8m0 0v4m0-4h4.0645M16 12v4m0 0v4.0645M16 16h4.0645"/>
                            </svg>
                        </h1>
                        <span>Hello</span>
                    </button>
                </li>
                <li>
                    <button type="button" class="active">
                        <h1 aria-label="World">
                            <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
                            <path fill="currentColor" d="M15.0524 2.01283c-.2634-.00221-.7706-.00646-1.3064.08808-.6053.10681-1.377.35866-1.975.99279-.557.59067-.8308 1.31504-.9706 1.92248-.1413.61388-.1628 1.1828-.1628 1.5327v1h1c.0429 0 .0873.00018.1333.00036.8172.00329 2.1026.00847 3.2375-.9589.7023-.59862.9572-1.43277 1.059-2.06861.0871-.54385.0798-1.08153.0758-1.37798-.0007-.051-.0013-.09486-.0013-.13038v-1h-1c-.0255 0-.0554-.00025-.0895-.00054Zm-3.0525 7.02912c-.2934 0-.3974-.0566-.7263-.23555-.1027-.05589-.2273-.12372-.3865-.20548-.6797-.34907-1.55211-.64467-3.12486-.59552-1.30968.04093-2.37715.88151-3.01521 2.0359-.64078 1.1594-.90215 2.7005-.65499 4.4145.1543 1.07.66239 2.84 1.39644 4.358.36735.7596.81762 1.5119 1.34963 2.0895C7.35502 21.4646 8.08053 22 8.99163 22c1.17857 0 1.86287-.2589 2.38977-.5504.1663-.092.2761-.1558.3523-.2001.1161-.0674.1542-.0895.1949-.0968.0198-.0035.0403-.0035.0708-.0035.0105 0 .0195-.0003.0268-.0005.0132-.0003.0222-.0006.031.0009.0193.0032.0373.0146.095.0514.0638.0408.1761.1125.3925.2382.5319.3091 1.2263.5608 2.4635.5608.9293 0 1.6712-.5145 2.2105-1.0909.5456-.5832.9936-1.3421 1.3526-2.1048.7186-1.5268 1.1845-3.2947 1.3365-4.3485.2471-1.714-.0142-3.2551-.655-4.4145-.6381-1.15439-1.7055-1.99497-3.0152-2.0359-1.5728-.04915-2.4451.24645-3.1248.59552-.1592.08176-.2839.14959-.3866.20548-.3289.17895-.4329.23555-.7263.23555Z"/>
                            </svg>
                        </h1>
                        <span>World</span>
                    </button>
                </li>
                <li>
                    <button type="button">
                        <h1 aria-label="Dashboard">
                            <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
                                <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20 14H4m6.5 3L8 20m5.5-3 2.5 3M4.88889 17H19.1111c.4909 0 .8889-.4157.8889-.9286V4.92857C20 4.41574 19.602 4 19.1111 4H4.88889C4.39797 4 4 4.41574 4 4.92857V16.0714c0 .5129.39797.9286.88889.9286ZM13 14v-3h4v3h-4Z"/>
                            </svg>
                        </h1>
                        <span>Dashboard</span>
                    </button>
                </li>
                <li>
                    <button type="button">
                        <h1 aria-label="User">
                            <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
                                <path stroke="currentColor" stroke-width="2" d="M7 17v1a1 1 0 0 0 1 1h8a1 1 0 0 0 1-1v-1a3 3 0 0 0-3-3h-4a3 3 0 0 0-3 3Zm8-9a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z"/>
                            </svg>
                        </h1>
                        <span>User</span>
                    </button>
                </li>
                <li>
                    <button type="button">
                        <h1 aria-label="Vehicle">
                            <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
                            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7h6l2 4m-8-4v8m0-8V6a1 1 0 0 0-1-1H4a1 1 0 0 0-1 1v9h2m8 0H9m4 0h2m4 0h2v-4m0 0h-5m3.5 5.5a2.5 2.5 0 1 1-5 0 2.5 2.5 0 0 1 5 0Zm-10 0a2.5 2.5 0 1 1-5 0 2.5 2.5 0 0 1 5 0Z"/>
                            </svg>
                        </h1>
                        <span>Vehicle</span>
                    </button>
                </li>
                <li>
                    <button type="button">
                        <h1 aria-label="Inventory">
                            <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
                                <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 4h1.5L9 16m0 0h8m-8 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4Zm8 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4Zm-8.5-3h9.25L19 7H7.312"/>
                            </svg>
                        </h1>
                        <span>Inventory</span>
                    </button>
                </li>
                <li>
                    <button type="button">
                        <h1 aria-label="Report">
                            <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
                                <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 4.5V19a1 1 0 0 0 1 1h15M7 14l4-4 4 4 5-5m0 0h-3.207M20 9v3.207"/>
                            </svg>
                        </h1>
                        <span>Report</span>
                    </button>
                </li>
            </ul>

            <ul class="menu-list">
                <li>
                    <button type="button">
                        <h1 aria-label="Settings">
                            <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
                            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16.872 9.687 20 6.56 17.44 4 4 17.44 6.56 20 16.873 9.687Zm0 0-2.56-2.56M6 7v2m0 0v2m0-2H4m2 0h2m7 7v2m0 0v2m0-2h-2m2 0h2M8 4h.01v.01H8V4Zm2 2h.01v.01H10V6Zm2-2h.01v.01H12V4Zm8 8h.01v.01H20V12Zm-2 2h.01v.01H18V14Zm2 2h.01v.01H20V16Z"/>
                            </svg>
                        </h1>
                        <span>Settings</span>
                    </button>
                </li>
            </ul>

        </div>
        
    </nav>
	<section class="content">
        <div>
            {@render children?.()}
        </div>
	</section> 
</main>



<style>
    main {
		display: grid;
		grid-template:
			"nav content" min-content
            / auto 1fr;
        overflow: hidden;
        isolation: isolate;
        background: white;
	}

    nav {
        grid-area: nav;
        min-height: 100vh;
        background-color: black;
        color: white;
        overflow: hidden;

        display: flex;
        flex-direction: column;

    }

    .logo {
        font-size: 1.5rem;
        color: white;
        text-align: center;
        padding: 0.5rem 1rem;
    }

    .menu {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        padding: auto;
        height: 100%;
        width: 100%;
        padding: 0.5rem;
    }

    .menu-list {
        list-style: none;
        padding: 0;
        margin: 0;
        display: flex;
        flex-direction: column;
        gap: 0.5rem;
    }



    .menu-list button {
        display: flex;
        flex-direction: column;
        align-items: center;
        background-color: transparent;
        border: none;
        color: white;
        font-size: 1.2rem;
        padding: 0.3rem 0.75rem;
        width: 100%;
        border-radius: 0.3rem;
        cursor: pointer;
        transition: background-color 0.3s ease, color 0.3s ease;

        &.active {
            background-color: white;
            color: black;
        }
    }

    .menu-list button:hover:not(.active) {
        background-color: rgba(255, 255, 255, 0.1);
        color: white;
    }

    .menu-list button:active {
        transition: transform 0.3s ease;
        transform: scale(0.85);
    }

    .menu-list button h1 {
        margin: 0;
        font-size: 0.8rem;
    }

    .menu-list button span {
        font-size: 0.6rem;
    }

    .content {
        grid-area: content;
        background-color: black;

        & div {
            padding: 2rem;
            background-color: white;
            color: black;
            overflow-y: auto;
            height: 100%;
            width: 100%;
            border-radius: 0.5rem;
        }
        
        
    }
</style>