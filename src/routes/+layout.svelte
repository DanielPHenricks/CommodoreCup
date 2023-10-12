<script>
	import Header from "./Header.svelte";
	import "./styles.css";
	import MissionStatement from "./MissionStatement.svelte";
	import Goals from "./Goals.svelte";
</script>

<div class="app">
	<div class="bgImage">
		<Header />
		<div class="mainPanel">
			<MissionStatement />
		</div>
		<div>
			<Goals />
		</div>
	</div>
</div>

<style>
	.mainPanel {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 20px;
	}
	.bgImage {
		background: url("images/Vandy.jpg") no-repeat center center fixed;
		background-size: cover;
		color: white;
		height: 100vh;
	}
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}
</style>
