<script>
import BeforeUpdate from "./components/BeforeUpdate.svelte";
let show=false;
</script>

<main style="background:lightgray">
			<BeforeUpdate />
</main>
<style>
	:global(h1) {
		color:crimson
	}
	main { 
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}
	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>