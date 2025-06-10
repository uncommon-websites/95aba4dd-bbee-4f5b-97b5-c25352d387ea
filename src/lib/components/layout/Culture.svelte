<script lang="ts">
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import { animate, stagger } from "motion";
	import { onMount } from "svelte";

	// Types
	export type Value = {
		title: string;
		description: string;
	};

	// Props
	const { values = [
  {
    title: 'Built from scratch',
    description: 'We engineer every component ourselves—hardware, firmware, software, and AI—for next-level performance.'
  },
  {
    title: 'Fast iterations, real results',
    description: 'We move quickly, learn by doing, and improve every system through rapid cycles in real QSRs.'
  },
  {
    title: 'Mission over ego',
    description: 'Impact beats consensus. Everyone is here to transform an industry, not to coast.'
  },
  {
    title: 'High autonomy, high accountability',
    description: 'Engineers and operators own big outcomes, not just tickets.'
  },
  {
    title: 'No legacy thinking',
    description: 'We refuse B.S. and legacy workarounds in favor of reinvention and simplicity.'
  },
  {
    title: 'London roots, global scale',
    description: 'A hands-on, close-knit team with world ambitions and operational rigor.'
  }
]: { values: Value[] } = $props();

	let cards: HTMLElement[] = $state([]);

	onMount(() => {
		if (!cards.length) return;
		if (window.self !== window.top) return;

		animate(
			cards,
			{
				y: ["1.5rem", 0],
				filter: ["blur(2px)", "blur(0px)"],
				opacity: [0, 1]
			},
			{
				duration: 0.3,
				ease: "easeOut",
				delay: stagger(0.1, {
					ease: "easeInOut"
				})
			}
		);
	});
</script>

<section class="bg-white dark:bg-gray-950">
	<div
		class="section-py section-px container mx-auto grid gap-8 [--gap:--spacing(8)] [--radius:var(--radius-2xl)]"
	>
		<SectionHeader title="Our culture." subtitle="The values that guide everything we do" />

		<div
			class="grid gap-(--gap)"
			style:grid-template-columns="repeat(auto-fit, minmax(280px, 1fr))"
		>
			{#each values as value, i}
				<div
					bind:this={cards[i]}
					class="relative border-t border-gray-200 pt-4 dark:border-gray-900"
				>
					<!-- Content -->
					<div class="text-caption z-10">
						<div>
							<div class="text-headline mb-[1em]">{value.title}</div>
							<div class="text-body text-gray-500 dark:text-gray-400">{value.description}</div>
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>
