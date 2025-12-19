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
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html, body {
  overflow-x: hidden;
  max-width: 100vw;
}

.automatta-site {
  font-family: 'JetBrains Mono', monospace;
  background: #0E0E0F;
  color: #F2F2F2;
  overflow-x: hidden;
  width: 100%;
  max-width: 100vw;
    left: 0;
    right: 0;
    z-index: 1000;
    background: rgba(14, 14, 15, 0.95);
    backdrop-filter: blur(20px);
    border-bottom: 1px solid #2B2E34;
}

.header-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
  width: 100%;
  max-width: 100vw;
  box-sizing: border-box;
}

.logo {
  font-weight: 900;
  font-size: 1.2rem;
  letter-spacing: 0.2em;
  color: #F2A93B;
  white-space: nowrap;

.nav-menu {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    background: rgba(14, 14, 15, 0.98);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 3rem;
    transform: translateX(-100%);
    transition: transform 0.3s ease;
    z-index: 999;
}

.nav-menu.mobile-open {
    transform: translateX(0);
}

.nav-menu a {
    color: #F2F2F2;
    text-decoration: none;
    font-weight: 600;
    font-size: 1.2rem;
    letter-spacing: 0.1em;
    position: relative;
    transition: color 0.3s;
}

.nav-menu a:hover {
    color: #E87A2F;
}

.nav-menu a::after {
    content: '';
    position: absolute;
    bottom: -5px;
    left: 0;
    width: 0;
    height: 2px;
    background: #E87A2F;
    transition: width 0.3s;
}

.nav-menu a:hover::after {
    width: 100%;
}

.header-controls {
    display: flex;
    align-items: center;
    gap: 1rem;
    justify-self: end;
}

.mobile-menu-btn {
    display: flex;
    flex-direction: column;
    width: 30px;
    height: 22px;
    cursor: pointer;
    justify-content: space-between;
    z-index: 1001;
}

.mobile-menu-btn span {
    width: 100%;
    height: 3px;
    background: #F2F2F2;
    transition: all 0.3s;
}

.mobile-menu-btn:hover span {
    background: #E87A2F;
}

.play-button {
    width: 40px;
    height: 40px;
    background: #E87A2F;
    color: #0E0E0F;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    font-weight: 900;
    font-size: 1.2rem;
    transition: all 0.3s;
}

.play-button:hover {
    background: #F2A93B;
    transform: scale(1.1);
}

.header-spotify {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.3s ease;
    background: #1C1E22;
}

.header-spotify.visible {
    max-height: 152px;
    border-bottom: 1px solid #2B2E34;
}

/* Hero Section */
.hero {
    min-height: 100vh;
    padding: 120px 0 0 0;
    display: flex;
    align-items: center;
}

.hero-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    width: 100%;
    height: 80vh;
}

