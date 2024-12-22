<script lang="ts">
    import { ListChecks, Note } from "phosphor-svelte";

    let currentView = $state<"lists" | "notes">("lists");
</script>

<footer>
    <div></div>
    <button onclick={() => currentView = 'lists'} aria-current={currentView == "lists" ? "page" : null} aria-label="Lists">
        <ListChecks size="1.75rem" />
    </button>
    <button onclick={() => currentView = 'notes'} aria-current={currentView == "notes" ? "page" : null} aria-label="Notes">
        <Note size="1.75rem" />
    </button>
</footer>

<style>
    footer {
        position: fixed;
        bottom: 0;
        width: 100%;

        display: flex;
        justify-content: space-evenly;

        button {
            position: relative;

            padding: 0.5rem 1.5rem;

            background-color: transparent;
            border: none;

            cursor: pointer;
        }

        div {
            content: "";

            position: absolute;
            inset: 0 0 auto;

            margin-inline: auto;

            width: 1rem;
            height: .25rem;

            border-radius: 9999px;

            background-color: var(--clr-primary);
        }
    }
</style>
