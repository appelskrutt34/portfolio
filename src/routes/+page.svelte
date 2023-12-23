<script>
  import Project from "../lib/components/Project.svelte";
    import Fire from "$lib/components/icons/Fire.svelte";
    import Code from "$lib/components/icons/Code.svelte";
    import Shield from "$lib/components/icons/Shield.svelte";
    import Eth from "$lib/components/icons/Eth.svelte";
    import Cube from "$lib/components/icons/Cube.svelte";
    import Terminal from "$lib/components/icons/Terminal.svelte"
  import Skill from "$lib/components/Skill.svelte";
  import Work from "$lib/components/Work.svelte";

</script>
<div class="flex flex-col justify-center items-center text-center">  
    <div class="container flex flex-col items-center px-4">
        <div class="flex my-44">
                <img src="my.jpg" alt="avatar" class="grayscale rounded-full h-full lg:h-[600px]">
                <div class="-ml-40 lg:-ml-24 mt-4 font-secondary z-10 text-left">
                    <p class="font-bold">Name: Ebba</p>
                    <p class="font-bold">Role: Programmer</p>
                </div>
        </div>
        <h1 class="font-header">Tech Toolbox</h1>
        <h2>Favorite Tools and Technologies for Success</h2>
        <div class="lg:flex lg:gap-16 gap-4 grid grid-cols-2 md:grid-cols-3 lg:grid-cols-5 pt-16">
            <p class="flex gap-2 items-center"><img src="/logos/svelte.png" alt="svelte logo" class="grayscale h-8 lg:h-16 mr-1">Svelte</p>
            <p class="flex gap-2 items-center"><img src="/logos/tailwind.png" alt="tailwind logo" class="grayscale h-8 lg:h-16 mr-1">TailwindCSS</p>
            <p class="flex gap-2 items-center"><img src="/logos/dotnet.png" alt="dotnet logo" class="grayscale h-8 lg:h-16 mr-1">DotNet</p>
            <p class="flex gap-2 items-center"><img src="/logos/devops.png" alt="azure devops logo" class="grayscale h-8 lg:h-16 mr-1">AzureDevOps</p>
            <p class="flex gap-2 items-center"><img src="/logos/burp.jpg" alt="burp suit logo" class="grayscale h-8  lg:h-16 mr-1">BurpSuit</p>
        </div>


        <div class="w-full my-64 text-left">
            <h1 class="font-header">What can I Do?</h1>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
                <Skill title="UI" description="Craft beautiful, responsive and accessible websites">
                    <img slot="image" src="/wallpapers/fading3.jpg" alt="" class="absolute top-0 left-0 h-full w-full object-cover opacity-30 grayscale">
                    <Fire slot="icon"></Fire>
                </Skill>
                <Skill title="Security" description="Build robust, extensible software systems with a security mindset">
                    <img slot="image" src="/wallpapers/flat.jpg" alt="" class="absolute top-0 left-0 h-full w-full object-cover opacity-20 grayscale">
                    <Shield slot="icon"></Shield>
                </Skill>
                <Skill title="Code" description="Write code with well-thought-out design principles and coding standards">
                    <img slot="image" src="/wallpapers/fading4.jpg" alt="" class="absolute top-0 left-0 w-full object-cover opacity-20 grayscale">
                    <Code slot="icon"></Code>
                </Skill>
                <Skill title="CI/CD" description="Set up automated build and release processes">
                    <img slot="image" src="/wallpapers/fading6.jpg" alt="" class="rotate-180 absolute top-0 left-0 h-full w-full object-cover opacity-40 grayscale">
                    <Cube slot="icon"></Cube>
                </Skill>
                <Skill title="Pen Testing" description="Test sites for vulnerabillities, exploits and bugs">
                    <img slot="image" src="/wallpapers/fading4.jpg" alt="" class="rotate-180 absolute top-0 left-0 w-full object-cover opacity-20 grayscale">
                    <Terminal slot="icon"></Terminal>
                </Skill>
                <Skill title="Blockchain" description="Build smart contracts, Connect websites and apps to blockchain">
                    <img slot="image" src="/wallpapers/fading6.jpg" alt="" class="absolute top-0 left-0 h-full w-full object-cover opacity-40 grayscale">
                    <Eth slot="icon"></Eth>
                </Skill>
               
            </div>
        </div>
    </div>
 
   
    <div class="w-full flex flex-col justify-center items-center relative bg-neutral-50 mt-80 px-4">
        <div class="-mt-[280px] text-right z-10">
            <h1 class="font-header mb-1">Professional History</h1>
            <div class="rounded-3xl container bg-neutral-900 border border-neutral-50 p-8 md:p-16">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-20 text-left">
                    <Work title="Fullstack Developer at Forefront"
                    tasks={["Maintenance and development of new features on websites built with asp.net and optimizely"
                            ,"Migrating data and sites from old servers to newer ones"
                                ,"Developing websites in blazor"
                                ,"Developing apps in flutter"
                                ,"Writing apis in .net"
                                , "Setting up build and release pipelines in azure"
                                ,"Setting up nuget publish flows in azure"
                                , "Updating websites to follow wcag guidlines"]}
                    stack="# asp.net, azure devops, sql server, blazor, flutter, c-sharp, java, javascript, sql, html, css, teamcity, octopus deploy, optimizely"
                    date="aug. 2023-now"></Work>
                    <Work title="Fullstack Developer at Sogeti"
                    tasks={["Maintenance and development of new features on websites built with asp.net and optimizely"
                                , "Setting up build and release pipelines in azure for .net projects"
                                , "Updating websites to follow wcag guidlines"
                                , "Building an app in vue.js with strapi"
                                , "Writing web jobs in azure functions"]} 
                    stack="# javascript, c-sharp, html, css, asp.net, react, sql server, azure
                    devops, octopus deploy, optimizely"
                    date="march 2022–juli 2023"></Work>
                    <Work title="Fullstack Developer at Bonigi"
                    tasks={["Maintenance and development of Bonigis CRM tool for fundraising organisations built in asp.net webforms"
                                , "Implementing jquery querybuilder for customers to make easy queries to the database"
                                , "Writing procedures and processing data in sql server"
                                , "Building an app in vue.js with strapi"
                                , "Writing web jobs in azure functions"]} 
                    stack="# asp.net, azure devops, azure functions, sql server, vue, strapi c-sharp, jquery, javascript, sql, html, css"
                    date="sep. 2020–nov. 2021"></Work>
                    <Work title="Software Developer at Husqvarna"
                    tasks={["Maintenance and development of Husqvarnas software for robotic lawnmowers"]} 
                    stack="# wpf, azure devops, html, css, javascript, c-sharp"
                    date="jan. 2020–june 2020"></Work>
                </div>
            </div>
        </div>

        
    

    <div class="container flex flex-col items-center my-44 z-10 text-neutral-900">
        <h1 class="font-header">Hobby Projects</h1>
        <h2>Some Websites and Apps I've Crafted and Contributed To</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 py-20">
            <Project image="/pages/njord.png" title="Njord.rs" description="Made with Svelte" source="https://www.njord.rs"></Project>
            <Project image="/pages/explorer.png" title="Kryptokrona Explorer" source="https://www.explorer.kryptokrona.org"></Project>
            <Project image="/pages/kryptokrona.png" title="Kryptokrona Website" source="https://www.kryptokrona.org"></Project>
            <Project image="/pages/ath.png" title="ATH Games" description="Made with Vue" source="https://www.ath.games"></Project>
            <Project image="/pages/kotlinSDK.png" title="Kryptokrona Kotlin SDK" description="Made with Svelte" source="https://sdk.kryptokrona.org/"></Project>
        </div>
    </div>
    <img src="/wallpapers/geometric.jpg" alt="" class="absolute top-0 left-0 h-full w-full object-cover opacity-20 grayscale">
</div>
</div>

