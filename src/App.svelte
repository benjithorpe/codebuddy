<script>
	import Output from './Output.svelte';
	import Navigation from './Navigation.svelte';
	let htmlContent = "<h1>Hello World!</h1>";
	let cssContent = "h1{ color: royalblue; }";

	$: outputMessage = `<style>${cssContent}</style> ${htmlContent}`;
	let mode = true;
	const changeMode = (e) => {
		if(e.detail){
			console.log("Light Mode");
			mode = e.detail;
		}else{
			console.log("Dark Mode");
			mode = e.detail;
		}
	}
</script>

<Navigation on:changeMode={changeMode}/>
<main>
	<section class="editor mode" class:darkMode={mode}>
		<section class="html">
			<div class="tag">HTML</div>
			<textarea name="" bind:value="{htmlContent}"></textarea>
		</section>

		<section class="css">
			<div class="tag">CSS</div>
			<textarea name="" bind:value="{cssContent}"></textarea>
		</section>
	</section>

	<Output outputMessage={outputMessage} />
</main>

<style>
	.editor > section{ position: relative; }
	/* .editor textarea{ background-color: #f4f4f4; } */
	textarea{
    outline: 0;
		border: none;
		padding: 0.7em;
		width: 100%;
		height: 100%;
		overflow: auto;
		resize: none;
		line-height: 1.4;
		background-color: #f4f4f4;
	}

	.mode textarea{
		background-color: orange;
		font-size: 3rem;
		color: blue;
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
