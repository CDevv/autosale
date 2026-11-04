<script lang="ts">
    import type { MouseEventHandler } from "svelte/elements";

    let {
        file,
        ondelete,
    }: {
        file: File;
        ondelete: MouseEventHandler<HTMLButtonElement>;
    } = $props();

    let url: string = $state("");
    $effect(() => {
        url = URL.createObjectURL(file);
    });
</script>

<div class="card flex flex-row gap-1">
    <div class="flex flex-col grow max-h-full">
        <div>
            <img src={url} alt={file.name} class="max-h-full" />
        </div>
        <p class="text-2xl">{file.name}</p>
    </div>

    <button class="button min-w-3xs" onclick={ondelete}>Изтрий</button>
</div>
