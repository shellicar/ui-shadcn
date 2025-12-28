<script lang="ts">
import type { Snippet } from 'svelte';
import { cn } from '../../utils.js';
import HomeButton from './HomeButton.svelte';
import PageHeader from './PageHeader.svelte';

interface Props {
  header?: {
    title: string;
    description?: string;
  };
  children?: Snippet;
  class?: string;
  showHomeButton?: boolean;
}

const { header, children, class: className = '', showHomeButton = false }: Props = $props();
</script>

<section class="w-full">
	<div class={cn('mx-auto max-w-3xl lg:max-w-4xl xl:max-w-5xl 2xl:max-w-6xl px-4 sm:px-6 lg:px-8 xl:px-12 py-6 sm:py-8 lg:py-12 xl:py-16 flex flex-col gap-6 lg:gap-8 xl:gap-10', className)}>
		{#if showHomeButton}
			<HomeButton />
		{/if}

		{#if header}
			<PageHeader title={header.title} description={header.description} />
		{/if}

		{@render children?.()}
	</div>
</section>
