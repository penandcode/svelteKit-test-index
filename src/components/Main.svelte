<script>
  import Body from "./Body.svelte";
  import Button from "./Button.svelte";
  let selectedButton = "employees";

  const handleButtonClick = (buttonType) => {
    selectedButton = buttonType;
  };

  let isSmallScreen = window.innerWidth <= 600;

  const handleResize = () => {
    isSmallScreen = window.innerWidth <= 600;
  };

  window.addEventListener("resize", handleResize);

  $: paddingStyle = !isSmallScreen
    ? "padding: 0;"
    : selectedButton === "employees"
      ? "padding-left: 120px;"
      : selectedButton === "temporary-office"
        ? "padding-right: 120px;"
        : "";
</script>

<main>
  <div class="buttons" style={paddingStyle}>
    <Button
      className="employees"
      text="Arbeitnehmer"
      selected={selectedButton === "employees"}
      on:click={() => handleButtonClick("employees")}
    />
    <Button
      className=""
      text="Arbeitgeber"
      selected={selectedButton === "employers"}
      on:click={() => handleButtonClick("employers")}
    />
    <Button
      className="temporary-office"
      text="Temporärbüro"
      selected={selectedButton === "temporary-office"}
      on:click={() => handleButtonClick("temporary-office")}
    />
  </div>
  <div class="main-text">
    {#if selectedButton === "employees"}
      <p>Drei einfache Schritte zu deinem neuen Job</p>
    {:else if selectedButton === "employers"}
      <p>Drei einfache Schritte zu deinem neuen Mitarbeiter</p>
    {:else if selectedButton === "temporary-office"}
      <p>Drei einfache Schritte zur Vermittlung neuer Mitarbeiter</p>
    {/if}
  </div>
  <Body />
</main>

<style>
  .buttons {
    margin-top: 33px;
    margin-bottom: 55px;
    display: flex;
    justify-content: center;
    transition: color 0.9s ease;
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
      overflow-x: hidden;
    }
    .main-text p {
      color: #4a5568;
      font-size: 21px;
      letter-spacing: 0px;
      width: 280px;
    }
  }
</style>
