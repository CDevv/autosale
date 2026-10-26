<script lang="ts">
    let { title, href } = $props();
</script>

<a
    {href}
    class="flex align-center justify-center hover:bg-amber-500 p-4 duration-75"
>
    <span class="text-white text-2xl">{title}</span>
</a>