.hero-left {
    padding: 0 4rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    background: linear-gradient(45deg, #0E0E0F, #1C1E22);
}

.hero-label {
  font-size: 0.6rem;
  letter-spacing: 0.2em;
  color: #F2A93B;
  margin-bottom: 0.8rem;
  font-weight: 600;
}

.hero-title {
  font-size: 2.2rem;
  font-weight: 900;
  letter-spacing: 0.05em;
  line-height: 0.9;
  margin-bottom: 1rem;
  color: #F2F2F2;
  word-break: keep-all;
}

.hero-subtitle {
  font-size: 0.9rem;
  letter-spacing: 0.1em;
  color: #B5B8BE;
  margin-bottom: 2rem;
  font-weight: 400;
  line-height: 1.4;
}

.hero-actions {
  display: flex;
  gap: 0.5rem;
  flex-direction: column;
  width: 100%;
}

.action-btn {
  padding: 1rem 1.5rem;
  font-family: inherit;
  font-weight: 700;
  letter-spacing: 0.1em;
  border: none;
  cursor: pointer;
  transition: all 0.3s;
  text-transform: uppercase;
  font-size: 0.8rem;
  width: 100%;
  box-sizing: border-box;

.action-btn.primary {
    background: #E87A2F;
    color: #F2F2F2;
}

.action-btn.secondary {
    background: transparent;
    color: #F2F2F2;
    border: 2px solid #E87A2F;
}

.action-btn:hover {
    transform: skew(-5deg);
}

.action-btn.primary:hover {
    background: #F2A93B;
}

.action-btn.secondary:hover {
    background: #E87A2F;
    color: #F2F2F2;
}

.hero-right {
    background: #0F2A3A;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
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
    gap: 4px;
    align-items: end;
    height: 200px;
}

.bar {
    width: 6px;
    background: #F2A93B;
    animation: frequency 2s infinite ease-in-out;
}

@keyframes frequency {

    0%,
    100% {
        height: 20px;
    }

    50% {
        height: 180px;
    }
}

/* Sections */
section {
    width: 100%;
  max-width: 100vw;
  padding: 2rem 1rem;
  box-sizing: border-box;
  overflow-x: hidden;
}

.section-header {
  display: flex;
  align-items: center;
  margin-bottom: 2rem;
  gap: 1rem;
  flex-wrap: wrap;
}

.section-number {
  font-size: 3rem;
  font-weight: 900;
  color: #2B2E34;
  line-height: 1;
  flex-shrink: 0;
}

.section-title {
  font-size: 1.5rem;
  font-weight: 900;
  letter-spacing: 0.1em;
  color: #F2F2F2;
  flex-shrink: 0;
.music-section {
    background: #1C1E22;
}

.album-showcase {
    max-width: 800px;
    margin: 0 auto;
}

/* About Section */
.about-section {
    background: #0E0E0F;
}

.about-grid {
    display: grid;
    grid-template-columns: 1fr;
    gap: 3rem;
    align-items: start;
}

.manifesto-text p {
    font-size: 1.1rem;
    line-height: 1.6;
    margin-bottom: 1.5rem;
    color: #B5B8BE;
}

.about-stats {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    gap: 2rem;
}

.stat-block {
    text-align: center;
}

.stat-number {
    font-size: 4rem;
    font-weight: 900;
    color: #F2A93B;
    line-height: 1;
}

.stat-label {
    font-size: 0.8rem;
    letter-spacing: 0.3em;
    color: #B5B8BE;
    margin-top: 0.5rem;
}

/* Contact Section */
.contact-section {
    background: #0F2A3A;
}

.contact-links {
    display: flex;
    flex-direction: column;
    gap: 1px;
    max-width: 100%;
}

.contact-link {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 2rem 1rem;
    background: #1C1E22;
    color: #F2F2F2;
    text-decoration: none;
    transition: all 0.3s;
    border: 1px solid #2B2E34;
    box-sizing: border-box;
    width: 100%;
}

.contact-link:hover {
    background: #E87A2F;
    color: #F2F2F2;
    transform: scale(1.02);
}

.link-label {
    font-size: 1.2rem;
    font-weight: 700;
    letter-spacing: 0.1em;
}

.link-arrow {
    font-size: 2rem;
    font-weight: 300;
}

/* Band Section */
.band-section {
    background: #1C1E22;
}

.carousel-container {
    position: relative;
    width: 100%;
    max-width: 100vw;
    margin: 0;
    box-sizing: border-box;
    padding: 0 1rem;
}

.carousel-wrapper {
    overflow: hidden;
    border: 1px solid #2B2E34;
    width: 100%;
    max-width: 100%;
    box-sizing: border-box;
}

.carousel-track {
    display: flex;
    transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
    width: 400%;
    /* 4 slides × 100% = 400% */
}

.member-slide {
    width: 25%;
    /* 100% / 4 slides = 25% cada */
    flex-shrink: 0;
    flex-grow: 0;
}

.member-card-large {
    display: grid;
    grid-template-columns: 300px 1fr;
    background: #0F2A3A;
    min-height: 400px;
    width: 100%;
    box-sizing: border-box;
}

.member-photo-large {
    background: #0E0E0F;
    display: flex;
    align-items: center;
    justify-content: center;
    border-right: 1px solid #2B2E34;
}

.photo-placeholder-large {
    width: 100%;
    height: 100%;
    background: #1C1E22;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #B5B8BE;
    font-weight: 700;
    font-size: 1rem;
    letter-spacing: 0.1em;
}

.member-info-large {
    padding: 3rem;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    justify-content: center;
}

.member-name-large {
    font-size: 2rem;
    font-weight: 900;
    letter-spacing: 0.1em;
    color: #F2F2F2;
}

.member-instrument-large {
    font-size: 1.2rem;
    font-weight: 700;
    letter-spacing: 0.2em;
    color: #E87A2F;
    text-transform: uppercase;
}

.member-description-large {
    font-size: 1rem;
    line-height: 1.7;
    color: #B5B8BE;
    font-weight: 400;
}

.member-social {
    display: flex;
    gap: 1rem;
    margin-top: 1.5rem;
}

.social-btn {
    width: 40px;
    height: 40px;
    background: #222222;
    border: 1px solid #333333;
    color: #ffffff;
    text-decoration: none;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all 0.3s;
    font-weight: 700;
    font-size: 0.8rem;
    letter-spacing: 0.1em;
}

.social-btn.instagram:hover {
    background: #E4405F;
    border-color: #E4405F;
    color: #ffffff;
    transform: scale(1.1);
}

.social-btn.whatsapp:hover {
    background: #25D366;
    border-color: #25D366;
    color: #ffffff;
    transform: scale(1.1);
}

.social-btn:hover {
    border-color: #00ff41;
}

.member-social {
    display: flex;
    gap: 1rem;
    margin-top: 1.5rem;
}

.social-btn {
    width: 40px;
    height: 40px;
    background: #222222;
    border: 1px solid #333333;
    color: #ffffff;
    text-decoration: none;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all 0.3s;
    font-weight: 700;
    font-size: 0.8rem;
    letter-spacing: 0.1em;
}

.social-btn.instagram:hover {
    background: #E4405F;
    border-color: #E4405F;
    color: #ffffff;
    transform: scale(1.1);
}

.social-btn.whatsapp:hover {
    background: #25D366;
    border-color: #25D366;
    color: #ffffff;
    transform: scale(1.1);
}

.social-btn:hover {
    border-color: #00ff41;
}

.carousel-controls {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 2rem 0;
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
    transition: all 0.4s ease;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: 700;
    font-size: 0.9rem;
    color: #B5B8BE;
    border: 1px solid #2B2E34;
}

.indicator.active {
    background: #E87A2F;
    color: #F2F2F2;
    border-color: #E87A2F;
    transform: scale(1.1);
}

.indicator:hover:not(.active) {
    background: #1F5F6B;
    color: #F2F2F2;
    border-color: #1F5F6B;
}

.carousel-buttons {
    display: flex;
    gap: 1rem;
}

.carousel-btn {
    width: 50px;
    height: 50px;
    background: #1C1E22;
    border: 1px solid #2B2E34;
    color: #F2F2F2;
    cursor: pointer;
    font-size: 1.5rem;
    font-weight: 300;
    transition: all 0.3s;
    display: flex;
    align-items: center;
    justify-content: center;
}

.carousel-btn:hover {
    background: #E87A2F;
    color: #F2F2F2;
    border-color: #E87A2F;
}

.members-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
    gap: 2px;
}

.member-card {
    display: grid;
    grid-template-columns: 200px 1fr;
    background: #111111;
    border: 1px solid #333333;
    transition: all 0.3s;
}

.member-card:hover {
    border-color: #00ff41;
    transform: scale(1.02);
}

.member-photo {
    background: #000000;
    display: flex;
    align-items: center;
    justify-content: center;
    border-right: 1px solid #333333;
}

.photo-placeholder {
    width: 100%;
    height: 200px;
    background: #222222;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #666666;
    font-weight: 700;
    font-size: 0.9rem;
    letter-spacing: 0.1em;
}

.member-info {
    padding: 2rem;
    display: flex;
    flex-direction: column;
    gap: 1rem;
}

.member-name {
    font-size: 1.4rem;
    font-weight: 900;
    letter-spacing: 0.1em;
    color: #ffffff;
}

.member-instrument {
    font-size: 1rem;
    font-weight: 700;
    letter-spacing: 0.2em;
    color: #00ff41;
    text-transform: uppercase;
}

.member-description {
    font-size: 0.9rem;
    line-height: 1.6;
    color: #cccccc;
    font-weight: 400;
}

/* Responsive */
@media (min-width: 768px) {
    .header-content {
        grid-template-columns: 1fr auto 1fr;
    }

    .logo {
        font-size: 1.5rem;
    }

    .nav-menu {
        position: static;
        width: auto;
        height: auto;
        background: none;
        flex-direction: row;
        justify-self: center;
        transform: none;
        gap: 3rem;
    }

    .nav-menu a {
        font-size: 0.9rem;
    }

    .mobile-menu-btn {
        display: none;
    }

    .hero-grid {
        grid-template-columns: 1fr 1fr;
        height: 80vh;
    }

    .hero-left {
        padding: 0 4rem;
        order: 1;
    }

    .hero-right {
        order: 2;
    }

    .hero-title {
        font-size: 5rem;
    }

    .hero-subtitle {
        font-size: 1.2rem;
        letter-spacing: 0.2em;
        margin-bottom: 3rem;
    }

    .hero-actions {
        flex-direction: row;
    }

    .action-btn {
        margin-bottom: 0;
    }

    section {
        padding: 6rem 4rem;
    }

    .section-header {
        margin-bottom: 4rem;
        gap: 2rem;
    }

    .section-number {
        font-size: 6rem;
    }

    .section-title {
        font-size: 3rem;
    }

    .about-grid {
        grid-template-columns: 2fr 1fr;
        gap: 4rem;
    }

    .manifesto-text p {
        font-size: 1.3rem;
        margin-bottom: 2rem;
    }

    .about-stats {
        flex-direction: column;
        gap: 3rem;
    }
}

@media (min-width: 1024px) {
    .hero-grid {
        grid-template-columns: 1fr 1fr;
        height: auto;
    }

    .hero-left {
        padding: 4rem 2rem;
    }

    .hero-title {
        font-size: 3rem;
    }

    .about-grid {
        grid-template-columns: 1fr;
        gap: 2rem;
    }

    .members-grid {
        grid-template-columns: 1fr;
    }

    .member-card {
        grid-template-columns: 150px 1fr;
    }

    .member-card-large {
        grid-template-columns: 250px 1fr;
        width: 100%;
    }

    .contact-links {
        grid-template-columns: 1fr;
    }
}

@media (max-width: 768px) {
    section {
        padding: 4rem 2rem;
    }

    .section-number {
        font-size: 3rem;
    }

    .section-title {
        font-size: 2rem;
    }

    .hero-actions {
        flex-direction: column;
    }

    .action-btn {
        width: 100%;
    }

    .member-card {
        grid-template-columns: 1fr;
    }

    .member-card-large {
        grid-template-columns: 1fr;
        min-height: auto;
        width: 100%;
    }

    .carousel-track {
        width: 400%;
    }

    .member-slide {
        width: 25%;
    }

    .member-photo {
        border-right: none;
        border-bottom: 1px solid #333333;
    }

    .member-photo-large {
        border-right: none;
        border-bottom: 1px solid #2B2E34;
        min-height: 200px;
    }

    .photo-placeholder {
        height: 150px;
    }

    .member-info-large {
        padding: 2rem;
    }

    .member-name-large {
        font-size: 1.5rem;
    }

    .carousel-controls {
        flex-direction: column;
        gap: 2rem;
    }

    .carousel-buttons {
        order: -1;
    }

    @media (max-width: 767px) {
        .header-content {
            padding: 1rem;
        }

        section {
            padding: 3rem 1rem;
        }

        .section-number {
            font-size: 3rem;
        }

        .section-title {
            font-size: 1.5rem;
        }

        .hero-label {
            font-size: 0.6rem;
        }

        .hero-title {
            font-size: 2rem;
        }

        .hero-subtitle {
            font-size: 0.9rem;
        }

        .action-btn {
            width: 100%;
            padding: 1.2rem;
            font-size: 0.8rem;
        }

        .member-card-large {
            grid-template-columns: 1fr;
            min-height: auto;
            width: 100%;
        }

        .carousel-track {
            width: 400%;
        }

        .member-slide {
            width: 25%;
        }

        .member-photo-large {
            border-right: none;
            border-bottom: 1px solid #2B2E34;
            min-height: 200px;
        }

        .member-info-large {
            padding: 2rem;
        }

        .member-name-large {
            font-size: 1.5rem;
        }

        .member-instrument-large {
            font-size: 1rem;
        }

        .member-description-large {
            font-size: 0.9rem;
        }

        .carousel-controls {
            flex-direction: column;
            gap: 2rem;
        }

        .carousel-buttons {
            order: -1;
        }

        .indicator {
            width: 40px;
            height: 40px;
            font-size: 0.8rem;
        }

        .contact-links {
            grid-template-columns: 1fr;
        }

        .contact-link {
            padding: 2rem;
        }

        .link-label {
            font-size: 1rem;
        }

        .frequency-bars {
            height: 150px;
        }

        .bar {
            width: 4px;
        }

        @keyframes frequency {

            0%,
            100% {
                height: 15px;
            }

            50% {
                height: 120px;
            }
        }
    }
</style>