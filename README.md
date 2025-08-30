<html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Body Health care</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f0fdf4;
            color: #166534;
            scroll-behavior: smooth;
        }
        .section-heading {
            position: relative;
            display: inline-block;
            padding-bottom: 0.5rem;
            margin-bottom: 2.5rem;
            font-size: 2.5rem;
            font-weight: 700; 
            color: #047857;
        }
        .section-heading::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 70%;
            height: 5px;
            background-color: #065f46;
            border-radius: 9999px;
        }
        .tip-card {
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }
        .tip-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }
        .carousel-container {
            position: relative;
            max-width: 100%;
            overflow: hidden;
            border-radius: 1.5rem;
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
            height: 400px;
        }
        .carousel-slide {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0;
            visibility: hidden;
            transition: opacity 1s ease-in-out, visibility 1s;
        }
        .carousel-slide.active {
            opacity: 1;
            visibility: visible;
        }
        .carousel-slide img {
            width: 100%;
            height: 400px;
            object-fit: cover;
        }
        .carousel-dot {
            height: 10px;
            width: 10px;
            margin: 0 4px;
            background-color: #cbd5e0;
            border-radius: 50%;
            display: inline-block;
            transition: background-color 0.6s ease;
            cursor: pointer;
        }
        .carousel-dot.active {
            background-color: #065f46;
        }
        .carousel-btn {
            cursor: pointer;
            position: absolute;
            top: 50%;
            width: auto;
            padding: 1rem;
            margin-top: -2.5rem;
            color: white;
            font-weight: bold;
            font-size: 1.5rem;
            transition: 0.6s ease;
            border-radius: 0 0.75rem 0.75rem 0;
            user-select: none;
            background-color: rgba(0, 0, 0, 0.5);
            z-index: 10;
        }
        .carousel-btn-prev {
            left: 0;
            border-radius: 0.75rem 0 0 0.75rem;
        }
        .carousel-btn-next {
            right: 0;
            border-radius: 0 0.75rem 0.75rem 0;
        }
        .carousel-btn:hover {
            background-color: rgba(0, 0, 0, 0.8);
        }
    </style>
