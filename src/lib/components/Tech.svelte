<script lang="ts">
	import type { Snippet } from 'svelte';

	type Props = {
		text: string;
		children: Snippet;
	};
	let { text, children }: Props = $props();
</script>

<div class="n-container flex flex-row">
	<div class="toggle">
		<input type="checkbox" />
		<span class="button"></span>
		<span class="label">
			{@render children()}
		</span>
	</div>
	<div class=" m-2 ml-2 text-black">
		{text}
	</div>
</div>

<style>
	.toggle {
		display: inline-block;
		margin-right: 1rem;
	}

	.toggle {
		position: relative;
		height: 100px;
		width: 100px;
	}

	.toggle .button {
		transition: all 300ms cubic-bezier(0.23, 1, 0.32, 1);
		box-shadow:
			0 15px 25px -4px rgba(0, 0, 0, 0.5),
			inset 0 -3px 4px -1px rgba(0, 0, 0, 0.2),
			0 -10px 15px -1px rgba(255, 255, 255, 0.6),
			inset 0 3px 4px -1px rgba(255, 255, 255, 0.2),
			inset 0 20px 30px 0 rgba(255, 255, 255, 0.2);
		border-radius: 68.8px;
		position: absolute;
		background: #eaeaea;
		margin-left: -34.4px;
		margin-top: -34.4px;
		display: block;
		height: 68.8px;
		width: 68.8px;
		left: 50%;
		top: 50%;
	}

	.toggle .label {
		transition: color 300ms ease-out;
		line-height: 101px;
		text-align: center;
		position: absolute;
		font-weight: 700;
		font-size: 28px;
		display: block;
		opacity: 0.9;
		height: 100%;
		width: 100%;
		color: rgba(0, 0, 0, 0.9);
	}

	.toggle input {
		opacity: 0;
		position: absolute;
		cursor: pointer;
		z-index: 1;
		height: 100%;
		width: 100%;
		left: 0;
		top: 0;
	}

	.toggle input:active ~ .button {
		filter: blur(0.5px);
		box-shadow:
			0 12px 25px -4px rgba(0, 0, 0, 0.4),
			inset 0 -8px 30px 1px rgba(255, 255, 255, 0.9),
			0 -10px 15px -1px rgba(255, 255, 255, 0.6),
			inset 0 8px 25px 0 rgba(0, 0, 0, 0.4),
			inset 0 0 10px 1px rgba(255, 255, 255, 0.6);
	}
</style>
