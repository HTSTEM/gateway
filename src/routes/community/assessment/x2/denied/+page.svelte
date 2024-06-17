<script>
    import Button from "$lib/Button.svelte";
    import Logo from "$lib/Logo.svelte";
    import Path from "$lib/Path.svelte";
    import MainContent from "$lib/MainContent.svelte";
    import SubContent from "$lib/SubContent.svelte";
</script>

<Path pathSegments={["Home", "Community", "Assessment"]}></Path>
<Logo />
<MainContent>
    <h1>Heterosexuality Assessment Form</h1>
    <SubContent>
        <h2>Camera access failed</h2>
        <p>
            Either you declined access, your device does not have a camera or your browser does not support cameras.
            Please enable camera access in your browser's settings.
        </p>
    </SubContent>
    <Button href="../x2" text="Go back" />
</MainContent>
