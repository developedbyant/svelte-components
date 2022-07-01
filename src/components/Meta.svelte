<script lang="ts">
    const site = {
        title:"A list of svelte components",
        desc:"A list of svelte components for your projects",
        name:"SC",
        backdropPath:"/favicon.png",
        domainUrl:"http://localhost:3000"
    }
    // passed variables
    export let title:string = ''
    export let desc:string = ''
    export let backdrop:string = ''
    import { page } from '$app/stores';
</script>

<svelte:head>
<title>{title?`${title} | ${site.name}`:`${site.title} | ${site.name}`}</title>
<meta name="description" content={desc?desc:site.desc} />
<meta name="keywords" content="stock, market, trade, trades, trading, trader" />
<meta property="og:site_name" content="{site.name}"/>
<meta property="og:locale" content="en_US"/>
<meta property="og:type" content="website"/>
<meta property="og:title" content={title?title:`${site.title} | ${site.name}`}/>
<meta property="og:description" content={desc?desc:site.desc} />
<meta property="og:url" content={$page.url.href}/>
<meta property="og:image" content="{backdrop?backdrop:`${site.domainUrl+site.backdropPath}`}"/>
<meta property="og:image:secure_url" content="{backdrop?backdrop:`${site.domainUrl+site.backdropPath}`}"/>
<meta property="twitter:card" content="summary"/>
<meta property="twitter:title" content={title?title:`${site.title} | ${site.name}`}/>
<meta property="twitter:description" content={desc?desc:site.desc}/>
</svelte:head>