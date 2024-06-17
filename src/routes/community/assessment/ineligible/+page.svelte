<script>
    import Logo from "$lib/Logo.svelte";
    import Path from "$lib/Path.svelte";
    import MainContent from "$lib/MainContent.svelte";
    import SubContent from "$lib/SubContent.svelte";
    import FormattedDate from "$lib/FormattedDate.svelte";
</script>

<style>
    .sorry {
        padding: 1rem 2rem;
        width: 100%;
        background-color: #770202;
        font-weight: 500;
        color: white;
    }
</style>

<Path pathSegments={["Home", "Community", "Assessment"]}></Path>
<Logo />
<MainContent>
    <h1>Heterosexuality Assessment Form</h1>
    <SubContent>
        <h2>Result</h2>
        <div class="sorry">
            <p>You are not eligible to continue being a member of HTwins STEM.</p>
        </div>
        <p>
            You must leave by <FormattedDate date={new Date(2024, 5, 23)} /> unless your status changes. Starting from
            that date, you will not be able to talk in the server.
        </p>
        <p>
            You may now close this tab or window.
        </p>
    </SubContent>
</MainContent>
