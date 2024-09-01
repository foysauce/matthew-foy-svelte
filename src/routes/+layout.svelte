<script lang="ts">
	import { ModeWatcher } from 'mode-watcher';
	import '../app.css';
	import DarkToggle from '$lib/components/DarkToggle.svelte';
</script>

<div class="flex flex-row justify-between border-b border-b-primary px-2 py-1">
	<a class="font-mono text-3xl text-accent" href="/">&lt;F&gt;</a>
	<div class="flex flex-row items-center justify-center gap-2">
		<h1 class="text-lg duration-300 ease-linear hover:text-accent">Home</h1>
		<h1 class="text-lg duration-300 ease-linear hover:text-accent">About</h1>
		<h1 class="text-lg duration-300 ease-linear hover:text-accent">Contact</h1>
		<DarkToggle />
	</div>
</div>

<ModeWatcher />

<slot></slot>
