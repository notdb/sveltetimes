<script>
  import Tab from "./Tab.svelte";
  export let tabs;
  export let selectTabHandler;
  export let selectedTab;
</script>

<style>

.tabs {
  border-bottom: 1px solid lightgrey;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: row;
  width: 100%;
  height: 47px;
  background-color: #fff;
}
.tabs .topics {
  display: flex;
  justify-content: none;
  align-items: center;
  flex-direction: row;
}

.tabs .topics .title {
  font-size: 12px;
  letter-spacing: 1px;
  font-weight: bold;
}

</style>

<div class="tabs">
  <div class="topics">
    <span class="title">Trending Topics:</span>
    {#each tabs as tab}
      <Tab {tab}  selectTabHandler={()=>selectTabHandler(tab)} selectedTab={tab} />
    {/each}
  </div>
</div>
