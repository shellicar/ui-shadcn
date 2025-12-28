<script lang="ts">
import type * as FormPrimitive from 'formsnap';
import { cn, type WithoutChild } from '$lib/utils.js';

const { ref = $bindable(null), class: className, ...restProps }: WithoutChild<FormPrimitive.LegendProps> = $props();
</script>

<FormPrimitive.Legend
	bind:ref
	class={cn("data-[fs-error]:text-destructive text-sm leading-none font-medium", className)}
	{...restProps}
/>
