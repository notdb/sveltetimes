<script>
import Card from "./Card.svelte";
export let cards;
export let key;
</script>

<style>
</style>

<div class="cards-container">
{#each cards as card}
<Card card={card} />
{/each}
</div>
