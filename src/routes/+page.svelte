<script>
    let hotels = [
        {
            name: "MEININGER Hotel Amsterdam Amstel",
            location: "Amsterdam",
            description: "Streamlined dorms & private rooms in a modern hotel featuring a bar & a guest kitchen.",
            price: "€ 102,-",
            rating: 4.2,
            reviews: 3975,
            image: "/images/room1.png"
        },
        {
            name: "Zaan Hotel Amsterdam Zaandam",
            location: "Amsterdam",
            description: "Warmly decorated rooms & suites in an informal hotel offering a bar",
            price: "€ 133,-",
            rating: 4.3,
            reviews: 1172,
            image: "/images/room2.png"
        },
        {
            name: "MEININGER Hotel Amsterdam City West",
            location: "Amsterdam",
            description: "Modern hotel offering private rooms & dorms plus a shared kitchen & funky bar with games.",
            price: "€ 93,-",
            rating: 4.2,
            reviews: 500,
            image: "/images/room3.png"
        },
        {
            name: "Conservatorium hotel",
            location: "Amsterdam",
            description: "Lorem ipsum dolor sit amet consectetur. Vestibulum duis facilisis tristique elit enim nunc curabitur magna. Lorem.",
            price: "€ 402,-",
            rating: 4.9,
            reviews: 980,
            image: "/images/room4.png"
        }
    ];
</script>

<style>
    .hero {
        background-image: url('/images/overlay.jpg');
    }
</style>

<div class="min-h-screen flex flex-col overflow-hidden">
    <!-- Header -->
    <header class="flex justify-between items-center p-4 pl-32 bg-white shadow">
        <img src="/images/logo.png" class="w-[136px]"  alt="logo" />
    </header>

    <!-- Hero Section -->
    <section class="hero bg-cover bg-center h-[500px] relative">
        <div class="-z-1 h-full w-full bg-black opacity-60 absolute top-0"></div>
        <div class="absolute bottom-0 left-[9%] bg-opacity-50 text-white p-6">
            <h1 class="text-4xl font-bold">Lorem ipsum dolor sit amet</h1>
            <p class="mt-2">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Rhoncus, at massa eleifend purus sagittis sed justo, purus diam.
            </p>
            <div class="mt-4 space-x-2">
                <button class="bg-[#FF9A00] hover:bg-[#FFAD33] text-black font-sans text-[16px] px-4 py-2 ">LOREM IPSUM</button>
                <button class="bg-[#DDDDDD] hover:bg-[#C4C4C4] text-black px-4 py-2">LOREM IPSUM</button>
            </div>
        </div>
    </section>


    <section class="py-12 bg-gray-100">
        <div class="container mx-auto px-4">
            <h2 class="text-2xl font-bold mb-6">Ontdek ons hotel aanbod</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-6 md:gap-8 md:gap-x-28">
                {#each hotels as hotel}
                    <div class="bg-white shadow overflow-hidden md:relative md:shadow-lg md:h-[626px] md:w-[785px]">
                        <img src={hotel.image} alt={hotel.name} class="w-full h-48 md:h-[500px] object-cover"/>
                        <div class="p-4 md:absolute md:bottom-0 md:left-32 md:w-11/12 md:max-w-[529px] md:max-h-[217px] md:bg-white md:border-gray-200 md:border-2 md:p-6 md:shadow-md">
                            <p class="text-gray-600 md:text-sm md:text-orange-500 md:font-semibold md:uppercase md:mb-2 md:text-center">{hotel.location}</p>
                            <h3 class="text-xl font-bold text-gray-800 mb-2 md:text-center">{hotel.name}</h3>
                            <p class="text-gray-600 mt-2 md:mt-0 md:text-[16px] mb-0 md:text-center">{hotel.description}</p>
                            <div class="flex flex-col items-center justify-between mt-1 md:mt-0">
                                <span class="text-yellow-500 md:mr-1 md:text-lg">
                                    ★{hotel.rating}
                                    <span class="text-gray-600 text-sm md:ml-1 md:text-center">({hotel.reviews})</span>
                                </span>
                                <span class="text-lg font-bold md:mb-0 md:text-gray-900 md:text-lg md:font-semibold md:text-center">{hotel.price}</span>
                            </div>
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-black text-white text-center p-4">
        FOOTER
    </footer>
</div>
