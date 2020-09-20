<script>
    let age = 21;
</script>

<main>
    {#if age > 30}
        <h3>Senior Programmer</h3>
    {:else if age > 20}
        <h3>Junior Programmer</h3>
    {:else}
        <h3>Programmer Muda</h3>
    {/if}
</main>