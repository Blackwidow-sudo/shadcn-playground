<script lang="ts">
    import DatePicker from "$lib/components/DatePicker.svelte";
    import { Button } from "$lib/components/ui/button"

    const buttonVariants = ['default', 'destructive', 'outline', 'secondary', 'ghost', 'link'] as const;
</script>

<div class="flex gap-4">
    <div class="flex gap-2">
        <div class="dark bg-background text-foreground p-4 flex flex-col gap-2">
            <h1>In dark mode</h1>
            {#each buttonVariants as variant}
                <Button variant={variant} aria-invalid>{variant}</Button>
            {/each}
        </div>
        <div class="p-4 flex flex-col gap-2">
            <h1>In light mode</h1>
            {#each buttonVariants as variant}
                <Button variant={variant} aria-invalid>{variant}</Button>
            {/each}
        </div>
    </div>
    <div>
        <DatePicker />
    </div>
</div>

