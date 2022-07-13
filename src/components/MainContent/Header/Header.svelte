<script>
  let riotGames = '/png/riotGames.png'
  let logo = '/png/logo.png'
</script>
<div class="Header">
    <div class="logo">
        <img src={riotGames} alt=""/>
    </div>
        <div class="separator"></div>
        <div class="logo">
            <img src={logo} alt=""/>
        </div>
</div>
<style>
    .Header{
        display: flex;
        width: 800px;
        height:200px;
        align-items: center;
    }
    .separator{
        padding-left: 60px;
        padding: 1px;
        padding-right: 60px;
        background-color: #fff;
        transform: rotate(90deg);
    }
</style>