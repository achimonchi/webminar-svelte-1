<script>
    export let todo = "";
    export let deleteTodo;

    const deleteData = () =>{
        deleteTodo(todo)
    }
</script>

<div class="card">
    <div class="left">
        <h3>{todo}</h3>
    </div>
    <div class="right">
        <button on:click={deleteData}>Delete</button>
    </div>
</div>

<style>
    .card{
        display: flex;
        /* border:1px solid #aaa; */
        width: 300px;
        align-items: center;
        padding: 10px 20px;
        border-radius: 5px;
        box-shadow: 0px 5px 20px rgba(0,0,0,.2);
        margin-bottom: 20px;
    }

    .left{
        flex: 2;
    }

    .right{
        flex:1;

    }

    .right button{
        width: 100%;
    }
</style>