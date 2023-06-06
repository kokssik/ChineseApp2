<script>
    import { page } from "$app/stores";
    export let links;
</script>

<div class="flex justify-center">
    <div class="flex flex-row gap-32 my-1 font-sans">
        {#each links as link}
            <a
                href={link.link}
                class="no-underline font-semibold text-lg hover:uppercase"
                >{link.text}
            </a>
        {/each}
    </div>
</div>
