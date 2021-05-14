<script>
	import MoneyForm from './components/MoneyForm.svelte';
	let modal;
</script>

<main>
	<form action="#">
		<MoneyForm />
	</form>
</main>


<style>
	main {
		width: 400px;
		margin: 0 auto;
		border-radius: 10px;
		background-color: #e3e3e3;
		padding: 20px;
		margin-top: 3em;
		
		box-sizing: border-box;

	}
	form {
		display: grid;
		justify-content: center;
	}
</style>