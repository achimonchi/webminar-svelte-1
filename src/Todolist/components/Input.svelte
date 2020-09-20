<script>
    export let addTodos;
    let todo = "";

    const add = () =>{
        addTodos(todo)
        todo="";
    }
</script>

<div class="form-input">
    <input type="text" placeholder="TodoList" bind:value={todo} >
    <button on:click={add}>
        Tambah
    </button>
</div>