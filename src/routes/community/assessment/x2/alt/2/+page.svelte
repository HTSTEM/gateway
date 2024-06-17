<script>
    import HAF from "$lib/HAF.svelte";
</script>

<HAF
        title="Are you lying?"
        choices={[
            {
                text: "Yes",
                href: "../../ineligible"
            },
            {
                text: "No",
                href: "../../eligible"
            }
        ]}
></HAF>