<script>
  import Body from "./Body.svelte";
  import Button from "./Button.svelte";
</script>

<main>
  <div class="buttons">
    <Button className="employees" text="Arbeitnehmer" selected />
    <Button className="" text="Arbeitgeber" />
    <Button className="temporary-office" text="Temporärbüro" />
  </div>
  <div class="main-text">
    <p>Drei einfache Schritte zu deinem neuen Job</p>
  </div>
  <Body />
</main>

<style>
  .buttons {
    margin-top: 33px;
    margin-bottom: 55px;
    display: flex;
    justify-content: center;
  }
  .main-text {
    color: #4a5568;
    font-size: 40px;
    letter-spacing: 0px;
    text-align: center;
  }

  .main-text p {
    width: 390px;
    color: #4a5568;
    font-size: 40px;
    letter-spacing: 0px;
    text-align: center;
    margin-inline: auto;
  }

  @media screen and (max-width: 1400px) {
    .buttons {
      overflow-x: scroll;
    }
    .main-text p {
      color: #4a5568;
      font-size: 21px;
      letter-spacing: 0px;
      width: 280px;
    }
  }
</style>
