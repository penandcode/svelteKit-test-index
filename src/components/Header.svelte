<script>
  export let showRegister = false;
</script>

<main>
  <div class="top-header"></div>
  <header>
    <div class="buttons">
      {#if showRegister}
        <button class="register">Kostenlos Registrieren</button>
      {/if}
      <button class="login">Login</button>
    </div>
  </header>
</main>

<style>
  main {
    position: fixed;
    z-index: 999999;
  }
  header {
    height: 67px;
    border-radius: 0 0 12px 12px;
    background: #fff;
    display: flex;
    flex-direction: column;
    align-items: end;
    justify-content: center;
    box-shadow: 0px 3px 6px #00000029;
    width: 100vw;
  }
  .top-header {
    height: 5px;
    width: 100%;
    background: linear-gradient(90deg, #319795 0%, #3182ce 100%);
  }
  .login {
    width: 100px;
    border: none;
    background: none;
    font-size: 14px;
    font-family: Lato;
    font-weight: 600;
    letter-spacing: 0.84px;
    color: #38b2ac;
  }
  .register {
    font: normal normal 600 14px/17px Lato;
    letter-spacing: 0.84px;
    color: #319795;
    border: none;
    background: #ffffff 0% 0% no-repeat padding-box;
    border: 1px solid #cbd5e0;
    border-radius: 12px;
    padding-inline: 30px;
    font-size: 12px;
  }
  .login:hover {
    text-decoration: underline;
    cursor: pointer;
  }
</style>
