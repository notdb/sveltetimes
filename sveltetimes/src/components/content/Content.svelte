<script>
  import Tabs from "./Tabs.svelte";
  import { tabData, cardData } from "../../data.js";
  import Cards from "./Cards.svelte";
  console.log(tabData);
  console.log(cardData);

  let selected = "all";
  let tfToggle = "true";

  let newArray = cardData;

  let user = { loggedIn: false };

  function toggle() {
    user.loggedIn = !user.loggedIn;
  }

  function changeSelected(tab) {
    selected = tab;
    console.log(selected);
    toggle();
    filterCards();
  }

  function filterCards() {
    let selected11 = selected;

    if (selected11 == "all") {
      console.log(cardData, user.loggedIn, " wooo");
  
      return cardData;
    } else {
      newArray = cardData.filter(function(card) {
        return card.tab == selected11;
      });
      newArray = newArray;
 
      console.log(newArray, user.loggedIn, " woo");
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

  {#if user.loggedIn}
    <Cards cards={filterCards()} key={cardData.headline} />
  {:else}
    <Cards cards={filterCards()} key={cardData.headline} />
  {/if}
</div>
