<script>
	export let outputMessage;
</script>

<section class="output">
	{@html outputMessage}
</section>

<style>
	section {
		/* padding: 0.2em; */
		font-size: 1.6rem;
		text-align: left;
		/* line-height: 1.4; */
		overflow-y: auto;
		border: none;
	}
/* 	@media screen and (max-width: 768px) {
		section {
			order: -1;
		}
	} */
</style>
