<script lang="ts">
	import { tweened, type Tweened, type Unsubscriber } from 'svelte/motion';

	import { linear } from 'svelte/easing';
	interface Props {
		text: string;
	}
	let { text }: Props = $props();

	let positionStore: Tweened<number> = $state(tweened(0, { easing: linear, duration: 3000 }));
	let position: number = $state(0);
	let cleanup = $state() as Unsubscriber;

	let animated_text = $state(text);

	$effect(() => {
		cleanup = positionStore.subscribe((val) => (position = val));
		positionStore.set(animated_text.length);

		return () => {
			if (cleanup) cleanup();
		};
	});
</script>

<p class="mx-auto mt-3 max-w-md text-base text-gray-500 sm:text-lg md:mt-5 md:max-w-3xl md:text-xl">
	{animated_text.substr(0, position)}<span class="cursor"> </span>
</p>

<style>
	.cursor {
		display: inline-block;
		width: 8px;
		height: 1.8rem;
		background: transparent;
		animation: blink 0.8s infinite;
	}

	@keyframes blink {
		0% {
			background: transparent;
		}
		40% {
			background: rgb(120, 28, 207);
		}
		to {
			background: rgb(120, 28, 207);
		}
	}
</style>
