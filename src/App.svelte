<script>
	export let name;
	import Login from './Login.svelte';

	let user = { loggedIn: true };
	function toggle() {
		user.loggedIn = !user.loggedIn;
	}
</script>

<!-- Create Text field for username -->

  


<main>
	<h1>Hello, Welcome to {name}!</h1>
	<p>Please login below</p>
</main>







{#if user.loggedIn}
	<button on:click={toggle}>
		Log out
	</button>
{:else}
	
	<Login/>
{/if}


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