<script>
	export let name;
	import TopBar from "./components/TopBar.svelte";
</script>

<style>
.main {
  display: flex;
  align-items: center;
  flex-direction: column;
  background-color: #f1f1f1;
  color: #333;
  font-family: 'PT Sans', sans-serif;

}
</style>

<div class="main">
<TopBar />
</div>
