<script>
  export let outputMessage;
</script>

<section class="output">
  {@html outputMessage}
</section>

<style>
  section.output{
		padding: 0.2em;
		font-size: 1.6rem;
		text-align: left;
		line-height: 1.4;
		overflow-y: auto;
	}

	@media screen and (max-width: 768px){
		section.output{ order: -1; }
	}
</style>
