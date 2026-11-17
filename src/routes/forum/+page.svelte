<script>
    import PostCard from "#lib/PostCard.svelte";
</script>

<h1 class="text-3xl">Форуми</h1>
<br />
<div class="card">
    <h2 class="text-3xl">Добре дошли във форума на autosale.bg!</h2>
    <br />
    <p class="text-2xl">Молим Ви да спазвате някои основни правила:</p>
    <ol class="text-2xl" type="1">
        <li>Спазвайте добрия тон</li>
        <li>Не се толерира омраза към други лица</li>
        <li>Не качвайте съдържание, което не е свързано с темата на сайта</li>
    </ol>
</div>
<br />
<div class="card flex flex-row gap-2 text-2xl">
    <input class="card p-0.5 grow" type="text" />
    <button class="button min-w-2xs">Търсене</button>
</div>
<br />
<div class="flex flex-col">
    <PostCard />
</div>
