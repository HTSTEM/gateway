<script>
    import Button from "$lib/Button.svelte";
    import Logo from "$lib/Logo.svelte";
    import Path from "$lib/Path.svelte";
    import MainContent from "$lib/MainContent.svelte";
    import SubContent from "$lib/SubContent.svelte";
    import FormattedDate from "$lib/FormattedDate.svelte";
</script>

<Path pathSegments={["Home", "Legal"]}></Path>
<Logo />
<MainContent>
    <h1>Privacy policy</h1>
    <p>
        We do not collect your data nor use any tracking technology, including cookies. All processing happens locally,
        on your device. However, Cloudflare may collect and process your data in accordance with their privacy policy.
    </p>
    <Button href="https://www.cloudflare.com/en-gb/privacypolicy/" text="View Cloudflare's privacy policy"/>
    <p>
        If you answered the assessment form, your browser may store the choices you have made in the
        form. If this is a concern for you, consult your browser's documentation on how to delete this data.
    </p>
    <p>
        (Also, if you couldn't tell, none of the content on this website is true.)
    </p>
</MainContent>
