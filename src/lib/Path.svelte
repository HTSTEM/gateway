<script>
    import Label from "$lib/Label.svelte";

    export let pathSegments = [];
</script>

<style>
    .path {
        display: flex;
        flex-direction: row;
        gap: 0.5rem;
        align-items: center;
        flex-wrap: nowrap;
    }

    .path-top {
        padding-bottom: 1rem;
        flex-wrap: wrap;
    }
</style>

<div class="path path-top">
    {#each pathSegments as segment, index}
        {#if index === 0}
            <Label>{segment}</Label>
        {:else}
            <div class="path">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <mask id="mask0_7_12" style="mask-type:alpha" maskUnits="userSpaceOnUse" x="0" y="0" width="24" height="24">
                        <rect width="24" height="24" fill="#D9D9D9"/>
                    </mask>
                    <g mask="url(#mask0_7_12)">
                        <path d="M12.6 12L8 7.4L9.4 6L15.4 12L9.4 18L8 16.6L12.6 12Z" fill="#1C1B1F"/>
                    </g>
                </svg>
                <Label>{segment}</Label>
            </div>
        {/if}
    {/each}
</div>