<script>
  import Tabs from "./Tabs.svelte";
  import { tabData, cardData } from "../../data.js";
  import Cards from "./Cards.svelte";
  console.log(tabData);
  console.log(cardData);

  let selected = "all";
 
     let newArray = cardData;
    $: newArray;

  function changeSelected(tab) {
    selected = tab;
    console.log(selected);
    filterCards();
    
  }

  function filterCards() {
    let selected11 = selected;

    if (selected11 == "all") {
       console.log(newArray, ' wooo');
      return newArray;
    } else {
      newArray = cardData.filter(function(card) {
        return card.tab == selected11;
      });
      console.log(newArray, ' woo');
            return newArray;
    }
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
  <Tabs
    tabs={tabData}
    selectTabHandler={changeSelected}
    selectedTab={selected} />
  <Cards cards={filterCards()} key={cardData.headline} />
</div>
