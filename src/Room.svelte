<script>
	import { onMount } from 'svelte';

	let container, api;

	onMount(() => {
		const options = {
			roomName: `universitas-indonesia/ossd`,
			parentNode: container,
		};
		api = new window.JitsiMeetExternalAPI('meet.jit.si', options);

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
