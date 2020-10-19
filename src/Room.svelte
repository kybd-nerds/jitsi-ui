<script>
	import { onMount } from 'svelte';
	import { roomName } from './stores';

	let container, api;

	onMount(() => {
		const options = {
			roomName: $roomName,
			parentNode: container,
		};
		api = new window.JitsiMeetExternalAPI('jitsi-nerds.cs.ui.ac.id', options);

		return () => api.dispose();
	});
</script>

<div bind:this={container} />

<style>
	div > :global(iframe) {
		position: absolute;
		top: 0;
		left: 0;
	}
</style>
