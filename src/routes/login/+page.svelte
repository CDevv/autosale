<br />
<h1 class="text-3xl mt-0.5 mb-0.5">Влизане</h1>
<br />

<div class="flex justify-center flex-col gap-2">
    <form class="min-w-4xl card flex flex-col gap-3">
        <div class="form-item">
            <label for="name" class="text-xl">Име</label>
            <input name="name" class="card p-0.5" />
        </div>
        <div class="form-item">
            <label for="email" class="text-xl">Имейл</label>
            <input name="email" class="card p-0.5" type="email" />
        </div>
        <div class="form-item">
            <label for="email" class="text-xl">Телефон</label>
            <input name="email" class="card p-0.5" type="tel" />
        </div>
        <div class="form-item">
            <label for="pass" class="text-xl">Парола</label>
            <input name="pass" class="card p-0.5" type="password" />
        </div>
        <div class="form-item">
            <input
                name="submit"
                type="submit"
                class="button"
                value="Регистрирай се"
            />
        </div>
    </form>
    <div class="card">
        <p class="tex-2xl">
            Нямате профил? <a class="link" href="/register">Регистрирайте се</a>
        </p>
    </div>
</div>
