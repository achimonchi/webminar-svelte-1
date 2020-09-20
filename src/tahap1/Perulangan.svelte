<script>
    let fruits = ["Pisang", "Apel", "Anggur"];
</script>

<div>
    {#each fruits as fruit, i}
        <li>{(i+1) + " " +fruit}</li>
    {/each}
</div>