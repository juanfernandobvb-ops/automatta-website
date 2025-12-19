<template>
    <div class="automatta-site">
        <!-- Fixed Header -->
        <header class="fixed-header">
            <div class="header-content">
                <div class="logo">AUTOMATTA</div>
                <nav class="nav-menu" :class="{ 'mobile-open': isMobileMenuOpen }">
                    <a href="#music" @click.prevent="scrollToSection('music')">MUSIC</a>
                    <a href="#about" @click.prevent="scrollToSection('about')">ABOUT</a>
                    <a href="#band" @click.prevent="scrollToSection('band')">BAND</a>
                    <a href="#contact" @click.prevent="scrollToSection('contact')">CONTACT</a>
                </nav>
                <div class="header-controls">
                    <div class="play-button" @click="togglePlayer">
                        {{ isPlayerVisible ? '■' : '▶' }}
                    </div>
                    <div class="mobile-menu-btn" @click="toggleMobileMenu">
                        <span></span>
                        <span></span>
                        <span></span>
                    </div>
                </div>
            </div>

            <!-- Collapsible Spotify Player -->
            <div class="header-spotify" :class="{ 'visible': isPlayerVisible }">
                <iframe src="https://open.spotify.com/embed/album/3bgwXXU7guiBQ4MSFtzCmQ?utm_source=generator&theme=0"
                    width="100%" height="152" frameBorder="0" allowfullscreen=""
                    allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy">
                </iframe>
            </div>
        </header>

        <!-- Hero Section -->
        <section class="hero">
            <div class="hero-grid">
                <div class="hero-left">
                    <div class="hero-label">EXPERIMENTAL SOUND</div>
                    <h1 class="hero-title">AUTOMATTA</h1>
                    <div class="hero-subtitle">REDEFINING MUSICAL BOUNDARIES</div>
                    <div class="hero-actions">
                        <button class="action-btn primary" @click="scrollToSection('music')">
                            LISTEN NOW
                        </button>
                        <button class="action-btn secondary" @click="scrollToSection('about')">
                            DISCOVER
                        </button>
                    </div>
                </div>
                <div class="hero-right">
                    <div class="hero-visual">
                        <div class="frequency-bars">
                            <div class="bar" v-for="n in 20" :key="n" :style="{ animationDelay: n * 0.1 + 's' }"></div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Music Section -->
        <section id="music" class="music-section">
            <div class="section-header">
                <div class="section-number">01</div>
                <h2 class="section-title">DISCOGRAPHY</h2>
            </div>
            <div class="music-grid">
                <div class="album-showcase">
                    <div class="album-cover">
                        <iframe
                            src="https://open.spotify.com/embed/album/3bgwXXU7guiBQ4MSFtzCmQ?utm_source=generator&theme=0"
                            width="100%" height="400" frameBorder="0" allowfullscreen=""
                            allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
                            loading="lazy">
                        </iframe>
                    </div>
                </div>
            </div>
        </section>

        <!-- About Section -->
        <section id="about" class="about-section">
            <div class="section-header">
                <div class="section-number">02</div>
                <h2 class="section-title">MANIFESTO</h2>
            </div>
            <div class="about-grid">
                <div class="about-content">
                    <div class="manifesto-text">
                        <p>AUTOMATTA transcends conventional musical boundaries, forging a new path through experimental
                            soundscapes and electronic innovation.</p>
                        <p>Our sound is the collision between organic and synthetic, where human emotion meets digital
                            precision.</p>
                        <p>We don't just make music. We architect experiences.</p>
                    </div>
                </div>
                <div class="about-stats">
                    <div class="stat-block">
                        <div class="stat-number">2024</div>
                        <div class="stat-label">ESTABLISHED</div>
                    </div>
                    <div class="stat-block">
                        <div class="stat-number">∞</div>
                        <div class="stat-label">POSSIBILITIES</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Band Members Section -->
        <section id="band" class="band-section">
            <div class="section-header">
                <div class="section-number">03</div>
                <h2 class="section-title">BAND</h2>
            </div>
            <div class="carousel-container">
                <div class="carousel-wrapper">
                    <div class="carousel-track" :style="{ transform: `translateX(-${currentSlide * 25}%)` }">
                        <div class="member-slide">
                            <div class="member-card-large">
                                <div class="member-photo-large">
                                    <div class="photo-placeholder-large">
                                        <span>PHOTO</span>
                                    </div>
                                </div>
                                <div class="member-info-large">
                                    <div class="member-name-large">NOME DO MEMBRO</div>
                                    <div class="member-instrument-large">INSTRUMENTO</div>
                                    <div class="member-description-large">
                                        Breve comentário sobre o membro, sua experiência musical e contribuição para o
                                        som da AUTOMATTA. Adicione aqui o que quiser sobre cada integrante da banda.
                                    </div>
                                    <div class="member-social">
                                        <a href="#" class="social-btn instagram" title="Instagram">
                                            <span>IG</span>
                                        </a>
                                        <a href="#" class="social-btn whatsapp" title="WhatsApp">
                                            <span>WA</span>
                                        </a>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="member-slide">
                            <div class="member-card-large">
                                <div class="member-photo-large">
                                    <div class="photo-placeholder-large">
                                        <span>PHOTO</span>
                                    </div>
                                </div>
                                <div class="member-info-large">
                                    <div class="member-name-large">NOME DO MEMBRO</div>
                                    <div class="member-instrument-large">INSTRUMENTO</div>
                                    <div class="member-description-large">
                                        Breve comentário sobre o membro, sua experiência musical e contribuição para o
                                        som da AUTOMATTA. Adicione aqui o que quiser sobre cada integrante da banda.
                                    </div>
                                    <div class="member-social">
                                        <a href="#" class="social-btn instagram" title="Instagram">
                                            <span>IG</span>
                                        </a>
                                        <a href="#" class="social-btn whatsapp" title="WhatsApp">
                                            <span>WA</span>
                                        </a>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="member-slide">
                            <div class="member-card-large">
                                <div class="member-photo-large">
                                    <div class="photo-placeholder-large">
                                        <span>PHOTO</span>
                                    </div>
                                </div>
                                <div class="member-info-large">
                                    <div class="member-name-large">NOME DO MEMBRO</div>
                                    <div class="member-instrument-large">INSTRUMENTO</div>
                                    <div class="member-description-large">
                                        Breve comentário sobre o membro, sua experiência musical e contribuição para o
                                        som da AUTOMATTA. Adicione aqui o que quiser sobre cada integrante da banda.
                                    </div>
                                    <div class="member-social">
                                        <a href="#" class="social-btn instagram" title="Instagram">
                                            <span>IG</span>
                                        </a>
                                        <a href="#" class="social-btn whatsapp" title="WhatsApp">
                                            <span>WA</span>
                                        </a>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="member-slide">
                            <div class="member-card-large">
                                <div class="member-photo-large">
                                    <div class="photo-placeholder-large">
                                        <span>PHOTO</span>
                                    </div>
                                </div>
                                <div class="member-info-large">
                                    <div class="member-name-large">NOME DO MEMBRO</div>
                                    <div class="member-instrument-large">INSTRUMENTO</div>
                                    <div class="member-description-large">
                                        Breve comentário sobre o membro, sua experiência musical e contribuição para o
                                        som da AUTOMATTA. Adicione aqui o que quiser sobre cada integrante da banda.
                                    </div>
                                    <div class="member-social">
                                        <a href="#" class="social-btn instagram" title="Instagram">
                                            <span>IG</span>
                                        </a>
                                        <a href="#" class="social-btn whatsapp" title="WhatsApp">
                                            <span>WA</span>
                                        </a>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="carousel-controls">
                    <div class="carousel-indicators">
                        <div v-for="(slide, index) in totalSlides" :key="index" class="indicator"
                            :class="{ active: currentSlide === index }" @click="goToSlide(index)">
                            {{ index + 1 }}
                        </div>
                    </div>
                    <div class="carousel-buttons">
                        <button class="carousel-btn prev" @click="prevSlide">‹</button>
                        <button class="carousel-btn next" @click="nextSlide">›</button>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="contact-section">
            <div class="section-header">
                <div class="section-number">04</div>
                <h2 class="section-title">CONNECT</h2>
            </div>
            <div class="contact-grid">
                <div class="contact-links">
                    <a href="#" class="contact-link">
                        <span class="link-label">SPOTIFY</span>
                        <span class="link-arrow">→</span>
                    </a>
                    <a href="#" class="contact-link">
                        <span class="link-label">INSTAGRAM</span>
                        <span class="link-arrow">→</span>
                    </a>
                    <a href="#" class="contact-link">
                        <span class="link-label">YOUTUBE</span>
                        <span class="link-arrow">→</span>
                    </a>
                    <a href="#" class="contact-link">
                        <span class="link-label">EMAIL</span>
                        <span class="link-arrow">→</span>
                    </a>
                </div>
            </div>
        </section>
    </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const isPlayerVisible = ref(false);
