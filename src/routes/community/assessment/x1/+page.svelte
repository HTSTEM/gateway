<script>
    import Button from "$lib/Button.svelte";
    import Logo from "$lib/Logo.svelte";
    import Path from "$lib/Path.svelte";
    import MainContent from "$lib/MainContent.svelte";
    import SubContent from "$lib/SubContent.svelte";

    function uploadHeterosexuality() {
        const input = document.createElement("input")
        input.type = "file"

        input.click()

        input.onchange = (e) => {
            if (e.target.files.length > 0) {
                document.location.href = "ineligible"
            }
        }
    }
</script>

<Path pathSegments={["Home", "Community", "Assessment"]}></Path>
<Logo />
<MainContent>
    <h1>Heterosexuality Assessment Form</h1>
    <SubContent>
        <h2>Please provide more evidence that you are heterosexual</h2>
        <p>
            To prove that you are heterosexual, please upload more evidence. Examples of accepted evidence include:
        </p>
        <ul>
            <li>Blood donor card</li>
            <li>Light truck</li>
            <li>AXE body spray</li>
        </ul>
    </SubContent>
    <div>
        <Button onclick={uploadHeterosexuality} text="Upload evidence of heterosexuality" />
    </div>
</MainContent>
