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

<slot />

<!-- <style>
  p {
    font-family: Arial, Helvetica, sans-serif;
  }

  h1 {
    font-family: Arial, Helvetica, sans-serif;
  }

  h2 {
    font-family: Arial, Helvetica, sans-serif;
  }
  a {
    font-family: Arial, Helvetica, sans-serif;
  }
  li {
    font-family: Arial, Helvetica, sans-serif;
  }
</style> -->
