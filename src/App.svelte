<script>
  import Header from "./components/Header.svelte";
  import Hero from "./components/Hero.svelte";
  import Main from "./components/Main.svelte";
  let isVisible = false;
  function handleVisibilityChange(event) {
    if (window.innerWidth <= 1400) {
      isVisible = true;
      return;
    }
    if (event.detail.isButtonVisible) {
      isVisible = true;
    } else {
      isVisible = false;
    }
  }
</script>

<main>
  <Header showRegister={!isVisible} />
  <Hero on:visibilityChange={handleVisibilityChange} />
  <Main />
</main>

<style>
  main {
    text-align: center;
    padding: 0;
    height: 100lvh;
    margin: 0 auto;
  }
</style>
