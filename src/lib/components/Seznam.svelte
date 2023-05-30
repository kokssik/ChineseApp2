<script>
    import { page } from "$app/stores";
    export let nadpis;
    export let odkaz;
    export let sub1;
    export let sub2;
    export let sub3;
    export let sub4;
</script>

<div class="text-column ml-64">
    <div class="font-sans leading-relaxed">
        <div class="text-2xl font-bold"><a href={odkaz}>{nadpis}</a></div>
        <div class="leading-relaxed ml-5">- {sub1}</div>
        <div class="leading-relaxed ml-5">- {sub2}</div>
        <div class="leading-relaxed ml-5">- {sub3}</div>
        <div class="leading-relaxed ml-5">- {sub4}</div>
    </div>
</div>
