<script>
    import HAF from "$lib/HAF.svelte";
</script>

<HAF
        title="Come on you have to be at least a little bit fruity"
        choices={[
            {
                text: "Okay fine",
                href: "../../eligible"
            },
            {
                text: "Absolutely not",
                href: "../../ineligible"
            }
        ]}
></HAF>