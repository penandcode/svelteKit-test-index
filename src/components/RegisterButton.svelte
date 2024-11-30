<script>
  import { createEventDispatcher, onMount } from "svelte";

  const dispatch = createEventDispatcher();
  let button;

  const observer = new IntersectionObserver(
    ([entry]) => {
      const isVisible = entry.isIntersecting;
      dispatch("visibilityChange", { isVisible });
    },
    { root: null, threshold: 0 }
  );

  onMount(() => {
    if (button) {
      observer.observe(button);
    }
    return () => observer.disconnect();
  });
</script>

<main>
  <button bind:this={button} class="signup">Kostenlos Registrieren</button>
</main>

<style>
  .signup {
    margin-top: 65px;
    background: transparent linear-gradient(95deg, #319795 0%, #3182ce 100%) 0%
      0% no-repeat padding-box;
    border-radius: 12px;
    width: 320px;
    color: #e6fffa;
    letter-spacing: 0.84px;
    font-size: 14px;
  }
</style>
