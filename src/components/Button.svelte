<script>
  export let text = "Click Me";
  export let selected = false;
  export let className = "employees";
</script>

<main>
  <button class={className} style={`${selected ? "background:#81E6D9; border:1px solid #81E6D9" : "background:#FFF; border:1px solid #CBD5E0"}`}>
    <p style={`${selected ? "color:#E6FFFA" : "color: #319795"}`}>
      {text}
    </p>
  </button>
</main>

<style>
  button {
    padding: 12px 32px;
    border: none;
    cursor: pointer;
    width: 160px;
    height: 40px;
  }
  p {
    font-weight: 600;
    font-size: 14px;
    font-family: Lato;
    letter-spacing: 0.84px;
  }
  .employees {
    border-radius: 12px 0px 0px 12px;
  }
  .temporary-office{
    border-radius: 0px 12px 12px 0px ;
  }
</style>
