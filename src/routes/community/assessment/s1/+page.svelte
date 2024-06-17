<script>
    import HAF from "$lib/HAF.svelte";
</script>

<HAF
        title="What is your gender?"
        choices={[
            {
                text: "Female",
                href: "s11"
            },
            {
                text: "Male",
                href: "s12"
            },
            {
                text: "Something else",
                href: "s13"
            },
            {
                text: "Sarah",
                href: "ineligible"
            }
        ]}
></HAF>