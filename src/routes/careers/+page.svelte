<script lang="ts">
	// Types

	// Components
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Card from "$lib/components/ui/Card.svelte";
	import JobList, { type JobOpening } from "./JobList.svelte";

	// Icons
	import IconBriefcase from "~icons/lucide/briefcase";
	import IconUsers from "~icons/lucide/users";
	import IconHeart from "~icons/lucide/heart";
	import IconGlobe from "~icons/lucide/globe";

	// Constants
	const SECTION_BASE_CLASSES = "section-py section-px container mx-auto";
	const GRADIENT_BG_CLASSES =
		"bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800";
	const ICON_CONTAINER_CLASSES =
		"bg-primary-50 text-primary-600 dark:bg-primary-950 dark:text-primary-400 flex items-center justify-center rounded-full";

	const benefits = [
	{
		title: "Tackle trillion-dollar challenges",
		description: "Define the next-generation of restaurant automation through robotics and AI—impacting a $1T industry.",
		icon: IconBriefcase
	},
	{
		title: "SpaceX-style engineering",
		description: "Work in a fast-moving, vertically integrated team where learning and experimentation happen daily.",
		icon: IconUsers
	},
	{
		title: "Rapid ownership and growth",
		description: "Ship real-world products quickly, gain responsibility, and shape both our company and your own career.",
		icon: IconHeart
	}
];

	const openings: JobOpening[] = [
		// Engineering
		{
			title: "Senior Frontend Developer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Backend Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Design Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Design
		{
			title: "UX/UI Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Product
		{
			title: "Product Manager",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Analyst",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Marketing
		{
			title: "Marketing Specialist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Content Strategist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Social Media Manager",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		}
	];

	const employeeTestimonials = [
  {
    name: "Kenji Watanabe",
    position: "Senior Mechanical Engineer",
    company: "Robotics Team",
    quote:
      "KAIKAKU is where innovation is a daily reality. The collaborative spirit and deep respect for new ideas make it easy to feel at home—everyone truly wants you to succeed.",
    image: "/generated/image-a-30-something-asian-man-with-a-friendly.webp"
  },
  {
    name: "Alyssa Thompson",
    position: "AI Software Developer",
    company: "Intelligence Platform",
    quote:
      "I joined to work on real-world AI, and stayed because every project challenges me to learn and grow. My voice is heard no matter my title.",
    image: "/generated/image-a-joyful-black-woman-in-her-late-20s-wea.webp"
  },
  {
    name: "Sophie Miller",
    position: "Operations Coordinator",
    company: "Operations Team",
    quote:
      "From my first day, I felt welcomed and supported. There are always new responsibilities to take on and opportunities to make an impact.",
    image: "/generated/image-a-friendly-young-white-woman-in-her-earl.webp"
  }
];

	const processSteps = [
	{
		step: 1,
		title: "Apply online",
		description: "Send us your resume and a few bullets on what you'd build or solve at KAIKAKU."
	},
	{
		step: 2,
		title: "Team chat",
		description: "A quick intro call with leads and engineers to see if there’s a mutual fit."
	},
	{
		step: 3,
		title: "Challenge",
		description: "Tackle a short technical, product, or problem-solving task—with guidance and open communication."
	},
	{
		step: 4,
		title: "Final interview & decision",
		description: "Meet the founders, get transparent feedback, and receive a decision—usually within 10 days."
	}
];

	const values = [
	{
		icon: IconHeart,
		title: "Always in beta",
		description: "We rapidly build, test, and iterate in real kitchens—failure is how we find what works."
	},
	{
		icon: IconUsers,
		title: "Engineered for outcomes",
		description: "We succeed by delivering real business and customer results—not surface metrics."
	},
	{
		icon: IconGlobe,
		title: "No passengers, just builders",
		description: "Everyone here creates and owns their work, with autonomy and an end-to-end mindset."
	}
];
</script>

<!-- Hero Section -->

<SecondaryHero

title="Invent the future of restaurants"
subtitle="Shape what's next with robotics and AI"
imageSrc="/generated/image-a-diverse-group-of-professionals-engaged.webp"
/>

<!--
At KAIKAKU, engineers, operators, and designers come together to transform the $1 trillion QSR industry—powered by robotics, AI, and vertical integration from the ground up. Inspired by a SpaceX-style approach to engineering, we move fast, design from first principles, and build in a tight loop with real operations. If you want impact, growth, and a team that's all in—this is where it starts.
-->


<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join us?" subtitle="Build your career while making an impact" />

	<div class="mt-16 grid gap-4 md:grid-cols-3">
		{#each benefits as benefit}
			<Card {...benefit} />
		{/each}
	</div>
</section>

<!-- Culture Section -->
<Culture {values} />

<Testimonials testimonials={employeeTestimonials} />

<!-- Application Process -->
<section class={SECTION_BASE_CLASSES}>
	<div class="mx-auto">
		<h2 class="text-title1 mb-16">Our application process</h2>

		<div class="grid gap-12 md:grid-cols-3">
			{#each processSteps as { step, title, description }, i}
				<div class="flex flex-col">
					<div class="{ICON_CONTAINER_CLASSES} mb-6 size-11">
						<span class="text-headline">{step}</span>
					</div>
					<h3 class="text-headline mb-3">{title}</h3>
					<p class="text-body text-emphasis-low">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
<!-- Current Openings Section -->
<section class={GRADIENT_BG_CLASSES}>
	<div class="section-px section-py container mx-auto grid w-full items-start lg:grid-cols-2">
		<SectionHeader title="Current openings" subtitle="Find your perfect role" />

		<JobList {openings} />
	</div>
</section>
