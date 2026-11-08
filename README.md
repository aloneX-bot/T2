 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#10110d">
<title>BOOK STUDIO | Create Your Next Ebook</title>
<meta name="description" content="Turn your ideas into beautifully designed ebooks with an AI-powered ebook creation platform.">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700;800&family=Manrope:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>

/* =========================================
   01. GLOBAL DESIGN SYSTEM
========================================= */

:root {
  --bg: #10110d;
  --bg2: #14160f;
  --panel: #1b1e16;
  --panel2: #22251c;
  --panel3: #292d21;
  --lime: #d7ff43;
  --lime2: #c4ed37;
  --white: #f7f8f1;
  --muted: #a1a695;
  --muted2: #777e6d;
  --line: rgba(255,255,255,.1);
  --radius: 18px;
  --max: 1160px;
  --font: "DM Sans", sans-serif;
  --heading: "Manrope", sans-serif;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  scroll-behavior: smooth;
  scroll-padding-top: 90px;
}

body {
  background: var(--bg);
  color: var(--white);
  font-family: var(--font);
  line-height: 1.6;
  overflow-x: hidden;
}

body.menu-open {
  overflow: hidden;
}

button,
input,
textarea,
select {
  font: inherit;
}

button,
a {
  -webkit-tap-highlight-color: transparent;
}

button {
  cursor: pointer;
  border: none;
}

a {
  color: inherit;
  text-decoration: none;
}

img {
  display: block;
  max-width: 100%;
}

.container {
  width: min(var(--max), calc(100% - 48px));
  margin-inline: auto;
}

.section {
  padding: 105px 0;
  position: relative;
}

.section-sm {
  padding: 65px 0;
}

.text-center {
  text-align: center;
}

.section-label {
  color: var(--lime);
  text-transform: uppercase;
  font-size: 11px;
  font-weight: 800;
  letter-spacing: 2px;
  margin-bottom: 17px;
}

.section-title {
  font-family: var(--heading);
  font-size: clamp(34px, 5vw, 57px);
  font-weight: 800;
  line-height: 1.12;
  letter-spacing: -2.2px;
}

.section-description {
  color: var(--muted);
  max-width: 650px;
  margin-top: 20px;
  font-size: 15px;
  line-height: 1.85;
}

.text-center .section-description {
  margin-inline: auto;
}

.highlight {
  color: var(--lime);
}

.muted {
  color: var(--muted);
}

.pill {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  border: 1px solid rgba(215,255,67,.28);
  background: rgba(215,255,67,.07);
  color: var(--lime);
  padding: 8px 14px;
  border-radius: 100px;
  font-size: 11px;
  font-weight: 800;
}

.dot {
  width: 7px;
  height: 7px;
  background: var(--lime);
  border-radius: 50%;
  display: inline-block;
}

/* =========================================
   02. BUTTONS
========================================= */

.btn {
  display: inline-flex;
  justify-content: center;
  align-items: center;
  gap: 9px;
  padding: 14px 22px;
  border-radius: 10px;
  font-size: 13px;
  font-weight: 800;
  transition: .25s ease;
  cursor: pointer;
}

.btn-primary {
  background: var(--lime);
  color: #17190f;
}

.btn-primary:hover {
  background: #e8ff9b;
  transform: translateY(-2px);
  box-shadow: 0 8px 30px rgba(215,255,67,.15);
}

.btn-outline {
  background: transparent;
  border: 1px solid var(--line);
  color: var(--white);
}

.btn-outline:hover {
  border-color: var(--lime);
  color: var(--lime);
}

.btn-dark {
  background: #202319;
  color: var(--white);
  border: 1px solid var(--line);
}

.btn-dark:hover {
  border-color: var(--lime);
}

.btn-full {
  width: 100%;
}

/* =========================================
   03. ANNOUNCEMENT BAR
========================================= */

.announcement {
  background: var(--lime);
  color: #17190f;
  text-align: center;
  padding: 9px 14px;
  font-size: 11px;
  font-weight: 800;
}

.announcement a {
  text-decoration: underline;
  margin-left: 5px;
}

/* =========================================
   04. NAVIGATION
========================================= */

.navbar {
  position: sticky;
  top: 0;
  z-index: 1000;
  background: rgba(16,17,13,.9);
  backdrop-filter: blur(18px);
  border-bottom: 1px solid var(--line);
}

.nav-inner {
  height: 76px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  font-family: var(--heading);
  font-size: 20px;
  font-weight: 800;
  letter-spacing: -.8px;
}

.logo-mark {
  width: 34px;
  height: 34px;
  background: var(--lime);
  color: #15170f;
  display: grid;
  place-items: center;
  border-radius: 10px;
  font-size: 18px;
  font-weight: 900;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 28px;
}

.nav-links a {
  color: #c0c4b5;
  font-size: 12px;
  font-weight: 600;
  transition: .2s;
}

.nav-links a:hover {
  color: var(--lime);
}

.nav-actions {
  display: flex;
  align-items: center;
  gap: 12px;
}

.nav-actions .btn {
  padding: 11px 17px;
  font-size: 11px;
}

.menu-toggle {
  display: none;
  width: 42px;
  height: 42px;
  border: 1px solid var(--line);
  border-radius: 10px;
  color: white;
  background: var(--panel);
  font-size: 22px;
}

/* =========================================
   05. HERO SECTION
========================================= */

.hero {
  padding: 100px 0 85px;
  position: relative;
  overflow: hidden;
}

.hero::before {
  content: "";
  position: absolute;
  width: 650px;
  height: 650px;
  background: rgba(174,218,41,.08);
  filter: blur(110px);
  border-radius: 50%;
  top: -300px;
  left: 50%;
  transform: translateX(-50%);
}

.hero-content {
  max-width: 900px;
  margin: auto;
  position: relative;
  text-align: center;
}

.hero h1 {
  font-family: var(--heading);
  font-size: clamp(44px, 7vw, 78px);
  font-weight: 800;
  letter-spacing: -4px;
  line-height: 1.06;
  margin: 25px 0 22px;
}

.hero-subtitle {
  max-width: 650px;
  margin: auto;
  color: #b5b9ab;
  font-size: 16px;
  line-height: 1.8;
}

.hero-actions {
  display: flex;
  justify-content: center;
  gap: 13px;
  flex-wrap: wrap;
  margin-top: 30px;
}

.hero-note {
  color: #858b7c;
  font-size: 11px;
  margin-top: 15px;
}

/* HERO PROMPT BOX */

.prompt-box {
  max-width: 790px;
  margin: 48px auto 0;
  padding: 20px;
  text-align: left;
  background: linear-gradient(145deg,#25291d,#191c15);
  border: 1px solid rgba(215,255,67,.23);
  border-radius: 20px;
  box-shadow: 0 25px 80px rgba(0,0,0,.3);
  position: relative;
}

.prompt-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 14px;
}

.prompt-heading {
  font-size: 12px;
  font-weight: 800;
}

.prompt-status {
  color: var(--lime);
  font-size: 10px;
  font-weight: 700;
}

.prompt-box textarea {
  width: 100%;
  min-height: 95px;
  resize: vertical;
  outline: none;
  border: none;
  background: transparent;
  color: white;
  font-size: 14px;
  line-height: 1.7;
}

.prompt-box textarea::placeholder {
  color: #858b7a;
}

.prompt-bottom {
  border-top: 1px solid var(--line);
  padding-top: 15px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 15px;
}

.prompt-options {
  display: flex;
  align-items: center;
  gap: 9px;
  flex-wrap: wrap;
}

