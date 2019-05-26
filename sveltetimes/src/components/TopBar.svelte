<script>

</script>

<style>

.container {

  width: 100%;
  display: flex;
  justify-content: none;
  align-items: none;
  flex-direction: row;
  color: #fff;
  letter-spacing: 1px;
  padding: 0 10px;

}

.topbar1 {

 width: 100%;
  display: flex;
  justify-content: center;
  align-items: none;
  flex-direction: row;
  position: fixed;
  height: 44px;
  background-color: #333;


}


.containerleft {

 display: flex;
  justify-content: none;
  align-items: center;
  flex-direction: row;
  flex: 1;
  font-size: 11px;


}


  .containerleft span {
    cursor: pointer;
    margin-right: 25%;
    font-weight: bold;
  }


.containercenter {

  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: row;
  flex: 3;
  font-size: 9px;
}

 .containercenter span {
    cursor: pointer;
    margin-right: 5%;
  }

 .containercenter span:last-child {
    margin-right: 0;
  }

 .containercenter span:hover {
    text-decoration: underline;
  }





.containerright {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  flex-direction: row;
  flex: 1;
  font-size: 11px;
  font-weight: bold;
}

.containerright span {
    cursor: pointer;
  }

</style>

<div class="topbar1">
  <div class="container">
    <div class="containerleft">
      <span>TOPICS</span>
      <span>SEARCH</span>
    </div>
    <div class="containercenter">
      <span>GENERAL</span>
      <span>BROWNBAG</span>
      <span>RANDOM</span>
      <span>MUSIC</span>
      <span>ANNOUNCEMENTS</span>
    </div>
    <div class="containerright">
      <span>LOG IN</span>
    </div>
  </div>
</div>
