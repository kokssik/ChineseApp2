<script>
  import List from "$lib/components/HanziCard.svelte";
  import Seznam from "$lib/components/Seznam.svelte";
</script>

<div>
  <h1 class="text-center font-sans">Seznam lekcí:</h1>

  <Seznam
    nadpis="Lekce 1"
    odkaz="/lekce/69"
    subs={["Výslovnost a přepis čínštiny", "Pinyin", "Český Pchin-jin"]}
  />
  <Seznam
    nadpis="Lekce 2"
    odkaz="/lekce/69"
    subs={["Základní větná stavba", "Pořadí slov ve větě", "Jednoduchá věta"]}
  />
  <Seznam nadpis="Lekce 3" odkaz="/lekce/69" subs={["Sloveso být", "Shi"]} />
  <Seznam
    nadpis="Lekce 4"
    odkaz="/lekce/69"
    subs={["'Velmi, příliš'", "tai"]}
  />
  <Seznam
    nadpis="Lekce 5"
    odkaz="/lekce/69"
    subs={["Používání přídavných jmen", "Jednoduché věty s přídavnými jmény"]}
  />
</div>
