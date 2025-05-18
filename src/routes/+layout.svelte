<script lang="ts">
	import '../app.css';
	
	let { children } = $props();
</script>

<main class="mx-auto px-4 sm:px-6 lg:px-8 py-8">
    {@render children()}
</main>
