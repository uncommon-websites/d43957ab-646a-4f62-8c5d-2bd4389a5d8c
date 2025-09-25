<!--
    @component
    Bold hero banner with eye-catching text and strong call-to-action. NEVER use title case.

    Usage:
    ```html
    <Hero
      title="Bold Claim"
      subtitle="Quick Value"
      imageSrc="https://www.unc.mn/image-placeholder.svg"
      callsToAction={[
        {
          href: "/start",
          label: "Go"
        },
        {
          href: "/learn",
          label: "More"
        }
      ]}
    />
    ```

    Props:
    - `title`: Main headline (string)
    - `subtitle`: Supporting text (string)
    - `imageSrc`: Hero image URL (string)
    - `callsToAction`: CTA buttons array (max two: primary, secondary)
-->

<script lang="ts">
	// Components
	import AnimateText from "$lib/components/animation/AnimateText.svelte";
	import Button from "$lib/components/ui/Button.svelte";

	// Constants
	import { cta } from "$lib/navigation";

	function handleImageError(e: Event) {
		const target = e.currentTarget as HTMLImageElement;
		target.src = "https://placehold.co/800x600/f8fafc/64748b?text=Hero+image";
	}

	// Types
	type Props = {
		centered?: boolean;
		title: string;
		subtitle: string;
		imageSrc?: string;
		callsToAction?: Array<{
			href: string;
			label: string;
		}>; // A maximum of two calls to action, with the first one being primary and the second one being secondary
		[key: string]: any;
	};

	let {
		title,
		subtitle,
		imageSrc,
		callsToAction = [cta],
		centered = false,
		...rest
	}: Props = $props();
</script>

{#if centered}
	<!-- Full screen hero with background image and overlay -->
	<div 
		class="relative h-screen bg-cover bg-center bg-no-repeat flex items-center justify-center" 
		style="background-image: url('https://images.unsplash.com/photo-1712397943847-e104395a1a8b?q=80&w=3432&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D')"
		{...rest}
	>
		<!-- Black overlay -->
		<div class="absolute inset-0 bg-black/70"></div>
		
		<!-- Content -->
		<div class="relative z-10 text-center text-white px-6 max-w-4xl mx-auto" data-enter-container>
			<div class="grid gap-6">
				<h1 class="text-display w-full text-white" data-enter>
					<span class="block"><AnimateText text={title} /></span>
				</h1>

				<p
					data-enter
					class={[
						"text-white/90 text-headline mx-auto block max-w-[45ch] transition duration-500 ease-out"
					]}
				>
					{subtitle}
				</p>
			</div>

			{#if callsToAction.length > 0}
				<div class="flex gap-4 justify-center mt-8" data-enter>
					{#each callsToAction as cta, index}
						<Button
							href={cta.href}
							size="lg"
							variant={index % 2 === 0 ? "primary" : "secondary"}
							class="max-lg:hidden">{cta.label}</Button
						>
						<Button
							href={cta.href}
							size="md"
							variant={index % 2 === 0 ? "primary" : "secondary"}
							class="lg:hidden">{cta.label}</Button
						>
					{/each}
				</div>
			{/if}
		</div>
	</div>
{:else}
	<!-- Original hero layout for non-centered -->
	<div class="bg-background" {...rest}>
		<header
			class={[
				"section-px container mx-auto grid items-end gap-16 gap-y-9 py-12 pt-24 text-balance xl:grid-cols-[1fr_auto]"
			]}
			data-enter-container
		>
			<div class="grid gap-6">
				<h1 class="text-display w-full" data-enter>
					<span class="block"><AnimateText text={title} /></span>
					<span class="text-emphasis-dim block"><AnimateText text={subtitle} /></span>
				</h1>
			</div>

			{#if callsToAction.length > 0}
				<div class="flex gap-4" data-enter>
					{#each callsToAction as cta, index}
						<Button
							href={cta.href}
							size="lg"
							variant={index % 2 === 0 ? "primary" : "secondary"}
							class="max-lg:hidden">{cta.label}</Button
						>
						<Button
							href={cta.href}
							size="md"
							variant={index % 2 === 0 ? "primary" : "secondary"}
							class="lg:hidden">{cta.label}</Button
						>
					{/each}
				</div>
			{/if}
		</header>

		{#if imageSrc}
			<div class="col-span-full aspect-video" data-enter>
				<img
					src={imageSrc}
					alt="Customer"
					class="size-full object-cover"
					onerror={handleImageError}
				/>
			</div>
		{/if}
	</div>
{/if}
