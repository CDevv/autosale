<script lang="ts">
    import ImageFileEntry from "#lib/ImageFileEntry.svelte";
    import ImageListInput from "#lib/ImageListInput.svelte";

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

<h1 class="text-3xl mt-0.5 mb-0.5">Нова обява</h1>
<br />

<div class="flex justify-center flex-col gap-2">
    <form class="min-w-4xl card flex flex-col gap-3">
        <div class="form-item">
            <label for="name" class="text-xl">Модел</label>
            <input name="name" class="card p-0.5" />
        </div>
        <div class="form-item">
            <label for="content" class="text-xl">Описание</label>
            <textarea name="content" class="card p-0.5　w-3xs"></textarea>
        </div>
        <div class="form-item">
            <label for="images" class="text-xl">Снимки</label>
            <ImageListInput />
        </div>
        <div class="form-item">
            <input
                name="submit"
                type="submit"
                class="button"
                value="Публикувай"
            />
        </div>
    </form>
</div>