.prompt-options select {
  background: #303426;
  color: #e5e9d9;
  border: 1px solid var(--line);
  border-radius: 8px;
  padding: 9px 11px;
  font-size: 11px;
  outline: none;
}

.prompt-submit {
  white-space: nowrap;
}

.prompt-feedback {
  display: none;
  margin-top: 14px;
  color: var(--lime);
  font-size: 12px;
  line-height: 1.6;
}

/* =========================================
   06. TRUST STRIP
========================================= */

.trust-strip {
  border-top: 1px solid var(--line);
  border-bottom: 1px solid var(--line);
  background: #13150f;
  padding: 30px 0;
}

.trust-title {
  text-align: center;
  color: var(--muted2);
  font-size: 10px;
  font-weight: 800;
  letter-spacing: 1.8px;
  text-transform: uppercase;
  margin-bottom: 23px;
}

.platforms {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 50px;
  flex-wrap: wrap;
}

.platform {
  color: #aeb3a4;
  font-family: var(--heading);
  font-weight: 800;
  font-size: 17px;
  opacity: .8;
}

.platform span {
  color: var(--lime);
}

/* =========================================
   07. SHOWCASE
========================================= */

.showcase {
  background: var(--bg2);
  overflow: hidden;
}

.showcase-heading {
  display: flex;
  align-items: end;
  justify-content: space-between;
  gap: 30px;
  margin-bottom: 45px;
}

.showcase-heading .section-description {
  max-width: 480px;
}

.book-showcase {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  gap: 22px;
}

.book-card {
  background: var(--panel);
  border: 1px solid var(--line);
  border-radius: 17px;
  padding: 15px;
  transition: .3s ease;
}

.book-card:hover {
  transform: translateY(-7px);
  border-color: rgba(215,255,67,.35);
}

.book-cover {
  aspect-ratio: 4 / 4.8;
  border-radius: 11px;
  overflow: hidden;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 25px;
}

