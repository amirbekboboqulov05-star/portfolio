<script setup lang="ts">
import { Head } from '@inertiajs/vue3';

const technologies = ['HTML', 'CSS', 'JavaScript', 'Vue.js', 'React', 'PHP', 'Laravel', 'MySQL', 'Git'];
const instruments = ['Doira', 'Ksilofon', 'Pianino'];
</script>

<template>
    <Head title="Men haqimda | Amirbek Boboqulov">
        <meta name="description" content="Amirbek Boboqulov, Junior dasturchi haqida batafsil ma’lumot." />
    </Head>

    <div class="min-h-screen bg-slate-950 text-white">
        <header class="mx-auto flex max-w-5xl items-center justify-between gap-4 px-5 py-6 sm:px-6 lg:px-8">
            <a href="/" class="text-lg font-semibold text-emerald-300">Amirbek Boboqulov</a>
            <a href="/" class="rounded-full border border-slate-700 px-4 py-2 text-sm text-slate-200 transition hover:border-emerald-300 hover:text-white">Bosh sahifa</a>
        </header>

        <main class="mx-auto max-w-5xl px-5 pb-20 sm:px-6 lg:px-8">
            <section class="grid gap-10 border-b border-slate-800 py-10 md:grid-cols-[1fr_220px] md:items-center md:py-16">
                <div>
                    <p class="text-sm font-semibold uppercase tracking-[0.2em] text-emerald-300">Men haqimda</p>
                    <h1 class="mt-4 text-4xl font-bold sm:text-5xl">Amirbek Boboqulov</h1>
                    <p class="mt-3 text-xl text-slate-300">Junior dasturchi · 3-Boyovut</p>
                    <p class="mt-6 max-w-2xl text-base leading-8 text-slate-300">
                        Men Amirbek Boboqulovman. Dasturlashga qiziqishim sababli ikki yildan beri ITLive’da frontend va backend yo‘nalishlarini o‘rganib kelaman. Yangi bilimlarni amaliyotda sinab ko‘rish, web-texnologiyalar bilan ishlash va o‘z loyihalarimni yaratish menga yoqadi.
                    </p>
                </div>
                <div class="mx-auto h-52 w-52 overflow-hidden rounded-3xl border border-slate-700 bg-slate-900 shadow-xl shadow-emerald-950/30 md:mx-0">
                    <img src="/profile-portrait.svg" alt="Amirbek Boboqulov" class="h-full w-full object-cover" />
                </div>
            </section>

            <section class="grid gap-10 border-b border-slate-800 py-12 md:grid-cols-[220px_1fr]">
                <div>
                    <p class="text-sm font-semibold uppercase tracking-[0.2em] text-emerald-300">Ta’lim</p>
                    <h2 class="mt-3 text-2xl font-bold">O‘rganish yo‘lim</h2>
                </div>
                <div class="space-y-5 text-slate-300">
                    <div>
                        <h3 class="text-lg font-semibold text-white">ITLive</h3>
                        <p class="mt-1 leading-7">Ikki yildan beri frontend va backend yo‘nalishlarida ta’lim olyapman. O‘qish davomida Frontend va Backend bo‘yicha sertifikat oldim.</p>
                    </div>
                    <p class="leading-7">Dasturlashni taxminan ikki yil avval qiziqishim sabab boshladim. Hozir bilimlarimni kengaytirib, mustaqil ravishda amaliy loyihalar ustida ishlashga e’tibor qarataman.</p>
                </div>
            </section>

            <section class="grid gap-10 border-b border-slate-800 py-12 md:grid-cols-[220px_1fr]">
                <div>
                    <p class="text-sm font-semibold uppercase tracking-[0.2em] text-emerald-300">Texnologiyalar</p>
                    <h2 class="mt-3 text-2xl font-bold">O‘rganganlarim</h2>
                </div>
                <div>
                    <p class="max-w-2xl leading-7 text-slate-300">Quyidagi texnologiyalar bilan tanishman. O‘z bilim darajamni hozircha o‘rta deb baholayman va muntazam ravishda mustahkamlab boryapman.</p>
                    <ul class="mt-5 flex flex-wrap gap-2">
                        <li v-for="technology in technologies" :key="technology" class="rounded-md border border-slate-700 bg-slate-900 px-3 py-2 text-sm text-slate-200">{{ technology }}</li>
                    </ul>
                </div>
            </section>

            <section class="grid gap-10 border-b border-slate-800 py-12 md:grid-cols-[220px_1fr]">
                <div>
                    <p class="text-sm font-semibold uppercase tracking-[0.2em] text-emerald-300">Loyiha</p>
                    <h2 class="mt-3 text-2xl font-bold">Gallaktus</h2>
                </div>
                <div class="text-slate-300">
                    <p class="leading-7">Gallaktus — tayyor shaxsiy dasturlash loyiham. Ustida ishlash orqali o‘rgangan bilimlarimni amalda qo‘llayman.</p>
                </div>
            </section>

            <section class="grid gap-10 border-b border-slate-800 py-12 md:grid-cols-[220px_1fr]">
                <div>
                    <p class="text-sm font-semibold uppercase tracking-[0.2em] text-emerald-300">Boshqa qiziqishlar</p>
                    <h2 class="mt-3 text-2xl font-bold">Musiqa</h2>
                </div>
                <div class="text-slate-300">
                    <p class="leading-7">Dasturlashdan tashqari musiqa bilan ham shug‘ullanganman. San’at maktabida besh yil tahsil olib, quyidagi cholg‘ularni o‘rgandim:</p>
                    <ul class="mt-4 flex flex-wrap gap-2">
                        <li v-for="instrument in instruments" :key="instrument" class="rounded-md border border-slate-700 bg-slate-900 px-3 py-2 text-sm text-slate-200">{{ instrument }}</li>
                    </ul>
                </div>
            </section>

            <section class="grid gap-10 py-12 md:grid-cols-[220px_1fr]">
                <div>
                    <p class="text-sm font-semibold uppercase tracking-[0.2em] text-emerald-300">Maqsad</p>
                    <h2 class="mt-3 text-2xl font-bold">Full-stack dasturchi</h2>
                </div>
                <p class="max-w-2xl leading-7 text-slate-300">Kelajakdagi maqsadim — frontend va backend bilimlarimni rivojlantirib, mustaqil ravishda to‘liq web-ilovalar yarata oladigan Full-stack dasturchi bo‘lish.</p>
            </section>

            <section class="flex flex-wrap gap-3 border-t border-slate-800 pt-8">
                <a href="https://t.me/AmirbeyLATUS" target="_blank" rel="noopener noreferrer" class="rounded-full bg-emerald-400 px-5 py-3 text-sm font-semibold text-slate-950 transition hover:bg-emerald-300">Telegram: @AmirbeyLATUS</a>
                <a href="https://github.com/amirbekboboqulov05-star" target="_blank" rel="noopener noreferrer" class="rounded-full border border-slate-700 px-5 py-3 text-sm font-semibold text-white transition hover:border-slate-500">GitHub</a>
                <a href="https://www.linkedin.com/in/amirbek-boboqulov-360538445/?isSelfProfile=true" target="_blank" rel="noopener noreferrer" class="rounded-full border border-slate-700 px-5 py-3 text-sm font-semibold text-white transition hover:border-slate-500">LinkedIn</a>
            </section>
        </main>

        <footer class="border-t border-slate-800 py-6 text-center text-sm text-slate-400">
            © {{ new Date().getFullYear() }} Amirbek Boboqulov
        </footer>
    </div>
</template>