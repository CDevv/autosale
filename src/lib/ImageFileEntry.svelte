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

<div class="card flex flex-row gap-1 max-h-144">
    <div class="flex flex-col grow max-h-full">
        <div class="max-h-full">
            <img
                src={url}
                alt={file.name}
                class="max-h-full max-w-full object-contain"
            />
        </div>
    </div>

    <button class="button min-w-3xs" onclick={ondelete}>Изтрий</button>
</div>
