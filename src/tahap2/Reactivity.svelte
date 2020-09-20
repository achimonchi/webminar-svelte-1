<script>
    let qty = 3;
    let price = 2000;

    $: total = qty * price;
    $: {
        console.log(`QTY Changed to ${qty} `)
        console.log(`PRICE Changed to ${price} `)
        console.log(`TOTAL Changed to ${total} `)
    }
    
    qty = 100;

    price = 10;

    const handleClick = () =>{
        qty += 1;
        price += 10;
    }
</script>

<main>
    <p>Quantity : {qty}</p>
    <p>Price : {price}</p>
    <p>Total : {qty} * {price} = {total}</p>

    <button on:click={handleClick}>+</button>
</main>