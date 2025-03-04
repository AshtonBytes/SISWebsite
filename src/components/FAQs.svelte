<script>
    import SectionWrapper from "./SectionWrapper.svelte";
    import { lightMode } from '../store';

    let faqs = [
        {
            question:"How will this help with my inventory shrinkage problem?",
            answer:"I'm glad you ask! By accurately monitoring the products on display, the system flags any discrepancies of missing products and notifies the store's manager."
        },
        {
            question:"Notifies the manager? Can it notify the District Manager as well?",
            answer:"Absolutely, in fact, the system can be set up to send notifications to up to five phone numbers with the basic plan."
        },
        {
            question:"Accurately monitoring products you say, how does it do that?",
            answer:"Thank you for asking! A patented device, invented by the company's founder, is used in conjunction with our proprietary software to measure the exact amount of product in each slot, of every tray, which the system is installed in."
        }
    ]

</script>
<SectionWrapper id="faqs">
    <div class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center {$lightMode ? "light" : "dark"}">
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
                For All Questions, Qualms, and Queries
            </p>
            <h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center">
                Frequently Asked Questions
            </h3>
        </div>
        <div class="flex flex-col gap-8 sm:gap-10 md:gap-14 w-full">
            {#each faqs as faq}
                <div class="flex flex-col gap-2 text-left max-w-[800px] w-full mx-auto relative p-4 px-6">
                    <div class="absolute top-0 left-0 w-1/3 h-[1px] bg-950 -translate-x-4"></div>
                    <div class="absolute top-0 left-0 h-2/3 w-[1px] bg-950 -translate-y-4"></div>
                    <h4 class="font-semibold text-lg sm:text-xl md:text-2xl pt-2">
                        {faq.question}
                        <div class="h-[2px] grayBackground w-1/4 mr-auto mb-4 mt-2"></div>
                    </h4>
                    <p class="pl-2">{faq.answer}</p>
                </div>
            {/each}
        </div>
    </div>
</SectionWrapper>