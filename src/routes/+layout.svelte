<script lang="ts">
	import { ModeWatcher } from 'mode-watcher';
	import '../app.css';
	import DarkToggle from '$lib/components/DarkToggle.svelte';
</script>

<ModeWatcher />

<DarkToggle />

<slot></slot>
