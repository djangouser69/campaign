<script>
  const { children } = $props();
  import { email } from "$lib/index.js";
</script>

<nav>
  <a href="/">Home</a>
  <a href="/about">About</a>
  <a href="/mission">Mission</a>
  <a href={`mailto:${email}`}>Contact</a>
</nav>
<main>
  {@render children()}
</main>

<style>
  :global(html) {
    font-family: sans-serif;
    background: #e3d7d7;
  }
  :global(html *) {
    box-sizing: border-box;
    /* padding: 0;
    margin: 0; */
  }
  nav {
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 1rem;
    justify-content: space-evenly;
    border-bottom: 2px solid black;
    a {
      text-decoration: none;
      color: navy;
      font-size: 1.2rem;
      font-weight: 550;
      transition: 0.7s;
      &:hover {
        color: red;
      }
    }
  }
  main {
    display: flex;
    flex-direction: column;
    padding: 1rem;
    margin: 0;
  }
</style>
