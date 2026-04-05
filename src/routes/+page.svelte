<script lang="ts">
	import { primaryText, text } from '$lib/uitils/classUtils';
	import { Avatar, Badge, Heading, P } from 'flowbite-svelte';
	import { ArrowRightOutline } from 'flowbite-svelte-icons';

	const expertise = [
		{
			title: 'Frontend Developer',
			description: 'Building visually stunning and user-friendly interfaces.',
			skills: ['JavaScript', 'Svelte', 'HTML', 'CSS']
		},
		{
			title: 'Backend Developer',
			description: 'Creating robust and scalable server-side applications.',
			skills: ['Python', 'Django', 'SvelteKit', 'SQL']
		},
		{
			title: 'Full Stack Developer',
			description: 'Combining frontend and backend expertise to deliver complete solutions.',
			skills: ['JavaScript', 'Svelte', 'Python', 'Django', 'SvelteKit', 'SQL']
		},
		{
			title: 'Full Stack Developer',
			description: 'Combining frontend and backend expertise to deliver complete solutions.',
			skills: ['JavaScript', 'Svelte', 'Python', 'Django', 'SvelteKit', 'SQL']
		}
	];
</script>

<div class="flex w-full flex-col gap-4">
	<div
		class="background-white-100 relative flex h-94 w-full items-center justify-around overflow-hidden"
	>
		<img
			src="/loc2.png"
			alt="loc"
			class="absolute inset-0 z-0 h-full w-full object-cover opacity-20"
		/>
		<div class="relative z-10 flex h-full w-full items-center justify-around">
			<div class="flex flex-col">
				<Heading class="z-20 text-white">NoDo</Heading>
			</div>

			<img src="/logo.png" alt="/logo.png" class="z-20 aspect-square h-[80%] rounded-2xl" />
		</div>
	</div>
	<div class="flex">
		{@render title('Capabilities', 'Core Expertise')}
		<a class={`hover:underline ${primaryText}`} href="/">See All Projects <ArrowRightOutline /></a>
	</div>
	<div class="scrollbar-hover flex min-w-full gap-4 overflow-x-auto p-4">
		{#each expertise as item}
			<div class="flex w-74 flex-col gap-4 rounded-2xl bg-neutral-800 px-4 py-10">
				<Avatar cornerStyle="rounded" />
				<div class="flex flex-col">
					<Heading class={`${text} text-xl `}>{item.title}</Heading>
					<P class={`${primaryText} text-sm`}>{item.description}</P>
				</div>
				<div class="flex flex-wrap gap-2">
					{#each item.skills as skill}
						<Badge class="text-[10px]">{skill}</Badge>
					{/each}
				</div>
			</div>
		{/each}
	</div>
	{@render title('Selected Works', 'Featured Projects')}
</div>
<!--  -->
{#snippet title(subtitle?: string, title?: string)}
	<div class="flex flex-col">
		<P class={`${primaryText} text-xs`}>{subtitle}</P>
		<Heading class={`text-2xl ${text}`}>{title}</Heading>
	</div>
{/snippet}
