<script>
    // your script goes here
    let count = 0;

    const increament=()=>{
        count += 1;
    }
</script>

<main>
    <button on:click={increament}>increament : {count}</button>
</main>

