<script lang="ts">
	import '../app.css';

	let { children } = $props();
</script>

<main class="container mx-auto flex items-center justify-center h-screen">
	{@render children()}
</main>

