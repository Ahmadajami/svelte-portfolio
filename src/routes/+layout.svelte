<script lang="ts">
	import Nav from '$lib/components/Nav.svelte';
	import '../app.css';
	let { children } = $props();
	let scrollY: number = $state(0);
	$effect(() => {
		alert('This is responsive');
	});
</script>

<svelte:window bind:scrollY />
<div class="flex h-full w-full flex-col overflow-hidden">
	<header class="z-10 flex-none">
		<Nav />
	</header>
	<div class=" flex h-full w-full flex-auto overflow-hidden" style="scrollbar-gutter: auto;">
		<div class="flex flex-1 flex-col space-y-8 overflow-x-hidden">
			{@render children()}
		</div>
	</div>
</div>
