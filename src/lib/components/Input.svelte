<script lang="ts">
	import type { HTMLInputAttributes } from "svelte/elements";

    interface Props extends HTMLInputAttributes {
        info?: string
        error?: string
        color?: Style.color
    }

    let {
        class: className,

        info = undefined,
        error = undefined,
        color = "blue",
        ...props
    }: Props = $props()
</script>

<div class="input-field">
    <input {...props} class={`${[className, color].filter(Boolean).join(' ')}`} />
    {#if info && !error}
        <span class={`${["tooltiptext", color].filter(Boolean).join(' ')}`}>{info}</span>
    {/if}
    {#if error}
        <span class="tooltiptext red">{error}</span>
    {/if}
</div>


<style>
    .input-field {
        position: relative;
        display: inline-block;

        & .tooltiptext {
            opacity: 0;
            visibility: hidden;
            transform: translateY(-0.25rem);
            transition: opacity 0.3s ease, visibility 0.3s ease, transform 0.3s ease;

            background-color: black;
            color: #fff;
            text-align: center;
            padding: 0.2rem 0.5rem;
            border-radius: 0.2rem;
            left: 105%;
            position: absolute;
            z-index: 1;

            &.red {
                background-color: var(--red-dark);
                color: white;
            }
            &.yellow {
                background-color: var(--yellow-dark);
                color: white;
            }
            &.green {
                background-color: var(--green-dark);
                color: white;
            }
            &.blue {
                background-color: var(--blue-dark);
                color: white;
            }
            &.purple {
                background-color: var(--purple-dark);
                color: white;
            }
        }

        &:hover .tooltiptext {
            visibility: visible;
            opacity: 1;
            transform: translateY(0);
        }
    }
    input {
        background-color: white;
        color: var(--red-dark);
        border: var(--red-dark) 1px solid;
        padding: 0.2rem 0.5rem;
        border-radius: 0.2rem;
        cursor: pointer;
        font-size: 16px;
        outline: none;

        &.red {
            background-color: white;
            color: var(--red-dark);
            border: var(--red-dark) 1px solid;

            &:hover {
                background-color: var(--red-dark);
                color: white;
            }
        }

        &.yellow {
            background-color: white;
            color: var(--yellow-dark);
            border: var(--yellow-dark) 1px solid;

            &:hover {
                background-color: var(--yellow-dark);
                color: white;
            }
        }

        &.green {
            background-color: white;
            color: var(--green-dark);
            border: var(--green-dark) 1px solid;

            &:hover {
                background-color: var(--green-dark);
                color: white;
            }
        }

        &.blue {
            background-color: white;
            color: var(--blue-dark);
            border: var(--blue-dark) 1px solid;

            &:hover {
                background-color: var(--blue-dark);
                color: white;
            }
        }

        &.purple {
            background-color: white;
            color: var(--purple-dark);
            border: var(--purple-dark) 1px solid;

            &:hover {
                background-color: var(--purple-dark);
                color: white;
            }
        }
    }
</style>