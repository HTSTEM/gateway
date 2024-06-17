<style>
    main {
        padding: 128px 32px 32px 32px;
        margin: auto;
        min-height: 100dvh;
        width: 100%;
        max-width: 48rem;
        font-size: 1.2em;

        display: flex;
        flex-direction: column;
        justify-content: space-between;
        gap: 16px;
    }

    @media (max-height: 50rem) {
        main {
            padding: 32px;
        }
    }

    a {
        opacity: 80%
    }
</style>

<main data-sveltekit-reload>
    <div>
        <slot />
    </div>
    <a href="/privacy">Privacy policy and disclaimer</a>
</main>