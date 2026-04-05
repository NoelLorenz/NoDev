<script lang="ts">
	import { page } from '$app/state';
	import { bg, bg2, border, primaryText, secondaryText, text } from '$lib/uitils/classUtils';
    import {Heading, NavLi, NavUl} from 'flowbite-svelte';
    let currentPage = $derived(page.url.pathname);

    const navItems = [
        {
            name: 'Home',
            href: '/'
        },
        {
            name: 'Projects',
            href: '/projects'
        }
    ]


</script>
<div class="flex w-full h-[7%] justify-center items-center {bg} p-4 border-b {border}">
    <Heading class={`${text} absolute left-4`} tag="h3">No<span class={primaryText}>
            Dev
        </span>
    </Heading>
    <NavUl>
        {#each navItems as item}
            <NavLi class={currentPage === item.href ? primaryText : secondaryText} href={item.href}>
            {item.name}
            </NavLi>
        {/each}
    </NavUl>
    <div class="flex"></div>
</div>
