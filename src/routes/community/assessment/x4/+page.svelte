<script>
    import Path from "$lib/Path.svelte";
    import Logo from "$lib/Logo.svelte";
    import SubContent from "$lib/SubContent.svelte";
    import Button from "$lib/Button.svelte";
    import MainContent from "$lib/MainContent.svelte";
    import {onMount} from "svelte";

    let invalid = true;

    function updateInvalid() {
        if (document.getElementById("input").value !== "") {
            invalid = false;
        }
    }
</script>

<style>
    input, input:active, input:focus {
        padding: 0.5em 1em;
        border: 2px solid black;
        outline: none;
        border-radius: 0 !important;
        background: none
    }

    @media (prefers-color-scheme: dark) {
        input, input:active, input:focus {
            border: 2px solid white
        }
    }
</style>

<Path pathSegments={["Home", "Community", "Assessment"]}></Path>
<Logo />
<MainContent>
    <h1>Heterosexuality Assessment Form</h1>
    <SubContent>
        <h2>Please provide more evidence that you are homosexual</h2>
        <p>
            Type in a homophobic slur in the bottom text entry to proceed:
        </p>
        <input type="text" id="input" on:change={updateInvalid}>
    </SubContent>
    <!-- onclick instead of href to mask destination :3 -->
    <Button onclick={() => {if (!invalid) document.location.href = "ineligible"}} invalid={invalid} text="Continue"></Button>
</MainContent>