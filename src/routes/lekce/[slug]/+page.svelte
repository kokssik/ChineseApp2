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

<div class="container bg-gradient-to-r from-purple-100 to-white">
  <div class="navbar">
    <ul>
      <li><a href="/lekce/1">Lekce 1</a></li>
      <li><a href="/lekce/2">Lekce 2</a></li>
      <li><a href="/lekce/3">Lekce 3</a></li>
      <li><a href="/lekce/4">Lekce 4</a></li>
    </ul>
  </div>

  <div class="content">
    <h1>{id}</h1>
    <div>{@html parsed}</div>
  </div>

  <div class="navbar" />
</div>

<style>
  .container {
    min-width: 100vw;
    min-height: 100vh;
    display: flex;
  }

  .navbar {
    flex: 1;
    max-width: 200px;
    padding-top: 100px;
    /*background-color: aquamarine;*/
    /* Add any other styling for the navbar */
  }

  .content {
    flex: 1;
    background-color: #ffffff; /* White background color */
    border: 1px solid #000000; /* Thin border */
    padding: 10px; /* Add padding for content */
    margin-top: 100px;
  }
</style>
