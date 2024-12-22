<script lang="ts">
    import "../reset.css";
    import "../app.css";
    import Footer from "$lib/sections/footer.svelte";

    let { children } = $props();
</script>

{@render children()}
<Footer />
