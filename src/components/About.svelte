<script>
  let someText = `Frontend Developer at MatCia.`;
  let count = 0;
  let styles = { darkMode: false };

  function sumar() {
    count += 1;
  }
  function resetClick() {
    count = 0;
  }
  function toggle() {
    styles.darkMode = !styles.darkMode;
    window.document.body.classList.toggle("dark-mode");
  }
</script>

<style>
  p {
    color: var(--theme-color);
  }
</style>

<div class="About">

  <button on:click={sumar}>click {count === 0 ? '' : count}</button>
  {#if count > 0}
    <button on:click={resetClick}>Reset</button>
  {/if}

  {#if !styles.darkMode}
    <p>{someText}</p>
  {:else}
    <p>hola darkMode</p>
  {/if}

  <button on:click={toggle}>Dark Mode</button>
</div>
