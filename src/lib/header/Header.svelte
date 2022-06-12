<script>
	import { page } from '$app/stores';
</script>

<header class="bg-gray-200">
	<nav>
		<ul class="flex justify-around">
			<li class:active={$page.url.pathname === '/'}>
				<button class="btn btn-link"><a sveltekit:prefetch href="/">Home</a></button>
			</li>
			<li class:active={$page.url.pathname === '/about'}>
				<button class="btn btn-link"><a sveltekit:prefetch href="/about">About</a></button>
			</li>
			<li class:active={$page.url.pathname === '/samples'}>
				<button class="btn btn-link"><a sveltekit:prefetch href="/samples">Samples</a></button>
			</li>
		</ul>
	</nav>

	<div class="corner">
		<!-- TODO put something else here? github link? -->
	</div>
</header>
