<script>
	import Hero from '$lib/components/Hero.svelte';
	import TechSection from '$lib/components/Tech-section.svelte';
	import TypeWriter from '$lib/components/TypeWriter.svelte';
</script>

<Hero />
<div class=" skull my-h n-container my-5 flex flex-col space-y-4 p-4">
	<section id="devStack">
		<TechSection />
	</section>
</div>
<div class="flex h-screen items-center justify-center text-center">
	<div class=" aspect-2">
		<img class="" src="/images/meme.jpg" alt="meme" />
	</div>
	<TypeWriter text="Comming More ..." />
</div>

<style>
	.my-h {
		height: 50svh;
	}
	@media (min-width: 640px) {
		.skull:h-screen {
			height: 100vh;
			margin-bottom: 4rem;
		}
	}
</style>