const isMobileMenuOpen = ref(false);
const currentSlide = ref(0);
const totalSlides = ref(4);
let carouselInterval = null;

const togglePlayer = () => {
    isPlayerVisible.value = !isPlayerVisible.value;
};

const toggleMobileMenu = () => {
    isMobileMenuOpen.value = !isMobileMenuOpen.value;
};

const scrollToSection = (sectionId) => {
    document.getElementById(sectionId).scrollIntoView({ behavior: 'smooth' });
    isMobileMenuOpen.value = false; // Fecha menu mobile após navegação
};

const nextSlide = () => {
    currentSlide.value = (currentSlide.value + 1) % totalSlides.value;
    resetCarouselTimer();
};

const prevSlide = () => {
    currentSlide.value = (currentSlide.value - 1 + totalSlides.value) % totalSlides.value;
    resetCarouselTimer();
};

const goToSlide = (index) => {
    currentSlide.value = index;
    resetCarouselTimer();
};

const startCarousel = () => {
    carouselInterval = setInterval(() => {
        nextSlide();
    }, 4000); // Muda a cada 4 segundos
};

const resetCarouselTimer = () => {
    if (carouselInterval) {
        clearInterval(carouselInterval);
    }
    startCarousel();
};

onMounted(() => {
    startCarousel();
});

