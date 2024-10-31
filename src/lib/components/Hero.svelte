<script lang="ts">
	import TypeWriter from './TypeWriter.svelte';

	let text =
		'Aspiring software developer leveraging  Flutter and SvelteKit  to craft innovative and user-friendly applications. ';
</script>

<div
	class=" relative mx-auto flex max-w-screen-xl flex-none flex-col items-center p-8 px-4 sm:px-6 md:flex-row"
>
	<div class="flex items-center py-5 md:w-1/2 md:pb-20 md:pr-10 md:pt-10">
		<div class="text-left">
			<h2
				class="text-4xl font-extrabold leading-10 tracking-tight text-gray-800 sm:text-5xl sm:leading-none md:text-6xl"
			>
				Software
				<span class="font-bold text-purple-500">Developer</span>
				<span class="text-blueGray-500 rounded-full text-xl font-semibold">2.0</span>
			</h2>

			<TypeWriter {text} />
			<!--
				Aspiring software developer leveraging <strong class=" text-purple-400">Flutter</strong>
				and
				<strong class="text-purple-400">SvelteKit</strong> to craft innovative and user-friendly applications.-->

			<!-- Section  Button-->

			<div class="mt-5 sm:flex md:mt-8">
				<div class="hero-button mt-3 rounded-md sm:ml-3 sm:mt-0">
					<a
						href="#devStack"
						class="  flex w-full items-center justify-center rounded-md px-8 py-3 text-base font-medium leading-6 md:px-10 md:py-4 md:text-lg"
					>
						Dev Stack
					</a>
				</div>
				<div class="hero-button-s mt-3 rounded-md sm:ml-3 sm:mt-0">
					<a
						href="#devStack"
						class="  flex w-full items-center justify-center rounded-md px-8 py-3 text-base font-medium leading-6 md:px-10 md:py-4 md:text-lg"
					>
						Booke Me!
					</a>
				</div>
			</div>
		</div>
	</div>
	<!-- Image -->
	<div class=" flex h-full w-full items-center py-5 md:w-1/2 md:pb-20 md:pl-10 md:pt-10">
		<img
			class="h-auto w-full rounded-2xl object-cover"
			src="static/images/profile.webp"
			alt="Profile"
		/>
	</div>
</div>

<style>
	.hero-button {
		border: 2px solid rgba(255, 255, 255, 0.3);
		box-shadow:
			4px 4px 6px 0 rgba(0, 0, 0, 0.1),
			-4px -4px 6px rgba(255, 255, 255, 1);
		border-radius: 0.375rem;
		font-family: 'Roboto', sans-serif;
		cursor: pointer;
		transition:
			color 0.2s ease-out,
			transform 0.2s ease-out;
		color: dimgray;
	}
	.hero-button:hover {
		transform: scale(1.05);
		box-shadow:
			4px 4px 10px 0 rgba(0, 0, 0, 0.1),
			-4px -4px 10px rgba(255, 255, 255, 1);
		color: rgb(120, 28, 207);
	}
	.hero-button-s {
		background-color: rgb(120, 28, 207);
		border: 2px solid rgba(255, 255, 255, 0.3);
		box-shadow:
			4px 4px 6px 0 rgba(0, 0, 0, 0.1),
			-4px -4px 6px rgba(255, 255, 255, 1);
		border-radius: 0.375rem;
		font-family: 'Roboto', sans-serif;
		cursor: pointer;
		transition:
			color 0.2s ease-out,
			transform 0.2s ease-out;
		color: white;
	}
	.hero-button-s:hover {
		transform: scale(1.05);
		box-shadow:
			4px 4px 10px 0 rgba(0, 0, 0, 0.1),
			-4px -4px 10px rgba(255, 255, 255, 1);
	}
</style>
