<script>
  import List from "$lib/components/HanziCard.svelte";
  import Seznam from "$lib/components/Seznam.svelte";
</script>

<div class="grid justify-center">
  <div class="">
    <div class="font-sans text-4xl font-bold mb-5">Seznam lekcí:</div>
    <Seznam
      nadpis="Lekce 1"
      odkaz="/lekce/1"
      subs={[
        "Základní větná stavba a sloveso být",
        "Pořadí slov ve větě",
        "Jednoduché věty",
      ]}
    />
    <Seznam
      nadpis="Lekce 2"
      odkaz="/lekce/2"
      subs={["Věty s přídavnými jmény", "很"]}
    />
    <Seznam
      nadpis="Lekce 3"
      odkaz="/lekce/3"
      subs={["Jak se zaptat na otázku", "吗", "呢"]}
    />
    <Seznam
      nadpis="Lekce 4"
      odkaz="/lekce/5656"
      subs={["Příliš", "Příliš se používá jinak", "太"]}
    />
    <Seznam
      nadpis="Lekce 5"
      odkaz="/lekce/4"
      subs={["Používání přídavných jmen", "Jednoduché věty s přídavnými jmény"]}
    />
  </div>
</div>
