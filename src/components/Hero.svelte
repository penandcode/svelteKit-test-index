<script>
  import RegisterButton from "./RegisterButton.svelte";
  import { createEventDispatcher } from "svelte";

  const dispatch = createEventDispatcher();
  let isButtonVisible = false;

  function handleVisibilityChange(event) {
    isButtonVisible = event.detail.isVisible;
    dispatch("visibilityChange", { isButtonVisible });
  }
</script>

<main>
  <div class="hero">
    <div class="container">
      <div>
        <div>
          <p>Deine Job website</p>
          <div class="btn">
            <RegisterButton on:visibilityChange={handleVisibilityChange} />
          </div>
        </div>
      </div>
      <div>
        <img src="undraw_agreement_aajr.svg" alt="register" />
      </div>
    </div>
  </div>
  <div class="register-btn">
    <RegisterButton />
  </div>
</main>

<style>
  .hero {
    background: transparent linear-gradient(102deg, #ebf4ff 0%, #e6fffa 100%) 0%
      0% no-repeat padding-box;
    width: 100%;
  }
  .container {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 144px;
    padding-top: 133px;
    padding-bottom: 67px;
  }
  .container img {
    height: 455px;
    width: 455px;
    border-radius: 50%;
    background-color: #fff;
  }
  p {
    width: 320px;
    letter-spacing: 1.95px;
    color: #2d3748;
    font-size: 65px;
    font-weight: bold;
    font-family: Lato;
    text-align: left;
  }
  .register-btn {
    display: none;
  }
  @media screen and (max-width: 1400px) {
    p {
      font-size: 42px;
      font-weight: 500;
      text-align: center;
    }
    .container {
      display: block;
    }
    .btn {
      display: none;
    }
    .register-btn {
      display: block;
      height: 100px;
      border-radius: 12px 12px 0px 0px;
      background: #ffffff 0% 0% no-repeat padding-box;
      box-shadow: 0px -1px 3px #00000033;
      margin-bottom: 100px;
    }
    .container img {
      height: 100lvw;
      width: 100lvw;
      border-radius: 0;
      background: transparent linear-gradient(102deg, #ebf4ff 0%, #e6fffa 100%)
        0% 0% no-repeat padding-box;
    }
  }
</style>
