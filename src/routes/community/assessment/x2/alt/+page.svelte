<script>
    import HAF from "$lib/HAF.svelte";
</script>

<HAF
        title="Are you heterosexual?"
        choices={[
            {
                text: "Yes",
                href: "alt/1"
            },
            {
                text: "No",
                href: "alt/2"
            }
        ]}
></HAF>