<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
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
];
</script>

<SecondaryHero
  title="Automating enterprise QSR operations"
  subtitle="AI and robotics built from the ground up to drive massive efficiency and margin growth"
  imageSrc="/generated/image-a-diverse-team-of-professionals-in-a-mod.webp"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"Josef Chen started KAIKAKU after seeing the same story repeat itself across the quick-service restaurant industry: constant burnout, high turnover, razor-thin profits. While tech trickled into every other sector, fast food was still patching over problems instead of rethinking how operations should work. Josef founded KAIKAKU not to tweak the system—but to rebuild it entirely.",
		"Inspired by the engineering philosophy at SpaceX, KAIKAKU builds every part of its operating system from the ground up: robotics, software, and intelligence. In early trials, the team worked side-by-side with real kitchens, treating each location like a living lab. The result is a vertically integrated system that performs fast, adapts to any format, and scales with minimal labor costs. This isn’t just automation bolted onto old processes—it’s a rethink of the entire kitchen budget.",
		"Today, KAIKAKU is building for the next era of restaurants—where operations are intelligent, labor is leveraged (not overworked), and every location runs like your top performer. We believe automation’s not about replacing people. It’s about letting them do their best work—because everything else runs by itself."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
  stakeholderType="team"
  title="Our founder"
  subtitle="Tech-led innovation, built in-house."
  stakeholders={[
    {
      name: "Josef Chen",
      position: "Founder & CEO",
      bio: "Josef Chen is founder and CEO of KAIKAKU, engineering the next-generation restaurant operating system with a tech-first, vertically integrated approach.",
      image: "/generated/image-a-professional-headshot-of-a-confident-e.webp"
    }
  ]}
/>

<StakeholderGrid
	stakeholderType="investor"
	title="Backed by the best."
	subtitle="Point Nine, TSIC and others"
	stakeholders={[
		{
			name: "Point Nine Capital",
			image: "https://cdn.brandfetch.io/pointnine.com/w/400/h/400/logo?c=1id_elLz2Bd5Ej-dWo7"
		},
		{
			name: "TSIC Ventures",
			image: "https://cdn.brandfetch.io/tiny.vc/w/400/h/400/logo?c=1a2b3c4d5e"
		},
		{
			name: "Sequoia Capital",
			image: "https://cdn.brandfetch.io/sequoiacap.com/w/400/h/400/logo"
		}
	]}
/>

<!-- CTA Section -->
<CallToAction
  title="Ready to lead the automation era?"
  subtitle="See KAIKAKU in action"
  description="If you’re building the future of QSR or want to help transform an industry from the inside, let’s connect. High bar. Big impact. No tourists."
  callsToAction={[
    { href: '/contact', label: 'Book a demo', variant: 'primary' },
    { href: '/careers', label: 'Join the team', variant: 'secondary' }
  ]}
/>
