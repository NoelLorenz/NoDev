<script lang="ts">
	import { border, primaryText, secondaryText, text } from "$lib/uitils/classUtils";
	import { FooterLink, FooterLinkGroup } from "flowbite-svelte";

    const footerItems  = [
        {
        name: 'Github',
        href: "https://github.com/NoelLorenz"
    }, {
        name: 'LinkedIn',
        href: "https://www.linkedin.com/in/noel-lorenz/"
    }
]

</script>
<div class={`flex justify-between w-full h-[10%] p-4 border-t ${border} px-4 items-center`}>

    <p class={`${text}`}>NoDev <br /><span class={`${secondaryText} text-xs`}>BUILT WITH PRECISION.</span></p>
<div class="flex ">
    <FooterLinkGroup class="flex ">
        {#each footerItems as item}
            <FooterLink href={item.href} class={`${secondaryText}`}>
                {item.name} 
            </FooterLink>
        {/each}
    </FooterLinkGroup>
</div>
</div>