<script>
    import Button from "./Button.svelte";
    import Card from "./Card.svelte";

    export let text
    // export let completed
</script>

<Card>
    <p>{text}</p>
    <div class="buttons-wrapper">
        <Button>Delete</Button>
        <Button>Archive</Button> 
    </div>
</Card>