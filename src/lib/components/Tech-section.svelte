<script lang="ts">
	import Tech from './Tech.svelte';
	const tech_text = [
		{
			text: 'Flutter, a breeze to code with, Builds apps with flair, swift and fluid.',
			icon: `<i class="fa-brands fa-flutter"></i>`
		},
		{
			text: 'Vue.js, a progressive JavaScript framework, creating engaging user interfaces with ease.',
			icon: `<i class="fa-brands fa-vuejs"></i>`
		},
		{
			text: 'Svelte: Your lightweight backend in a box. Build full-stack apps with ease, no server setup required.',
			icon: `<img class="z-1 mx-0 my-4" src='/images/svelte-logo.svg' alt="svelte logo" />`
		},
		{
			text: 'PocketBase: Your lightweight backend in a box. Build full-stack apps with ease, no server setup required.',
			icon: `<img class="z-1 mx-0 my-8" src='/images/pb.svg' alt="svelte logo" />`
		}
	];
</script>

<div class=" n-con w-max">My Tech Stack <i class="fa-brands fa-stack-overflow"></i></div>
<div id="#devstack" class=" grid grid-cols-1 gap-8 md:grid-cols-2">
	{#each tech_text as el}
		<div>
			<Tech text={el.text}>
				{@html el.icon}
			</Tech>
		</div>
	{/each}
</div>

<style>
	.n-con {
		color: black;
		padding: 0.5rem 1.5rem;
		border: 2px solid rgba(255, 255, 255, 0.3);
		box-shadow:
			4px 4px 6px 0 rgba(0, 0, 0, 0.1),
			-4px -4px 6px rgba(255, 255, 255, 1);
		border-radius: 10px;
		font-family: 'Roboto', sans-serif;

		transition:
			color 0.2s ease-out,
			transform 0.2s ease-out;
	}
</style>
