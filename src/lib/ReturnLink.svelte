<script lang="ts">
    let { href, title }: { href: string; title: string } = $props();
</script>

<a
    {href}
    class="inline-flex items-center gap-2 text-slate-600 hover:text-orange-600 font-semibold mb-5 transition-colors"
>
    <span class="text-xl">←</span>
    {title}
</a>
