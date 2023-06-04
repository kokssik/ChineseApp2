<script>
  export let data;
  import mdParser from "$lib/utils/md-parser";
  import { onMount } from "svelte";
  import SQLite from "tauri-plugin-sqlite-api";

  let rows = [];

  let id = data.slug; // to recognize which lection is opened

  let query = `SELECT * FROM lekce WHERE id = ?`;

  let parsed;

  onMount(async () => {
    const db = await SQLite.open("./hanzi.db");

    rows = await db.select(query, [id]);

    console.log(rows[0].markdown);
    parsed = mdParser(rows[0].markdown);
  });
</script>

<div class="bg-gradient-to-r from-purple-100 to-white flex">
  <div class="pr-5 pl-10 pt-20 basis-2/12">
    <ul class="pl-0">
      <li><a href="/lekce/1">Lekce 1</a></li>
      <li><a href="/lekce/2">Lekce 2</a></li>
      <li><a href="/lekce/3">Lekce 3</a></li>
      <li><a href="/lekce/4">Lekce 4</a></li>
    </ul>
  </div>

  <div class="border-2 border-solid p-5 bg-white mt-20 border-black basis-8/12">
    <h1>{id}</h1>
    <div>{@html parsed}</div>
  </div>

  <div class="pr-5 pl-10 pt-20 basis-2/12" />
</div>

<style>
  .container {
    min-width: 100vw;
    min-height: 100vh;
    display: flex;
  }

  .navbar {
    flex: 1;
    width: 10rem;
    padding-top: 100px;
    /*background-color: aquamarine;*/
    /* Add any other styling for the navbar */
  }

  /* .content {
    flex: 1;
    background-color: #ffffff; 
    border: 1px solid #000000; 
    padding: 10px; 
    margin-top: 100px;
  } */
</style>
