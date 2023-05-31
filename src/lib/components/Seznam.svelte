<script>
    import { page } from "$app/stores";
    export let nadpis;
    export let odkaz;
    export let subs;
</script>

<div class="text-column ml-64">
    <div class="font-sans leading-relaxed">
        <div class="text-2xl font-bold"><a href={odkaz}>{nadpis}</a></div>
        {#each subs as sub}
            <div class="leading-relaxed ml-5">- {sub}</div>
        {/each}
    </div>
</div>
