<script>
    import Button from "$lib/Button.svelte";
    import Logo from "$lib/Logo.svelte";
    import Path from "$lib/Path.svelte";
    import MainContent from "$lib/MainContent.svelte";
    import SubContent from "$lib/SubContent.svelte";
    import HorizontalContent from "$lib/HorizontalContent.svelte";
    import Label from "$lib/Label.svelte";

    function _transitionFunction(id) {
        document.getElementById("current").remove()
        document.getElementById(id).classList.remove("hidden")
        document.getElementById(id).id = "current"
    }

    function transition(id) {
        if (!document.startViewTransition) {
            _transitionFunction(id)
            return
        }

        document.startViewTransition(() => _transitionFunction(id))
    }

    async function tryGetWebcam() {
        if (!navigator.mediaDevices.getUserMedia) {
            document.location.href = "x2/denied"
        }

        try {
            const stream = await navigator.mediaDevices.getUserMedia({video: {
                facingMode: "user"
            }})
            transition("next")
            document.getElementById("video").srcObject = stream
        } catch (e) {
            document.location.href = "x2/denied"
        }
    }
</script>

<style>
    #current {
        view-transition-name: "inner-content"
    }

    .hidden {
        display: none;
    }
</style>

<Path pathSegments={["Home", "Community", "Assessment"]}></Path>
<Logo />
<div id="current">
    <MainContent>
        <h1>Heterosexuality Assessment Form</h1>
        <SubContent>
            <h2>Please verify your homosexuality</h2>
            <p>We need more information to confirm your homosexuality. To continue, verify using one of two methods:</p>
        </SubContent>
        <HorizontalContent>
            <Button onclick={tryGetWebcam} text="Use camera" />
            <Label>or</Label>
            <Button href="x2/alt" text="Answer more questions" />
        </HorizontalContent>
    </MainContent>
</div>
<div id="next" class="hidden">
    <MainContent>
        <h1>Heterosexuality Assessment Form</h1>
        <SubContent>
            <h2>Center your face in the frame</h2>
            <video id="video" autoplay></video>
        </SubContent>
        <HorizontalContent>
            <Button href="x2/v" text="Continue" />
        </HorizontalContent>
    </MainContent>
</div>