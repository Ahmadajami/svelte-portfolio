<div class=" overflow-hidden">
	<ul class="nav box-border">
		<li class="name n-container">Ahmad Alajami</li>
		<li class="n-button hidden w-full md:block md:w-auto">
			<a href="https://github.com/Ahmadajami" aria-label="github-link">
				<i class="fa-brands fa-github"></i>
			</a>
		</li>

		<li class=" n-button hidden w-full md:block md:w-auto">
			<a href="mailto:a.alajami963@gmail.com" aria-label="mail-me">
				<i class="fa-regular fa-envelope"></i></a
			>
		</li>
	</ul>
</div>

<div class="holder n-container">
	<div class="news">Flutter Dev Free to Work</div>
</div>

<style>
	.nav {
		width: 100vw;
		height: 100px;
		background-color: #efeeee;
		box-shadow: 10px 10px 12px 0 rgba(0, 0, 0, 0.07);
		border-radius: 0 0 10px 10px;
		display: flex;

		justify-content: flex-end;
		align-items: center;
		padding: 0 3rem;
		list-style-type: none;
	}

	.nav li.name {
		margin-right: auto;
		font-size: 1.5rem;
		color: dimgray;
		font-weight: 900;
		text-shadow:
			2px 2px 4px rgba(0, 0, 0, 0.3),
			-2px -2px 4px rgba(255, 255, 255, 1);
	}

	.holder {
		overflow: hidden;
		color: #090909;
		padding: 0.7em 1.7em;
		font-size: 18px;
		border-radius: 0.5em;
		background: #e8e8e8;
		cursor: pointer;
		border: 1px solid #e8e8e8;
		transition: all 0.3s;
		box-shadow: -6px -6px 12px #ffffff;
	}
	.news {
		animation: slide 10s linear infinite;
	}

	@keyframes slide {
		0% {
			transform: translatex(0%);
		}

		100% {
			transform: translatex(100%);
		}
	}
</style>
