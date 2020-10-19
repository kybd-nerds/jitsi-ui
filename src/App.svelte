<script>
	import Landing from './Landing.svelte';
	import Room from './Room.svelte';
	import { roomName } from './stores';
</script>

{#if $roomName}
	<Room />
{:else}
	<Landing />
{/if}

<style>
	:global(body) {
		font-family: 'Quicksand', sans-serif;
	}
</style>
