<style>
    .Footer {
        background-color: rgba(28, 41, 56, 0.8);
        color: white;
        padding: 1.5em 0;
        margin: 2em 0 0 0;
        font-size: 13px;
        font-weight: 300;
    }
    .Footer-container {
        display: grid;
        grid-template-columns: minmax(auto, 1024px);
        justify-content: center;
        align-items: center;
    }
    .Footer-content {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .Footer-info {
        display: flex;
        align-self: center;
    }
    .Footer-info img {
        margin: 0 0 0 0.5em;
    }
</style>

<footer class="Footer">
    <div class="Footer-container">
        <div class="Footer-content">
            <div class="Footer-copy">Made with love in Mexico</div>
            <div class="Footer-info">
                Proudly powered by Svelte
                <img src="/img/svelte-icon.png" alt="Svelte logo" />
            </div>
        </div>
    </div>
</footer>
