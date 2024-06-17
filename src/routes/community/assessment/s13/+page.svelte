<script>
    import Button from "$lib/Button.svelte";
    import Logo from "$lib/Logo.svelte";
    import Path from "$lib/Path.svelte";
    import MainContent from "$lib/MainContent.svelte";
    import SubContent from "$lib/SubContent.svelte";
    import HorizontalContent from "$lib/HorizontalContent.svelte";
    import Label from "$lib/Label.svelte";

    function uploadGender() {
        const input = document.createElement("input")
        input.type = "file"

        input.click()

        input.onchange = (e) => {
            if (e.target.files.length > 0) {
                document.location.href = "eligible"
            }
        }
    }

    function uploadGenderFolder() {
        const input = document.createElement("input")
        input.type = "file"
        input.webkitdirectory = true
        input.multiple = true

        input.click()

        input.onchange = (e) => {
            if (e.target.files.length > 0) {
                document.location.href = "eligible"
            }
        }
    }
</script>

<Path pathSegments={["Home", "Community", "Assessment"]}></Path>
<Logo />
<MainContent>
    <h1>Heterosexuality Assessment Form</h1>
    <h2>Please upload your gender</h2>
    <p>
        To continue, please upload your gender.
    </p>
    <HorizontalContent>
        <Button onclick={uploadGender} text="Upload gender" />
        <Label>or</Label>
        <Button onclick={uploadGenderFolder} text="Upload folder of genders" />
    </HorizontalContent>
</MainContent>
