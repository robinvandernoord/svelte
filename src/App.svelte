<script>
	let name = 'World';
	$: yesyesyes = `hallo? ${name}`;
	let test = 3;
	$: test2 = test + 1


	function askname(){
		name = prompt('he gozer hoe heet jij dan?') || name;
		test++
	}
</script>

<main>
	<h1>Hello {name}, how are you today?</h1>
	<p>This is a test if auto-deploy is working!</p>

	<button on:click={askname}>Zo heet ik niet!</button>

	<b>{yesyesyes}, {test}, {test2}</b>
	

</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>