.cover-one {
  background:
    radial-gradient(circle at 70% 20%,#e4d29a,transparent 35%),
    linear-gradient(145deg,#254d37,#102a20);
}

.cover-two {
  background:
    radial-gradient(circle at 50% 30%,#d8a76b,transparent 35%),
    linear-gradient(145deg,#412c26,#1c1918);
}

.cover-three {
  background:
    radial-gradient(circle at 50% 20%,#b6cfba,transparent 35%),
    linear-gradient(145deg,#233e51,#111f2b);
}

.cover-four {
  background:
    radial-gradient(circle at 70% 20%,#e8c9b0,transparent 35%),
    linear-gradient(145deg,#623f43,#241b25);
}

.cover-five {
  background:
    radial-gradient(circle at 40% 25%,#d9db93,transparent 35%),
    linear-gradient(145deg,#4d5130,#202417);
}

.cover-six {
  background:
    radial-gradient(circle at 60% 30%,#e6c18d,transparent 35%),
    linear-gradient(145deg,#4c3421,#211b16);
}

.cover-content {
  max-width: 240px;
  position: relative;
  z-index: 1;
}

.cover-kicker {
  font-size: 9px;
  letter-spacing: 2px;
  text-transform: uppercase;
  margin-bottom: 18px;
  opacity: .8;
}

.cover-content h3 {
  font-family: var(--heading);
  font-size: clamp(20px,2.4vw,30px);
  line-height: 1.15;
  font-weight: 800;
}

.cover-content p {
  font-size: 10px;
  margin-top: 17px;
  letter-spacing: 1px;
}

.book-info {
  padding: 16px 4px 5px;
}

.book-info h3 {
  font-size: 14px;
  font-weight: 800;
}

.book-info p {
  font-size: 11px;
  color: var(--muted);
  margin-top: 5px;
}

.book-tag {
  display: inline-block;
  font-size: 9px;
  color: var(--lime);
  background: rgba(215,255,67,.08);
  padding: 5px 9px;
  border-radius: 20px;
  margin-top: 12px;
}

/* =========================================
   08. VALUE PROPOSITION
========================================= */

.value-grid {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  gap: 18px;
  margin-top: 55px;
}

.value-card {
  background: var(--panel);
  border: 1px solid var(--line);
  border-radius: var(--radius);
  padding: 28px;
}

.value-icon {
  width: 47px;
  height: 47px;
  display: grid;
  place-items: center;
  background: rgba(215,255,67,.1);
  color: var(--lime);
  border-radius: 13px;
  font-size: 22px;
  margin-bottom: 24px;
}

.value-card h3 {
  font-family: var(--heading);
  font-size: 18px;
  margin-bottom: 11px;
}

.value-card p {
  color: var(--muted);
  font-size: 13px;
  line-height: 1.8;
}

/* =========================================
   09. BIG FEATURE SECTION
========================================= */

.feature-section {
  background: var(--bg2);
}

.feature-layout {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 70px;
  align-items: center;
}

.feature-visual {
  min-height: 430px;
  border-radius: 22px;
  background:
    radial-gradient(circle at 20% 20%,rgba(215,255,67,.14),transparent 35%),
    linear-gradient(145deg,#272c1e,#151811);
  border: 1px solid var(--line);
  padding: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

.editor-preview {
  width: 100%;
  max-width: 420px;
  background: #f1eee5;
  color: #20241c;
  border-radius: 10px;
  padding: 25px;
  box-shadow: 0 25px 60px rgba(0,0,0,.35);
  transform: rotate(-2deg);
}

.editor-top {
  display: flex;
  justify-content: space-between;
  color: #5b6252;
  font-size: 9px;
  border-bottom: 1px solid #d7d6cd;
  padding-bottom: 13px;
}

.editor-preview h3 {
  font-family: Georgia,serif;
  font-size: 27px;
  line-height: 1.2;
  margin: 28px 0 12px;
}

.editor-preview p {
  font-family: Georgia,serif;
  color: #64665c;
  font-size: 11px;
  line-height: 1.8;
}

.editor-line {
  height: 6px;
  background: #d7d8cd;
  border-radius: 10px;
  margin-top: 12px;
}

.editor-line.short {
  width: 65%;
}

.feature-copy h2 {
  font-family: var(--heading);
  font-size: clamp(32px,4vw,48px);
  line-height: 1.15;
  letter-spacing: -1.8px;
}

.feature-copy > p {
  color: var(--muted);
  margin-top: 20px;
  font-size: 14px;
  line-height: 1.9;
}

.feature-list {
  list-style: none;
  margin-top: 27px;
  display: grid;
  gap: 15px;
}

.feature-list li {
  display: flex;
  gap: 12px;
  color: #d4d8ca;
  font-size: 13px;
  align-items: flex-start;
}

.check {
  width: 20px;
  height: 20px;
  flex-shrink: 0;
  border-radius: 50%;
  background: rgba(215,255,67,.12);
  color: var(--lime);
  display: grid;
  place-items: center;
  font-size: 11px;
}

/* =========================================
   10. THREE STEP PROCESS
========================================= */

.steps-grid {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  gap: 20px;
  margin-top: 55px;
}

.step-card {
  position: relative;
  padding: 28px;
  border: 1px solid var(--line);
  border-radius: 18px;
  background: linear-gradient(145deg,#1e2118,#171912);
}

.step-number {
  font-family: var(--heading);
  color: rgba(215,255,67,.25);
  font-size: 44px;
  font-weight: 800;
  line-height: 1;
  margin-bottom: 30px;
}

.step-card h3 {
  font-family: var(--heading);
  font-size: 18px;
  margin-bottom: 12px;
}

.step-card p {
  color: var(--muted);
  font-size: 13px;
  line-height: 1.8;
}

/* =========================================
   11. BOOK TYPES
========================================= */

.types-section {
  background: var(--bg2);
}

.types-grid {
  display: grid;
  grid-template-columns: repeat(4,1fr);
  gap: 15px;
  margin-top: 45px;
}

.type-card {
  padding: 24px 20px;
  background: var(--panel);
  border: 1px solid var(--line);
  border-radius: 15px;
  transition: .25s;
}

.type-card:hover {
  border-color: var(--lime);
  transform: translateY(-4px);
}

.type-symbol {
  color: var(--lime);
  font-size: 24px;
  margin-bottom: 16px;
}

.type-card h3 {
  font-size: 14px;
  margin-bottom: 8px;
}

.type-card p {
  color: var(--muted);
  font-size: 11px;
  line-height: 1.7;
}

/* =========================================
   12. CUSTOMIZATION SECTION
========================================= */

.custom-layout {
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  gap: 65px;
}

.custom-preview {
  background: linear-gradient(145deg,#252a1d,#171a13);
  border: 1px solid var(--line);
  border-radius: 20px;
  padding: 28px;
}

.preview-window {
  background: #f0eee5;
  color: #24271e;
  border-radius: 12px;
  padding: 24px;
}

.preview-window small {
  color: #777d6d;
  font-size: 9px;
}

.preview-window h3 {
  font-family: Georgia,serif;
  font-size: 28px;
  line-height: 1.2;
  margin: 18px 0 12px;
}

.preview-window p {
  color: #686c61;
  font-family: Georgia,serif;
  font-size: 11px;
  line-height: 1.8;
}

.preview-columns {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 12px;
  margin-top: 20px;
}

.preview-block {
  background: #dfe1d5;
  height: 85px;
  border-radius: 6px;
}

.custom-points {
  display: grid;
  gap: 19px;
  margin-top: 28px;
}

.custom-point {
  display: flex;
  gap: 15px;
  align-items: flex-start;
}

.custom-point-icon {
  flex-shrink: 0;
  width: 38px;
  height: 38px;
  border-radius: 11px;
  background: rgba(215,255,67,.1);
  color: var(--lime);
  display: grid;
  place-items: center;
}

.custom-point h3 {
  font-size: 14px;
  margin-bottom: 5px;
}

.custom-point p {
  color: var(--muted);
  font-size: 12px;
  line-height: 1.7;
}

/* =========================================
   13. EXPORT FORMATS
========================================= */

.export-section {
  background: var(--bg2);
}

.export-grid {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  gap: 18px;
  margin-top: 45px;
}

.export-card {
  background: var(--panel);
  border: 1px solid var(--line);
  padding: 28px;
  border-radius: 17px;
  text-align: center;
}

.export-file {
  width: 58px;
  height: 66px;
  margin: 0 auto 20px;
  border-radius: 9px;
  display: grid;
  place-items: center;
  font-family: var(--heading);
  font-size: 14px;
  font-weight: 800;
  background: rgba(215,255,67,.12);
  color: var(--lime);
  border: 1px solid rgba(215,255,67,.2);
}

.export-card h3 {
  font-size: 17px;
  margin-bottom: 8px;
}

.export-card p {
  color: var(--muted);
  font-size: 12px;
  line-height: 1.8;
}

/* =========================================
   14. AUDIENCE SECTION
========================================= */

.audience-grid {
  display: grid;
  grid-template-columns: repeat(4,1fr);
  gap: 14px;
  margin-top: 45px;
}

.audience-card {
  border: 1px solid var(--line);
  background: var(--panel);
  padding: 22px;
  border-radius: 14px;
}

.audience-card h3 {
  font-size: 13px;
  margin-bottom: 8px;
}

.audience-card p {
  font-size: 11px;
  color: var(--muted);
  line-height: 1.7;
}

/* =========================================
   15. PRICING
========================================= */

.pricing-section {
  background: var(--bg2);
}

.pricing-grid {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  gap: 19px;
  margin-top: 50px;
  align-items: stretch;
}

.price-card {
  padding: 29px;
  border-radius: 19px;
  background: var(--panel);
  border: 1px solid var(--line);
  position: relative;
}

.price-card.featured {
  border: 1px solid var(--lime);
  background: linear-gradient(160deg,#292e1d,#1b1e15);
  box-shadow: 0 15px 55px rgba(215,255,67,.07);
}

.popular-tag {
  position: absolute;
  top: -13px;
  right: 22px;
  padding: 6px 12px;
  background: var(--lime);
  color: #17190f;
  border-radius: 20px;
  font-size: 9px;
  font-weight: 900;
  text-transform: uppercase;
}

.price-name {
  font-size: 16px;
  font-weight: 800;
}

.price-description {
  color: var(--muted);
  font-size: 11px;
  margin-top: 7px;
  min-height: 38px;
}

.price-amount {
  font-family: var(--heading);
  font-size: 43px;
  font-weight: 800;
  letter-spacing: -2px;
  margin-top: 22px;
}

.price-amount span {
  font-size: 13px;
  color: var(--muted);
  letter-spacing: 0;
  font-weight: 500;
}

.price-credit {
  font-size: 11px;
  color: var(--lime);
  margin-top: 5px;
}

.price-divider {
  height: 1px;
  background: var(--line);
  margin: 23px 0;
}

.price-features {
  list-style: none;
  display: grid;
  gap: 13px;
  margin-bottom: 26px;
}

.price-features li {
  display: flex;
  gap: 10px;
  color: #c5caba;
  font-size: 11px;
}

.price-features li::before {
  content: "✓";
  color: var(--lime);
  font-weight: 900;
}

.pricing-note {
  text-align: center;
  color: var(--muted2);
  font-size: 10px;
  margin-top: 23px;
}

/* =========================================
   16. FAQ
========================================= */

.faq-section {
  background: var(--bg);
}

.faq-list {
  max-width: 820px;
  margin: 48px auto 0;
  display: grid;
  gap: 12px;
}

.faq-item {
  background: var(--panel);
  border: 1px solid var(--line);
  border-radius: 13px;
  overflow: hidden;
}

.faq-question {
  width: 100%;
  background: transparent;
  color: var(--white);
  text-align: left;
  padding: 21px 22px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 15px;
  font-weight: 700;
  font-size: 13px;
}

.faq-symbol {
  color: var(--lime);
  font-size: 21px;
  transition: .2s;
}

.faq-answer {
  display: none;
  padding: 0 22px 21px;
  color: var(--muted);
  font-size: 12px;
  line-height: 1.8;
}

.faq-item.active .faq-answer {
  display: block;
}

.faq-item.active .faq-symbol {
  transform: rotate(45deg);
}

/* =========================================
   17. FINAL CTA
========================================= */

.final-cta {
  padding: 95px 0;
  background:
    radial-gradient(circle at 50% 120%,rgba(215,255,67,.15),transparent 50%),
    #171a12;
  border-top: 1px solid var(--line);
  border-bottom: 1px solid var(--line);
}

.cta-inner {
  max-width: 760px;
  margin: auto;
  text-align: center;
}

.cta-inner h2 {
  font-family: var(--heading);
  font-size: clamp(36px,5vw,58px);
  line-height: 1.1;
  letter-spacing: -2px;
}

.cta-inner p {
  color: var(--muted);
  margin: 20px auto 27px;
  max-width: 540px;
  font-size: 14px;
  line-height: 1.8;
}

/* =========================================
   18. FOOTER
========================================= */

.footer {
  padding: 65px 0 25px;
  background: #0c0d09;
}

.footer-grid {
  display: grid;
  grid-template-columns: 1.6fr 1fr 1fr 1fr;
  gap: 40px;
  padding-bottom: 45px;
}

.footer-about p {
  color: var(--muted);
  font-size: 12px;
  max-width: 280px;
  margin-top: 17px;
  line-height: 1.8;
}

.footer-column h3 {
  font-size: 12px;
  margin-bottom: 19px;
}

.footer-column a {
  display: block;
  color: var(--muted);
  font-size: 11px;
  margin-bottom: 12px;
  transition: .2s;
}

.footer-column a:hover {
  color: var(--lime);
}

.footer-bottom {
  border-top: 1px solid var(--line);
  padding-top: 22px;
  display: flex;
  justify-content: space-between;
  gap: 15px;
  color: var(--muted2);
  font-size: 10px;
}

/* =========================================
   19. NOTIFICATION
========================================= */

.toast {
  position: fixed;
  bottom: 25px;
  left: 50%;
  transform: translate(-50%,20px);
  opacity: 0;
  pointer-events: none;
  background: var(--lime);
  color: #17190f;
  padding: 13px 19px;
  border-radius: 10px;
  font-size: 12px;
  font-weight: 800;
  z-index: 2000;
  transition: .3s;
  box-shadow: 0 10px 35px rgba(0,0,0,.35);
}

.toast.show {
  opacity: 1;
  transform: translate(-50%,0);
}

/* =========================================
   20. SCROLL ANIMATIONS
========================================= */

.reveal {
  opacity: 0;
  transform: translateY(24px);
  transition: opacity .7s ease, transform .7s ease;
}

.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}

/* =========================================
   21. RESPONSIVE DESIGN
========================================= */

@media(max-width:1000px) {
  .nav-links {
    gap: 17px;
  }

  .nav-links a {
    font-size: 11px;
  }

  .feature-layout,
  .custom-layout {
    gap: 35px;
  }

  .audience-grid {
    grid-template-columns: repeat(2,1fr);
  }
}

@media(max-width:800px) {
  .section {
    padding: 78px 0;
  }

  .menu-toggle {
    display: grid;
    place-items: center;
  }

  .nav-links {
    position: fixed;
    top: 76px;
    left: 0;
    right: 0;
    height: calc(100dvh - 76px);
    background: #10110d;
    display: flex;
    flex-direction: column;
    align-items: stretch;
    gap: 0;
    padding: 20px 25px;
    transform: translateX(100%);
    transition: .3s;
    border-top: 1px solid var(--line);
  }

  .nav-links.open {
    transform: translateX(0);
  }

  .nav-links a {
    padding: 18px 5px;
    border-bottom: 1px solid var(--line);
    font-size: 15px;
  }

  .nav-actions .btn-outline {
    display: none;
  }

  .hero {
    padding-top: 75px;
  }

  .hero h1 {
    letter-spacing: -2.5px;
  }

  .showcase-heading {
    display: block;
  }

  .showcase-heading .section-description {
    margin-bottom: 20px;
  }

  .book-showcase {
    grid-template-columns: repeat(2,1fr);
  }

  .feature-layout,
  .custom-layout {
    grid-template-columns: 1fr;
  }

  .feature-visual {
    min-height: 340px;
  }

  .steps-grid {
    grid-template-columns: 1fr;
  }

  .types-grid {
    grid-template-columns: repeat(2,1fr);
  }

  .pricing-grid {
    grid-template-columns: 1fr;
    max-width: 500px;
    margin-inline: auto;
    margin-top: 45px;
  }

  .export-grid {
    grid-template-columns: 1fr;
  }

  .value-grid {
    grid-template-columns: 1fr 1fr;
  }

  .footer-grid {
    grid-template-columns: 1fr 1fr;
  }
}

@media(max-width:540px) {
  .container {
    width: min(var(--max), calc(100% - 32px));
  }

  .announcement {
    font-size: 9px;
  }

  .nav-inner {
    height: 68px;
  }

  .nav-links {
    top: 68px;
    height: calc(100dvh - 68px);
  }

  .logo {
    font-size: 17px;
  }

  .logo-mark {
    width: 30px;
    height: 30px;
  }

  .nav-actions .btn {
    display: none;
  }

  .hero {
    padding: 65px 0 65px;
  }

  .hero h1 {
    font-size: 44px;
    letter-spacing: -2.5px;
  }

  .hero-subtitle {
    font-size: 13px;
  }

  .hero-actions {
    flex-direction: column;
  }

  .hero-actions .btn {
    width: 100%;
  }

  .prompt-box {
    padding: 15px;
    margin-top: 35px;
  }

  .prompt-bottom {
    align-items: stretch;
    flex-direction: column;
  }

  .prompt-submit {
    width: 100%;
  }

  .prompt-options select {
    flex: 1;
  }

  .platforms {
    gap: 22px;
  }

  .platform {
    font-size: 14px;
  }

  .book-showcase {
    gap: 12px;
  }

  .book-card {
    padding: 9px;
  }

  .book-info h3 {
    font-size: 12px;
  }

  .book-info p {
    font-size: 10px;
  }

  .cover-content h3 {
    font-size: 21px;
  }

  .cover-content p {
    font-size: 8px;
  }

  .value-grid {
    grid-template-columns: 1fr;
  }

  .value-card {
    padding: 23px;
  }

  .types-grid {
    grid-template-columns: 1fr 1fr;
    gap: 10px;
  }

  .type-card {
    padding: 17px 14px;
  }

  .type-card h3 {
    font-size: 12px;
  }

  .audience-grid {
    grid-template-columns: 1fr 1fr;
    gap: 10px;
  }

  .audience-card {
    padding: 16px;
  }

  .feature-visual {
    min-height: 290px;
    padding: 15px;
  }

  .editor-preview {
    padding: 18px;
  }

  .editor-preview h3 {
    font-size: 22px;
  }

  .preview-window {
    padding: 17px;
  }

  .preview-window h3 {
    font-size: 23px;
  }

  .footer-grid {
    grid-template-columns: 1fr 1fr;
    gap: 30px 20px;
  }

  .footer-about {
    grid-column: 1 / -1;
  }

  .footer-bottom {
    flex-direction: column;
  }

  .section-title {
    letter-spacing: -1.4px;
  }
}

@media(prefers-reduced-motion:reduce) {
  html {
    scroll-behavior: auto;
  }

  *,
  *::before,
  *::after {
    transition-duration: .01ms !important;
    animation-duration: .01ms !important;
  }
}

</style>
</head>

<body>

<!-- =====================================
     ANNOUNCEMENT BAR
===================================== -->

<div class="announcement">
  Your next big idea deserves to become a book.
  <a href="#create">Start creating →</a>
</div>

<!-- =====================================
     NAVIGATION
===================================== -->

<header class="navbar">
  <div class="container nav-inner">

    <a href="#home" class="logo">
      <span class="logo-mark">B</span>
      <span>BOOK STUDIO</span>
    </a>

    <nav class="nav-links" id="navLinks">
      <a href="#how">How it works</a>
      <a href="#features">Features</a>
      <a href="#examples">Examples</a>
      <a href="#pricing">Pricing</a>
      <a href="#faq">FAQ</a>
    </nav>

    <div class="nav-actions">
      <a href="#create" class="btn btn-outline">Try it free</a>
      <a href="#create" class="btn btn-primary">Create your ebook ↗</a>
      <button class="menu-toggle" id="menuToggle" aria-label="Open navigation">☰</button>
    </div>

  </div>
</header>

<main>

<!-- =====================================
     HERO
===================================== -->

<section class="hero" id="home">
  <div class="container hero-content">

    <div class="pill">
      <span class="dot"></span>
      YOUR IDEAS. YOUR NEXT BIG BOOK.
    </div>

    <h1>
      Turn your ideas into
      <span class="highlight">beautiful ebooks.</span>
    </h1>

    <p class="hero-subtitle">
      From a simple idea to a professionally structured ebook.
      Bring your knowledge, creativity and stories to life with
      an easier book creation experience.
    </p>

    <div class="hero-actions">
      <a href="#create" class="btn btn-primary">
        Create your first ebook →
      </a>

      <a href="#examples" class="btn btn-outline">
        Explore examples
      </a>
    </div>

    <p class="hero-note">
      ✦ Explore the experience before connecting your AI account.
    </p>

    <!-- PROMPT INTERFACE -->

    <div class="prompt-box" id="create">

      <div class="prompt-top">
        <span class="prompt-heading">What would you like to create?</span>
        <span class="prompt-status">✦ BOOK CREATOR</span>
      </div>

      <textarea
        id="ebookPrompt"
        placeholder="Example: Create a practical beginner's guide to personal finance, covering budgeting, saving, investing basics and building healthy money habits..."
      ></textarea>

      <div class="prompt-bottom">

        <div class="prompt-options">

          <select id="bookType" aria-label="Ebook type">
            <option value="Guide">Guide</option>
            <option value="Ebook">Ebook</option>
            <option value="Workbook">Workbook</option>
            <option value="Report">Report</option>
            <option value="Novel">Novel</option>
            <option value="Lead magnet">Lead magnet</option>
          </select>

          <select id="bookLanguage" aria-label="Book language">
            <option value="English">English</option>
            <option value="Hindi">Hindi</option>
            <option value="Marathi">Marathi</option>
            <option value="Spanish">Spanish</option>
          </select>

        </div>

        <button class="btn btn-primary prompt-submit" id="createButton">
          Generate my idea →
        </button>

      </div>

      <div class="prompt-feedback" id="promptFeedback"></div>

    </div>

  </div>
</section>

<!-- =====================================
     TRUST / PLATFORM STRIP
===================================== -->

<section class="trust-strip">
  <div class="container">

    <p class="trust-title">
      Create content ready for your publishing journey
    </p>

    <div class="platforms">
      <div class="platform">amazon <span>kindle</span></div>
      <div class="platform">Apple Books</div>
      <div class="platform">Gumroad</div>
      <div class="platform">Etsy</div>
      <div class="platform">Kobo</div>
    </div>

  </div>
</section>

<!-- =====================================
     EBOOK EXAMPLES
===================================== -->

<section class="section showcase" id="examples">

  <div class="container">

    <div class="showcase-heading reveal">

      <div>
        <div class="section-label">WHAT YOU CAN CREATE</div>

        <h2 class="section-title">
          Your ideas can become
          <span class="highlight">real books.</span>
        </h2>

        <p class="section-description">
          Explore different types of ebooks you could create.
          From educational guides to workbooks and creative stories,
          your content can take many forms.
        </p>
      </div>

      <a href="#create" class="btn btn-outline">
        Create something similar →
      </a>

    </div>

    <div class="book-showcase">

      <article class="book-card reveal">
        <div class="book-cover cover-one">
          <div class="cover-content">
            <div class="cover-kicker">THE COMPLETE GUIDE</div>
            <h3>THE ART OF PERSONAL FINANCE</h3>
            <p>A PRACTICAL GUIDE TO MONEY</p>
          </div>
        </div>

        <div class="book-info">
          <h3>Personal Finance Guide</h3>
          <p>Educational ebook · Beginner friendly</p>
          <span class="book-tag">GUIDE</span>
        </div>
      </article>

      <article class="book-card reveal">
        <div class="book-cover cover-two">
          <div class="cover-content">
            <div class="cover-kicker">A BETTER EVERYDAY</div>
            <h3>BUILD BETTER HABITS</h3>
            <p>SMALL STEPS. BIG CHANGES.</p>
          </div>
        </div>

        <div class="book-info">
          <h3>Habits and Productivity</h3>
          <p>Self-development · Practical workbook</p>
          <span class="book-tag">WORKBOOK</span>
        </div>
      </article>

      <article class="book-card reveal">
        <div class="book-cover cover-three">
          <div class="cover-content">
            <div class="cover-kicker">THE CREATOR'S PLAYBOOK</div>
            <h3>GROW YOUR DIGITAL BRAND</h3>
            <p>CREATE. CONNECT. GROW.</p>
          </div>
        </div>

        <div class="book-info">
          <h3>Digital Business Blueprint</h3>
          <p>Business ebook · Actionable ideas</p>
          <span class="book-tag">BUSINESS</span>
        </div>
      </article>

      <article class="book-card reveal">
        <div class="book-cover cover-four">
          <div class="cover-content">
            <div class="cover-kicker">THE CREATIVE MIND</div>
            <h3>WRITE YOUR OWN STORY</h3>
            <p>LET YOUR IMAGINATION LEAD</p>
          </div>
        </div>

        <div class="book-info">
          <h3>Creative Writing Collection</h3>
          <p>Creative writing · Storytelling</p>
          <span class="book-tag">STORIES</span>
        </div>
      </article>

      <article class="book-card reveal">
        <div class="book-cover cover-five">
          <div class="cover-content">
            <div class="cover-kicker">A HEALTHIER LIFE</div>
            <h3>EVERYDAY WELLNESS</h3>
            <p>YOUR GUIDE TO BETTER ROUTINES</p>
          </div>
        </div>

        <div class="book-info">
          <h3>Everyday Wellness</h3>
          <p>Lifestyle ebook · Helpful routines</p>
          <span class="book-tag">LIFESTYLE</span>
        </div>
      </article>

      <article class="book-card reveal">
        <div class="book-cover cover-six">
          <div class="cover-content">
            <div class="cover-kicker">THE KNOWLEDGE SERIES</div>
            <h3>LEARN SOMETHING NEW</h3>
            <p>KNOWLEDGE MADE SIMPLE</p>
          </div>
        </div>

        <div class="book-info">
          <h3>Learning and Education</h3>
          <p>Educational content · Learning guide</p>
          <span class="book-tag">EDUCATION</span>
        </div>
      </article>

    </div>

  </div>
</section>

<!-- =====================================
     MAIN VALUE PROPOSITION
===================================== -->

<section class="section" id="features">

  <div class="container">

    <div class="text-center reveal">
      <div class="section-label">A BETTER WAY TO CREATE</div>

      <h2 class="section-title">
        Everything starts with
        <span class="highlight">one idea.</span>
      </h2>

      <p class="section-description">
        You don't need to start with a blank document.
        Organize your ideas, build your structure and develop
        your ebook through a guided creative process.
      </p>
    </div>

    <div class="value-grid">

      <article class="value-card reveal">
        <div class="value-icon">✦</div>
        <h3>Start with an idea</h3>
        <p>
          Describe what you want to create. Begin with a topic,
          a rough concept or a detailed book idea.
        </p>
      </article>

      <article class="value-card reveal">
        <div class="value-icon">☷</div>
        <h3>Build your structure</h3>
        <p>
          Organize your content into a logical outline with
          chapters, sections and a clear reading journey.
        </p>
      </article>

      <article class="value-card reveal">
        <div class="value-icon">✎</div>
        <h3>Make it your own</h3>
        <p>
          Refine the writing, adjust the tone and shape
          your ebook around your intended audience.
        </p>
      </article>

      <article class="value-card reveal">
        <div class="value-icon">▣</div>
        <h3>Design your cover</h3>
        <p>
          Create a visual direction that gives your ebook
          a consistent and recognizable identity.
        </p>
      </article>

      <article class="value-card reveal">
        <div class="value-icon">◎</div>
        <h3>Review every chapter</h3>
        <p>
          Read through your work, edit sections and improve
          the flow before preparing the final book.
        </p>
      </article>

      <article class="value-card reveal">
        <div class="value-icon">↗</div>
        <h3>Prepare to publish</h3>
        <p>
          Organize your finished content for the formats
          and publishing destinations you choose.
        </p>
      </article>

    </div>

  </div>
</section>

<!-- =====================================
     EDITOR FEATURE
===================================== -->

<section class="section feature-section">

  <div class="container feature-layout">

    <div class="feature-visual reveal">

      <div class="editor-preview">

        <div class="editor-top">
          <span>YOUR BOOK · CHAPTER 01</span>
          <span>01 / 08</span>
        </div>

        <h3>The Power of Starting Small</h3>

        <p>
          Every meaningful journey begins with a first step.
          The biggest changes in life rarely happen overnight.
          They develop through consistent decisions and small,
          intentional actions.
        </p>

        <div class="editor-line"></div>
        <div class="editor-line"></div>
        <div class="editor-line short"></div>

        <p style="margin-top:22px">
          Progress is not about doing everything at once.
          It is about creating a system that makes improvement
          possible every day.
        </p>

        <div class="editor-line"></div>
        <div class="editor-line short"></div>

      </div>

    </div>

    <div class="feature-copy reveal">

      <div class="section-label">YOUR CONTENT, YOUR CONTROL</div>

      <h2>
        More than just
        <span class="highlight">generating text.</span>
      </h2>

      <p>
        A useful ebook creation experience should give you
        control over the complete process. Your structure,
        your writing, your cover and your final presentation
        should work together.
      </p>

      <ul class="feature-list">

        <li>
          <span class="check">✓</span>
          <span>Organize your ebook into chapters and sections.</span>
        </li>

        <li>
          <span class="check">✓</span>
          <span>Review and edit the content before publishing.</span>
        </li>

        <li>
          <span class="check">✓</span>
          <span>Maintain a consistent writing style throughout.</span>
        </li>

        <li>
          <span class="check">✓</span>
          <span>Develop a cover and a consistent visual identity.</span>
        </li>

        <li>
          <span class="check">✓</span>
          <span>Prepare your content for different ebook formats.</span>
        </li>

      </ul>

      <a href="#create" class="btn btn-primary" style="margin-top:30px">
        Start with your idea →
      </a>

    </div>

  </div>
</section>

<!-- =====================================
     HOW IT WORKS
===================================== -->

<section class="section" id="how">

  <div class="container">

    <div class="text-center reveal">

      <div class="section-label">SIMPLE WORKFLOW</div>

      <h2 class="section-title">
        From idea to ebook
        <span class="highlight">in three steps.</span>
      </h2>

      <p class="section-description">
        A guided process designed to help you move from
        a rough concept to a complete book.
      </p>

    </div>

    <div class="steps-grid">

      <article class="step-card reveal">

        <div class="step-number">01</div>

        <h3>Tell us your idea</h3>

        <p>
          Describe your topic, choose the type of book,
          define your audience and decide the direction
          you want your content to take.
        </p>

      </article>

      <article class="step-card reveal">

        <div class="step-number">02</div>

        <h3>Develop your book</h3>

        <p>
          Build an outline, organize your chapters,
          develop the writing and review the content
          to make the book your own.
        </p>

      </article>

      <article class="step-card reveal">

        <div class="step-number">03</div>

        <h3>Prepare your ebook</h3>

        <p>
          Finalize your book's presentation, prepare
          the cover and organize your content for
          your preferred publishing format.
        </p>

      </article>

    </div>

  </div>
</section>

<!-- =====================================
     TYPES OF EBOOKS
===================================== -->

<section class="section types-section">

  <div class="container">

    <div class="text-center reveal">

      <div class="section-label">POSSIBILITIES</div>

      <h2 class="section-title">
        What will you
        <span class="highlight">write today?</span>
      </h2>

      <p class="section-description">
        Create different kinds of digital publications
        for different readers, goals and interests.
      </p>

    </div>

    <div class="types-grid">

      <article class="type-card reveal">
        <div class="type-symbol">▤</div>
        <h3>Educational Guides</h3>
        <p>Explain complex subjects in a clear and organized way.</p>
      </article>

      <article class="type-card reveal">
        <div class="type-symbol">✎</div>
        <h3>Workbooks</h3>
        <p>Build exercises, activities and practical learning resources.</p>
      </article>

      <article class="type-card reveal">
        <div class="type-symbol">◈</div>
        <h3>Lead Magnets</h3>
        <p>Create useful resources to share with your audience.</p>
      </article>

      <article class="type-card reveal">
        <div class="type-symbol">▧</div>
        <h3>Business Reports</h3>
        <p>Organize research, insights and business information.</p>
      </article>

      <article class="type-card reveal">
        <div class="type-symbol">✦</div>
        <h3>Personal Development</h3>
        <p>Develop content about goals, habits and productivity.</p>
      </article>

      <article class="type-card reveal">
        <div class="type-symbol">◇</div>
        <h3>Fiction and Stories</h3>
        <p>Explore characters, storytelling and creative writing.</p>
      </article>

      <article class="type-card reveal">
        <div class="type-symbol">▦</div>
        <h3>Digital Courses</h3>
        <p>Structure educational material into lessons and modules.</p>
      </article>

      <article class="type-card reveal">
        <div class="type-symbol">◎</div>
        <h3>Practical Checklists</h3>
        <p>Turn useful processes into easy-to-follow resources.</p>
      </article>

    </div>

  </div>
</section>

<!-- =====================================
     CUSTOMIZATION
===================================== -->

<section class="section">

  <div class="container custom-layout">

    <div class="custom-preview reveal">

      <div class="preview-window">

        <small>YOUR BOOK PREVIEW</small>

        <h3>Make Your Ideas Matter</h3>

        <p>
          A practical collection of ideas, lessons and
          strategies designed to help readers understand
          a subject and take meaningful action.
        </p>

        <div class="preview-columns">
          <div class="preview-block"></div>
          <div class="preview-block"></div>
        </div>

        <p style="margin-top:17px">
          Chapter 01 — Getting Started
        </p>

      </div>

    </div>

    <div class="reveal">

      <div class="section-label">PERSONALIZE YOUR BOOK</div>

      <h2 class="section-title">
        Your voice.
        Your style.
        <span class="highlight">Your book.</span>
      </h2>

      <p class="section-description">
        A book should feel like a complete piece of work,
        not a collection of unrelated paragraphs. Give your
        content a clear direction and a consistent identity.
      </p>

      <div class="custom-points">

        <div class="custom-point">
          <div class="custom-point-icon">Aa</div>
          <div>
            <h3>Writing tone</h3>
            <p>Choose a professional, conversational, educational or creative direction.</p>
          </div>
        </div>

        <div class="custom-point">
          <div class="custom-point-icon">◎</div>
          <div>
            <h3>Target audience</h3>
            <p>Shape the content around the knowledge level and needs of your readers.</p>
          </div>
        </div>

        <div class="custom-point">
          <div class="custom-point-icon">▤</div>
          <div>
            <h3>Book structure</h3>
            <p>Organize chapters and sections to create a logical reading experience.</p>
          </div>
        </div>

        <div class="custom-point">
          <div class="custom-point-icon">✦</div>
          <div>
            <h3>Visual direction</h3>
            <p>Give your book a cover and presentation that fit its subject.</p>
          </div>
        </div>

      </div>

    </div>

  </div>
</section>

<!-- =====================================
     EXPORT FORMATS
===================================== -->

<section class="section export-section">

  <div class="container">

    <div class="text-center reveal">

      <div class="section-label">READY FOR YOUR NEXT STEP</div>

      <h2 class="section-title">
        One book.
        <span class="highlight">Different formats.</span>
      </h2>

      <p class="section-description">
        Prepare your ebook for different reading and
        publishing experiences. Actual downloads will
        be connected in a later development stage.
      </p>

    </div>

    <div class="export-grid">

      <article class="export-card reveal">
        <div class="export-file">PDF</div>
        <h3>PDF Document</h3>
        <p>
          A fixed-layout format suitable for guides,
          reports, workbooks and digital sharing.
        </p>
      </article>

      <article class="export-card reveal">
        <div class="export-file">EPUB</div>
        <h3>EPUB Ebook</h3>
        <p>
          A reflowable ebook format designed for
          compatible digital reading applications.
        </p>
      </article>

      <article class="export-card reveal">
        <div class="export-file">DOCX</div>
        <h3>Word Document</h3>
        <p>
          An editable document format for additional
          writing, formatting and review.
        </p>
      </article>

    </div>

  </div>
</section>

<!-- =====================================
     WHO IS IT FOR?
===================================== -->

<section class="section">

  <div class="container">

    <div class="text-center reveal">

      <div class="section-label">MADE FOR IDEAS</div>

      <h2 class="section-title">
        Built for people who
        <span class="highlight">have something to share.</span>
      </h2>

      <p class="section-description">
        Whether you teach, create, consult or simply
        have knowledge worth organizing, your next
        ebook can begin with an idea.
      </p>

    </div>

    <div class="audience-grid">

      <article class="audience-card reveal">
        <h3>✦ Content Creators</h3>
        <p>Turn your experience and content into useful digital resources.</p>
      </article>

      <article class="audience-card reveal">
        <h3>▤ Coaches</h3>
        <p>Develop guides and workbooks for your learning programs.</p>
      </article>

      <article class="audience-card reveal">
        <h3>◎ Consultants</h3>
        <p>Organize your expertise into structured publications.</p>
      </article>

      <article class="audience-card reveal">
        <h3>◇ Entrepreneurs</h3>
        <p>Create educational resources for your business audience.</p>
      </article>

      <article class="audience-card reveal">
        <h3>✎ Authors</h3>
        <p>Develop book concepts and organize creative writing projects.</p>
      </article>

      <article class="audience-card reveal">
        <h3>▧ Educators</h3>
        <p>Build learning materials, explanations and study guides.</p>
      </article>

      <article class="audience-card reveal">
        <h3>◈ Students</h3>
        <p>Organize knowledge into notes, guides and learning resources.</p>
      </article>

      <article class="audience-card reveal">
        <h3>✧ Beginners</h3>
        <p>Start creating your first ebook without a complicated workflow.</p>
      </article>

    </div>

  </div>
</section>

<!-- =====================================
     PRICING
===================================== -->

<section class="section pricing-section" id="pricing">

  <div class="container">

    <div class="text-center reveal">

      <div class="section-label">SIMPLE AND TRANSPARENT</div>

      <h2 class="section-title">
        Choose the right way
        <span class="highlight">to create.</span>
      </h2>

      <p class="section-description">
        These are illustrative pricing layouts for the
        website design. Final plans, prices and credit
        limits will be decided before launch.
      </p>

    </div>

    <div class="pricing-grid">

      <article class="price-card reveal">

        <div class="price-name">Free Preview</div>

        <p class="price-description">
          Explore the creation experience.
        </p>

        <div class="price-amount">₹0</div>

        <div class="price-credit">Free preview access</div>

        <div class="price-divider"></div>

        <ul class="price-features">
          <li>Explore ebook creation</li>
          <li>Try example prompts</li>
          <li>View sample book structures</li>
          <li>Explore design previews</li>
          <li>No payment required</li>
        </ul>

        <a href="#create" class="btn btn-outline btn-full">
          Try for free
        </a>

      </article>

      <article class="price-card featured reveal">

        <span class="popular-tag">Popular</span>

        <div class="price-name">Creator</div>

        <p class="price-description">
          For people creating ebooks regularly.
        </p>

        <div class="price-amount">₹499<span>/month</span></div>

        <div class="price-credit">Illustrative plan</div>

        <div class="price-divider"></div>

        <ul class="price-features">
          <li>Everything in Free Preview</li>
          <li>Expanded creation allowance</li>
          <li>More customization options</li>
          <li>Book editing workspace</li>
          <li>Export features when available</li>
        </ul>

        <a href="#create" class="btn btn-primary btn-full">
          Explore creator plan
        </a>

      </article>

      <article class="price-card reveal">

        <div class="price-name">Pro</div>

        <p class="price-description">
          For advanced and frequent creators.
        </p>

        <div class="price-amount">₹999<span>/month</span></div>

        <div class="price-credit">Illustrative plan</div>

        <div class="price-divider"></div>

        <ul class="price-features">
          <li>Everything in Creator</li>
          <li>Higher creation allowance</li>
          <li>Advanced book customization</li>
          <li>More project capacity</li>
          <li>Priority support when available</li>
        </ul>

        <a href="#create" class="btn btn-outline btn-full">
          Explore Pro plan
        </a>

      </article>

    </div>

    <p class="pricing-note">
      Pricing shown is a design placeholder, not an active subscription offer.
    </p>

  </div>
</section>

<!-- =====================================
     FAQ
===================================== -->

<section class="section faq-section" id="faq">

  <div class="container">

    <div class="text-center reveal">

      <div class="section-label">HAVE QUESTIONS?</div>

      <h2 class="section-title">
        Frequently asked
        <span class="highlight">questions.</span>
      </h2>

      <p class="section-description">
        A few things you may want to know before
        starting your ebook creation journey.
      </p>

    </div>

    <div class="faq-list">

      <article class="faq-item active">

        <button class="faq-question">
          What is this platform?
          <span class="faq-symbol">+</span>
        </button>

        <div class="faq-answer">
          It is an ebook creation website concept designed
          to guide users through planning, writing, editing
          and preparing digital books.
        </div>

      </article>

      <article class="faq-item">

        <button class="faq-question">
          Do I need to know how to write a book?
          <span class="faq-symbol">+</span>
        </button>

        <div class="faq-answer">
          No professional publishing experience is required.
          The intended workflow helps you organize an idea
          into a book structure and develop it step by step.
        </div>

      </article>

      <article class="faq-item">

        <button class="faq-question">
          What kinds of ebooks can I create?
          <span class="faq-symbol">+</span>
        </button>

        <div class="faq-answer">
          The planned platform is intended for guides,
          workbooks, reports, educational resources,
          lead magnets and creative writing projects.
        </div>

      </article>

      <article class="faq-item">

        <button class="faq-question">
          Can I edit the generated content?
          <span class="faq-symbol">+</span>
        </button>

        <div class="faq-answer">
          The planned editing experience will let users
          review and refine their chapters, structure
          and writing before preparing the final book.
        </div>

      </article>

      <article class="faq-item">

        <button class="faq-question">
          Which download formats will be supported?
          <span class="faq-symbol">+</span>
        </button>

        <div class="faq-answer">
          PDF, EPUB and DOCX are the intended export formats.
          Download functionality needs to be implemented
          before those formats can be offered.
        </div>

      </article>

      <article class="faq-item">

        <button class="faq-question">
          Is AI generation available right now?
          <span class="faq-symbol">+</span>
        </button>

        <div class="faq-answer">
          This frontend preview does not yet connect to an AI
          provider. AI generation will require a secure backend
          integration before it can produce real books.
        </div>

      </article>

      <article class="faq-item">

        <button class="faq-question">
          Can I publish my ebook on other platforms?
          <span class="faq-symbol">+</span>
        </button>

        <div class="faq-answer">
          The website is being designed around common ebook
          publishing destinations. Publishing itself will
          depend on each destination's requirements and
          the final export functionality.
        </div>

      </article>

      <article class="faq-item">

        <button class="faq-question">
          Can I start for free?
          <span class="faq-symbol">+</span>
        </button>

        <div class="faq-answer">
          The current frontend includes a free preview design.
          Actual account access, usage limits and paid plans
          will be configured before the product launches.
        </div>

      </article>

    </div>

  </div>
</section>

<!-- =====================================
     FINAL CALL TO ACTION
===================================== -->

<section class="final-cta">

  <div class="container">

    <div class="cta-inner reveal">

      <div class="section-label">YOUR NEXT CHAPTER STARTS HERE</div>

      <h2>
        You have the idea.
        Now give it
        <span class="highlight">a book.</span>
      </h2>

      <p>
        Start with a topic, a thought or a story.
        Give your knowledge a structure and take
        the first step towards creating your ebook.
      </p>

      <a href="#create" class="btn btn-primary">
        Start creating your ebook →
      </a>

    </div>

  </div>
</section>

</main>

<!-- =====================================
     FOOTER
===================================== -->

<footer class="footer">

  <div class="container">

    <div class="footer-grid">

      <div class="footer-about">

        <a href="#home" class="logo">
          <span class="logo-mark">B</span>
          <span>BOOK STUDIO</span>
        </a>

        <p>
          A simpler way to turn ideas into structured
          digital books. Create, refine and prepare
          your next ebook.
        </p>

      </div>

      <div class="footer-column">

        <h3>Explore</h3>

        <a href="#features">Features</a>
        <a href="#how">How it works</a>
        <a href="#examples">Examples</a>
        <a href="#pricing">Pricing</a>

      </div>

      <div class="footer-column">

        <h3>Resources</h3>

        <a href="#examples">Ebook ideas</a>
        <a href="#how">Getting started</a>
        <a href="#features">Creation process</a>
        <a href="#faq">Help and FAQ</a>

      </div>

      <div class="footer-column">

        <h3>Company</h3>

        <a href="#home">About</a>
        <a href="#faq">Contact</a>
        <a href="#faq">Privacy</a>
        <a href="#faq">Terms</a>

      </div>

    </div>

    <div class="footer-bottom">

      <span>© 2026 BOOK STUDIO. All rights reserved.</span>

      <span>Made for ideas worth sharing.</span>

    </div>

  </div>

</footer>

<!-- =====================================
     TOAST NOTIFICATION
===================================== -->

<div class="toast" id="toast"></div>

<!-- =====================================
     JAVASCRIPT
===================================== -->

<script>

/* =====================================
   01. MOBILE NAVIGATION
===================================== */

const menuToggle = document.getElementById("menuToggle");

const navLinks = document.getElementById("navLinks");

menuToggle.addEventListener("click", () => {

  navLinks.classList.toggle("open");

  document.body.classList.toggle("menu-open");

  menuToggle.textContent =
    navLinks.classList.contains("open") ? "×" : "☰";

});

document.querySelectorAll(".nav-links a").forEach(link => {

  link.addEventListener("click", () => {

    navLinks.classList.remove("open");

    document.body.classList.remove("menu-open");

    menuToggle.textContent = "☰";

  });

});

/* =====================================
   02. TOAST MESSAGE
===================================== */

const toast = document.getElementById("toast");

let toastTimer;

function showToast(message) {

  toast.textContent = message;

  toast.classList.add("show");

  clearTimeout(toastTimer);

  toastTimer = setTimeout(() => {

    toast.classList.remove("show");

  }, 3000);

}

/* =====================================
   03. PROMPT INTERACTION
===================================== */

const createButton = document.getElementById("createButton");

const ebookPrompt = document.getElementById("ebookPrompt");

const bookType = document.getElementById("bookType");

const bookLanguage = document.getElementById("bookLanguage");

const promptFeedback = document.getElementById("promptFeedback");

createButton.addEventListener("click", () => {

  const idea = ebookPrompt.value.trim();

  const type = bookType.value;

  const language = bookLanguage.value;

  if (!idea) {

    ebookPrompt.focus();

    promptFeedback.style.display = "block";

    promptFeedback.textContent =
      "Please describe your ebook idea first.";

    return;

  }

  promptFeedback.style.display = "block";

  promptFeedback.innerHTML =
    "Your idea has been captured for this preview.<br>" +
    "<strong>Type:</strong> " + escapeHTML(type) +
    " · <strong>Language:</strong> " + escapeHTML(language) +
    "<br>AI generation will be connected after the backend integration.";

  showToast("Your ebook idea is ready for the next development step.");

});

/* =====================================
   04. SAFE TEXT DISPLAY
===================================== */

function escapeHTML(value) {

  return String(value).replace(/[&<>"']/g, character => {

    const entities = {

      "&": "&amp;",
      "<": "&lt;",
      ">": "&gt;",
      '"': "&quot;",
      "'": "&#039;"

    };

    return entities[character];

  });

}

/* =====================================
   05. FAQ ACCORDION
===================================== */

const faqItems = document.querySelectorAll(".faq-item");

faqItems.forEach(item => {

  const question = item.querySelector(".faq-question");

  question.addEventListener("click", () => {

    const wasActive = item.classList.contains("active");

    faqItems.forEach(otherItem => {

      otherItem.classList.remove("active");

    });

    if (!wasActive) {

      item.classList.add("active");

    }

  });

});

/* =====================================
   06. SCROLL REVEAL
===================================== */

const revealElements = document.querySelectorAll(".reveal");

if ("IntersectionObserver" in window) {

  const observer = new IntersectionObserver((entries, currentObserver) => {

    entries.forEach(entry => {

      if (entry.isIntersecting) {

        entry.target.classList.add("visible");

        currentObserver.unobserve(entry.target);

      }

    });

  }, {

    threshold: 0.12

  });

  revealElements.forEach(element => {

    observer.observe(element);

  });

} else {

  revealElements.forEach(element => {

    element.classList.add("visible");

  });

}

/* =====================================
   07. NAVIGATION SCROLL STATE
===================================== */

const navbar = document.querySelector(".navbar");

window.addEventListener("scroll", () => {

  if (window.scrollY > 30) {

    navbar.style.boxShadow = "0 8px 35px rgba(0,0,0,.22)";

  } else {

    navbar.style.boxShadow = "none";

  }

});

/* =====================================
   08. SMOOTH ANCHOR NAVIGATION
===================================== */

document.querySelectorAll('a[href^="#"]').forEach(anchor => {

  anchor.addEventListener("click", event => {

    const targetId = anchor.getAttribute("href");

    const target = document.querySelector(targetId);

    if (!target) return;

    event.preventDefault();

    target.scrollIntoView({

      behavior: "smooth",

      block: "start"

    });

  });

});

/* =====================================
   09. KEYBOARD ACCESSIBILITY
===================================== */

document.addEventListener("keydown", event => {

  if (event.key === "Escape") {

    navLinks.classList.remove("open");

    document.body.classList.remove("menu-open");

    menuToggle.textContent = "☰";

  }

});

/* =====================================
   10. INITIAL PAGE SETUP
===================================== */

document.addEventListener("DOMContentLoaded", () => {

  document.querySelectorAll(".reveal").forEach(element => {

    if (element.getBoundingClientRect().top < window.innerHeight) {

      element.classList.add("visible");

    }

  });

});

</script>

</body>
</html>
