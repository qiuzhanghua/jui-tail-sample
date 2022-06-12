<script context="module">
	import { browser, dev } from '$app/env';

	// we don't need any JS on this page, though we'll load
	// it in dev so that we get hot module replacement...
	export const hydrate = dev;

	// ...but if the client-side router is already loaded
	// (i.e. we came here from elsewhere in the app), use it
	export const router = browser;

	// since there's no dynamic data here, we can prerender
	// it so that it gets served as a static asset in prod
	export const prerender = true;
</script>

<script>
	import { Button } from '@opentj/jui';
	import { Icon } from '@steeze-ui/svelte-icon';
	import { Upload, Star } from '@steeze-ui/heroicons';
</script>

<svelte:head>
	<title>Buttons</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="mt-4" />

<div class="mt-4 flex justify-between">
	<Button
		type="button"
		class="py-2 px-4  bg-indigo-600 hover:bg-indigo-700 focus:ring-indigo-500 focus:ring-offset-indigo-200 text-white w-full transition ease-in duration-200 text-center text-base font-semibold shadow-md focus:outline-none focus:ring-2 focus:ring-offset-2  rounded-lg "
	>
		Button
	</Button>
	<Button
		type="button"
		class="py-2 px-4 flex justify-center items-center  bg-red-600 hover:bg-red-700 focus:ring-red-500 focus:ring-offset-red-200 text-white w-full transition ease-in duration-200 text-center text-base font-semibold shadow-md focus:outline-none focus:ring-2 focus:ring-offset-2  rounded-lg "
	>
		<Icon src={Upload} theme="solid" width={20} />
		Upload
	</Button>
	<Button
		type="button"
		class="py-2 px-4 flex justify-center items-center  bg-blue-600 hover:bg-blue-700 focus:ring-blue-500 focus:ring-offset-blue-200 text-white w-full transition ease-in duration-200 text-center text-base font-semibold shadow-md focus:outline-none focus:ring-2 focus:ring-offset-2  w-12 h-12 rounded-lg "
	>
		<Icon src={Upload} theme="solid" width={20} />
	</Button>
	<Button
		type="button"
		class="py-2 px-4  bg-pink-600 hover:bg-pink-700 focus:ring-pink-500 focus:ring-offset-pink-200 text-white w-full transition ease-in duration-200 text-center text-base font-semibold shadow-md focus:outline-none focus:ring-2 focus:ring-offset-2  rounded-full"
	>
		Follow
	</Button>

	<div class="flex items-center">
		<Button
			type="button"
			class="w-full flex items-center border-l border-t border-b text-base font-medium rounded-l-md text-black bg-white hover:bg-gray-100 px-4 py-2"
		>
			<Icon src={Star} theme="solid" width={20} />
			Star
		</Button>
		<Button
			type="button"
			class="w-full border text-base font-medium rounded-r-md text-black bg-white hover:bg-gray-100 px-4 py-2"
		>
			654
		</Button>
	</div>

	<div class="flex items-center">
		<button
			type="button"
			class="w-full border-l border-t border-b text-base font-medium rounded-l-md text-black bg-white hover:bg-gray-100 px-4 py-2"
		>
			Left
		</button>
		<button
			type="button"
			class="w-full border text-base font-medium text-black bg-white hover:bg-gray-100 px-4 py-2"
		>
			Center
		</button>
		<button
			type="button"
			class="w-full border-t border-b border-r text-base font-medium rounded-r-md text-black bg-white hover:bg-gray-100 px-4 py-2"
		>
			Right
		</button>
	</div>

	<Button
		class=" px-6 py-2  transition ease-in duration-200 uppercase rounded-full hover:bg-gray-800 hover:text-white border-2 border-gray-900 focus:outline-none"
	>
		Play
	</Button>

	<Button
		type="button"
		class="py-2 px-4  bg-gradient-to-r from-green-400 to-blue-500 text-white w-full transition ease-in duration-200 text-center text-base font-semibold shadow-md focus:outline-none focus:ring-2 focus:ring-offset-2 "
	>
		Free space
	</Button>
</div>

<div class="mt-4">
	<button><a href="https://www.tailwind-kit.com/components/buttons">更多用法 ...</a></button>
</div>
