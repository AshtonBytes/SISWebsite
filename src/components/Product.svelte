<script>
    import ProductCard from "./ProductCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    import { lightMode } from '../store';
    
    let productFeatures = [
        {
            featureList: [
                "Gives clerks enough time to resolve mistakes",
                "Stay informed of discrepancies",
                "Time Stamped for your convenience",
                "Learn when the problems are resolved"
            ],
            description: "Receive notifications within 2 minutes.",
            imgUrl: "assets/SISTitleScreen.png",
        },
        {
            featureList: [
                "All popular Cigarette Packs and Cartons",
                "All popular Smokeless Tobacco Products",
                "The Lion's Share of all Electronic Nicotine Delivery Systems"
            ],
            description: "Seamless integration of 100+ Products",
            imgUrl: "assets/SISTitleScreen.png",
        },
        {
            featureList: [
                "It is as easy as scan, click, load",
                "Scan the product's barcode",
                "Select the location you'd like to assign to the product",
                "Load the product and let the system measure its thickness.",
            ],
            description: "Simply and easily add new products without hassle",
            imgUrl: "assets/SISTitleScreen.png",
        },
        {
            featureList: [
                "Razors, Razor Blades, and Personal Care Items",
                "Liquor, Minis, and Energy Drinks",
                "Over the Counter Medications and Supplements"
            ],
            description: "Think of the possibilities with lower shrinkage.",
            imgUrl: "assets/SISTitleScreen.png",
        },
    ];
</script>

<SectionWrapper id="product">
    <div class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14 {$lightMode ? "light" : "dark"}">
        <div class="flex flex-col gap-2">
            <p class="opacity 60 text-base sm:text-lg md:text-xl text-center">
                Unlock the potential of your business...
            </p>
            <h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center">
                What We Can Do For You
            </h3>
        </div>
        {#each productFeatures as productFeature, index}
            <ProductCard {productFeature} {index}>
                {#if index === 0}
                    <span class="text-400 font-medium">Instant Discrepancy Notifications</span>
                {:else if index === 1}
                    <span class="text-400 font-medium">Large Product Library</span>
                {:else if index === 2}
                    <span class="text-400 font-medium">Freely Add Products to Sell</span>
                {:else}
                    <span class="text-400 font-medium">Bring Back High Ticket Items</span>
                {/if}
            </ProductCard>
        {/each}
    </div>
</SectionWrapper>

        