</head>
<body class="antialiased">

    <nav class="bg-emerald-800 p-4 shadow-md sticky top-0 z-50">
        <div class="max-w-7xl mx-auto flex justify-between items-center">
            <a href="#" class="text-white text-2xl font-bold tracking-wide hover:text-emerald-200 transition duration-300">HEALTH CARE TIPS </a>
            <div class="hidden md:flex space-x-8">
                <a href="#" class="text-white hover:text-emerald-200 transition duration-300 ease-in-out px-3 py-2 rounded-md hover:bg-emerald-700">Home</a>
                <a href="#about-us" class="text-white hover:text-emerald-200 transition duration-300 ease-in-out px-3 py-2 rounded-md hover:bg-emerald-700">About</a>
                <a href="#health-tips" class="text-white hover:text-emerald-200 transition duration-300 ease-in-out px-3 py-2 rounded-md hover:bg-emerald-700">Health Tips</a>
            </div>
            <div class="md:hidden">
                <button id="mobile-menu-btn" class="text-white focus:outline-none">
                    <svg class="w-7 h-7" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                    </svg>
                </button>
            </div>
        </div>
        <div id="mobile-menu" class="md:hidden hidden bg-emerald-900 mt-4 rounded-lg">
            <a href="#" class="block px-4 py-3 text-white hover:bg-emerald-800 rounded-md">Home</a>
            <a href="#about-us" class="block px-4 py-3 text-white hover:bg-emerald-800 rounded-md">About</a>
            <a href="#health-tips" class="block px-4 py-3 text-white hover:bg-emerald-800 rounded-md">Health Tips</a>
        </div>
    </nav>

    <header class="bg-gradient-to-r from-emerald-600 to-green-700 text-white py-20 px-4 sm:px-6 lg:px-8 shadow-xl rounded-b-3xl">
        <div class="max-w-7xl mx-auto text-center">
            <h1 class="text-5xl sm:text-6xl font-extrabold leading-tight mb-4">
                Harmonize Your Body, Optimize Your Life! 💚
            </h1>
            <p class="text-xl sm:text-2xl mb-8 opacity-90">
                Dive deep into understanding and nurturing every part of your amazing body.
            </p>
            <a href="#health-tips" class="inline-block bg-white text-emerald-700 hover:bg-gray-100 font-bold py-3 px-8 rounded-full shadow-lg transform transition duration-300 hover:scale-105">
                Explore Body Health Tips
            </a>
        </div>
    </header>

    <section class="max-w-7xl mx-auto my-16 px-4 sm:px-6 lg:px-8">
        <div class="carousel-container">
            <div class="carousel-slide fade">
                <img src="https://placehold.co/1200x400/81c784/ffffff?text=Balanced+Nutrition+for+Organs" alt="Balanced Nutrition for Organs">
            </div>
            <div class="carousel-slide fade">
                <img src="https://placehold.co/1200x400/64b5f6/ffffff?text=Active+Lifestyle+for+Muscles" alt="Active Lifestyle for Muscles">
            </div>
            <div class="carousel-slide fade">
                <img src="https://placehold.co/1200x400/ffb74d/ffffff?text=Mindfulness+for+Mental+Wellness" alt="Mindfulness for Mental Wellness">
            </div>

            <a class="carousel-btn carousel-btn-prev" onclick="changeSlide(-1)">&#10094;</a>
            <a class="carousel-btn carousel-btn-next" onclick="changeSlide(1)">&#10095;</a>
        </div>
        <div class="text-center mt-6">
            <span class="carousel-dot" onclick="currentCarouselSlide(1)"></span>
            <span class="carousel-dot" onclick="currentCarouselSlide(2)"></span>
            <span class="carousel-dot" onclick="currentCarouselSlide(3)"></span>
        </div>
    </section>

    <section id="health-tips" class="py-16 px-4 sm:px-6 lg:px-8 bg-green-50 rounded-xl mx-auto max-w-7xl mt-12 shadow-md">
        <div class="text-center mb-16">
            <h2 class="section-heading">Nurture Every Part of Your Body ✨</h2>
            <p class="text-lg text-green-700 max-w-3xl mx-auto">
                Explore vital tips for the well-being of your essential body systems.
            </p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <a href="#heart-lungs-detail" class="tip-card bg-white p-6 rounded-xl shadow-lg border border-green-100 block hover:border-green-300">
                <div class="flex items-center mb-4">
                    <span class="text-3xl mr-3">❤️‍🩹</span>
                    <h3 class="text-2xl font-semibold text-emerald-800">Heart & Lungs Health</h3>
                </div>
                <p class="text-green-800 text-base leading-relaxed">
                    Keep your cardiovascular and respiratory systems strong with these essential practices.
                </p>
            </a>
            <a href="#digestive-detail" class="tip-card bg-white p-6 rounded-xl shadow-lg border border-green-100 block hover:border-green-300">
                <div class="flex items-center mb-4">
                    <span class="text-3xl mr-3">🍎</span>
                    <h3 class="text-2xl font-semibold text-emerald-800">Digestive System Support</h3>
                </div>
                <p class="text-green-800 text-base leading-relaxed">
                    Understand how to fuel your body and maintain a healthy gut for optimal function.
                </p>
            </a>
            <a href="#musculoskeletal-detail" class="tip-card bg-white p-6 rounded-xl shadow-lg border border-green-100 block hover:border-green-300">
                <div class="flex items-center mb-4">
                    <span class="text-3xl mr-3">💪</span>
                    <h3 class="text-2xl font-semibold text-emerald-800">Musculoskeletal Strength</h3>
                </div>
                <p class="text-green-800 text-base leading-relaxed">
                    Tips for strong bones, flexible joints, and robust muscles to support your active life.
                </p>
            </a>
            <a href="#brain-nerves-detail" class="tip-card bg-white p-6 rounded-xl shadow-lg border border-green-100 block hover:border-green-300">
                <div class="flex items-center mb-4">
                    <span class="text-3xl mr-3">🧠</span>
                    <h3 class="text-2xl font-semibold text-emerald-800">Brain & Nervous System</h3>
                </div>
                <p class="text-green-800 text-base leading-relaxed">
                    Strategies to enhance cognitive function, reduce stress, and promote mental clarity.
                </p>
            </a>
            <a href="#skin-detail" class="tip-card bg-white p-6 rounded-xl shadow-lg border border-green-100 block hover:border-green-300">
                <div class="flex items-center mb-4">
                    <span class="text-3xl mr-3">🧖‍♀️</span>
                    <h3 class="text-2xl font-semibold text-emerald-800">Skin & Hair Wellness</h3>
                </div>
                <p class="text-green-800 text-base leading-relaxed">
                    Discover habits for radiant skin and healthy hair, reflecting your inner vitality.
                </p>
            </a>
            <a href="#immune-detail" class="tip-card bg-white p-6 rounded-xl shadow-lg border border-green-100 block hover:border-green-300">
                <div class="flex items-center mb-4">
                    <span class="text-3xl mr-3">🛡️</span>
                    <h3 class="text-2xl font-semibold text-emerald-800">Immune System Boost</h3>
                </div>
                <p class="text-green-800 text-base leading-relaxed">
                    Strengthen your body's natural defenses against illness and stay resilient.
                </p>
            </a>
        </div>
    </section>

    <section id="heart-lungs-detail" class="py-16 px-4 sm:px-6 lg:px-8 bg-white rounded-xl mx-auto max-w-7xl my-12 shadow-md">
        <div class="text-center mb-16">
            <h2 class="section-heading">Deep Dive: Heart & Lungs Health ❤️‍🩹</h2>
        </div>
        <div class="max-w-4xl mx-auto text-green-800 leading-relaxed text-lg">
            <p class="mb-6">
                Your **heart** and **lungs** work tirelessly to keep you alive and energetic. The heart pumps oxygen-rich blood throughout your body, while your lungs bring in that vital oxygen and expel carbon dioxide. Maintaining their health is paramount.
            </p>
            <h3 class="text-2xl font-semibold text-emerald-800 mb-4">Key Tips for Optimal Function:</h3>
            <ul class="list-disc list-inside space-y-2 mb-6">
                <li>**Cardio Exercise:** Engage in activities like brisk walking, jogging, swimming, or cycling for at least 30 minutes, 3-5 times a week. This strengthens your heart muscle and improves lung capacity.</li>
                <li>**Balanced Diet:** Limit saturated and trans fats, cholesterol, and sodium. Focus on whole grains, lean proteins, fruits, and vegetables to support arterial health.</li>
                <li>**Avoid Smoking:** Smoking is extremely damaging to both your heart and lungs, significantly increasing the risk of heart disease, stroke, and various lung conditions.</li>
                <li>**Manage Blood Pressure & Cholesterol:** Regularly monitor these levels and follow medical advice to keep them within a healthy range.</li>
            </ul>
            <p>
                A healthy heart and strong lungs are the foundation of a vibrant life. Take proactive steps to care for them daily.
            </p>
            <div class="mt-8 text-center">
                <img src="https://placehold.co/600x300/e0f2f7/00796b?text=Healthy+Heart+%26+Lungs" alt="Healthy Heart and Lungs" class="rounded-xl shadow-lg inline-block">
            </div>
        </div>
    </section>
    <hr class="max-w-7xl mx-auto my-12 border-green-200">

    <section id="digestive-detail" class="py-16 px-4 sm:px-6 lg:px-8 bg-green-50 rounded-xl mx-auto max-w-7xl my-12 shadow-md">
        <div class="text-center mb-16">
            <h2 class="section-heading">Deep Dive: Digestive System Support 🍎</h2>
        </div>
        <div class="max-w-4xl mx-auto text-green-800 leading-relaxed text-lg">
            <p class="mb-6">
                Your **digestive system** is a complex network responsible for breaking down food, absorbing nutrients, and eliminating waste. A healthy gut is crucial for overall well-being, influencing everything from energy levels to immune function.
            </p>
            <h3 class="text-2xl font-semibold text-emerald-800 mb-4">Key Tips for a Healthy Gut:</h3>
            <ul class="list-disc list-inside space-y-2 mb-6">
                <li>**Fiber-Rich Foods:** Consume plenty of fruits, vegetables, and whole grains. Fiber aids digestion, prevents constipation, and feeds beneficial gut bacteria.</li>
                <li>**Probiotics & Prebiotics:** Include foods rich in probiotics (yogurt, kimchi, sauerkraut) and prebiotics (garlic, onions, bananas) to foster a healthy gut microbiome.</li>
                <li>**Stay Hydrated:** Water is essential for breaking down food and ensuring smooth passage through the digestive tract.</li>
                <li>**Mindful Eating:** Eat slowly, chew your food thoroughly, and avoid overeating. This helps your body process food more efficiently.</li>
            </ul>
            <p>
                Listen to your gut! Taking care of your digestive system is a cornerstone of good health.
            </p>
            <div class="mt-8 text-center">
                <img src="https://placehold.co/600x300/f0f9ff/00796b?text=Healthy+Digestion" alt="Healthy Digestive System" class="rounded-xl shadow-lg inline-block">
            </div>
        </div>
    </section>
    <hr class="max-w-7xl mx-auto my-12 border-green-200">

    <section id="musculoskeletal-detail" class="py-16 px-4 sm:px-6 lg:px-8 bg-white rounded-xl mx-auto max-w-7xl my-12 shadow-md">
        <div class="text-center mb-16">
            <h2 class="section-heading">Deep Dive: Musculoskeletal Strength 💪</h2>
        </div>
        <div class="max-w-4xl mx-auto text-green-800 leading-relaxed text-lg">
            <p class="mb-6">
                Your **musculoskeletal system**—comprising bones, muscles, cartilage, tendons, ligaments, and joints—provides support, stability, and movement. Keeping it strong and flexible is vital for independence and quality of life.
            </p>
            <h3 class="text-2xl font-semibold text-emerald-800 mb-4">Key Tips for Strong Bones & Muscles:</h3>
            <ul class="list-disc list-inside space-y-2 mb-6">
                <li>**Weight-Bearing Exercise:** Activities like walking, running, dancing, and weightlifting help build and maintain bone density and muscle mass.</li>
                <li>**Calcium & Vitamin D:** Ensure adequate intake through diet (dairy, leafy greens) and sunlight exposure or supplements for strong bones.</li>
                <li>**Flexibility & Stretching:** Regular stretching and activities like yoga improve joint mobility and reduce muscle stiffness.</li>
                <li>**Proper Posture:** Maintain good posture to protect your spine and joints from unnecessary strain.</li>
            </ul>
            <p>
                Invest in your musculoskeletal health to enjoy a full, active life at any age.
            </p>
            <div class="mt-8 text-center">
                <img src="https://placehold.co/600x300/e0f2f7/00796b?text=Strong+Bones+%26+Muscles" alt="Strong Bones and Muscles" class="rounded-xl shadow-lg inline-block">
            </div>
        </div>
    </section>
    <hr class="max-w-7xl mx-auto my-12 border-green-200">

    <section id="brain-nerves-detail" class="py-16 px-4 sm:px-6 lg:px-8 bg-green-50 rounded-xl mx-auto max-w-7xl my-12 shadow-md">
        <div class="text-center mb-16">
            <h2 class="section-heading">Deep Dive: Brain & Nervous System 🧠</h2>
        </div>
        <div class="max-w-4xl mx-auto text-green-800 leading-relaxed text-lg">
            <p class="mb-6">
                Your **brain** is the control center of your body, and your **nervous system** is the communication network. Nurturing these systems is crucial for cognitive function, emotional well-being, and overall body control.
            </p>
            <h3 class="text-2xl font-semibold text-emerald-800 mb-4">Key Tips for Brain Health:</h3>
            <ul class="list-disc list-inside space-y-2 mb-6">
                <li>**Mental Stimulation:** Keep your brain active with puzzles, reading, learning new skills, and engaging in social activities.</li>
                <li>**Quality Sleep:** Sufficient sleep is vital for memory consolidation, cognitive processing, and emotional regulation.</li>
                <li>**Stress Reduction:** Chronic stress can negatively impact brain health. Practice mindfulness, meditation, or spend time in nature.</li>
                <li>**Omega-3 Fatty Acids:** Include foods rich in omega-3s (fatty fish, flaxseeds) which are essential for brain structure and function.</li>
            </ul>
            <p>
                A healthy mind is as important as a healthy body. Prioritize habits that support your brain and nervous system.
            </p>
            <div class="mt-8 text-center">
                <img src="https://placehold.co/600x300/f0f9ff/00796b?text=Healthy+Brain" alt="Healthy Brain and Nervous System" class="rounded-xl shadow-lg inline-block">
            </div>
        </div>
    </section>
    <hr class="max-w-7xl mx-auto my-12 border-green-200">

    <section id="skin-detail" class="py-16 px-4 sm:px-6 lg:px-8 bg-white rounded-xl mx-auto max-w-7xl my-12 shadow-md">
        <div class="text-center mb-16">
            <h2 class="section-heading">Deep Dive: Skin & Hair Wellness 🧖‍♀️</h2>
        </div>
        <div class="max-w-4xl mx-auto text-green-800 leading-relaxed text-lg">
            <p class="mb-6">
                Your **skin** is your body's largest organ, acting as a protective barrier against the environment. Healthy skin and hair not only look good but also indicate overall internal wellness.
            </p>
            <h3 class="text-2xl font-semibold text-emerald-800 mb-4">Key Tips for Radiant Skin & Hair:</h3>
            <ul class="list-disc list-inside space-y-2 mb-6">
                <li>**Sun Protection:** Always use sunscreen, wear protective clothing, and seek shade to prevent sun damage, which can lead to premature aging and skin cancer.</li>
                <li>**Gentle Cleansing & Moisturizing:** Use mild products suited for your skin type. Hydrate your skin regularly to maintain its barrier function.</li>
                <li>**Nutrient-Rich Diet:** A diet rich in antioxidants (berries, leafy greens) and healthy fats (avocado, nuts) supports skin elasticity and hair strength.</li>
                <li>**Adequate Hydration:** Water keeps your skin supple and helps flush out toxins, contributing to a clear complexion.</li>
            </ul>
            <p>
                Nourish your skin and hair from the inside out for a healthy, vibrant appearance.
            </p>
            <div class="mt-8 text-center">
                <img src="https://placehold.co/600x300/e0f2f7/00796b?text=Healthy+Skin+%26+Hair" alt="Healthy Skin and Hair" class="rounded-xl shadow-lg inline-block">
            </div>
        </div>
    </section>
    <hr class="max-w-7xl mx-auto my-12 border-green-200">

    <section id="immune-detail" class="py-16 px-4 sm:px-6 lg:px-8 bg-green-50 rounded-xl mx-auto max-w-7xl my-12 shadow-md">
        <div class="text-center mb-16">
            <h2 class="section-heading">Deep Dive: Immune System Boost 🛡️</h2>
        </div>
        <div class="max-w-4xl mx-auto text-green-800 leading-relaxed text-lg">
            <p class="mb-6">
                Your **immune system** is your body's defense army, constantly working to protect you from harmful pathogens. A strong immune system is key to staying healthy and recovering quickly from illness.
            </p>
            <h3 class="2xl font-semibold text-emerald-800 mb-4">Key Tips for a Robust Immune System:</h3>
            <ul class="list-disc list-inside space-y-2 mb-6">
                <li>**Vitamin & Mineral Rich Diet:** Consume foods high in Vitamin C (citrus, bell peppers), Vitamin D (fatty fish, fortified foods), and Zinc (nuts, legumes) to support immune function.</li>
                <li>**Regular Exercise:** Moderate exercise can boost immune cell activity, but avoid overtraining, which can suppress immunity.</li>
                <li>**Adequate Sleep:** During sleep, your body produces protective proteins called cytokines. Chronic sleep deprivation weakens your immune response.</li>
                <li>**Stress Management:** High stress levels can compromise your immune system. Practice relaxation techniques to keep stress in check.</li>
            </ul>
            <p>
                Empower your immune system with these habits to build a strong shield against illness.
            </p>
            <div class="mt-8 text-center">
                <img src="https://placehold.co/600x300/f0f9ff/00796b?text=Strong+Immune+System" alt="Strong Immune System" class="rounded-xl shadow-lg inline-block">
            </div>
        </div>
    </section>

    <section id="about-us" class="py-16 px-4 sm:px-6 lg:px-8 bg-white rounded-xl mx-auto max-w-7xl my-12 shadow-md">
        <div class="text-center mb-16">
            <h2 class="section-heading">About Us 🌟</h2>
            <p class="text-lg text-green-700 max-w-3xl mx-auto">
                Our mission is to empower you with knowledge to make informed decisions about your health.
            </p>
        </div>
        <div class="max-w-4xl mx-auto text-green-800 leading-relaxed text-lg">
            <p class="mb-6">
                Welcome to Body Health Hub, your trusted source for reliable and easy-to-understand health information focusing on different parts of your amazing body. In today's fast-paced world, maintaining good health can be challenging. Our goal is to simplify this by providing practical tips, actionable advice, and clear explanations on various aspects of health and wellness.
            </p>
            <p class="mb-6">
                We believe that everyone deserves access to accurate health guidance. Whether you're looking for nutrition advice, exercise routines, stress management techniques, or simply want to learn more about preventive care, we're here to help. Our content is carefully curated to ensure it's both informative and easy to implement into your daily life.
            </p>
            <p>
                Join us on a journey towards a healthier, happier you! We're committed to supporting your well-being every step of the way.
            </p>
        </div>
    </section>

    <footer class="bg-emerald-900 text-white py-8 px-4 sm:px-6 lg:px-8 text-center rounded-t-xl mt-12">
        <div class="max-w-7xl mx-auto">
            <p>&copy; 2025 <span class="font-bold">SA2</span>. All rights reserved.</p>
            <div class="flex justify-center space-x-4 mt-4">
                <a href="#" class="text-gray-300 hover:text-white transition duration-300">PRATHMESH REDDY </a>
                <a href="#" class="text-gray-300 hover:text-white transition duration-300">ANKIT SINGH</a>
            </div><a href="#" class="text-gray-300 hover:text-white transition duration-300">NIKHIL GOSAVI</a>
                <a href="#" class="text-gray-300 hover:text-white transition duration-300">   /   DEEPAK PATIL</a>
                <a href="#" class="text-gray-300 hover:text-white transition duration-300">    /  RUPESH PANDIT</a>
                
        </div>
    </footer>

    <script>
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');

        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        let slideIndex = 1;
        showSlides(slideIndex);

        function changeSlide(n) {
            showSlides(slideIndex += n);
        }

        function currentCarouselSlide(n) {
            showSlides(slideIndex = n);
        }

        function showSlides(n) {
            let i;
            let slides = document.getElementsByClassName("carousel-slide");
            let dots = document.getElementsByClassName("carousel-dot");

            if (n > slides.length) { slideIndex = 1; }
            if (n < 1) { slideIndex = slides.length; }

            for (i = 0; i < slides.length; i++) {
                slides[i].classList.remove('active');
            }
            for (i = 0; i < dots.length; i++) {
                dots[i].className = dots[i].className.replace(" active", "");
            }

            slides[slideIndex-1].classList.add('active');
            dots[slideIndex-1].className += " active";
        }

        let autoSlideIndex = 0;
        autoCarousel();

        function autoCarousel() {
            let i;
            let slides = document.getElementsByClassName("carousel-slide");
            let dots = document.getElementsByClassName("carousel-dot");

            for (i = 0; i < slides.length; i++) {
                slides[i].classList.remove('active');
            }
            autoSlideIndex++;
            if (autoSlideIndex > slides.length) { autoSlideIndex = 1; }
            for (i = 0; i < dots.length; i++) {
                dots[i].className = dots[i].className.replace(" active", "");
            }
            slides[autoSlideIndex-1].classList.add('active');
            dots[autoSlideIndex-1].className += " active";
            setTimeout(autoCarousel, 5000);
        }
    </script>
</body>
</html>
