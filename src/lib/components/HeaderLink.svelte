<script>
    import { page } from "$app/stores";
    export let link;
    export let text;
</script>

<div class={$page.url.pathname === link ? "bg-cyan-200" : ""}>
    <a href={link}>{text}</a>
</div>
