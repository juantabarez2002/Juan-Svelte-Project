<!-- Minimal Hello World in SvelteKit (Tailwind styles) -->
<script lang="ts">
	// Simple reactive counter example
	let count = 0;

	function increment() {
		count += 1;
	}
</script>

<main class="flex min-h-screen items-center justify-center bg-gray-100">
	<!-- Card container centered on the page -->
	<div
		class="mx-4 w-full max-w-3xl -translate-y-8 transform rounded-xl bg-white p-8 text-gray-900 shadow-lg sm:mx-6 md:mx-0"
	>
		<div class="mx-auto max-w-2xl">
			<h1 class="text-4xl font-extrabold text-indigo-600">Hello World!</h1>
			<p class="mt-2 text-lg text-gray-600">This is my first SvelteKit component.</p>

			<!-- Interactive example: counter -->
			<div class="mt-6 flex items-center gap-4">
				<button
					on:click={increment}
					class="cursor-pointer rounded-md bg-indigo-600 px-4 py-2 text-white hover:bg-indigo-700 focus:ring-2 focus:ring-indigo-300 focus:outline-none"
				>
					Click me
				</button>

				<span class="text-gray-700">You clicked {count} {count === 1 ? 'time' : 'times'}.</span>
			</div>

			<p class="mt-6 text-sm text-gray-500">
				See the docs at <a href="https://svelte.dev" class="text-indigo-600 underline">svelte.dev</a>
			</p>
		</div>
	</div>
</main>
