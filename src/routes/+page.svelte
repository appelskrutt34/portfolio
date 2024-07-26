<script>
  import Project from "../lib/components/Project.svelte";
    import Fire from "$lib/components/icons/Fire.svelte";
    import Code from "$lib/components/icons/Code.svelte";
    import Shield from "$lib/components/icons/Shield.svelte";
    import Eth from "$lib/components/icons/Eth.svelte";
    import Cube from "$lib/components/icons/Cube.svelte";
    import Terminal from "$lib/components/icons/Terminal.svelte"
    import Github from "$lib/components/icons/Github.svelte"
  import Skill from "$lib/components/Skill.svelte";
  import Work from "$lib/components/Work.svelte";
</script>

<main class="flex flex-col justify-center items-center text-center" id="main" tabindex="-1">  
    <div class="container flex flex-col items-center px-4 relative">
        <section class="flex flex-col gap-6 md:gap-0 md:flex-row justify-center items-center h-[100vh]">
            <div>
                <img src="my.jpg" alt="little my" class="grayscale rounded-full h-full md:h-[600px] border border-neutral-900 object-contain">
            </div>
                
                <div class="md:-mt-60 md:-ml-24 p-4 font-secondary z-10 text-left bg-neutral-50 text-neutral-900 border border-neutral-900 rounded-lg">
                    <p class="font-bold">Name: My</p>
                    <p class="font-bold">Role: Developer</p>
                </div>
        </section>
        <section class="w-full my-44 text-left" id="skills">
            <h1 class="font-header">What I offer</h1>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
                <Skill title="UI" description="Craft beautiful, responsive and accessible websites">
                    <img slot="image" src="/wallpapers/fading3.jpg" alt="pattern background" aria-hidden="true" class="absolute top-0 left-0 h-full w-full object-cover opacity-10 grayscale">
                    <Fire slot="icon"></Fire>
                </Skill>
                <Skill title="Security" description="Build robust, extensible software systems with a security mindset">
                    <img slot="image" src="/wallpapers/flat.jpg" alt="pattern background" aria-hidden="true" class="absolute top-0 left-0 h-full w-full object-cover opacity-10 grayscale">
                    <Shield slot="icon"></Shield>
                </Skill>
                <Skill title="Code" description="Write code with well-thought-out design principles and coding standards">
                    <img slot="image" src="/wallpapers/fading4.jpg" alt="pattern background" aria-hidden="true" class="absolute top-0 left-0 w-full object-cover opacity-20 grayscale">
                    <Code slot="icon"></Code>
                </Skill>
                <Skill title="CI/CD" description="Set up automated build and release processes">
                    <img slot="image" src="/wallpapers/fading6.jpg" alt="pattern background" aria-hidden="true" class="rotate-180 absolute top-0 left-0 h-full w-full object-cover opacity-10 grayscale">
                    <Cube slot="icon"></Cube>
                </Skill>
                <Skill title="Pen Testing" description="Test sites for vulnerabillities, exploits and bugs">
                    <img slot="image" src="/wallpapers/fading4.jpg" alt="pattern background" aria-hidden="true" class="rotate-180 absolute top-0 left-0 w-full object-cover opacity-20 grayscale">
                    <Terminal slot="icon"></Terminal>
                </Skill>
                <Skill title="Blockchain" description="Build smart contracts, Connect websites and apps to blockchain">
                    <img slot="image" src="/wallpapers/fading6.jpg" alt="pattern background" aria-hidden="true" class="absolute top-0 left-0 h-full w-full object-cover opacity-20 grayscale">
                    <Eth slot="icon"></Eth>
                </Skill>
            </div>
        </section>

        <section class="my-44" id="toolbox">
            <h1 class="font-header mb-1">Tech Toolbox</h1>
            <h2>Most used tools and technologies</h2>
            <div class="lg:flex lg:gap-20 gap-4 md:gap-8 grid grid-cols-3 lg:grid-cols-5 pt-16">
                <p class="flex flex-col gap-2 items-center justify-center"><img src="/logos/svelte.png" alt="svelte logo" class="grayscale h-8 lg:h-16 mr-1">Svelte</p>
                <p class="flex flex-col gap-2 items-center justify-center"><img src="/logos/tailwind.png" alt="tailwind logo" class="grayscale h-8 lg:h-16 mr-1">TailwindCSS</p>
                <p class="flex flex-col gap-2 items-center justify-center"><img src="/logos/dotnet.png" alt="dotnet logo" class="grayscale h-8 lg:h-16 mr-1">DotNet</p>
                <p class="flex flex-col gap-2 items-center justify-center"><img src="/logos/devops.png" alt="azure devops logo" class="grayscale h-8 lg:h-16 mr-1">AzureDevOps</p>
                <p class="flex flex-col gap-2 items-center justify-center"><img src="/logos/burp.jpg" alt="burp suit logo" class="grayscale h-8 lg:h-16 mr-1">BurpSuit</p>
                <p class="flex flex-col gap-2 items-center justify-center"><img src="/logos/sqlserver.png" alt="sql server logo" class="grayscale h-8 lg:h-16 mr-1">SqlServer</p>
            </div>
        </section>
</div>

<section class="mt-44 w-full flex flex-col items-center" id="history">
        <h1 class="font-header mb-1 w-full text-right container px-4">Professional History</h1>
        <div class="w-full flex justify-center bg-neutral-50 py-20 relative">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 text-left container z-10 px-4">
                <Work title="Backend Developer at Google"
                tasks={["Architect scalable backend services to support large-scale applications and high traffic loads."
                        ,"Develop microservices to break down complex systems into manageable, deployable components."
                            ,"Implement OAuth 2.0 for secure authentication."
                            , "Refactor database schema to improve query efficiency."
                            ,"Implement TLS/SSL encryption for all data transmissions."
                            ,"Analyze slow-running queries using performance monitoring tools."]}
                stack="# go, python, java, c++, django, sql server, google cloud build, prometheus"
                date="aug. 2019-now"></Work>
                <Work title="Frontend Developer at Netflix"
                tasks={["Implement code-splitting and lazy loading for images and components to improve initial page load times."
                            , "Ensure accessibility compliance."
                            , "Integrate frontend code with backend services and APIs to fetch and display data."
                            ,"Implement video player features."
                            , "Write unit tests."]} 
                stack="# javascript, sass, react.js, webpack, lighthouse, graphql"
                date="march 2016–aug 2019"></Work>
            </div>
            <img src="/wallpapers/geometry.png" alt="" class="absolute left-0 bottom-0 w-full object-cover opacity-30 grayscale">
        </div>
   </section>
        
<section class="py-44 w-full flex justify-center relative" id="projects">
    <div class="container px-4 z-10">
        <h1 class="font-header">Hobby Projects</h1>
        <h2>Websites and apps I've crafted</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-20 py-20 text-left">
            <Project title="Apple pie" description="Made with Svelte & .Net Web APIs"><Github size="50%"></Github></Project>
            <Project title="Pear" description="Made with React & Express"><Github size="50%"></Github></Project>
            <Project title="Orange juice" description="Contributed as Svelte developer"><Github size="50%"></Github></Project>
            <Project title="Bacon sandwich" description="Made with Vue and Strapi"><Github size="50%"></Github></Project>
            <Project title="Pancakes" description="Contributed as Svelte developer"><Github size="50%"></Github></Project>
        </div>
    </div>
    <img src="/wallpapers/geometry.png" alt="" class="absolute left-0 top-0 w-full object-cover opacity-20 grayscale rotate-180">
</section>
</main>

