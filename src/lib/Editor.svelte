<script>
  import { output } from "../lib/store.js";
  import Textarea from "./Textarea.svelte";

  let htmlContent = "<h1>Hello World!</h1>";
  let cssContent = "h1{ color: royalblue; }";

  $: $output = `<style>${cssContent}</style> ${htmlContent}`;
</script>

<div class="basis-full border-b-[1px] border-b-white">
  <Textarea bind:value={htmlContent} />
</div>

<div class="basis-full">
  <Textarea bind:value={cssContent} />
</div>
