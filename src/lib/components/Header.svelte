<script>
    import { page } from "$app/stores";
    export let links;
</script>

<div class="flex justify-center drop-shadow-sm">
    <div class="flex flex-row gap-32">
        {#each links as link}
            <a href={link.link}>{link.text}</a>
        {/each}
    </div>
</div>
