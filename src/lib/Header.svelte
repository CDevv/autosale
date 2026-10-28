<script>
    import PageButton from "./PageButton.svelte";
</script>

<div class="bg-amber-600 min-h-18 flex content-center">
    <div class="min-h-max flex">
        <a
            href="/"
            class="bg-amber-50 text-shadow-black align-middle text-center text-3xl rounded-md p-2 m-1.5"
        >
            <span> autosale.bg </span>
        </a>
    </div>
    <div class="grow min-h-max flex">
        <PageButton href="/" title="Начало"></PageButton>
        <PageButton href="/dealers" title="Дилъри"></PageButton>
        <PageButton href="/offers" title="Коли"></PageButton>
    </div>
    <PageButton href="/" title="Регистрация"></PageButton>
</div>
