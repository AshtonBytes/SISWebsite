<script>
    import ReviewCard from "./ReviewCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    import Stars from "./Stars.svelte";
    import { lightMode } from '../store';

    let lim = true

    let reviewsList = [
        {
            name: "John Doe",
            review: "“I was losing over a thousand dollars a month to shrinkage. In the first month since installing the Security in Inventory System, my shrinkage problem dropped by over 70% for related products.” <Example Review>",
            features: [
                "“Professional and Personable”"
            ]
        },
        {
            name: "John Doe",
            review: "“I was losing over a thousand dollars a month to shrinkage. In the first month since installing the Security in Inventory System, my shrinkage problem dropped by over 70% for related products.” <Example Review>",
            features: [
                "“Professional and Personable”"
            ]
        },
        {
            name: "John Doe",
            review: "“I was losing over a thousand dollars a month to shrinkage. In the first month since installing the Security in Inventory System, my shrinkage problem dropped by over 70% for related products.” <Example Review>",
            features: [
                "“Professional and Personable”"
            ]
        },
        {
            name: "John Doe",
            review: "“I was losing over a thousand dollars a month to shrinkage. In the first month since installing the Security in Inventory System, my shrinkage problem dropped by over 70% for related products.” <Example Review>",
            features: [
                "“Professional and Personable”"
            ]
        },
        {
            name: "John Doe",
            review: "“I was losing over a thousand dollars a month to shrinkage. In the first month since installing the Security in Inventory System, my shrinkage problem dropped by over 70% for related products.” <Example Review>",
            features: [
                "“Professional and Personable”"
            ]
        },
        {
            name: "John Doe",
            review: "“I was losing over a thousand dollars a month to shrinkage. In the first month since installing the Security in Inventory System, my shrinkage problem dropped by over 70% for related products.” <Example Review>",
            features: [
                "“Professional and Personable”"
            ]
        },
        {
            name: "John Doe",
            review: "“I was losing over a thousand dollars a month to shrinkage. In the first month since installing the Security in Inventory System, my shrinkage problem dropped by over 70% for related products.” <Example Review>",
            features: [
                "“Professional and Personable”"
            ]
        },
    ]
</script>
<SectionWrapper id="reviews">
    <div class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center {$lightMode ? "light" : "dark"}">
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
                Don't just take our word for it
            </p>
            <h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center">
                See What <span class="text-400 red">Others</span> Have To Say
            </h3>
        </div>
        <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
            <div class="flex flex-col gap-8">
                {#each lim ? reviewsList.slice(0,4) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} left={true} {index}/>
                {/each}
            </div>
            <div class="w-[1px] bg-slate-950 hidden md:flex"></div>
            <div class="flex flex-col gap-8">
                {#each lim ? reviewsList.slice(0,4) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} left={false} {index}/>
                {/each}
            </div>
        </div>
        <button on:click={() => lim = !lim} class="conversionBtnOne {$lightMode ? "light" : "dark"}">
            <p>{lim ? "Show More" : "Show Less"}</p>
        </button>
        <div class="flex flex-col gap-10">
            <p class="mx-auto text-lg sm:text-xl md:text-2xl font-semibold">
                Trusted by 639 Professionals
            </p>
            <Stars/>
        </div>
    </div>
</SectionWrapper>