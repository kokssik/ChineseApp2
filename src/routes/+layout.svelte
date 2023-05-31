<script>
  import "../app.postcss";
  import Header from "../lib/components/Header.svelte";
</script>

<Header
  links={[
    { text: "Home", link: "/" },
    { text: "Lekce", link: "/lekce" },
    { text: "Hanzi", link: "/hanzi" },
    { text: "Stroke order", link: "/" },
    { text: "Admin", link: "/admin" },
    { text: "Amogus", link: "/lmao" },
  ]}
/>

<div class="container bg-gradient-to-r from-purple-100 to-white">
  <slot />
</div>

<style>
  .container {
    min-width: 100vw;
    min-height: 100vh;
  }
</style>
