<script>
    import { Card } from 'flowbite-svelte';

    export const images = [
        {
            "alt": "Maël Ferri",
            "src": "src/lib/assets/1686850961537.jpg",
            "title": "Maël Ferri"
        },
        {
            "alt": "Titouan-Lysandre André",
            "src": "src/lib/assets/1206568483505053786.webp",
            "title": "Titouan-Lysandre André"
        },
        {
            "alt": "Eric Ciotti",
            "src": "src/lib/assets/GQWWyTJWMAAUyDC.jpg",
            "title": "Eric Ciotti"
        },
        {
            "alt": "Elouan Rival",
            "src": "src/lib/assets/1725865171180.jpg",
            "title": "Elouan Rival"
        },
        {
            "alt": "Incroyable",
            "src": "src/lib/assets/F5xlYjUWwAAU7iP.jpg",
            "title": "Incroyable"
        },
        {
            "alt": "J'ai pas les mots",
            "src": "src/lib/assets/F62izsRWIAAE-Qg.png",
            "title": "J'ai pas les mots"
        }
    ];
</script>

<div class="w-full h-screen bg-slate-800 flex flex-col justify-center items-center text-white">
    <div class="text-center mb-8">
        <h1 class="text-4xl">Bienvenue sur ce super site Dockerisé</h1>
        <h2 class="text-2xl">Par Jérémy Girard</h2>
    </div>

    <div class="grid grid-cols-3 gap-4">
        {#each images as image}
            <Card key={image.title} class="overflow-hidden h-64">
                <img src={image.src} alt={image.alt} class="w-full h-full object-cover" />
                <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">{image.title}</h5>
            </Card>
        {/each}
    </div>
</div>
