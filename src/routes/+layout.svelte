<script lang="ts">
    import "./layout.css";
    import favicon from "#lib/assets/favicon.svg";
    import type { LayoutProps } from "./$types";
    import PageButton from "#lib/PageButton.svelte";
    import Header from "#lib/Header.svelte";

    let { children }: LayoutProps = $props();
</script>

<svelte:head>
    <link rel="icon" href={favicon} />
</svelte:head>

<Header />

<div class="ml-60 mr-60">
    {@render children()}
</div>
