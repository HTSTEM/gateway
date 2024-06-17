<script>
    import Button from "$lib/Button.svelte";
    import Logo from "$lib/Logo.svelte";
    import Path from "$lib/Path.svelte";
    import MainContent from "$lib/MainContent.svelte";
    import SubContent from "$lib/SubContent.svelte";
    import {onMount} from "svelte";

    onMount(() => {
        if (Math.random() > 0.25) {
            setTimeout(() => {
                document.location.href = "../eligible"
            }, 5000)
        } else {
            setTimeout(() => {
                document.location.href = "../ineligible"
            }, 5000)
        }
    })
</script>

<style>
    @keyframes rotation {
        0% {
            transform: rotate(0deg);
        }
        100% {
            transform: rotate(360deg);
        }
    }

    .loader {
        width: min(100%, 300px);
        aspect-ratio: 1;
        margin: 4em auto;

        border: 1em solid #797979;
        border-bottom-color: #0B7702;
        border-radius: 50%;
        display: inline-block;
        animation: rotation 1s linear infinite;
    }
</style>

<Path pathSegments={["Home", "Community", "Assessment"]}></Path>
<Logo />
<MainContent>
    <h1>Heterosexuality Assessment Form</h1>
    <SubContent>
        <h2>Determining homosexuality status...</h2>
        <p>
            Do not close this window.
        </p>

        <span class="loader"></span>
    </SubContent>
</MainContent>
