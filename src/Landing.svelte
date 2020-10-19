<script>
	import { roomName } from './stores';

	let name;
	function join() {
		$roomName = name;
	}
</script>

<div class="wrapper">
	<header>
		<nav>
			<img src="jassets/logo.png" alt="logo universitas indonesia" />
			<h2>Keyboard Nerds</h2>
		</nav>
		<section>
			<div>
				<div>
					<h1>Premium and Limitless Classroom Meeting.</h1>
					<h1>Now Free for UI Students.</h1>
					<p>Powered by Jitsi</p>
				</div>
				<div><input type="text" bind:value={name} /> <button on:click={join}>Join</button></div>
			</div>
			<div><img src="jassets/preview.png" alt="classroom preview" /></div>
		</section>
		<div>
			<small>Open Source Software Development</small>
			<small>Faculty of Computer Science, University of Indonesia</small>
		</div>
	</header>
</div>

<style>
	.wrapper {
		background-color: rgb(249, 251, 254);
	}
	.wrapper > * {
		max-width: 84rem;
		margin: 0 auto;
	}

	header {
		min-height: 100vh;

		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-between;

		padding: 1em;
		background-color: rgb(249, 251, 254);
	}

	header nav {
		width: 100%;
		display: flex;
		align-items: center;
	}
	header nav :not(:first-child) {
		margin-left: 0.5em;
	}
	header nav img {
		height: 6em;
	}
	header > div {
		display: grid;
		text-align: center;
	}

	header section {
		display: grid;
		gap: 2em;
		grid-template-columns: 1fr 1fr;
		align-content: stretch;
		text-align: left;
	}
	header section > :first-child {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}
	header section > :last-child {
		padding: 1.5em;
		border-radius: 0.5em;
		box-shadow: 0 1px 2px 0 rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
	}
	header section img {
		width: 100%;
		border-radius: inherit;
	}

	header section > :first-child > div:last-child {
		display: grid;
		gap: 0.5em;
		grid-template-columns: 1fr auto;
	}
	/* main {
		max-width: 84em;
		padding: 2em 0;
		margin: 0 auto;

		display: grid;
		gap: 2em;
		grid-template-columns: 2fr 3fr;

		line-height: 1.5;
	}
	main > :not(.description) {
		border: 1px solid red;
	}
	.description :not(:first-child) {
		margin-top: 1em;
	}
	*/

	h1 {
		font-size: 3rem;
		font-weight: bolder;
	}
	h1 + p {
		margin-top: 0.5em;
		font-size: 1.5rem;
	}
	h2 {
		font-size: 3rem;
	}
	input {
		border: 1px solid #000;
	}
</style>
