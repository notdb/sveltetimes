<script>
export let tab;
export let selectTabHandler;
export let selectedTab;

let testName ="";
tab=tab;
if (tab == selectedTab) {
testName = "tab active-tab";
} else {
testName = "tab";
}


function newName(tab) {
selectTabHandler(tab);
}

</script>

<style>


.tab {
  display: flex;
  justify-content: none;
  align-items: center;
  flex-direction: row;
  color: #fff;
  background-color: #333;
  margin: 0 5px;
  padding: 2px 10px;
  font-size: 12px;
  letter-spacing: 2px;
  cursor: pointer;
  font-weight: bold;
}

.tab:hover {
  text-decoration: underline;
}


.active-tab {
  background-color: #fff;
  color: #333;
  border: 2px solid #333;
}

</style>

<div class={testName} on:click|preventDefault={newName}>
{tab}
</div>