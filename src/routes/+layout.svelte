<script>
  import "../app.postcss";
  import HeaderLink from "../lib/components/HeaderLink.svelte";
</script>

<div class="mx-52">
  <div class="flex flex-row justify-between">
    <HeaderLink text="Home" link="/" />
    <HeaderLink text="Lekce" link="/lekce" />
    <HeaderLink text="Hanzi" link="/hanzi" />
    <HeaderLink text="Stroke Order" link="/stroke_order" />
    <HeaderLink text="Admin" link="/admin" />
    <HeaderLink text="amogus" link="/lmao" />
  </div>
</div>

<div class="container bg-gradient-to-r from-purple-100 to-white">
  <slot />
</div>

<style>
  .container {
    min-width: 100vw;
    min-height: 100vh;
  }
</style>
