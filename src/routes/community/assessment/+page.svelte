<script>
    import Button from "$lib/Button.svelte";
    import Logo from "$lib/Logo.svelte";
    import Path from "$lib/Path.svelte";
    import MainContent from "$lib/MainContent.svelte";
    import SubContent from "$lib/SubContent.svelte";
    import FormattedDate from "$lib/FormattedDate.svelte";
    import {onMount} from "svelte";

    onMount(() => {
        document.getElementById("jsButton").classList.remove("hidden");

        const chr = (/(?<=Chrome\/)\d+/i).exec(navigator.userAgent)

        if (chr === null || parseInt(chr[0]) > 126) {
            document.getElementById("chrome").classList.remove("hidden");
        }
    });
</script>

<style>
    .hidden {
        display: none;
    }
</style>

<Path pathSegments={["Home", "Community", "Assessment"]}></Path>
<Logo />
<MainContent>
    <h1>Heterosexuality Assessment Form</h1>
    <SubContent>
        <p>
            Starting <FormattedDate date={new Date(2024, 5, 17)} />, both new and existing HTSTEM members will need to
            pass a heterosexuality assessment form to talk in our community. The form must be completed by
            <FormattedDate date={new Date(2024, 5, 23)} />, after which people that have not completed the form will
            not be able to speak in the server until they do.
        </p>
        <p>
            This form will assess your eligibility to continue participating in the HTwins STEM community. You may find
            it easier to use an Android mobile phone during the assessment process.
            <span id="chrome" class="hidden">Tested on Firefox 126. For the best experience, use Chrome 126 or later.</span>
        </p>
    </SubContent>
    <div id="jsButton" class="hidden">
        <Button href="/community/assessment/s1" text="Start" />
    </div>
    <noscript>
        <Button invalid="true" text="Requires JavaScript" />
    </noscript>
</MainContent>
