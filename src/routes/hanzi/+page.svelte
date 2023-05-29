<script>
    import SQLite from "tauri-plugin-sqlite-api";
    import { onMount } from "svelte";
    import HanziCard from "$lib/components/HanziCard.svelte";

    let rows = [];

    onMount(async () => {
        const db = await SQLite.open("./hanzi.db");

        rows = await db.select("SELECT * FROM hanzi");

        console.log(rows);
    });
</script>

<!-- Creates a <HanziCard/> element for each element in the rows array -->
{#each rows as row}
    <HanziCard
        character={row.symbol}
        pronunciation={row.pronounciation}
        meaning={row.meaning}
        word1={row.word1}
        word2={row.word2}
    />
{/each}
