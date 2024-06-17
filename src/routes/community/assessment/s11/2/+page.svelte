<script>
    import HAF from "$lib/HAF.svelte";
</script>

<!-- s11/1 - No -->

<HAF
        title="Are you attracted, romantically or sexually, to women?"
        choices={[
            {
                text: "Yes",
                href: "../x2"
            },
            {
                text: "No",
                href: "../eligible"
            }
        ]}
></HAF>