<script>
    import CtAs from "./CTAs.svelte";   
    import Header from "./Header.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    import Stars from "./Stars.svelte";
    import { lightMode } from '../store';

</script>
<SectionWrapper id="hero">
    <Header/>
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-10 md:gap-14 lg:gap-20 relative text-base mt-xl">
        <div class="flex flex-col lg:flex-row items-center justify-between w-full"> <!-- Change flex direction based on screen size -->
            <h2 class="text-3xl sm:text-4xl md:text-5xl text-left {$lightMode ? "light" : "dark"} mr-0 lg:margin-xl">
                <span class="!font-bold text-400 sis-red">Shrinkage</span>
                Costs You!<br/>
                Shrink your Shrinkage with Us to
                Maximize Your <span class="!font-bold sis-green">Profits</span>
                <div class = "margin-xl">
                    <p class="text-xl text-left mx-auto w-full">
                        The Security in Inventory System accurately tracks every product on display to report and
                        disincentivize theft at every opportunity once a product is in the system.
                    </p>
                </div>
                
                <div class = "margin-xl">
                    <CtAs />
                </div>
                <div class="margin-xl">
                    <Stars />
                </div>
            </h2>
        </div>
        <img src="assets/SISTitleScreen.png" alt="Security Inventory Systems Title Screen" class="w-full beveledCorners dropShadow" /> <!-- Adjust image width as needed -->
    </div>
</SectionWrapper>