<script>
    export let date = new Date()
</script>

<b>
    {date.toLocaleDateString(undefined, {
        year: 'numeric',
        day: 'numeric',
        month: 'long'
    })}
</b>