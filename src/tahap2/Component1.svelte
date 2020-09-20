<script>
    import Component2 from "./Component2.svelte";
    import Button from "./Button.svelte";
    let mhs = {
        name : "NooBeeID",
        age : 21
    }

    let text = "<h1>Ini TAG Heading 1</h1>";

</script>

<main>
    <Component2 
        {...mhs}
    />

    <Button>
        Primary
    </Button>
    <Button>
        Secondary
        <a href="camp.noobee.id">NooBeeCamp</a>
    </Button>

    <!-- HTML Tag -->
    {@html text}
</main>

<style>
    a{
        color:lightblue;
    }
</style>