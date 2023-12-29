<script>
	import { onMount } from 'svelte';

	let navbarClass = 'invisible';

	onMount(() => {
		window.addEventListener('scroll', () => {
			navbarClass = window.scrollY >= window.innerHeight ? 'visible' : 'invisible';
		});
	});
</script>

<nav class="fixed top-0 w-full z-50 transition-all duration-500 {navbarClass}">
	<div class="flex flex-row">Drumbase</div>
</nav>
