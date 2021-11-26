<script lang="ts">

	let count:number = 0;

	const increment = () => {
		count++;
	};

	const decrement = () => {
		count--;
	};

	const reset = () => {
		count = 0;
	}

</script>

<!-- link bootstrap CDN in header -->
<svelte:head>
	<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
	<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM" crossorigin="anonymous"></script>
</svelte:head>

<!-- HTML markup -->
<main>
	<h1> This is an Example Svelte App</h1>
	<br />
	<h3>It uses a little bit of bootstrap too</h3>
	<br />
	<h3>Oh, and TypeScript as well</h3>
	<br />
	<button class="btn btn-primary" on:click={increment}>Increment</button>
	<button class="btn btn-secondary" on:click={decrement}>Decrement</button>
	<button class="btn btn-danger" on:click={reset}>Reset</button>
	<br />
	<h1>Count: {count}</h1>
</main>
<!-- End of HTML markup -->

<style>
	main {
		text-align: center;
		padding: 1em;
		/*max-width: 240px;*/
		margin: 0 auto;
	}

	button {
		margin: 1rem;
		padding: 1rem;
		border-radius: 20px;
	}

	h1 {
		font-family: sans-serif;
		width: auto;
	}

	h3 {
		font-family: sans-serif;
	}
</style>