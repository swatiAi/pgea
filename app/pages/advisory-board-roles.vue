<script setup>
import AppContainer from "~/components/ui/AppContainer.vue";

useHead({
    title: "Advisory & Board Roles | Philippe Gerwill",
    meta: [
        {
            name: "description",
            content:
                "Philippe Gerwill advises organizations at the intersection of AI, digital health, longevity, and human-centered innovation.",
        },
    ],
});

const introText =
    "Shaping the Future of Health and Longevity";

const contentSections = [
    {
        title: "Strategic Advisory",
        text: "Over the past years, I have established myself as a trusted strategic advisor and board member across a diverse ecosystem of organizations operating at the intersection of artificial intelligence, digital health, longevity, and human-centered innovation. My advisory portfolio reflects not only the breadth of my global network but also my ability to translate emerging technologies into meaningful, scalable, and impactful solutions.",
    },
    {
        title: "Digital Healthcare Humanist",
        text: "My approach to advisory is deeply rooted in my philosophy as a Digital Healthcare Humanist. I consistently advocate for a balanced integration of technology and humanity, ensuring that innovation serves people rather than displacing them. This perspective has made me a sought-after partner for organizations navigating complex transformations in healthcare, particularly in regions undergoing rapid digital acceleration such as the Middle East, Europe, and emerging global markets.",
    },
    {
        title: "Executive & Founder Support",
        text: "In my advisory roles, I support executive teams and founders on strategic positioning, market expansion, ecosystem building, and thought leadership. I am particularly valued for my ability to connect stakeholders across industries, from healthcare providers and technology companies to policymakers, investors, and academic institutions. My unique strength lies in bridging silos and fostering collaborations that accelerate innovation adoption while maintaining ethical and societal considerations.",
    },
    {
        title: "Board-Level Contribution",
        text: "My board and advisory engagements span a wide range of organizations, including healthtech startups, AI-driven platforms, longevity initiatives, and global innovation communities. These roles often involve shaping strategic direction, contributing to product and service innovation, supporting go-to-market strategies, and enhancing international visibility through my influence and speaking engagements. I also play an active role in mentoring leadership teams, helping them align their vision with rapidly evolving technological and regulatory landscapes.",
    },
    {
        title: "Future-Focused Strategy",
        text: "A key dimension of my contribution is my ability to anticipate future trends and translate them into actionable strategies. Whether advising on AI integration in clinical workflows, digital therapeutics, mental health platforms, or longevity-focused ecosystems, I bring a forward-looking perspective grounded in real-world experience. My insights are informed by decades of leadership in multinational corporations, combined with my current role as a global keynote speaker and innovation strategist.",
    },
    {
        title: "Connector & Catalyst",
        text: "Beyond strategy, I am recognized for my role as a connector and catalyst. I actively facilitate high-value introductions between organizations, enabling partnerships that drive tangible outcomes. This includes connecting startups with investors, linking healthcare institutions with technology providers, and supporting cross-border collaborations that unlock new market opportunities.",
    },
    {
        title: "Long-Term Partnerships",
        text: "My advisory philosophy is not transactional but relational. I invest in long-term partnerships where I can contribute meaningfully to growth, impact, and purpose. I selectively engage with organizations that share my vision of leveraging technology to improve human health, wellbeing, and longevity.",
    },
];

const closingText =
    "Through my advisory and board roles, I continue to shape the future of healthcare and innovation on a global scale, ensuring that progress remains not only technologically advanced but also deeply human.";
</script>

<template>
    <main class="bg-white text-black transition-colors duration-200 dark:bg-black dark:text-white">
        <section class="py-14 sm:py-16 lg:py-20">
            <AppContainer>
                <div class="mx-auto max-w-6xl">
                    <div class="max-w-5xl">
                        <p
                            class="text-[13px] font-[700] uppercase tracking-[0.22em] text-[#4A1BC4] dark:text-[#C8EB00]">
                            Advisory & Board Roles
                        </p>

                        <h1
                            class="mt-5 max-w-5xl text-[48px] font-[500] uppercase leading-[0.92] tracking-[-0.08em] text-[#4A1BC4] dark:text-[#C8EB00] sm:text-[55px] lg:text-[60px]">
                            Where Technology Meets Humanity
                        </h1>

                        <p
                            class="mt-7 max-w-3xl text-[18px] font-[500] leading-[1.25] tracking-[-0.04em] text-black/70 dark:text-white/75 sm:text-[18px]">
                            {{ introText }}
                        </p>
                    </div>

                    <div class="mt-14 grid gap-8 lg:grid-cols-[0.75fr_1.25fr] lg:gap-14">
                        <aside class="hidden lg:block">
                            <div class="sticky top-28 rounded-[28px] bg-[#EDEDED] p-8 dark:bg-[#101010]">
                                <p
                                    class="text-[14px] font-[700] uppercase tracking-[0.2em] text-[#4A1BC4] dark:text-[#C8EB00]">
                                    Focus Areas
                                </p>

                                <div class="mt-8 flex flex-col gap-4">
                                    <span
                                        class="rounded-full bg-white px-5 py-3 text-[14px] font-[700] tracking-[-0.03em] text-black dark:bg-black dark:text-white">
                                        AI & Digital Health
                                    </span>

                                    <span
                                        class="rounded-full bg-white px-5 py-3 text-[14px] font-[700] tracking-[-0.03em] text-black dark:bg-black dark:text-white">
                                        Longevity Innovation
                                    </span>

                                    <span
                                        class="rounded-full bg-white px-5 py-3 text-[14px] font-[700] tracking-[-0.03em] text-black dark:bg-black dark:text-white">
                                        Strategic Positioning
                                    </span>

                                    <span
                                        class="rounded-full bg-white px-5 py-3 text-[14px] font-[700] tracking-[-0.03em] text-black dark:bg-black dark:text-white">
                                        Ecosystem Building
                                    </span>

                                    <span
                                        class="rounded-full bg-white px-5 py-3 text-[14px] font-[700] tracking-[-0.03em] text-black dark:bg-black dark:text-white">
                                        Human-Centered Innovation
                                    </span>
                                </div>
                            </div>
                        </aside>

                        <div class="space-y-8">
                            <article v-for="section in contentSections" :key="section.title"
                                class="rounded-[28px] bg-[#EDEDED] p-6 transition-colors duration-200 dark:bg-[#101010] sm:p-8 lg:p-10">
                                <div class="mb-5 h-[4px] w-16 rounded-full bg-[#4A1BC4] dark:bg-[#C8EB00]"
                                    aria-hidden="true"></div>

                                <h2
                                    class="text-[26px] font-[700] leading-[1.05] tracking-[-0.05em] text-black dark:text-white sm:text-[32px]">
                                    {{ section.title }}
                                </h2>

                                <p
                                    class="mt-5 text-[17px] font-[500] leading-[1.75] tracking-[-0.035em] text-black/75 dark:text-white/75 sm:text-[18px]">
                                    {{ section.text }}
                                </p>
                            </article>

                            <article class="rounded-[28px] bg-[#4A1BC4] p-7 text-[#C8EB00] sm:p-9 lg:p-10">
                                <p
                                    class="text-[24px] font-[500] leading-[1.2] tracking-[-0.055em] sm:text-[32px] lg:text-[38px]">
                                    {{ closingText }}
                                </p>
                            </article>
                        </div>
                    </div>
                </div>
            </AppContainer>
        </section>
    </main>
</template>