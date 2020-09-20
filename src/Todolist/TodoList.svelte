<script>
import Card from "./components/Card.svelte";
import Input from "./components/Input.svelte";
import Footer from "./layouts/Footer.svelte";
import Header from "./layouts/Header.svelte";

let todos = ["Makan"];

const addTodos = (newTodo) =>{
    todos = [newTodo, ...todos];
}

const deleteTodo = (todo) =>{
    todos = todos.filter((t)=> t!== todo);
}
</script>

<Header/>
<main>
    <div class="input">
        <Input {addTodos} />
    </div>
    <div class="list">
        {#each todos as todo}
            <Card {deleteTodo} {todo} />
        {/each}
    </div>
</main>
<Footer/>

<style>
    .input{
        display: flex;
        justify-content: center;
        margin-top: 50px;
        flex-direction: column;
        align-items: center;
    }

    .list{
        display: flex;
        justify-content: center;
        margin-top: 50px;
        flex-direction: column;
        align-items: center;
        margin-left: auto;
        margin-right: auto;
    }
</style>