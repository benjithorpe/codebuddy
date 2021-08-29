<script>
	import Header from './Header.svelte';
	import Output from './Output.svelte';
	let htmlContent = "<h1>Hello World!</h1>";
	let cssContent = "h1{ color: royalblue; }";


	$: outputMessage = `<style>
											*{box-sizing: border-box}
											ul, ol{list-style-position: inside;}
												${cssContent}
											</style>
											${htmlContent}`;
</script>

<main>
	<Header/>
	<section class="editor">
		<section class="html">
			<div class="tag">HTML</div>
			<textarea name="" bind:value={htmlContent}></textarea>
		</section>

		<section class="css">
			<div class="tag">CSS</div>
			<textarea name="" bind:value={cssContent}></textarea>
		</section>
	</section>

	<Output outputMessage={outputMessage} />
</main>

<style>
	.editor{
		width: 40%;
	}
	.editor > section{ position: relative; }
	textarea{
    outline: 0;
		border: none;
		padding: 0.7em;
		width: 100%;
		height: 100%;
		overflow: auto;
		resize: none;
		line-height: 1.4;
		background-color: #fcfcfc;
	}
	div.tag{
		position: absolute;
		top: 0;
		right: 0;
		padding: .4em;
		font-size: 1.4rem;
		font-family: monospace;
		background-color: rgba(0, 0, 0, 0.836);
		color: white;
		font-weight: bold;
	}
</style>
