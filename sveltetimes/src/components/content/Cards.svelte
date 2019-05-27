<script>
import Card from "./Card.svelte";
export let cards;
export let key;
</script>

<style>
.cards-container {
  display: flex;
  justify-content: space-evenly;
  align-items: none;
  flex-direction: row;
  width: 100%;
  margin-top: 16px;
  flex-wrap: wrap;
}

</style>

<div class="cards-container">
{#each cards as card}
<Card card={card} />
{/each}
</div>
