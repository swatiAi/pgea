<script setup>
import { ref } from "vue";
import AppContainer from "~/components/ui/AppContainer.vue";

const expandedCards = ref([]);

const testimonials = [
    {
        text: `We had the absolute privilege of hosting Philippe as a keynote speaker at the 2025 Smart Health Africa Summit, and he was a joy to work with. His presentation on the future of healthcare was not only insightful but also delivered a deep sense of passion for the industry.

Beyond the stage, Philippe was an absolute gentleman – professional, approachable, and a joy to work with throughout the entire process. From preparation to delivery, he made the experience seamless for our team.

We couldn’t recommend Philippe highly enough as both a thought leader and a collaborative partner.`,
        name: "Kelly Bentley",
        role: "The Rebel Element",
        icon: "lucide:mic-2",
    },
    {
        text: `I am delighted to write a recommendation for Philippe Gerwill, a formidable advocate for innovation and a highly respected futurist. As a remarkable speaker, talented presenter, and leading authority in cutting-edge technologies, Philippe has consistently impressed audiences at international forums with his deep insights and thought leadership on topics such as Digital Health, Artificial Intelligence, Internet of Things, Big Data, Augmented Reality/Virtual Reality, 5G, Blockchain, and the intriguing concept of Healthcare in the Metaverse.

His humanist approach to digitalization sets Philippe apart from many experts in the field. His deep understanding that technology should serve humanity rather than dictate it adds a vital perspective to the current discourse on the advancement of technology. His ability to articulate complex ideas and technological paradigms with a deep focus on the human element is refreshing and much-needed.

Drawing from a career spanning 30 years, with equal exposure to the specialty chemicals and pharmaceutical industries, Philippe’s depth and breadth of experience are exceptional. His global roles have led him across continents, enabling him to appreciate and incorporate diverse cultural nuances in his discourse. This cultural sensitivity enhances the relevance and reach of his messages.

Philippe is not one to rest on his laurels, and despite stepping into an early retirement phase, he continues to contribute to various communities actively. His drive to catalyze positive change is inspirational and reflects his profound responsibility toward future generations.

Currently serving in various capacities as an executive advisor, board member, industry advisor, and consultant, Philippe continues to make significant contributions to companies across multiple geographies and industries. This is a testament to his adaptability, broad knowledge, and leadership capabilities.

I would strongly recommend Philippe Gerwill for any speaking engagement, advisory role, or consultancy work, particularly within the digital health and innovation spheres. His unique perspective, vast experience, and articulate communication style make him a valuable asset to any organization.`,
        name: "Dr Harvey Castro",
        role: "Physician Futurist – Chief AI Officer",
        icon: "lucide:brain-circuit",
    },
    {
        text: `I’m deeply grateful to Philippe Gerwill for being a mentor who guided me through AI in healthcare, digital health and Healthtech.

From the very beginning of my transition into AI and digital health, Philippe has been a steady source of clarity in a space that can often feel overwhelming and noisy. He has an exceptional ability to ground every conversation in real world impact, ethics, and patient centered thinking which matters deeply to me as both a clinician and a patient advocate.

Beyond mentorship, Philippe is a powerful and compelling keynote speaker in the HealthTech space. He speaks from deep personal experience critically reviewing, evaluating, and discussing health technologies through the lens of lived experience, clinical relevance, and long term impact. This gives his insights an authenticity and credibility that resonate strongly with diverse audiences.

Philippe is also a prominent advocate for AI and technology in healthcare particularly in the UAE, while maintaining a strong global presence. His work, thought leadership, and public engagement consistently push conversations forward championing responsible, ethical, and human centric adoption of AI in healthcare systems worldwide.

He continues to guide, challenge, and support my thinking as I evolve helping me identify opportunities, refine my voice, and stay anchored to why we use AI in healthcare in the first place: to improve lives safely and meaningfully.

If you are looking for someone who combines deep expertise, powerful communication, integrity, and genuine generosity, Philippe is that rare speaker and mentor.
I highly recommend him to anyone navigating HealthTech and AI whether you are a clinician, founder, policymaker, or innovator.

Thank you, Philippe, for continuing to be a guide on this journey.`,
        name: "Dr Aswathy Sudhakar",
        role: "Founder AITHEAL",
        icon: "lucide:heart-handshake",
    },
];

const toggleCard = (index) => {
    expandedCards.value[index] = !expandedCards.value[index];
};
</script>

<template>
    <section class="bg-white py-16 text-black transition-colors duration-200 dark:bg-black dark:text-white lg:py-24">
        <AppContainer>
            <h2
                class="text-center text-[36px] font-[500] leading-none tracking-[-0.06em] sm:text-[44px] lg:text-[52px]">
                Testimonials
            </h2>

            <div class="mt-12 grid items-start gap-8 md:grid-cols-3 lg:mt-16">
                <article v-for="(item, index) in testimonials" :key="item.name"
                    class="group flex flex-col rounded-[6px] bg-gradient-to-b from-white via-[#FBFFE8] to-[#E8FF65] px-8 py-7 text-black shadow-sm transition duration-300 hover:-translate-y-1 lg:px-9 lg:py-8"
                    :class="expandedCards[index]
                            ? 'min-h-[430px] sm:min-h-[460px] lg:min-h-[500px]'
                            : 'h-[430px] sm:h-[460px] lg:h-[500px]'
                        ">
                    <div class="flex flex-1 flex-col">
                        <span class="block text-[76px] font-[900] leading-[0.6] tracking-[-0.08em] text-black">
                            “
                        </span>

                        <div class="mt-5">
                            <p class="whitespace-pre-line text-[14px] font-[400] leading-[1.14] tracking-[-0.035em] lg:text-[15px]"
                                :class="expandedCards[index] ? '' : 'line-clamp-[11]'">
                                {{ item.text }}
                            </p>

                            <button type="button"
                                class="mt-2 w-fit text-[12px] font-[800] uppercase leading-none tracking-[-0.03em] text-black underline underline-offset-4 transition hover:opacity-70"
                                @click="toggleCard(index)">
                                {{ expandedCards[index] ? "Read less" : "Read more" }}
                            </button>
                        </div>
                    </div>

                    <div class="mt-8 flex items-center gap-3">
                        <span
                            class="flex size-9 shrink-0 items-center justify-center rounded-full bg-black text-[#C8EB00]"
                            aria-hidden="true">
                            <Icon :name="item.icon" class="size-5" />
                        </span>

                        <div>
                            <h3 class="text-[12px] font-[800] leading-none tracking-[-0.03em] text-black">
                                {{ item.name }}
                            </h3>

                            <p class="mt-1 text-[12px] font-[700] leading-tight tracking-[-0.03em] text-black">
                                {{ item.role }}
                            </p>
                        </div>
                    </div>
                </article>
            </div>
        </AppContainer>
    </section>
</template>