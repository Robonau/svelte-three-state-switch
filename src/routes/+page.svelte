<script lang="ts">
	import ThreeStateSwitch from '$lib/three-state-switch.svelte';
	import { scale } from 'svelte/transition';
	let switchState: 'on' | 'off' | 'intermediate' = $state('intermediate');
</script>

<h1>Welcome to your library project</h1>
<p>Create your package using @sveltejs/package and preview/showcase your work with SvelteKit</p>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<div class="flex items-center justify-center space-x-2">
	<ThreeStateSwitch
		bind:state={switchState}
		size="lg"
		on="bg-green-900 dark:bg-green-300 cursor-pointer"
		intermediate="bg-yellow-600 dark:bg-yellow-500 cursor-pointer"
		off="bg-red-400 dark:bg-red-700 cursor-pointer"
	></ThreeStateSwitch>
	<ThreeStateSwitch bind:state={switchState} size="md">
		{#snippet onThumb()}
			<svg
				in:scale={{ delay: 100, duration: 100 }}
				out:scale={{ duration: 100 }}
				xmlns="http://www.w3.org/2000/svg"
				class="absolute top-0 text-base-token"
				viewBox="0 0 24 24"
			>
				<path fill="currentColor" d="M21 7L9 19l-5.5-5.5l1.41-1.41L9 16.17L19.59 5.59z" />
			</svg>
		{/snippet}

		{#snippet intermediateThumb()}
			<svg
				in:scale={{ delay: 100, duration: 100 }}
				out:scale={{ duration: 100 }}
				xmlns="http://www.w3.org/2000/svg"
				class="absolute top-0 text-base-token"
				viewBox="0 0 24 24"
			>
				<path fill="currentColor" d="M19 13H5v-2h14z" />
			</svg>
		{/snippet}

		{#snippet offThumb()}
			<svg
				in:scale={{ delay: 100, duration: 100 }}
				out:scale={{ duration: 100 }}
				xmlns="http://www.w3.org/2000/svg"
				class="absolute top-0 text-base-token"
				viewBox="0 0 24 24"
			>
				<path
					fill="currentColor"
					d="M19 6.41L17.59 5L12 10.59L6.41 5L5 6.41L10.59 12L5 17.59L6.41 19L12 13.41L17.59 19L19 17.59L13.41 12z"
				/>
			</svg>
		{/snippet}
	</ThreeStateSwitch>
	<ThreeStateSwitch
		bind:state={switchState}
		size="sm"
		onThumbBg="bg-green-900 dark:bg-green-300"
		intermediateThumbBg="bg-yellow-600 dark:bg-yellow-500"
		offThumbBg="bg-red-400 dark:bg-red-700"
		rounded="rounded-lg"
	></ThreeStateSwitch>
</div>
<div class="flex justify-center align-middle">
	{switchState}
</div>
