<script lang="ts">
type Props = {
  title: string;
  description?: string;
};

const { title, description }: Props = $props();
</script>

<header class="flex flex-col gap-2">
	<h1 class="text-4xl sm:text-5xl font-extrabold tracking-tight text-foreground">{title}</h1>
	{#if description}
		<p class="max-w-2xl text-base sm:text-lg text-muted-foreground">{description}</p>
	{/if}
</header>
