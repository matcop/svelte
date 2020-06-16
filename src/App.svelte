<script>
  import About from "./components/About.svelte";
  import Text from "./components/Text.svelte";
  import Skills from "./components/Skills.svelte";
  export let name;
  export let hace;
  let logoSvelte = "https://arepa.s3.amazonaws.com/svelte-logo.png";
</script>

<style>
  /* indicara que esta section cambiara a toda la aplicacion */
  :global(body) {
    background: #f2eee2;
    color: #0084f6;
  }

  :global(:root) {
    /* esta es una convension de color */
    --theme-color: purple;
  }
  :global(body.dark-mode) {
    background-color: #1d3040;
    color: #bfc2c7;
  }

  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  main img {
    width: 30%;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<main>
  <h1>{name} {hace}🍊</h1>
  <About />
  <Skills />
  <Text anotherText="holitas" />
  <img src={logoSvelte} alt="el logo de svelte" />
</main>
