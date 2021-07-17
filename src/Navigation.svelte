<script>
  import { createEventDispatcher } from 'svelte';

  let dispatch = createEventDispatcher();
  let isLightMode = true;
  const changeMode = () => {
    isLightMode = !isLightMode;
    dispatch("changeMode", isLightMode);
  }
</script>

<nav>
  <h1>This is the nav</h1>

  <button on:click="{changeMode}">
    {#if isLightMode}
    <span>Dark Mode</span>
    {:else}
    <span>Light Mode</span>
    {/if}
  </button>
</nav>

<style>
  nav{
    min-height: 5vh;
    display: grid;
    place-content: center;
    width: 100%;
    padding: .5em 0em;
  }

  button{
    display: inline-block;
    padding: .7em 1em;
    border: none;
    background-color: #13283a;
    color: white;
    font-weight: bold;
    cursor: pointer;
  }
</style>
