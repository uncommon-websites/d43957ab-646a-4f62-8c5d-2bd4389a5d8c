<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Efficiency",
			description: "Turning 3-hour daily tasks into 3-minute checks through intelligent automation."
		},
		{
			title: "Reliability",
			description: "Building automation that works consistently without breaking when systems change."
		},
		{
			title: "Empowerment",
			description: "Helping operations teams scale productivity without adding headcount."
		}
	];
</script>

<SecondaryHero
	title="Work once. Scale forever."
	subtitle="Automation that learns by watching"
	imageSrc="/generated/image-a-candid-scene-of-a-diverse-small-profes.webp"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"Operations managers are spending more than 15 hours a week chasing data, copy-pasting into spreadsheets, and refreshing dashboards that never sync. It's the kind of work that eats into mornings, drains morale, and prevents teams from scaling without hiring. Most tools promise automation, but require heavy integration, constant maintenance, or break when websites change—leaving managers back where they started.",
		"With MindfulScale, you just perform the task once—clicking through fields, tabs, filters like you normally would. Our browser automation records every action and then runs it automatically across any web-based tool, no matter what it is. This works without integrations or API access because we mimic your actual clicks, just like a human would. The result is a workflow that runs reliably, without breaking, in minutes—not months.",
		"MindfulScale lets growing operations teams generate reports, update tools, and sync data without adding headcount. Update CRMs, pull analytics, or fill spreadsheets—without logging in a dozen times a day. Our users reclaim their mornings, eliminate human error, and focus on what actually moves the business forward."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- Team and investor sections removed - no founder information available -->

<!-- CTA Section -->
<CallToAction
	title="Stop drowning in daily reports"
	subtitle="Start automating in minutes"
	description="Transform your 3-hour operational tasks into 3-minute automated checks. Record once, run forever—across any web application, without breaking when systems change."
	imageSrc="/generated/image-a-confident-operations-manager-stands-in.webp"
/>
