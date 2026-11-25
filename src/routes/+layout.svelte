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

<div id="top">
    <Header />
    <div
        class="ml-60 mr-60 mt-4 mb-4 mx-auto px-4 md:px-6 py-8 relative top-16"
    >
        {@render children()}
    </div>
</div>

<style>
    :global(body) {
        margin: 0;
        padding: 0;
        background-image: url("/niekverlaan-car-718781_1920.png");
        background-attachment: fixed;
        background-repeat: repeat-y;
        font-family: "RobotoCondensed";
    }
</style>
