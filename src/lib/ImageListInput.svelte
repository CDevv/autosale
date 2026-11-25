<script lang="ts">
    import ImageFileEntry from "#lib/ImageFileEntry.svelte";
    import { onMount } from "svelte";

    let imageFiles: File[] = $state([]);
    let { input }: { input: HTMLInputElement } = $props();

    function onFileChoose(event: any) {
        const elem: HTMLInputElement = event.target;

        let file = elem.files?.item(0);
        if (file) {
            console.log(elem.files);
            imageFiles.push(file);
        }
    }

    onMount(() => {
        input.onchange = onFileChoose;
    });
</script>

<div class="flex flex-col gap-2">
    {#each imageFiles as file, index}
        <ImageFileEntry
            {file}
            ondelete={() => {
                imageFiles.splice(index, 1);
            }}
        ></ImageFileEntry>
    {/each}
</div>
