<script lang="ts">
	import type { Snippet } from "svelte";
	import type { HTMLButtonAttributes } from "svelte/elements";

    interface Props extends HTMLButtonAttributes {
        children?: Snippet
        color?: Style.color
    }
    let {
        children,
        class: className,
        color = "blue",
        ...props
    }: Props = $props()

</script>

<button {...props} class={`${[className, color].filter(Boolean).join(' ')}`}>
    {@render children?.()}
</button>

<style>
    button {
        background-color: white;
        color: var(--red-dark);
        border: var(--red-dark) 1px solid;
        padding: 0.2rem 0.5rem;
        border-radius: 0.3rem;
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