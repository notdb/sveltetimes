<script>
export let card;
card=card;
</script>

<style>
</style>

<div class="card">
<div class="headline">
{card.headline}
</div>
<div class="author">
     <div class="img-container">
     <img src={card.img} />
     </div>
     <span>By {card.author} </span>
     </div>
</div>