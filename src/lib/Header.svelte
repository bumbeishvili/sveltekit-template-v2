<script>
	import { page } from '$app/state';
	import { resolve } from '$app/paths';

	/** @type {Array<{ path: import('$app/types').RouteId, title: string }>} */
	const pagesConfigs = [
		{
			path: '/',
			title: 'Index'
		},
		{
			path: '/components',
			title: 'Components'
		}
	];
</script>

<header class="bg-gray-100 w-full flex justify-center">
	<nav class="max-w-screen-xl w-full flex items-center justify-center bg-red-100 py-5 px-5">
		<ul class="flex w-full items-center">
			<li class="mr-12 mt-2"></li>
			{#each pagesConfigs as pageConfig (pageConfig.path)}
				<li
					class="text-gray-600 mr-5 font-regular"
					class:active={page.url.pathname === pageConfig.path}
				>
					<a href={resolve(pageConfig.path)}>{pageConfig.title}</a>
				</li>
			{/each}
		</ul>
	</nav>
</header>

<style>
	.active a {
		color: #000;
		font-weight: medium;
	}
</style>
