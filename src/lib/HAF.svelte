<script>
    import Button from "$lib/Button.svelte";
    import Logo from "$lib/Logo.svelte";
    import Path from "$lib/Path.svelte";
    import MainContent from "$lib/MainContent.svelte";
    import SubContent from "$lib/SubContent.svelte";

    export let title = undefined;
    export let choices = [
        {
            text: "Yes",
            href: "/"
        }
    ];

    function transition(ev) {
        ev.preventDefault()

        for (const [idx, choice] of choices.entries()) {
            if (document.getElementById(`choice${idx}`).checked) {
                window.location.href = choice.href
            }
        }
    }
</script>

<style>
    label {
        position: relative;
        display: flex;
        flex-direction: row;
        gap: 1rem;
        align-items: center;
    }

    input[type="radio"] {
        width: 2rem;
        height: 2rem;
        opacity: 0;
    }

    .radio-circle {
        position: absolute;
        left: 0;
        top: 0;
        width: 2rem;
        height: 2rem;
        pointer-events: none;
    }

    .radio-inner-circle {
        visibility: hidden;
    }

    input[type="radio"]:checked ~ .radio-inner-circle {
        visibility: visible;
    }
</style>

<Path pathSegments={["Home", "Community", "Assessment"]}></Path>
<Logo/>
<form on:submit={transition}>
    <MainContent>
        <h1>Heterosexuality Assessment Form</h1>
        <SubContent>
            <h2>{title}</h2>
            {#each choices as choice, idx}
                <label>
                    <input type="radio" name="radio" id="choice{idx}" required>
                    <svg class="radio-circle radio-inner-circle" width="32" height="32" viewBox="0 0 32 32" fill="none"
                         xmlns="http://www.w3.org/2000/svg">
                        <circle cx="16" cy="16" r="8" fill="black"/>
                    </svg>
                    <svg class="radio-circle" width="32" height="32" viewBox="0 0 32 32" fill="none"
                         xmlns="http://www.w3.org/2000/svg">
                        <rect x="1" y="1" width="30" height="30" rx="15" stroke="black" stroke-width="2"/>
                    </svg>
                    {choice.text}
                </label>
            {/each}
        </SubContent>
        <Button text="Continue" isInput/>
    </MainContent>
</form>

