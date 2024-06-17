<script>
    export let href = undefined;
    export let isInput = false;
    export let text = undefined;
    export let invalid = false;
    export let onclick = undefined;
</script>

<style>
    .button {
        display: flex;
        padding: 0.5rem 2rem;
        width: 100%;
        align-items: center;
        justify-content: center;
        background-color: #0B7702;
        border: none;
        cursor: pointer;

        margin-top: 0;
        margin-bottom: 4px;
        box-shadow: 0 4px #064500;
    }

    .button:invalid, .button[data-invalid='true'] {
        background-color: #797979;

        margin-top: 0;
        margin-bottom: 4px;
        box-shadow: 0 4px #525252;
        cursor: not-allowed;
    }

    .button:not(:invalid, [data-invalid='true']):hover {
        margin-top: 4px;
        margin-bottom: 0;
        box-shadow: none;
        background-color: #064500;
    }

    @media (min-width: 70rem) {
        .button {
            min-width: 16rem;
            max-width: max-content;
        }
    }

    .button-inner {
        font-weight: 500;
        color: white;
    }
</style>

{#if isInput}
    <input type="submit" class="button button-inner" value={text}/>
{:else}
    <a class="button" on:click={onclick} href={href} data-invalid={invalid}>
        <p class="button-inner">{text}</p>
    </a>
{/if}