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
	import { Button, Modal } from '@opentj/jui';
	let showModal = false;
</script>

<svelte:head>
	<title>Modals</title>
	<meta name="description" content="About Modals" />
</svelte:head>

<div class="mt-4">
	<Button class="btn btn-active" on:click={() => (showModal = !showModal)}>Open Modal</Button>
</div>

<Modal
	on:close={() => (showModal = false)}
	{showModal}
	modalClass="fixed top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 shadow-xl z-50 overflow-auto bg-white rounded-lg"
	backdropClass="absolute top-0 left-0 h-screen w-screen z-10 inset-0 overflow-y-auto bg-gray-400/50"
>
	<div class="flex flex-col m-8">
		<div class="p-1 flex justify-center text-lg">Header</div>
		<div class="p-1 mt-4">This is a Dialog</div>
		<div class="flex justify-end mt-4">
			<Button
				on:click={() => (showModal = false)}
				class="px-6 py-2  transition ease-in duration-200 uppercase rounded-full hover:bg-gray-800 hover:text-white border-2 border-gray-900 focus:outline-none"
			>
				Close
			</Button>
		</div>
	</div>
</Modal>

<div class="mt-4">
	<Button><a href="https://www.tailwind-kit.com/components/alert">更多用法 ...</a></Button>
</div>
