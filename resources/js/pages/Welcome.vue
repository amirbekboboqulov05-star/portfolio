<script setup lang="ts">
import { Head } from '@inertiajs/vue3';

const profile = {
    name: 'Amirbek Boboqulov',
    role: 'Junior dasturchi',
    intro: "Harakat qiling, to'xtamang!",
    location: 'Uzbekistan',
    linkedin: 'https://www.linkedin.com/in/amirbek-boboqulov-360538445/?isSelfProfile=true',
    github: 'https://github.com/amirbekboboqulov05-star',
    telegram: 'https://t.me/AmirbeyLATUS',
    email: 'https://mail.google.com/mail/u/0/#inbox',
};

const stats = [
    { label: 'ITLive ta’limi', value: '2 yil' },
    { label: 'Tayyor loyiha', value: '1' },
    { label: 'Maqsad', value: 'Full-stack' },
];

const skills = [
    'HTML va CSS',
    'JavaScript asoslari',
    'Vue.js',
    'Responsive dizayn',
    'Git va GitHub',
    'Muammolarni yechish',
];

const projects = [
    {
        title: 'Gallaktus',
        description: 'Amirbekning tayyor shaxsiy dasturlash loyihasi.',
    },
];
</script>

<template>
    <Head title="Amirbek Boboqulov | Portfolio">
        <meta name="description" content="Amirbek Boboqulov portfolio page" />
    </Head>

    <div class="min-h-screen bg-slate-950 text-white">
        <header class="mx-auto max-w-6xl px-5 py-6 sm:px-6 lg:px-8">
            <nav class="flex items-center justify-between gap-4">
                <div class="text-lg font-semibold tracking-wide text-emerald-300">
                    {{ profile.name }}
                </div>
                <div class="hidden items-center gap-6 text-sm text-slate-300 md:flex">
                    <a href="/about" class="transition hover:text-white">Men haqimda</a>
                    <a href="#skills" class="transition hover:text-white">Ko'nikmalar</a>
                    <a href="#projects" class="transition hover:text-white">Loyiha</a>
                    <a href="#contact" class="transition hover:text-white">Aloqa</a>
                </div>
            </nav>
        </header>

        <main>
            <section class="mx-auto max-w-6xl px-5 pb-16 pt-8 sm:px-6 lg:px-8 lg:pb-24">
                <div class="grid items-center gap-10 lg:grid-cols-[1.2fr_0.8fr]">
                    <div>
                        <span class="inline-flex items-center rounded-full border border-emerald-400/30 bg-emerald-400/10 px-3 py-1 text-xs font-medium uppercase tracking-[0.2em] text-emerald-300">
                            {{ profile.role }}
                        </span>
                        <h1 class="mt-6 text-4xl font-bold tracking-tight text-white sm:text-5xl lg:text-6xl">
                            {{ profile.name }}
                        </h1>
                        <p class="mt-4 max-w-xl text-lg text-slate-300">
                            {{ profile.intro }}
                        </p>
                        <p class="mt-6 max-w-xl text-base leading-7 text-slate-400">
                            Men web-dasturlashni o‘rganayotgan Junior dasturchiman. Zamonaviy, qulay va turli qurilmalarda yaxshi ishlaydigan web-saytlar yaratishga qiziqaman.
                        </p>

                        <div class="mt-8 flex flex-wrap gap-4">
                            <a
                                :href="profile.linkedin"
                                target="_blank"
                                rel="noopener noreferrer"
                                class="rounded-full bg-emerald-400 px-5 py-3 text-sm font-semibold text-slate-950 transition hover:bg-emerald-300"
                            >
                                LinkedIn
                            </a>
                            <a
                                :href="profile.github"
                                target="_blank"
                                rel="noopener noreferrer"
                                class="rounded-full border border-slate-600 bg-slate-900 px-5 py-3 text-sm font-semibold text-white transition hover:border-slate-500 hover:bg-slate-800"
                            >
                                GitHub
                            </a>
                        </div>
                    </div>

                    <div class="relative">
                        <div class="absolute inset-0 -z-10 rounded-[2rem] bg-gradient-to-br from-emerald-400/20 via-sky-500/10 to-transparent blur-2xl"></div>
                        <div class="rounded-[2rem] border border-slate-800 bg-slate-900/80 p-6 shadow-2xl shadow-emerald-500/10 backdrop-blur-sm">
                            <div class="mb-4 flex items-center justify-between">
                                <span class="text-sm text-slate-400">Profile</span>
                                <span class="rounded-full border border-emerald-500/30 bg-emerald-500/10 px-2.5 py-1 text-xs text-emerald-300">
                                    Active
                                </span>
                            </div>

                            <div class="flex items-center gap-4">
                                <div class="h-16 w-16 overflow-hidden rounded-2xl border border-emerald-400/30 bg-slate-800 shadow-lg shadow-emerald-500/10">
                                    <img
                                        src="/profile-portrait.svg"
                                        alt="Amirbek Boboqulov"
                                        class="h-full w-full object-cover"
                                    />
                                </div>
                                <div>
                                    <h2 class="text-xl font-semibold text-white">{{ profile.name }}</h2>
                                    <p class="text-sm text-slate-400">{{ profile.role }}</p>
                                </div>
                            </div>

                            <div class="mt-6 grid grid-cols-3 gap-3">
                                <div v-for="item in stats" :key="item.label" class="rounded-xl border border-slate-800 bg-slate-950/70 p-3 text-center">
                                    <div class="text-xl font-bold text-white">{{ item.value }}</div>
                                    <div class="mt-1 text-[11px] text-slate-400">{{ item.label }}</div>
                                </div>
                            </div>

                            <div class="mt-6 space-y-3 text-sm text-slate-300">
                                <div class="flex items-center justify-between rounded-lg border border-slate-800 bg-slate-950/60 px-3 py-2">
                                    <span>Location</span>
                                    <span class="text-white">{{ profile.location }}</span>
                                </div>
                                <div class="flex items-center justify-between rounded-lg border border-slate-800 bg-slate-950/60 px-3 py-2">
                                    <span>Telegram</span>
                                    <a :href="profile.telegram" target="_blank" rel="noopener noreferrer" class="text-emerald-300 hover:text-emerald-200">@AmirbeyLATUS</a>
                                </div>
                                <div class="flex items-center justify-between rounded-lg border border-slate-800 bg-slate-950/60 px-3 py-2">
                                    <span>Email</span>
                                    <a :href="profile.email" target="_blank" rel="noopener noreferrer" class="text-emerald-300 hover:text-emerald-200">Gmail</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <section id="about" class="border-y border-slate-800 bg-slate-900/60">
                <div class="mx-auto grid max-w-6xl gap-8 px-5 py-16 sm:px-6 lg:grid-cols-2 lg:px-8">
                    <div>
                        <p class="text-sm font-semibold uppercase tracking-[0.2em] text-emerald-300">Haqida</p>
                        <h2 class="mt-4 text-3xl font-bold text-white">Dasturlashga qiziqish va o‘sish</h2>
                    </div>
                    <div class="text-base leading-8 text-slate-300">
                        Men dasturlash asoslarini muntazam o‘rganib, bilimlarimni amaliy loyihalarda qo‘llayman. Maqsadim — foydalanuvchilar uchun qulay, tushunarli va ishonchli web-ilovalar yaratib, tajribali dasturchi sifatida rivojlanish.
                    </div>
                </div>
            </section>

            <section id="skills" class="mx-auto max-w-6xl px-5 py-16 sm:px-6 lg:px-8">
                <p class="text-sm font-semibold uppercase tracking-[0.2em] text-emerald-300">Ko'nikmalar</p>
                <h2 class="mt-4 text-3xl font-bold text-white">Asosiy sohalar</h2>

                <div class="mt-8 grid gap-4 sm:grid-cols-2 lg:grid-cols-3">
                    <div v-for="skill in skills" :key="skill" class="rounded-2xl border border-slate-800 bg-slate-900 p-5 text-slate-200 shadow-lg shadow-slate-950/20">
                        <div class="mb-3 h-2 w-12 rounded-full bg-gradient-to-r from-emerald-400 to-lime-300"></div>
                        <p class="text-lg font-medium text-white">{{ skill }}</p>
                    </div>
                </div>
            </section>

            <section id="projects" class="bg-slate-900/70 py-16">
                <div class="mx-auto max-w-6xl px-5 sm:px-6 lg:px-8">
                    <p class="text-sm font-semibold uppercase tracking-[0.2em] text-emerald-300">Loyihalar</p>
                    <h2 class="mt-4 text-3xl font-bold text-white">Ishlab chiqilgan yechimlar</h2>

                    <div class="mt-8 grid gap-6 lg:grid-cols-3">
                        <article v-for="project in projects" :key="project.title" class="rounded-3xl border border-slate-800 bg-slate-950 p-6 shadow-lg shadow-slate-950/30">
                            <div class="mb-4 inline-flex rounded-full border border-emerald-500/30 bg-emerald-500/10 px-3 py-1 text-xs font-medium uppercase tracking-[0.18em] text-emerald-300">
                                Project
                            </div>
                            <h3 class="text-xl font-semibold text-white">{{ project.title }}</h3>
                            <p class="mt-4 text-sm leading-7 text-slate-300">
                                {{ project.description }}
                            </p>
                        </article>
                    </div>
                </div>
            </section>

            <section id="contact" class="mx-auto max-w-6xl px-5 py-16 sm:px-6 lg:px-8">
                <div class="rounded-[2rem] border border-emerald-400/20 bg-gradient-to-br from-slate-900 to-slate-950 p-8 text-center shadow-2xl shadow-emerald-500/10">
                    <p class="text-sm font-semibold uppercase tracking-[0.2em] text-emerald-300">Aloqa</p>
                    <h2 class="mt-4 text-3xl font-bold text-white">Ishlash va hamkorlik uchun bog'laning</h2>
                    <p class="mx-auto mt-4 max-w-2xl text-slate-300">
                        Web-loyiha, hamkorlik yoki dasturlash bo‘yicha takliflaringiz bo‘lsa, men bilan bog‘laning.
                    </p>

                    <div class="mt-8 flex flex-wrap items-center justify-center gap-4">
                        <a :href="profile.linkedin" target="_blank" rel="noopener noreferrer" class="rounded-full bg-emerald-400 px-5 py-3 text-sm font-semibold text-slate-950 transition hover:bg-emerald-300">LinkedIn</a>
                        <a :href="profile.telegram" target="_blank" rel="noopener noreferrer" class="rounded-full border border-slate-700 bg-slate-900 px-5 py-3 text-sm font-semibold text-white transition hover:border-slate-500 hover:bg-slate-800">Telegram</a>
                        <a :href="profile.email" target="_blank" rel="noopener noreferrer" class="rounded-full border border-slate-700 bg-slate-900 px-5 py-3 text-sm font-semibold text-white transition hover:border-slate-500 hover:bg-slate-800">Email</a>
                    </div>
                </div>
            </section>
        </main>

        <footer class="border-t border-slate-800 py-6 text-center text-sm text-slate-400">
            © {{ new Date().getFullYear() }} {{ profile.name }}. Barcha huquqlar himoyalangan.
        </footer>
    </div>
</template>
