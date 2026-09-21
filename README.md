<!DOCTYPE html>
<html lang="en">
<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Bushra Abdul Rasheed — Web Developer</title>

    <meta
        name="description"
        content="Bushra Abdul Rasheed — Web Developer specializing in WordPress, Shopify, Framer and modern CMS websites."
    >

    <!-- Google Font -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

    <link
        href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Space+Grotesk:wght@400;500;600;700&display=swap"
        rel="stylesheet"
    >

    <style>

        /* =========================================================
           RESET
        ========================================================= */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background: #07090d;
            color: #f5f7fa;
            font-family: "DM Sans", sans-serif;
            overflow-x: hidden;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        button {
            font-family: inherit;
        }

        ::selection {
            background: #7c6cff;
            color: #ffffff;
        }


        /* =========================================================
           GLOBAL BACKGROUND
        ========================================================= */

        body::before {
            content: "";
            position: fixed;
            width: 550px;
            height: 550px;
            top: -220px;
            left: -180px;
            background: #6557ff;
            opacity: 0.10;
            filter: blur(150px);
            pointer-events: none;
            z-index: -2;
        }

        body::after {
            content: "";
            position: fixed;
            width: 500px;
            height: 500px;
            right: -200px;
            bottom: -200px;
            background: #00b7ff;
            opacity: 0.08;
            filter: blur(150px);
            pointer-events: none;
            z-index: -2;
        }


        /* =========================================================
           GRID BACKGROUND
        ========================================================= */

        .grid-bg {
            position: fixed;
            inset: 0;
            z-index: -3;
            pointer-events: none;

            background-image:
                linear-gradient(
                    rgba(255,255,255,0.025) 1px,
                    transparent 1px
                ),
                linear-gradient(
                    90deg,
                    rgba(255,255,255,0.025) 1px,
                    transparent 1px
                );

            background-size: 70px 70px;

            mask-image: linear-gradient(
                to bottom,
                black,
                transparent 75%
            );
        }


        /* =========================================================
           CONTAINER
        ========================================================= */

        .container {
            width: min(1180px, calc(100% - 50px));
            margin: auto;
        }


        /* =========================================================
           NAVIGATION
        ========================================================= */

        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 999;

            background: rgba(7, 9, 13, 0.72);
            backdrop-filter: blur(18px);
            -webkit-backdrop-filter: blur(18px);

            border-bottom: 1px solid rgba(255,255,255,0.06);
        }

        nav {
            height: 76px;

            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            font-family: "Space Grotesk", sans-serif;
            font-size: 21px;
            font-weight: 700;
            letter-spacing: -0.8px;
        }

        .logo span {
            color: #8175ff;
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 34px;
        }

        .nav-links a {
            font-size: 13px;
            color: #8f97a5;
            transition: 0.3s ease;
        }

        .nav-links a:hover {
            color: #ffffff;
        }

        .nav-contact {
            padding: 10px 17px;
            border: 1px solid rgba(255,255,255,0.10);
            border-radius: 8px;
            color: #ffffff !important;
            background: rgba(255,255,255,0.04);
        }

        .nav-contact:hover {
            border-color: rgba(129,117,255,0.5);
            background: rgba(129,117,255,0.10);
        }


        /* =========================================================
           HERO
        ========================================================= */

        .hero {
            min-height: 100vh;

            display: flex;
            align-items: center;

            padding-top: 120px;
            padding-bottom: 100px;
        }

        .hero-content {
            max-width: 900px;
        }

        .availability {
            display: inline-flex;
            align-items: center;
            gap: 9px;

            padding: 8px 13px;

            border: 1px solid rgba(255,255,255,0.08);
            background: rgba(255,255,255,0.035);

            border-radius: 50px;

            color: #9ca4b2;
            font-size: 12px;

            margin-bottom: 30px;
        }

        .status-dot {
            width: 7px;
            height: 7px;

            border-radius: 50%;
            background: #55d88b;

            box-shadow: 0 0 12px rgba(85,216,139,0.7);
        }

        .hero h1 {
            font-family: "Space Grotesk", sans-serif;

            font-size: clamp(55px, 8vw, 100px);

            line-height: 0.98;

            letter-spacing: -5px;

            max-width: 950px;

            margin-bottom: 32px;
        }

        .gradient-text {
            background: linear-gradient(
                100deg,
                #ffffff 10%,
                #9388ff 48%,
                #55d8ff 90%
            );

            -webkit-background-clip: text;
            background-clip: text;

            -webkit-text-fill-color: transparent;
        }

        .hero-description {
            max-width: 680px;

            color: #929aa8;

            font-size: 17px;

            line-height: 1.8;

            margin-bottom: 35px;
        }

        .hero-buttons {
            display: flex;
            align-items: center;
            gap: 13px;

            flex-wrap: wrap;
        }

        .button {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 9px;

            padding: 14px 21px;

            border-radius: 9px;

            font-size: 13px;
            font-weight: 600;

            transition: 0.3s ease;
        }

        .button-primary {
            background: #ffffff;
            color: #07090d;
        }

        .button-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 35px rgba(255,255,255,0.12);
        }

        .button-dark {
            background: rgba(255,255,255,0.04);

            border: 1px solid rgba(255,255,255,0.09);

            color: #ffffff;
        }

        .button-dark:hover {
            transform: translateY(-3px);

            border-color: rgba(129,117,255,0.45);

            background: rgba(129,117,255,0.08);
        }

        .hero-meta {
            margin-top: 65px;

            display: flex;
            gap: 45px;

            color: #697281;
        }

        .hero-meta-item strong {
            display: block;

            font-family: "Space Grotesk", sans-serif;

            font-size: 20px;

            color: #dce0e7;

            margin-bottom: 4px;
        }

        .hero-meta-item span {
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 1.2px;
        }


        /* =========================================================
           SECTION
        ========================================================= */

        section {
            scroll-margin-top: 90px;
        }

        .section {
            padding: 120px 0;
        }

        .section-label {
            display: flex;
            align-items: center;
            gap: 12px;

            color: #8278ff;

            font-size: 11px;
            font-weight: 700;

            letter-spacing: 2px;
            text-transform: uppercase;

            margin-bottom: 18px;
        }

        .section-label::before {
            content: "";
            width: 28px;
            height: 1px;

            background: #8278ff;
        }

        .section-title {
            font-family: "Space Grotesk", sans-serif;

            font-size: clamp(34px, 5vw, 54px);

            letter-spacing: -2.5px;

            line-height: 1.05;

            margin-bottom: 18px;
        }

        .section-description {
            max-width: 650px;

            color: #858d9b;

            line-height: 1.8;

            font-size: 15px;
        }


        /* =========================================================
           ABOUT
        ========================================================= */

        .about-grid {
            display: grid;

            grid-template-columns: 1.1fr 0.9fr;

            gap: 70px;

            align-items: center;
        }

        .about-text p {
            color: #929aa8;

            line-height: 1.9;

            font-size: 15px;

            margin-bottom: 20px;
        }

        .about-text p:last-child {
            margin-bottom: 0;
        }

        .about-card {
            padding: 30px;

            border: 1px solid rgba(255,255,255,0.07);

            background:
                linear-gradient(
                    145deg,
                    rgba(255,255,255,0.055),
                    rgba(255,255,255,0.018)
                );

            border-radius: 18px;
        }

        .about-card-top {
            display: flex;
            justify-content: space-between;
            align-items: center;

            padding-bottom: 22px;

            margin-bottom: 22px;

            border-bottom: 1px solid rgba(255,255,255,0.07);
        }

        .about-card-title {
            font-family: "Space Grotesk", sans-serif;

            font-size: 18px;
            font-weight: 600;
        }

        .about-card-number {
            color: #8175ff;

            font-size: 12px;
            font-weight: 600;
        }

        .capability {
            display: flex;
            align-items: center;
            justify-content: space-between;

            padding: 14px 0;

            border-bottom: 1px solid rgba(255,255,255,0.05);
        }

        .capability:last-child {
            border-bottom: 0;
        }

        .capability span:first-child {
            color: #cbd0d9;
            font-size: 13px;
        }

        .capability span:last-child {
            color: #6e7786;
            font-size: 11px;
        }


        /* =========================================================
           PROJECTS
        ========================================================= */

        .projects-header {
            display: flex;

            align-items: flex-end;
            justify-content: space-between;

            gap: 30px;

            margin-bottom: 55px;
        }

        .projects-header .section-description {
            max-width: 440px;
        }

        .projects-grid {
            display: grid;

            grid-template-columns: repeat(2, 1fr);

            gap: 20px;
        }

        .project {
            position: relative;

            min-height: 285px;

            padding: 28px;

            overflow: hidden;

            border: 1px solid rgba(255,255,255,0.07);

            border-radius: 18px;

            background:
                linear-gradient(
                    145deg,
                    rgba(255,255,255,0.055),
                    rgba(255,255,255,0.018)
                );

            transition:
                transform 0.35s ease,
                border-color 0.35s ease,
                background 0.35s ease;
        }

        .project::after {
            content: "";

            position: absolute;

            width: 220px;
            height: 220px;

            right: -100px;
            top: -100px;

            border-radius: 50%;

            background: #7166ff;

            filter: blur(100px);

            opacity: 0;

            transition: 0.4s ease;
        }

        .project:hover {
            transform: translateY(-7px);

            border-color: rgba(129,117,255,0.38);

            background:
                linear-gradient(
                    145deg,
                    rgba(255,255,255,0.075),
                    rgba(255,255,255,0.025)
                );
        }

        .project:hover::after {
            opacity: 0.12;
        }

        .project-top {
            position: relative;
            z-index: 2;

            display: flex;

            align-items: center;
            justify-content: space-between;

            margin-bottom: 55px;
        }

        .project-number {
            font-family: "Space Grotesk", sans-serif;

            color: #737d8c;

            font-size: 12px;
        }

        .project-arrow {
            width: 37px;
            height: 37px;

            display: flex;
            align-items: center;
            justify-content: center;

            border-radius: 50%;

            border: 1px solid rgba(255,255,255,0.09);

            color: #aeb5c1;

            transition: 0.35s ease;
        }

        .project:hover .project-arrow {
            background: #ffffff;
            color: #07090d;

            transform: rotate(45deg);
        }

        .project h3 {
            position: relative;
            z-index: 2;

            font-family: "Space Grotesk", sans-serif;

            font-size: 25px;

            letter-spacing: -0.8px;

            margin-bottom: 10px;
        }

        .project-url {
            position: relative;
            z-index: 2;

            color: #737c8b;

            font-size: 12px;

            margin-bottom: 25px;
        }

        .project-tags {
            position: relative;
            z-index: 2;

            display: flex;
            flex-wrap: wrap;
            gap: 7px;
        }

        .tag {
            padding: 6px 9px;

            border-radius: 6px;

            background: rgba(255,255,255,0.045);

            border: 1px solid rgba(255,255,255,0.055);

            color: #929aa8;

            font-size: 10px;
        }


        /* =========================================================
           MORE PROJECTS
        ========================================================= */

        .more-projects {
            margin-top: 90px;
        }

        .more-title {
            display: flex;

            align-items: center;
            gap: 18px;

            margin-bottom: 30px;
        }

        .more-title h3 {
            font-family: "Space Grotesk", sans-serif;

            font-size: 22px;

            letter-spacing: -0.5px;
        }

        .more-title span {
            height: 1px;

            flex: 1;

            background: rgba(255,255,255,0.07);
        }

        .more-grid {
            display: grid;

            grid-template-columns: repeat(3, 1fr);

            gap: 12px;
        }

        .more-card {
            display: flex;

            align-items: center;
            justify-content: space-between;

            gap: 15px;

            padding: 18px 19px;

            border-radius: 11px;

            border: 1px solid rgba(255,255,255,0.06);

            background: rgba(255,255,255,0.025);

            color: #cbd0d8;

            transition: 0.3s ease;
        }

        .more-card:hover {
            transform: translateY(-3px);

            border-color: rgba(129,117,255,0.35);

            background: rgba(129,117,255,0.06);
        }

        .more-card div:first-child {
            min-width: 0;
        }

        .more-number {
            display: block;

            color: #606a79;

            font-size: 10px;

            margin-bottom: 4px;
        }

        .more-name {
            display: block;

            font-size: 13px;

            white-space: nowrap;

            overflow: hidden;

            text-overflow: ellipsis;
        }

        .more-arrow {
            color: #717b89;

            font-size: 14px;
        }


        /* =========================================================
           SERVICES / CAPABILITIES
        ========================================================= */

        .capabilities-grid {
            display: grid;

            grid-template-columns: repeat(4, 1fr);

            gap: 12px;

            margin-top: 55px;
        }

        .capability-box {
            padding: 28px 22px;

            min-height: 180px;

            border: 1px solid rgba(255,255,255,0.07);

            border-radius: 15px;

            background: rgba(255,255,255,0.025);

            transition: 0.3s ease;
        }

        .capability-box:hover {
            transform: translateY(-5px);

            border-color: rgba(129,117,255,0.3);

            background: rgba(129,117,255,0.045);
        }

        .capability-icon {
            width: 42px;
            height: 42px;

            display: flex;
            align-items: center;
            justify-content: center;

            margin-bottom: 25px;

            border-radius: 10px;

            color: #9c92ff;

            background: rgba(129,117,255,0.09);

            border: 1px solid rgba(129,117,255,0.12);

            font-size: 17px;
        }

        .capability-box h3 {
            font-family: "Space Grotesk", sans-serif;

            font-size: 15px;

            margin-bottom: 8px;
        }

        .capability-box p {
            color: #737d8b;

            font-size: 12px;

            line-height: 1.7;
        }


        /* =========================================================
           EXPERIENCE STRIP
        ========================================================= */

        .experience-box {
            display: grid;

            grid-template-columns: 1fr auto;

            align-items: center;

            gap: 30px;

            padding: 35px;

            border: 1px solid rgba(255,255,255,0.07);

            border-radius: 18px;

            background:
                linear-gradient(
                    100deg,
                    rgba(129,117,255,0.07),
                    rgba(255,255,255,0.025)
                );
        }

        .experience-company {
            font-family: "Space Grotesk", sans-serif;

            font-size: 23px;

            margin-bottom: 8px;
        }

        .experience-role {
            color: #858e9c;

            font-size: 13px;
        }

        .experience-side {
            text-align: right;
        }

        .experience-side strong {
            display: block;

            color: #ffffff;

            font-size: 14px;

            margin-bottom: 5px;
        }

        .experience-side span {
            color: #687281;

            font-size: 11px;
        }


        /* =========================================================
           CONTACT
        ========================================================= */

        .contact {
            padding: 130px 0 100px;
        }

        .contact-box {
            position: relative;

            overflow: hidden;

            text-align: center;

            padding: 90px 30px;

            border-radius: 25px;

            border: 1px solid rgba(255,255,255,0.08);

            background:
                radial-gradient(
                    circle at 50% 0%,
                    rgba(129,117,255,0.13),
                    transparent 55%
                ),
                rgba(255,255,255,0.025);
        }

        .contact-box::before {
            content: "";

            position: absolute;

            width: 300px;
            height: 300px;

            left: 50%;
            top: -220px;

            transform: translateX(-50%);

            background: #7166ff;

            filter: blur(130px);

            opacity: 0.10;
        }

        .contact-box > * {
            position: relative;
            z-index: 2;
        }

        .contact-box .section-label {
            justify-content: center;
        }

        .contact-box .section-label::before {
            display: none;
        }

        .contact-box h2 {
            font-family: "Space Grotesk", sans-serif;

            font-size: clamp(40px, 6vw, 70px);

            letter-spacing: -3px;

            line-height: 1;

            margin-bottom: 20px;
        }

        .contact-box p {
            max-width: 550px;

            margin: auto auto 32px;

            color: #858e9c;

            line-height: 1.8;

            font-size: 14px;
        }

        .contact-email {
            display: inline-flex;

            align-items: center;
            gap: 10px;

            color: #ffffff;

            font-size: 14px;

            padding-bottom: 5px;

            border-bottom: 1px solid rgba(255,255,255,0.3);

            transition: 0.3s ease;
        }

        .contact-email:hover {
            color: #9d94ff;

            border-color: #9d94ff;
        }


        /* =========================================================
           FOOTER
        ========================================================= */

        footer {
            border-top: 1px solid rgba(255,255,255,0.06);

            padding: 28px 0;

            color: #606977;

            font-size: 11px;
        }

        .footer-inner {
            display: flex;

            align-items: center;
            justify-content: space-between;
        }

        .footer-links {
            display: flex;
            gap: 20px;
        }

        .footer-links a {
            transition: 0.3s ease;
        }

        .footer-links a:hover {
            color: #ffffff;
        }


        /* =========================================================
           SCROLL REVEAL
        ========================================================= */

        .reveal {
            opacity: 0;

            transform: translateY(25px);

            transition:
                opacity 0.7s ease,
                transform 0.7s ease;
        }

        .reveal.show {
            opacity: 1;

            transform: translateY(0);
        }


        /* =========================================================
           RESPONSIVE
        ========================================================= */

        @media (max-width: 900px) {

            .about-grid {
                grid-template-columns: 1fr;
            }

            .capabilities-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .more-grid {
                grid-template-columns: repeat(2, 1fr);
            }

        }


        @media (max-width: 700px) {

            .container {
                width: min(100% - 35px, 1180px);
            }

            .nav-links {
                display: none;
            }

            .hero {
                padding-top: 125px;
                min-height: auto;
            }

            .hero h1 {
                font-size: 53px;
                letter-spacing: -3px;
            }

            .hero-description {
                font-size: 15px;
            }

            .hero-meta {
                gap: 25px;
                flex-wrap: wrap;
            }

            .section {
                padding: 80px 0;
            }

            .projects-header {
                display: block;
            }

            .projects-header .section-description {
                margin-top: 20px;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .more-grid {
                grid-template-columns: 1fr;
            }

            .capabilities-grid {
                grid-template-columns: 1fr;
            }

            .experience-box {
                grid-template-columns: 1fr;
            }

            .experience-side {
                text-align: left;
            }

            .contact {
                padding-top: 80px;
            }

            .contact-box {
                padding: 65px 22px;
            }

            .contact-box h2 {
                letter-spacing: -2px;
            }

            .footer-inner {
                flex-direction: column;

                gap: 15px;

                text-align: center;
            }

        }


        @media (max-width: 450px) {

            .hero h1 {
                font-size: 45px;
            }

            .hero-buttons {
                width: 100%;
            }

            .button {
                width: 100%;
            }

            .hero-meta {
                display: grid;

                grid-template-columns: 1fr 1fr;

                gap: 20px;
            }

            .project {
                min-height: 265px;
            }

        }

    </style>

</head>


<body>


    <!-- Background grid -->

    <div class="grid-bg"></div>


    <!-- =========================================================
         NAVIGATION
    ========================================================== -->

    <header>

        <nav class="container">

            <a href="#home" class="logo">
                Bushra<span>.</span>
            </a>

            <div class="nav-links">

                <a href="#about">
                    About
                </a>

                <a href="#work">
                    Work
                </a>

                <a href="#capabilities">
                    Capabilities
                </a>

                <a href="#contact" class="nav-contact">
                    Let's Talk
                </a>

            </div>

        </nav>

    </header>


    <!-- =========================================================
         HERO
    ========================================================== -->

    <main id="home">

        <section class="hero">

            <div class="container">

                <div class="hero-content reveal">

                    <div class="availability">

                        <span class="status-dot"></span>

                        Open to Remote Opportunities

                    </div>


                    <h1>

                        I build websites
                        <br>

                        that
                        <span class="gradient-text">
                            work beautifully.
                        </span>

                    </h1>


                    <p class="hero-description">

                        I'm Bushra, a Web Developer focused on WordPress
                        and modern CMS development. I turn designs and
                        ideas into responsive, functional websites with
                        attention to detail, performance and usability.

                    </p>


                    <div class="hero-buttons">

                        <a
                            href="#work"
                            class="button button-primary"
                        >
                            Explore My Work
                            <span>↗</span>
                        </a>


                        <a
                            href="mailto:bushirasheed2000@gmail.com"
                            class="button button-dark"
                        >
                            Get In Touch
                        </a>

                    </div>


                    <div class="hero-meta">

                        <div class="hero-meta-item">

                            <strong>2.5+</strong>

                            <span>
                                Years Experience
                            </span>

                        </div>


                        <div class="hero-meta-item">

                            <strong>4+</strong>

                            <span>
                                CMS Platforms
                            </span>

                        </div>


                        <div class="hero-meta-item">

                            <strong>Remote</strong>

                            <span>
                                International Work
                            </span>

                        </div>

                    </div>

                </div>

            </div>

        </section>


        <!-- =====================================================
             ABOUT
        ====================================================== -->

        <section class="section" id="about">

            <div class="container">

                <div class="about-grid">


                    <div class="about-text reveal">

                        <div class="section-label">
                            About
                        </div>

                        <h2 class="section-title">
                            More than just
                            <span class="gradient-text">
                                building pages.
                            </span>
                        </h2>


                        <p>

                            I enjoy turning designs, ideas and
                            requirements into websites that feel
                            polished and work smoothly across devices.

                        </p>


                        <p>

                            My work is mainly focused on WordPress and
                            CMS-based development, with experience across
                            Shopify, Framer and Wix. I care about the
                            details behind a website too — responsiveness,
                            performance, SEO and maintainability.

                        </p>


                    </div>


                    <div class="about-card reveal">

                        <div class="about-card-top">

                            <div class="about-card-title">
                                What I Work With
                            </div>

                            <div class="about-card-number">
                                01 — 04
                            </div>

                        </div>


                        <div class="capability">

                            <span>WordPress</span>

                            <span>CMS</span>

                        </div>


                        <div class="capability">

                            <span>Shopify</span>

                            <span>E-commerce</span>

                        </div>


                        <div class="capability">

                            <span>Framer</span>

                            <span>Web Design</span>

                        </div>


                        <div class="capability">

                            <span>Wix</span>

                            <span>CMS</span>

                        </div>


                    </div>


                </div>

            </div>

        </section>


        <!-- =====================================================
             FEATURED WORK
        ====================================================== -->

        <section class="section" id="work">

            <div class="container">


                <div class="projects-header reveal">

                    <div>

                        <div class="section-label">
                            Selected Work
                        </div>

                        <h2 class="section-title">
                            Things I've
                            <span class="gradient-text">
                                built.
                            </span>
                        </h2>

                    </div>


                    <p class="section-description">

                        A selection of websites I've worked on across
                        different industries, platforms and requirements.

                    </p>

                </div>


                <div class="projects-grid">


                    <!-- PROJECT 01 -->

                    <a
                        href="https://troncon-montage.nl/"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="project reveal"
                    >

                        <div class="project-top">

                            <span class="project-number">
                                01 / 07
                            </span>

                            <span class="project-arrow">
                                ↗
                            </span>

                        </div>


                        <h3>
                            Troncon Montage
                        </h3>

                        <div class="project-url">
                            troncon-montage.nl
                        </div>


                        <div class="project-tags">

                            <span class="tag">
                                WordPress
                            </span>

                            <span class="tag">
                                Responsive
                            </span>

                            <span class="tag">
                                CMS
                            </span>

                        </div>

                    </a>


                    <!-- PROJECT 02 -->

                    <a
                        href="https://movasupport.nl/"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="project reveal"
                    >

                        <div class="project-top">

                            <span class="project-number">
                                02 / 07
                            </span>

                            <span class="project-arrow">
                                ↗
                            </span>

                        </div>


                        <h3>
                            MOVA Support
                        </h3>

                        <div class="project-url">
                            movasupport.nl
                        </div>


                        <div class="project-tags">

                            <span class="tag">
                                WordPress
                            </span>

                            <span class="tag">
                                Responsive
                            </span>

                            <span class="tag">
                                CMS
                            </span>

                        </div>

                    </a>


                    <!-- PROJECT 03 -->

                    <a
                        href="https://allesvoorpadellen.nl/"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="project reveal"
                    >

                        <div class="project-top">

                            <span class="project-number">
                                03 / 07
                            </span>

                            <span class="project-arrow">
                                ↗
                            </span>

                        </div>


                        <h3>
                            Alles Voor Padellen
                        </h3>

                        <div class="project-url">
                            allesvoorpadellen.nl
                        </div>


                        <div class="project-tags">

                            <span class="tag">
                                WordPress
                            </span>

                            <span class="tag">
                                E-commerce
                            </span>

                            <span class="tag">
                                WooCommerce
                            </span>

                        </div>

                    </a>


                    <!-- PROJECT 04 -->

                    <a
                        href="https://rnt-motorsports.com/"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="project reveal"
                    >

                        <div class="project-top">

                            <span class="project-number">
                                04 / 07
                            </span>

                            <span class="project-arrow">
                                ↗
                            </span>

                        </div>


                        <h3>
                            RNT Motorsports
                        </h3>

                        <div class="project-url">
                            rnt-motorsports.com
                        </div>


                        <div class="project-tags">

                            <span class="tag">
                                WordPress
                            </span>

                            <span class="tag">
                                Responsive
                            </span>

                            <span class="tag">
                                Development
                            </span>

                        </div>

                    </a>


                    <!-- PROJECT 05 -->

                    <a
                        href="https://abonnementdonaldduck.nl/"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="project reveal"
                    >

                        <div class="project-top">

                            <span class="project-number">
                                05 / 07
                            </span>

                            <span class="project-arrow">
                                ↗
                            </span>

                        </div>


                        <h3>
                            Abonnement Donald Duck
                        </h3>

                        <div class="project-url">
                            abonnementdonaldduck.nl
                        </div>


                        <div class="project-tags">

                            <span class="tag">
                                WordPress
                            </span>

                            <span class="tag">
                                CMS
                            </span>

                            <span class="tag">
                                Responsive
                            </span>

                        </div>

                    </a>


                    <!-- PROJECT 06 -->

                    <a
                        href="https://winkind.co.za/"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="project reveal"
                    >

                        <div class="project-top">

                            <span class="project-number">
                                06 / 07
                            </span>

                            <span class="project-arrow">
                                ↗
                            </span>

                        </div>


                        <h3>
                            Winkind
                        </h3>

                        <div class="project-url">
                            winkind.co.za
                        </div>


                        <div class="project-tags">

                            <span class="tag">
                                WordPress
                            </span>

                            <span class="tag">
                                Responsive
                            </span>

                            <span class="tag">
                                CMS
                            </span>

                        </div>

                    </a>


                    <!-- PROJECT 07 -->

                    <a
                        href="https://www.coknowledge.nl/"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="project reveal"
                    >

                        <div class="project-top">

                            <span class="project-number">
                                07 / 07
                            </span>

                            <span class="project-arrow">
                                ↗
                            </span>

                        </div>


                        <h3>
                            CoKnowledge
                        </h3>

                        <div class="project-url">
                            coknowledge.nl
                        </div>


                        <div class="project-tags">

                            <span class="tag">
                                WordPress
                            </span>

                            <span class="tag">
                                CMS
                            </span>

                            <span class="tag">
                                Responsive
                            </span>

                        </div>

                    </a>


                </div>


                <!-- =================================================
                     MORE PROJECTS
                ================================================== -->

                <div class="more-projects reveal">

                    <div class="more-title">

                        <h3>
                            More Projects
                        </h3>

                        <span></span>

                    </div>


                    <div class="more-grid">


                        <a
                            href="https://lezzat.co.uk"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="more-card"
                        >

                            <div>

                                <span class="more-number">
                                    08
                                </span>

                                <span class="more-name">
                                    Lezzat
                                </span>

                            </div>

                            <span class="more-arrow">
                                ↗
                            </span>

                        </a>


                        <a
                            href="https://www.socksmad.co.uk"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="more-card"
                        >

                            <div>

                                <span class="more-number">
                                    09
                                </span>

                                <span class="more-name">
                                    Socks Mad
                                </span>

                            </div>

                            <span class="more-arrow">
                                ↗
                            </span>

                        </a>


                        <a
                            href="https://2ezi.au"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="more-card"
                        >

                            <div>

                                <span class="more-number">
                                    10
                                </span>

                                <span class="more-name">
                                    2EZI
                                </span>

                            </div>

                            <span class="more-arrow">
                                ↗
                            </span>

                        </a>


                        <a
                            href="http://2ezigiveaways.au"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="more-card"
                        >

                            <div>

                                <span class="more-number">
                                    11
                                </span>

                                <span class="more-name">
                                    2EZI Giveaways
                                </span>

                            </div>

                            <span class="more-arrow">
                                ↗
                            </span>

                        </a>


                        <a
                            href="https://adelaidefurnitureremovals.net.au"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="more-card"
                        >

                            <div>

                                <span class="more-number">
                                    12
                                </span>

                                <span class="more-name">
                                    Adelaide Furniture Removals
                                </span>

                            </div>

                            <span class="more-arrow">
                                ↗
                            </span>

                        </a>


                        <a
                            href="https://123laptophoezen.nl"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="more-card"
                        >

                            <div>

                                <span class="more-number">
                                    13
                                </span>

                                <span class="more-name">
                                    123 Laptop Hoezen
                                </span>

                            </div>

                            <span class="more-arrow">
                                ↗
                            </span>

                        </a>


                        <a
                            href="https://www.antennasnearme.com"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="more-card"
                        >

                            <div>

                                <span class="more-number">
                                    14
                                </span>

                                <span class="more-name">
                                    Antennas Near Me
                                </span>

                            </div>

                            <span class="more-arrow">
                                ↗
                            </span>

                        </a>


                        <a
                            href="https://bartercard.com.au"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="more-card"
                        >

                            <div>

                                <span class="more-number">
                                    15
                                </span>

                                <span class="more-name">
                                    Bartercard
                                </span>

                            </div>

                            <span class="more-arrow">
                                ↗
                            </span>

                        </a>


                        <a
                            href="https://teacher4u.co.il"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="more-card"
                        >

                            <div>

                                <span class="more-number">
                                    16
                                </span>

                                <span class="more-name">
                                    Teacher4U
                                </span>

                            </div>

                            <span class="more-arrow">
                                ↗
                            </span>

                        </a>


                    </div>

                </div>

            </div>

        </section>


        <!-- =====================================================
             CAPABILITIES
        ====================================================== -->

        <section class="section" id="capabilities">

            <div class="container">

                <div class="reveal">

                    <div class="section-label">
                        Capabilities
                    </div>

                    <h2 class="section-title">
                        What I bring
                        <span class="gradient-text">
                            to a project.
                        </span>
                    </h2>

                    <p class="section-description">

                        From the first design handoff to a polished
                        live website, I focus on building experiences
                        that are responsive, practical and easy to manage.

                    </p>

                </div>


                <div class="capabilities-grid">


                    <div class="capability-box reveal">

                        <div class="capability-icon">
                            ◇
                        </div>

                        <h3>
                            WordPress Development
                        </h3>

                        <p>
                            Custom websites, page builder development,
                            CMS setup and content management.
                        </p>

                    </div>


                    <div class="capability-box reveal">

                        <div class="capability-icon">
                            &lt;/&gt;
                        </div>

                        <h3>
                            Figma to Website
                        </h3>

                        <p>
                            Turning designs into accurate,
                            responsive and functional pages.
                        </p>

                    </div>


                    <div class="capability-box reveal">

                        <div class="capability-icon">
                            ◫
                        </div>

                        <h3>
                            E-commerce
                        </h3>

                        <p>
                            WooCommerce and Shopify websites,
                            product structures and store experiences.
                        </p>

                    </div>


                    <div class="capability-box reveal">

                        <div class="capability-icon">
                            ⚡
                        </div>

                        <h3>
                            Performance & SEO
                        </h3>

                        <p>
                            Responsive implementation, site speed,
                            Core Web Vitals and on-page SEO.
                        </p>

                    </div>


                </div>

            </div>

        </section>


        <!-- =====================================================
             EXPERIENCE
        ====================================================== -->

        <section class="section">

            <div class="container">

                <div class="experience-box reveal">


                    <div>

                        <div class="experience-company">
                            WanneerOnline
                        </div>

                        <div class="experience-role">
                            Web Developer · Remote · Netherlands
                        </div>

                    </div>


                    <div class="experience-side">

                        <strong>
                            Nov 2025 — Present
                        </strong>

                        <span>
                            International Client Work
                        </span>

                    </div>


                </div>

            </div>

        </section>


        <!-- =====================================================
             CONTACT
        ====================================================== -->

        <section class="contact" id="contact">

            <div class="container">

                <div class="contact-box reveal">

                    <div class="section-label">
                        Get In Touch
                    </div>


                    <h2>
                        Have a project
                        <br>
                        in mind?
                    </h2>


                    <p>

                        Whether you're looking for a website,
                        CMS development or help turning a design
                        into a working site, I'd be happy to hear
                        about it.

                    </p>


                    <a
                        href="mailto:bushirasheed2000@gmail.com"
                        class="contact-email"
                    >

                        bushirasheed2000@gmail.com

                        <span>↗</span>

                    </a>

                </div>

            </div>

        </section>

    </main>


    <!-- =========================================================
         FOOTER
    ========================================================== -->

    <footer>

        <div class="container footer-inner">

            <div>
                © 2026 Bushra Abdul Rasheed
            </div>


            <div class="footer-links">

                <a
                    href="https://github.com/bushraabdulrasheed"
                    target="_blank"
                    rel="noopener noreferrer"
                >
                    GitHub
                </a>


                <a
                    href="https://linkedin.com/in/bushra-abdul-rasheed-b17044231"
                    target="_blank"
                    rel="noopener noreferrer"
                >
                    LinkedIn
                </a>


                <a href="mailto:bushirasheed2000@gmail.com">
                    Email
                </a>

            </div>

        </div>

    </footer>


    <!-- =========================================================
         JAVASCRIPT
    ========================================================== -->

    <script>

        const revealElements =
            document.querySelectorAll(".reveal");


        const observer =
            new IntersectionObserver(

                (entries) => {

                    entries.forEach(
                        (entry) => {

                            if (entry.isIntersecting) {

                                entry.target.classList.add("show");

                                observer.unobserve(entry.target);

                            }

                        }
                    );

                },

                {
                    threshold: 0.12
                }

            );


        revealElements.forEach(
            (element) => {

                observer.observe(element);

            }
        );


    </script>


</body>
</html>
