<script lang="ts">
	import { ModeWatcher } from 'mode-watcher';
	import '../app.css';
	import DarkToggle from '$lib/components/DarkToggle.svelte';
	import { onMount } from 'svelte';

	let y: number;
	let windowHeight: number;
	let fullHeight: number;
	let scrollableHeight: number;
	let scrollPercentage: number;
	$: scrollPercentage = Math.floor((y / scrollableHeight) * 100);

	onMount(() => {
		fullHeight = document.body.scrollHeight;
		windowHeight = window.innerHeight;
		scrollableHeight = fullHeight - windowHeight;
	});
</script>

<svelte:window bind:scrollY={y} />

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

<div class="fixed bottom-0 right-0 p-4">
	<h1 class="mx-1 font-mono">
		Let <span class="text-accent">&lt;F&gt;:</span> string =
		<span class="text-accent">"MATTHEW FOY"</span>
	</h1>
	<div class="">
		[
		<span>{'#'.repeat(Math.floor(scrollPercentage / 3.25))}</span>
		<span>{'. '.repeat(35 - Math.floor(scrollPercentage / 2.85))}</span>
		]
	</div>
</div>

<ModeWatcher />

<slot></slot>
