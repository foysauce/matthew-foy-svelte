<script lang="ts">
	import { ModeWatcher } from 'mode-watcher';
	import '../app.css';
	import DarkToggle from '$lib/components/DarkToggle.svelte';
</script>

<div
	class="fixed top-0 z-10 flex w-full flex-row justify-between border-b border-b-primary bg-primary-foreground px-2 py-1"
>
	<a class="font-mono text-3xl text-accent" href="/">&lt;F&gt;</a>
	<div class="flex flex-row items-center justify-center gap-2">
		<h1 class="text-lg duration-300 ease-linear hover:text-accent">Home</h1>
		<h1 class="text-lg duration-300 ease-linear hover:text-accent">About</h1>
		<h1 class="text-lg duration-300 ease-linear hover:text-accent">Contact</h1>
		<DarkToggle />
	</div>
</div>

<div class="fixed bottom-0 right-0 p-3">
	<h1 class="font-mono">Let &lt;F&gt;: string = "Matthew Foy";</h1>
	<h1>[##.................................................................]</h1>
</div>

<ModeWatcher />

<slot></slot>
