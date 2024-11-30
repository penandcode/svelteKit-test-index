<script>
</script>

<main>
  <div class="step-container">
    <div class="step step-1">
      <div class="text-container">
        <div class="number">
          <p>1.</p>
        </div>
        <div class="text">Erstellen dein Lebenslauf</div>
      </div>
      <img src="profile_data.svg" alt="Profile data" />
    </div>
    <div class="connector-container">
      <img class="connector" src="connector.svg" alt="connector" />
    </div>
  </div>
  <div class="step-container">
    <div class="step step-2">
      <img src="task.svg" alt="Task" />
      <div class="text-container">
        <div class="number">
          <p>2.</p>
        </div>
        <div class="text">Erstellen dein Lebenslauf</div>
      </div>
    </div>
    <div class="connector-container">
      <img
        class="connector-reverse"
        src="connector-right.svg"
        alt="connector"
      />
    </div>
    <div class="step-container">
      <div class="step-3">
        <div class="text-container">
          <div class="number">
            <p>3.</p>
          </div>
          <div class="text">Mit nur einem Klick bewerben</div>
        </div>
        <img src="personal.svg" alt="Personal" />
      </div>
    </div>
  </div>
</main>

<style>
  .step-container {
    position: relative;
    margin-bottom: 250px;
  }
  .step {
    display: flex;
    justify-content: center;
    align-items: baseline;
    gap: 2rem;
  }
  .step-2 {
    background: linear-gradient(104deg, #e6fffa 0%, #ebf4ff 100%);
    padding-left: 200px;
  }
  .step-3 {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 2rem;
    padding-left: 200px;
    padding-top: 150px;
  }
  .number {
    width: 208px;
    height: 208px;
    background-color: #f7fafc;
    opacity: 0.5;
    border-radius: 50%;
  }
  .number p {
    color: #718096;
    font-size: 130px;
  }
  .text {
    color: #718096;
    letter-spacing: 0.9px;
    font-size: 30px;
  }
  img {
    position: relative;
    top: 50px;
  }
  .connector {
    position: absolute;
    right: 38lvw;
    top: 33lvh;
    z-index: 2;
  }
  .connector-reverse {
    position: absolute;
    right: 38lvw;
    top: 33lvh;
    z-index: 2;
  }
  .text-container {
    display: flex;
    align-items: baseline;
  }
  @media screen and (max-width: 1400px) {
    .step-container {
      padding: 0;
      margin: 0;
    }
    img {
      max-width: 100%;
    }
    .text {
      width: 185px;
      font-size: 15.75px;
    }
    .step {
      display: block;
    }
    .connector {
      display: none;
    }
    .connector-reverse {
      display: none;
    }
    .step-1 {
      display: flex;
      flex-direction: column-reverse;
    }
    .step-2 {
      background: transparent linear-gradient(134deg, #e6fffa 0%, #ebf4ff 100%)
        0% 0% no-repeat padding-box;
      display: flex;
      flex-direction: column-reverse;
    }
    .step-2,
    .step-3 {
      display: block;
      padding: 0;
    }
  }
</style>
