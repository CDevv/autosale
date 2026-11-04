<script lang="ts">
    import ImageFileEntry from "#lib/ImageFileEntry.svelte";

    let imageFiles: File[] = $state([]);

    function onFileChoose(event: any) {
        const elem: HTMLInputElement = event.target;

        let file = elem.files?.item(0);
        if (file) {
            console.log(elem.files);
            imageFiles.push(file);
        }
    }
</script>

<input
    class="card p-0.5"
    type="file"
    accept=".jpg, .jpeg, .png"
    onchange={onFileChoose}
/>
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
