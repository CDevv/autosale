<script lang="ts">
    let { title }: { title: string } = $props();
</script>

<div class="flex items-center gap-3 mb-2 grow">
    <span class="w-1.5 h-10 rounded-full bg-orange-600"></span>

    <h1 class="text-3xl md:text-4xl font-black text-slate-950">
        {title}
    </h1>
</div>