onUnmounted(() => {
    if (carouselInterval) {
        clearInterval(carouselInterval);
    }
});
</script>

<style scoped>
/* ============================================
   AUTOMATTA - Modern Band Website Styles
   Industrial Design with Cyberpunk Aesthetic
   ============================================ */

/* Reset & Base Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
    overflow-x: hidden;
}

body, html {
    max-width: 100vw;
    overflow-x: hidden;
}

.automatta-site {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: linear-gradient(135deg, #0E0E0F 0%, #1C1E22 100%);
    color: #F2F2F2;
    line-height: 1.6;
    min-height: 100vh;
}

/* ============================================
   HEADER & NAVIGATION
   ============================================ */

.fixed-header {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    width: 100%;
    background: rgba(14, 14, 15, 0.95);
    backdrop-filter: blur(10px);
    border-bottom: 2px solid #E87A2F;
    z-index: 1000;
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.5);
}

.header-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 2rem;
    max-width: 1400px;
    margin: 0 auto;
}

.logo {
    font-size: 1.8rem;
    font-weight: 900;
    letter-spacing: 3px;
    background: linear-gradient(135deg, #F2A93B, #E87A2F);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-transform: uppercase;
    cursor: pointer;
    transition: transform 0.3s ease;
}

.logo:hover {
    transform: scale(1.05);
}

.nav-menu {
    display: flex;
    gap: 3rem;
    align-items: center;
}

.nav-menu a {
    color: #F2F2F2;
    text-decoration: none;
    font-weight: 600;
    font-size: 0.95rem;
    letter-spacing: 1px;
    text-transform: uppercase;
    position: relative;
    transition: color 0.3s ease;
}

.nav-menu a::before {
    content: '';
    position: absolute;
    bottom: -8px;
    left: 0;
    width: 0;
    height: 2px;
    background: linear-gradient(90deg, #E87A2F, #F2A93B);
    transition: width 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

.nav-menu a:hover {
    color: #E87A2F;
}

.nav-menu a:hover::before {
    width: 100%;
}

.header-controls {
    display: flex;
    gap: 1.5rem;
    align-items: center;
}

.play-button {
    width: 45px;
    height: 45px;
    background: linear-gradient(135deg, #E87A2F, #F2A93B);
    color: #0E0E0F;
    border: none;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    font-weight: 900;
    font-size: 1.2rem;
    transition: all 0.3s ease;
    border-radius: 4px;
}

.play-button:hover {
    transform: scale(1.1);
    box-shadow: 0 0 20px rgba(232, 122, 47, 0.5);
}

.mobile-menu-btn {
    display: none;
    flex-direction: column;
    width: 28px;
    height: 22px;
    cursor: pointer;
    justify-content: space-between;
    gap: 5px;
}

.mobile-menu-btn span {
    width: 100%;
    height: 3px;
    background: #F2F2F2;
    transition: all 0.3s ease;
    border-radius: 2px;
}

.header-spotify {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    background: rgba(28, 30, 34, 0.8);
    border-top: 1px solid #2B2E34;
}

.header-spotify.visible {
    max-height: 180px;
    padding: 1rem;
}

.header-spotify iframe {
    border: none;
    border-radius: 4px;
}

/* ============================================
   HERO SECTION
   ============================================ */

.hero {
    min-height: 100vh;
    padding-top: 80px;
    display: flex;
    align-items: center;
    overflow: hidden;
}

.hero-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    width: 100%;
    gap: 4rem;
    align-items: center;
    max-width: 1400px;
    margin: 0 auto;
    padding: 0 2rem;
}

.hero-left {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 1.5rem;
    animation: slideInLeft 0.8s ease-out;
}

@keyframes slideInLeft {
    from {
        opacity: 0;
        transform: translateX(-50px);
    }
    to {
        opacity: 1;
        transform: translateX(0);
    }
}

.hero-label {
    font-size: 0.85rem;
    letter-spacing: 2px;
    color: #E87A2F;
    text-transform: uppercase;
    font-weight: 700;
}

.hero-title {
    font-size: clamp(3rem, 8vw, 5rem);
    font-weight: 900;
    letter-spacing: 4px;
    line-height: 1.1;
    text-transform: uppercase;
    background: linear-gradient(135deg, #F2F2F2, #B5B8BE);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}

.hero-subtitle {
    font-size: 1.2rem;
    letter-spacing: 2px;
    color: #B5B8BE;
    text-transform: uppercase;
    font-weight: 500;
}

.hero-actions {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
    margin-top: 1rem;
}

.action-btn {
    padding: 1rem 2rem;
    font-size: 0.9rem;
    font-weight: 700;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    border: 2px solid;
    cursor: pointer;
    transition: all 0.3s ease;
    border-radius: 4px;
    font-family: inherit;
}

.action-btn.primary {
    background: linear-gradient(135deg, #E87A2F, #F2A93B);
    color: #0E0E0F;
    border-color: transparent;
}

.action-btn.primary:hover {
    transform: translateY(-3px);
    box-shadow: 0 15px 35px rgba(232, 122, 47, 0.3);
}

.action-btn.secondary {
    background: transparent;
    color: #F2A93B;
    border-color: #F2A93B;
}

.action-btn.secondary:hover {
    background: rgba(242, 169, 59, 0.1);
    transform: translateY(-3px);
}

.hero-right {
    display: flex;
    align-items: center;
    justify-content: center;
    background: radial-gradient(circle at center, rgba(232, 122, 47, 0.05) 0%, transparent 70%);
    min-height: 500px;
    border-radius: 8px;
    animation: slideInRight 0.8s ease-out;
}

@keyframes slideInRight {
    from {
        opacity: 0;
        transform: translateX(50px);
    }
    to {
        opacity: 1;
        transform: translateX(0);
    }
}

.hero-visual {
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}

.frequency-bars {
    display: flex;
    gap: 8px;
    align-items: flex-end;
    height: 250px;
    justify-content: center;
}

.bar {
    width: 8px;
    background: linear-gradient(180deg, #E87A2F, #F2A93B);
    border-radius: 4px;
    animation: frequency 0.8s ease-in-out infinite;
    box-shadow: 0 0 10px rgba(232, 122, 47, 0.5);
}

@keyframes frequency {
    0%, 100% { height: 20px; }
    50% { height: 200px; }
}

/* ============================================
   SECTIONS - GENERAL
   ============================================ */

section {
    width: 100%;
    max-width: 100%;
    padding: 5rem 2rem;
    box-sizing: border-box;
}

.section-header {
    display: flex;
    align-items: baseline;
    gap: 2rem;
    margin-bottom: 3rem;
    flex-wrap: wrap;
}

.section-number {
    font-size: 4rem;
    font-weight: 900;
    color: #2B2E34;
    line-height: 1;
}

.section-title {
    font-size: 3rem;
    font-weight: 900;
    letter-spacing: 2px;
    color: #F2F2F2;
    text-transform: uppercase;
}

/* ============================================
   MUSIC SECTION
   ============================================ */

.music-section {
    background: linear-gradient(135deg, rgba(28, 30, 34, 0.8), rgba(14, 14, 15, 0.8));
    border-top: 2px solid #E87A2F;
}

.music-grid {
    display: flex;
    justify-content: center;
    align-items: center;
    max-width: 900px;
    margin: 0 auto;
}

.album-showcase {
    width: 100%;
    animation: fadeInUp 0.8s ease-out;
}

@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.album-cover {
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 20px 50px rgba(0, 0, 0, 0.5);
}

.album-cover iframe {
    width: 100%;
    border: none;
    border-radius: 8px;
}

/* ============================================
   ABOUT SECTION
   ============================================ */

.about-section {
    background: linear-gradient(135deg, #0E0E0F, rgba(28, 30, 34, 0.5));
    border-top: 2px solid #E87A2F;
}

.about-grid {
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 4rem;
    max-width: 1200px;
    margin: 0 auto;
    align-items: start;
}

.manifesto-text p {
    font-size: 1.15rem;
    line-height: 1.8;
    margin-bottom: 2rem;
    color: #B5B8BE;
}

.about-stats {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
}

.stat-block {
    background: rgba(232, 122, 47, 0.1);
    padding: 2rem;
    border-left: 4px solid #E87A2F;
    border-radius: 4px;
    transition: all 0.3s ease;
}

.stat-block:hover {
    transform: translateX(10px);
    background: rgba(232, 122, 47, 0.2);
}

.stat-number {
    font-size: 2.5rem;
    font-weight: 900;
    color: #E87A2F;
    line-height: 1;
    margin-bottom: 0.5rem;
}

.stat-label {
    font-size: 0.8rem;
    letter-spacing: 2px;
    color: #B5B8BE;
    text-transform: uppercase;
}

/* ============================================
   BAND SECTION - CAROUSEL
   ============================================ */

.band-section {
    background: linear-gradient(135deg, rgba(28, 30, 34, 0.8), rgba(14, 14, 15, 0.8));
    border-top: 2px solid #E87A2F;
}

.carousel-container {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
}

.carousel-wrapper {
    overflow: hidden;
    border: 2px solid #E87A2F;
    border-radius: 8px;
    background: rgba(15, 42, 58, 0.3);
}

.carousel-track {
    display: flex;
    transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
    width: 400%;
}

.member-slide {
    width: 25%;
    flex-shrink: 0;
    padding: 2rem;
}

.member-card-large {
    display: grid;
    grid-template-columns: 300px 1fr;
    background: rgba(15, 42, 58, 0.5);
    min-height: 400px;
    border-radius: 8px;
    overflow: hidden;
    transition: all 0.3s ease;
}

.member-card-large:hover {
    box-shadow: 0 15px 40px rgba(232, 122, 47, 0.2);
    transform: translateY(-5px);
}

.member-photo-large {
    background: #0E0E0F;
    display: flex;
    align-items: center;
    justify-content: center;
    border-right: 2px solid #E87A2F;
    position: relative;
    overflow: hidden;
}

.photo-placeholder-large {
    width: 100%;
    height: 100%;
    background: linear-gradient(135deg, #1C1E22, #2B2E34);
    display: flex;
    align-items: center;
    justify-content: center;
    color: #B5B8BE;
    font-weight: 700;
    letter-spacing: 1px;
    font-size: 0.9rem;
    position: relative;
}

.photo-placeholder-large::before {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, rgba(232, 122, 47, 0.1), transparent);
    pointer-events: none;
}

.member-info-large {
    padding: 2rem;
    display: flex;
    flex-direction: column;
    gap: 1rem;
    justify-content: center;
}

.member-name-large {
    font-size: 1.8rem;
    font-weight: 900;
    letter-spacing: 1px;
    color: #F2F2F2;
    text-transform: uppercase;
}

.member-instrument-large {
    font-size: 1rem;
    font-weight: 700;
    letter-spacing: 2px;
    color: #E87A2F;
    text-transform: uppercase;
}

.member-description-large {
    font-size: 0.95rem;
    line-height: 1.6;
    color: #B5B8BE;
    margin-top: 0.5rem;
}

.member-social {
    display: flex;
    gap: 1rem;
    margin-top: 1.5rem;
}

.social-btn {
    width: 45px;
    height: 45px;
    background: #1C1E22;
    border: 2px solid #2B2E34;
    color: #F2F2F2;
    text-decoration: none;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: 700;
    font-size: 0.75rem;
    letter-spacing: 1px;
    cursor: pointer;
    transition: all 0.3s ease;
    border-radius: 4px;
    text-transform: uppercase;
}

.social-btn:hover {
    border-color: #E87A2F;
    transform: scale(1.1);
}

.social-btn.instagram:hover {
    background: #E4405F;
    border-color: #E4405F;
    box-shadow: 0 0 15px rgba(228, 64, 95, 0.3);
}

.social-btn.whatsapp:hover {
    background: #25D366;
    border-color: #25D366;
    box-shadow: 0 0 15px rgba(37, 211, 102, 0.3);
}

.carousel-controls {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 2rem 0;
    gap: 2rem;
}

.carousel-indicators {
    display: flex;
    gap: 1rem;
    justify-content: center;
    flex: 1;
}

.indicator {
    width: 50px;
    height: 50px;
    background: #2B2E34;
    cursor: pointer;
    transition: all 0.3s ease;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: 700;
    color: #B5B8BE;
    border: 2px solid #2B2E34;
    border-radius: 4px;
    text-transform: uppercase;
    font-size: 0.8rem;
}

.indicator:hover {
    border-color: #E87A2F;
    color: #E87A2F;
}

.indicator.active {
    background: #E87A2F;
    color: #0E0E0F;
    border-color: #E87A2F;
    transform: scale(1.05);
    box-shadow: 0 0 20px rgba(232, 122, 47, 0.4);
}

.carousel-buttons {
    display: flex;
    gap: 1rem;
}

.carousel-btn {
    width: 50px;
    height: 50px;
    background: #1C1E22;
    border: 2px solid #E87A2F;
    color: #F2F2F2;
    cursor: pointer;
    font-size: 1.5rem;
    font-weight: 300;
    transition: all 0.3s ease;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 4px;
}

.carousel-btn:hover {
    background: #E87A2F;
    color: #0E0E0F;
    transform: scale(1.1);
    box-shadow: 0 0 20px rgba(232, 122, 47, 0.4);
}

/* ============================================
   CONTACT SECTION
   ============================================ */

.contact-section {
    background: linear-gradient(135deg, rgba(15, 42, 58, 0.5), #0E0E0F);
    border-top: 2px solid #E87A2F;
}

.contact-grid {
    max-width: 800px;
    margin: 0 auto;
}

.contact-links {
    display: flex;
    flex-direction: column;
    gap: 1px;
}

.contact-link {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 2rem;
    background: #1C1E22;
    color: #F2F2F2;
    text-decoration: none;
    border: 1px solid #2B2E34;
    transition: all 0.3s ease;
    font-weight: 600;
    letter-spacing: 1px;
}

.contact-link:first-child {
    border-radius: 8px 8px 0 0;
}

.contact-link:last-child {
    border-radius: 0 0 8px 8px;
}

.contact-link:hover {
    background: #E87A2F;
    color: #0E0E0F;
    border-color: #E87A2F;
    transform: translateX(10px);
    box-shadow: 0 10px 30px rgba(232, 122, 47, 0.2);
}

.link-label {
    font-size: 1.1rem;
    font-weight: 700;
    text-transform: uppercase;
}

.link-arrow {
    font-size: 1.5rem;
    font-weight: 300;
    transition: transform 0.3s ease;
}

.contact-link:hover .link-arrow {
    transform: translateX(10px);
}

/* ============================================
   RESPONSIVE DESIGN
   ============================================ */

@media (max-width: 1024px) {
    .hero-grid {
        gap: 2rem;
    }

    .hero-title {
        font-size: clamp(2.5rem, 6vw, 4rem);
    }

    .hero-right {
        min-height: 400px;
    }

    .frequency-bars {
        height: 200px;
    }

    .about-grid {
        grid-template-columns: 1fr;
    }

    .section-number {
        font-size: 3rem;
    }

    .section-title {
        font-size: 2.5rem;
    }

    .member-card-large {
        grid-template-columns: 200px 1fr;
        min-height: 300px;
    }

    .member-photo-large {
        border-right: 2px solid #E87A2F;
    }

    .member-info-large {
        padding: 1.5rem;
    }

    .member-name-large {
        font-size: 1.4rem;
    }

    .member-slide {
        padding: 1rem;
    }
}

@media (max-width: 768px) {
    .header-content {
        padding: 1rem;
    }

    .nav-menu {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100vh;
        background: rgba(14, 14, 15, 0.98);
        display: flex;
        flex-direction: column;
        gap: 3rem;
        align-items: center;
        justify-content: center;
        transform: translateX(-100%);
        transition: transform 0.3s ease;
        z-index: 999;
    }

    .nav-menu.mobile-open {
        transform: translateX(0);
    }

    .mobile-menu-btn {
        display: flex;
    }

    .hero-grid {
        grid-template-columns: 1fr;
        gap: 2rem;
        padding: 0 1rem;
    }

    .hero-left {
        text-align: center;
    }

    .hero-title {
        font-size: clamp(2rem, 5vw, 3.5rem);
    }

    .hero-actions {
        flex-direction: column;
    }

    .action-btn {
        width: 100%;
    }

    .hero-right {
        min-height: 300px;
    }

    .frequency-bars {
        height: 150px;
        gap: 6px;
    }

    .bar {
        width: 6px;
    }

    section {
        padding: 3rem 1rem;
    }

    .section-header {
        flex-direction: column;
        gap: 1rem;
    }

    .section-number {
        font-size: 2.5rem;
    }

    .section-title {
        font-size: 2rem;
    }

    .about-stats {
        grid-template-columns: 1fr;
    }

    .manifesto-text p {
        font-size: 1rem;
    }

    .carousel-wrapper {
        border: 1px solid #E87A2F;
        border-radius: 4px;
    }

    .member-card-large {
        grid-template-columns: 1fr;
        min-height: auto;
    }

    .member-photo-large {
        border-right: none;
        border-bottom: 2px solid #E87A2F;
        min-height: 250px;
    }

    .member-slide {
        padding: 1rem 0;
    }

    .member-info-large {
        padding: 1.5rem;
    }

    .member-name-large {
        font-size: 1.3rem;
    }

    .carousel-controls {
        flex-direction: column;
        gap: 1.5rem;
        padding: 1.5rem 0;
    }

    .carousel-indicators {
        gap: 0.5rem;
    }

    .indicator {
        width: 40px;
        height: 40px;
        font-size: 0.7rem;
    }

    .carousel-buttons {
        gap: 0.5rem;
    }

    .carousel-btn {
        width: 45px;
        height: 45px;
    }

    .contact-link {
        padding: 1.5rem;
        font-size: 0.95rem;
    }

    .link-label {
        font-size: 1rem;
    }

    .link-arrow {
        font-size: 1.2rem;
    }
}

@media (max-width: 480px) {
    .header-content {
        padding: 0.75rem;
    }

    .logo {
        font-size: 1.3rem;
    }

    .nav-menu a {
        font-size: 1.1rem;
    }

    .hero-title {
        font-size: 2rem;
    }

    .hero-subtitle {
        font-size: 0.95rem;
    }

    .action-btn {
        padding: 0.8rem 1.5rem;
        font-size: 0.85rem;
    }

    .frequency-bars {
        height: 120px;
        gap: 4px;
    }

    .bar {
        width: 4px;
    }

    .section-number {
        font-size: 2rem;
        order: 2;
    }

    .section-title {
        font-size: 1.5rem;
        order: 1;
    }

    .member-name-large {
        font-size: 1.1rem;
    }

    .member-instrument-large {
        font-size: 0.9rem;
    }

    .member-description-large {
        font-size: 0.85rem;
    }

    .contact-link {
        padding: 1rem;
    }

    .link-label {
        font-size: 0.9rem;
    }
}
</style>