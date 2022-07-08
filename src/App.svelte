<script>
  import "./assets/app.css";
  import { output } from "./lib/store.js";
  import Editor from "./lib/Editor.svelte";
  import Output from "./lib/Output.svelte";
</script>

<main class="grid h-screen grid-cols-2">
  <!-- Input section -->
  <section class="flex flex-col">
    <Editor />
  </section>

  <!-- Output section -->
  <section>
    <Output outputMessage={$output} />
  </section>
</main>
