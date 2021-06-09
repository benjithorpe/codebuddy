<script>
	let htmlOutput = `<!DOCTYPE html>
<html lang='en'>
<head>
  <meta charset='utf-8'>
  <meta name='viewport' content='width=device-width,initial-scale=1'>
  <title>Simple HTMl Editor</title>

  <style>
    h1{ color: royalblue; }
  </style>
</head>

<body>
  <h1>Hello World!!</h1>
</body>
</html>`;
</script>

<main>
	<section class="editor">
		<textarea name="" id="" bind:value="{htmlOutput}"
placeholder=""></textarea>
	</section>

	<section class="output">
		{@html htmlOutput}
	</section>
</main>

<style>
	main {
		display: flex;
		text-align: center;
		height: 100vh;
	}

	main section{
		border: 1px solid rgba(0, 0, 0, 0.3);
		flex-basis: 100%;
		height: 100%;
	}

	section.output{
		padding: 0.5em;
		font-size: 1.6rem;
	}

	textarea{
		outline-color: #999;
		border: none;
		padding: 0.5em;
		min-width: 200px;
		min-height: 200px;
		width: 100%;
		height: 100%;
		color: #444;
	}

	@media (min-width: 768px) {}
</style>
