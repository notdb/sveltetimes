<script>
  export let card;
  card = card;
</script>

<style>
.card {
  border-bottom: 1px solid lightgrey;
  display: flex;
  justify-content: space-between;
  align-items: none;
  flex-direction: column;
  background-color: #fff;
  width: 380px;
  margin-bottom: 16px;
  margin-right: 16px;
  padding: 24px;
}

.card .headline {
  font-size: 25px;
  font-family: Didot, serif;
}

.card .author {
  display: flex;
  justify-content: none;
  align-items: center;
  flex-direction: row;
  margin-top: 15px;
}

.card .author .img-container {
  padding-right: 10px;
  border-right: 1px solid lightgrey;
  height: 40px;
}

.card .author .img-container img {
  width: 40px;
}

.card .author span {
  padding-left: 10px;
  font-size: 12px;
  letter-spacing: 1px;
  font-weight: bold;
}

</style>

<div class="card">
  <div class="headline"> {card.headline} </div>
  <div class="author">
    <div class="img-container">
      <img src={card.img} alt={card.author}/>
    </div>
    <span>By {card.author} </span>
  </div>
</div>
