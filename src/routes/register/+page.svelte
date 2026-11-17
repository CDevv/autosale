<h1 class="text-3xl mt-0.5 mb-0.5">Регистрация</h1>
<br />

<div class="flex flex-col justify-center text-2xl">
    <div class="max-w-4xl flex justify-center flex-col gap-2">
        <form class="card flex flex-col gap-3">
            <div class="form-item">
                <label for="name">Име</label>
                <input name="name" class="card p-0.5" />
            </div>
            <div class="form-item">
                <label for="email">Имейл</label>
                <input name="email" class="card p-0.5" type="email" />
            </div>
            <div class="form-item">
                <label for="email">Телефон</label>
                <input name="email" class="card p-0.5" type="tel" />
            </div>
            <div class="form-item">
                <label for="pass">Парола</label>
                <input name="pass" class="card p-0.5" type="password" />
            </div>
            <div class="form-item">
                <label for="passrepeat">Повтори парола</label>
                <input name="passrepeat" class="card p-0.5" type="password" />
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
                Вече имате профил? <a class="link" href="/login">Влезте</a>
            </p>
        </div>
    </div>
</div>
