<script>
    import Logo from "$lib/Logo.svelte";
    import Path from "$lib/Path.svelte";
    import MainContent from "$lib/MainContent.svelte";
    import SubContent from "$lib/SubContent.svelte";
    import FormattedDate from "$lib/FormattedDate.svelte";

    function getDate() {
        let date = new Date()
        date.setFullYear(date.getFullYear() + 1)

        return date
    }
</script>

<style>
    .congratulations {
        padding: 1rem 2rem;
        width: 100%;
        background-color: #0B7702;
        font-weight: 500;
        color: white;
    }
</style>

<Path pathSegments={["Home", "Community", "Assessment"]}></Path>
<Logo />
<MainContent>
    <h1>Heterosexuality Assessment Form</h1>
    <SubContent>
        <h2>Congratulations</h2>
        <div class="congratulations">
            <p>You are eligible to continue being a member of HTwins STEM.</p>
        </div>
        <p>
            You must complete this assessment again by <FormattedDate date={getDate()}/> to continue to talk in HTwins
            STEM.
        </p>
        <p>
            You may now close this tab or window.
        </p>
    </SubContent>
</MainContent>
