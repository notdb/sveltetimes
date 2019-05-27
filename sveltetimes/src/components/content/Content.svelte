<script>
  import Tabs from "./Tabs.svelte";
  import { tabData, cardData } from "../../data.js";

  console.log(tabData);
  console.log(cardData);

  let selected = "all";

function changeSelected(tab) {
    selected = tab;
    console.log(selected);
  }
</script>

<style>
  .content-container {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
</style>

<div class="content-container">
  <Tabs tabs={tabData} selectTabHandler={changeSelected} selectedTab={selected}/>
</div>
