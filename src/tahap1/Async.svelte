<script>
    const tunggu = () =>{
        return new Promise((resolve, reject)=>{
            // try{
            //     let a = parseInt("Reyhan");
                setTimeout(()=>{
                    console.log(30);
                    // resolve(b);
                    reject("Test Error");
                }, 3000)  
            // } catch(err){
            //     console.log("Error")
            // }
        })
    }

    $: waktu = tunggu();
</script>

<main>
    {#await waktu}
        Menunggu ...
    {:then res} 
        {res}
    {:catch error}
        Error : {error}
    {/await}
</main>