<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">

    <meta
        name="viewport"
        content="width=device-width, initial-scale=1.0"
    >

    <meta
        name="description"
        content="Srimanth Vasireddy - Android Engineer, AI Developer, Kotlin Multiplatform Developer and Fintech/POS Engineer."
    >

    <meta
        name="keywords"
        content="Srimanth Vasireddy, Android Developer, Kotlin Developer, Jetpack Compose, KMP, Kotlin Multiplatform, Gemini AI, ML Kit, POS Developer, Fintech Developer"
    >

    <meta name="author" content="Srimanth Vasireddy">

    <title>
        Srimanth Vasireddy | Android Engineer
    </title>

    <!-- Google Font -->
    <link
        rel="preconnect"
        href="https://fonts.googleapis.com"
    >

    <link
        rel="preconnect"
        href="https://fonts.gstatic.com"
        crossorigin
    >

    <link
        href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600;700&family=Inter:wght@400;500;600;700;800&display=swap"
        rel="stylesheet"
    >

    <!-- Font Awesome -->
    <link
        rel="stylesheet"
        href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css"
    >

    <style>

        /* ============================================================
           GLOBAL
        ============================================================ */

        :root {
            --bg: #050810;
            --bg-secondary: #080d18;
            --card: rgba(16, 23, 40, 0.72);
            --card-hover: rgba(24, 34, 58, 0.90);

            --text: #f4f7ff;
            --muted: #9ba9c3;

            --primary: #00e5ff;
            --secondary: #7c4dff;
            --green: #00e676;
            --orange: #ff9800;
            --pink: #ff4081;

            --border: rgba(255, 255, 255, 0.09);

            --gradient:
                linear-gradient(
                    135deg,
                    #00e5ff,
                    #7c4dff,
                    #ff4081
                );

            --shadow:
                0 20px 60px rgba(0, 0, 0, 0.40);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background:
                radial-gradient(
                    circle at 10% 10%,
                    rgba(0, 229, 255, 0.07),
                    transparent 25%
                ),
                radial-gradient(
                    circle at 90% 15%,
                    rgba(124, 77, 255, 0.08),
                    transparent 30%
                ),
                radial-gradient(
                    circle at 50% 90%,
                    rgba(255, 64, 129, 0.05),
                    transparent 25%
                ),
                var(--bg);

            color: var(--text);

            font-family: "Inter", sans-serif;

            overflow-x: hidden;
        }

        body::before {
            content: "";

            position: fixed;

            inset: 0;

            pointer-events: none;

            background-image:
                linear-gradient(
                    rgba(255,255,255,0.015) 1px,
                    transparent 1px
                ),
                linear-gradient(
                    90deg,
                    rgba(255,255,255,0.015) 1px,
                    transparent 1px
                );

            background-size: 60px 60px;

            z-index: -3;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        img {
            max-width: 100%;
        }

        .container {
            width: min(1180px, 92%);
            margin: auto;
        }

        section {
            padding: 90px 0;
        }


        /* ============================================================
           SCROLLBAR
        ============================================================ */

        ::-webkit-scrollbar {
            width: 9px;
        }

        ::-webkit-scrollbar-track {
            background: #050810;
        }

        ::-webkit-scrollbar-thumb {
            background:
                linear-gradient(
                    var(--primary),
                    var(--secondary)
                );

            border-radius: 20px;
        }


        /* ============================================================
           PARTICLES
        ============================================================ */

        #particles {
            position: fixed;

            inset: 0;

            z-index: -2;

            overflow: hidden;

            pointer-events: none;
        }

        .particle {
            position: absolute;

            width: 3px;
            height: 3px;

            border-radius: 50%;

            background: rgba(0, 229, 255, .6);

            box-shadow:
                0 0 10px rgba(0,229,255,.7);

            animation:
                particleMove linear infinite;
        }

        @keyframes particleMove {

            from {
                transform:
                    translateY(110vh)
                    scale(.3);

                opacity: 0;
            }

            15% {
                opacity: 1;
            }

            80% {
                opacity: 1;
            }

            to {
                transform:
                    translateY(-20vh)
                    scale(1);

                opacity: 0;
            }
        }


        /* ============================================================
           NAVBAR
        ============================================================ */

        nav {
            position: fixed;

            top: 0;
            left: 0;
            right: 0;

            z-index: 1000;

            background:
                rgba(5, 8, 16, .65);

            backdrop-filter: blur(20px);

            border-bottom:
                1px solid rgba(255,255,255,.05);
        }

        .nav-inner {
            height: 70px;

            display: flex;

            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: "Fira Code", monospace;

            font-size: 20px;

            font-weight: 700;

            background: var(--gradient);

            background-size: 200%;

            -webkit-background-clip: text;

            color: transparent;

            animation:
                gradientMove 4s linear infinite;
        }

        .nav-links {
            display: flex;
            gap: 26px;

            color: var(--muted);

            font-size: 14px;
        }

        .nav-links a {
            transition: .3s;
        }

        .nav-links a:hover {
            color: var(--primary);
        }


        /* ============================================================
           HERO
        ============================================================ */

        .hero {
            min-height: 100vh;

            display: flex;

            align-items: center;

            padding-top: 100px;

            position: relative;
        }

        .hero-grid {
            display: grid;

            grid-template-columns:
                1.25fr .75fr;

            gap: 60px;

            align-items: center;
        }

        .status {
            display: inline-flex;

            align-items: center;

            gap: 9px;

            padding:
                9px 14px;

            border:
                1px solid rgba(0,230,118,.25);

            border-radius: 50px;

            color: var(--green);

            background:
                rgba(0,230,118,.05);

            font-size: 13px;

            margin-bottom: 28px;
        }

        .status-dot {
            width: 8px;
            height: 8px;

            background: var(--green);

            border-radius: 50%;

            box-shadow:
                0 0 15px var(--green);

            animation:
                pulse 1.5s infinite;
        }

        @keyframes pulse {

            0%, 100% {
                opacity: 1;
                transform: scale(1);
            }

            50% {
                opacity: .35;
                transform: scale(.75);
            }
        }

        .hero h1 {
            font-size:
                clamp(48px, 7vw, 86px);

            line-height: 1.02;

            letter-spacing: -4px;

            font-weight: 800;

            margin-bottom: 20px;
        }

        .gradient-text {
            background: var(--gradient);

            background-size: 250%;

            -webkit-background-clip: text;

            color: transparent;

            animation:
                gradientMove 6s linear infinite;
        }

        @keyframes gradientMove {

            0% {
                background-position: 0%;
            }

            100% {
                background-position: 200%;
            }
        }

        .typing-container {
            font-family:
                "Fira Code",
                monospace;

            color: var(--primary);

            font-size:
                clamp(18px, 2.2vw, 25px);

            min-height: 36px;

            margin-bottom: 24px;
        }

        .cursor {
            display: inline-block;

            width: 2px;
            height: 23px;

            background: var(--primary);

            vertical-align: middle;

            animation:
                blink .7s infinite;
        }

        @keyframes blink {

            50% {
                opacity: 0;
            }
        }

        .hero-description {
            max-width: 700px;

            color: var(--muted);

            font-size: 17px;

            line-height: 1.8;

            margin-bottom: 32px;
        }

        .hero-buttons {
            display: flex;

            gap: 14px;

            flex-wrap: wrap;

            margin-bottom: 28px;
        }

        .btn {
            display: inline-flex;

            align-items: center;

            gap: 10px;

            padding:
                13px 21px;

            border-radius: 10px;

            font-size: 14px;

            font-weight: 600;

            transition: .3s;
        }

        .btn-primary {
            background: var(--gradient);

            background-size: 200%;

            color: white;

            box-shadow:
                0 12px 35px rgba(0,229,255,.15);
        }

        .btn-primary:hover {
            transform: translateY(-3px);

            box-shadow:
                0 18px 40px rgba(0,229,255,.25);
        }

        .btn-outline {
            border:
                1px solid var(--border);

            background:
                rgba(255,255,255,.035);
        }

        .btn-outline:hover {
            border-color:
                rgba(0,229,255,.4);

            color: var(--primary);

            transform: translateY(-3px);
        }


        /* ============================================================
           HERO TERMINAL CARD
        ============================================================ */

        .terminal {
            background:
                rgba(9, 14, 26, .78);

            border:
                1px solid var(--border);

            border-radius: 18px;

            overflow: hidden;

            box-shadow: var(--shadow);

            animation:
                floating 5s ease-in-out infinite;

            position: relative;
        }

        .terminal::before {
            content: "";

            position: absolute;

            inset: -2px;

            z-index: -1;

            border-radius: inherit;

            background: var(--gradient);

            filter: blur(30px);

            opacity: .12;
        }

        @keyframes floating {

            0%,100% {
                transform:
                    translateY(0px);
            }

            50% {
                transform:
                    translateY(-14px);
            }
        }

        .terminal-header {
            display: flex;

            align-items: center;

            gap: 8px;

            padding:
                15px 18px;

            border-bottom:
                1px solid var(--border);
        }

        .terminal-dot {
            width: 11px;
            height: 11px;

            border-radius: 50%;
        }

        .red {
            background: #ff5f56;
        }

        .yellow {
            background: #ffbd2e;
        }

        .green {
            background: #27c93f;
        }

        .terminal-body {
            padding:
                26px;

            font-family:
                "Fira Code",
                monospace;

            font-size: 13px;

            line-height: 2;
        }

        .term-blue {
            color: var(--primary);
        }

        .term-green {
            color: var(--green);
        }

        .term-purple {
            color: #b388ff;
        }

        .term-muted {
            color: #71809d;
        }


        /* ============================================================
           SECTION TITLES
        ============================================================ */

        .section-label {
            font-family:
                "Fira Code",
                monospace;

            color: var(--primary);

            font-size: 14px;

            margin-bottom: 8px;
        }

        .section-title {
            font-size:
                clamp(33px,4vw,48px);

            letter-spacing: -1.5px;

            margin-bottom: 15px;
        }

        .section-description {
            color: var(--muted);

            line-height: 1.8;

            max-width: 720px;

            margin-bottom: 45px;
        }


        /* ============================================================
           STATS
        ============================================================ */

        .impact-grid {
            display: grid;

            grid-template-columns:
                repeat(4,1fr);

            gap: 20px;
        }

        .impact-card {
            position: relative;

            padding:
                30px 20px;

            text-align: center;

            background: var(--card);

            border:
                1px solid var(--border);

            border-radius: 16px;

            overflow: hidden;

            transition: .35s;
        }

        .impact-card:hover {
            transform:
                translateY(-8px);

            border-color:
                rgba(0,229,255,.35);

            background:
                var(--card-hover);
        }

        .impact-number {
            font-size: 40px;

            font-weight: 800;

            margin-bottom: 8px;

            background: var(--gradient);

            -webkit-background-clip: text;

            color: transparent;
        }

        .impact-card p {
            color: var(--muted);

            font-size: 14px;
        }


        /* ============================================================
           PROJECTS
        ============================================================ */

        .projects-grid {
            display: grid;

            grid-template-columns:
                repeat(2,1fr);

            gap: 26px;
        }

        .project-card {
            background: var(--card);

            border:
                1px solid var(--border);

            border-radius: 20px;

            overflow: hidden;

            transition: .4s;

            position: relative;
        }

        .project-card:hover {
            transform:
                translateY(-10px);

            border-color:
                rgba(0,229,255,.32);

            box-shadow:
                0 25px 60px
                rgba(0,0,0,.35);
        }

        .project-visual {
            min-height: 220px;

            display: flex;

            justify-content: center;
            align-items: center;

            font-size: 70px;

            background:
                radial-gradient(
                    circle,
                    rgba(0,229,255,.17),
                    transparent 60%
                ),
                #090f1b;

            position: relative;
        }

        .project-visual i {
            filter:
                drop-shadow(
                    0 0 25px
                    rgba(0,229,255,.4)
                );
        }

        .project-body {
            padding: 28px;
        }

        .project-number {
            font-family:
                "Fira Code",
                monospace;

            color: var(--primary);

            font-size: 12px;

            margin-bottom: 12px;
        }

        .project-title {
            font-size: 25px;

            margin-bottom: 10px;
        }

        .project-description {
            color: var(--muted);

            line-height: 1.7;

            font-size: 14px;

            margin-bottom: 20px;
        }

        .tags {
            display: flex;

            flex-wrap: wrap;

            gap: 7px;
        }

        .tag {
            font-family:
                "Fira Code",
                monospace;

            font-size: 11px;

            padding:
                6px 10px;

            border-radius: 6px;

            color: #a9dfff;

            background:
                rgba(0,229,255,.07);

            border:
                1px solid
                rgba(0,229,255,.12);
        }


        /* ============================================================
           TECH
        ============================================================ */

        .tech-groups {
            display: grid;

            grid-template-columns:
                repeat(2,1fr);

            gap: 22px;
        }

        .tech-card {
            padding: 28px;

            border:
                1px solid var(--border);

            border-radius: 18px;

            background: var(--card);

            transition: .3s;
        }

        .tech-card:hover {
            border-color:
                rgba(124,77,255,.5);

            transform:
                translateY(-5px);
        }

        .tech-card h3 {
            display: flex;

            align-items: center;

            gap: 10px;

            margin-bottom: 20px;

            font-size: 18px;
        }

        .tech-card h3 i {
            color: var(--primary);
        }

        .skills {
            display: flex;

            flex-wrap: wrap;

            gap: 10px;
        }

        .skill {
            padding:
                9px 12px;

            border-radius: 8px;

            font-size: 12px;

            font-family:
                "Fira Code",
                monospace;

            color: var(--muted);

            background:
                rgba(255,255,255,.035);

            border:
                1px solid var(--border);

            transition: .25s;
        }

        .skill:hover {
            color: var(--primary);

            transform:
                translateY(-3px);

            border-color:
                rgba(0,229,255,.35);
        }


        /* ============================================================
           WORK
        ============================================================ */

        .timeline {
            position: relative;

            padding-left: 35px;
        }

        .timeline::before {
            content: "";

            position: absolute;

            left: 7px;
            top: 0;
            bottom: 0;

            width: 2px;

            background:
                linear-gradient(
                    var(--primary),
                    var(--secondary),
                    transparent
                );
        }

        .timeline-item {
            position: relative;

            padding:
                0 0 45px 24px;
        }

        .timeline-dot {
            position: absolute;

            width: 15px;
            height: 15px;

            border-radius: 50%;

            background: var(--primary);

            left: -35px;
            top: 5px;

            box-shadow:
                0 0 18px var(--primary);
        }

        .timeline-date {
            color: var(--primary);

            font-family:
                "Fira Code",
                monospace;

            font-size: 12px;

            margin-bottom: 8px;
        }

        .timeline-item h3 {
            font-size: 23px;

            margin-bottom: 5px;
        }

        .timeline-item h4 {
            color: #b3c3dd;

            font-weight: 500;

            margin-bottom: 16px;
        }

        .timeline-item ul {
            padding-left: 20px;

            color: var(--muted);

            line-height: 1.8;
        }


        /* ============================================================
           GITHUB
        ============================================================ */

        .github-images {
            display: grid;

            grid-template-columns:
                repeat(2,1fr);

            gap: 20px;

            margin-bottom: 24px;
        }

        .github-image {
            background:
                rgba(255,255,255,.02);

            border:
                1px solid var(--border);

            border-radius: 14px;

            padding: 10px;

            overflow: hidden;
        }

        .github-image img {
            width: 100%;
        }

        .contribution {
            text-align: center;

            background: var(--card);

            border:
                1px solid var(--border);

            border-radius: 18px;

            padding: 20px;

            overflow-x: auto;
        }


        /* ============================================================
           CURRENTLY
        ============================================================ */

        .now-grid {
            display: grid;

            grid-template-columns:
                repeat(3,1fr);

            gap: 20px;
        }

        .now-card {
            padding: 28px;

            background: var(--card);

            border:
                1px solid var(--border);

            border-radius: 17px;

            transition: .3s;
        }

        .now-card:hover {
            transform:
                translateY(-5px);
        }

        .now-icon {
            font-size: 24px;

            color: var(--primary);

            margin-bottom: 18px;
        }

        .now-card h3 {
            margin-bottom: 9px;
        }

        .now-card p {
            color: var(--muted);

            line-height: 1.7;

            font-size: 14px;
        }


        /* ============================================================
           ACHIEVEMENTS
        ============================================================ */

        .achievement-grid {
            display: grid;

            grid-template-columns:
                repeat(4,1fr);

            gap: 20px;
        }

        .achievement {
            text-align: center;

            padding: 25px 15px;

            background: var(--card);

            border:
                1px solid var(--border);

            border-radius: 17px;

            transition: .3s;
        }

        .achievement:hover {
            transform:
                translateY(-8px)
                scale(1.02);
        }

        .achievement img {
            width: 85px;

            margin-bottom: 13px;
        }

        .achievement h3 {
            font-size: 15px;
        }


        /* ============================================================
           CONNECT
        ============================================================ */

        .connect-box {
            border:
                1px solid var(--border);

            border-radius: 24px;

            background:
                linear-gradient(
                    140deg,
                    rgba(0,229,255,.08),
                    rgba(124,77,255,.06),
                    rgba(255,64,129,.05)
                );

            padding:
                55px;

            display: grid;

            grid-template-columns:
                1fr auto;

            align-items: center;

            gap: 35px;
        }

        .connect-box h2 {
            font-size:
                clamp(32px,4vw,48px);

            margin-bottom: 14px;
        }

        .connect-box p {
            color: var(--muted);

            line-height: 1.7;

            max-width: 650px;
        }

        .socials {
            display: flex;

            gap: 12px;

            flex-wrap: wrap;

            margin-top: 25px;
        }

        .social {
            width: 45px;
            height: 45px;

            display: flex;

            justify-content: center;
            align-items: center;

            border-radius: 10px;

            background:
                rgba(255,255,255,.05);

            border:
                1px solid var(--border);

            transition: .3s;
        }

        .social:hover {
            color: var(--primary);

            border-color:
                var(--primary);

            transform:
                translateY(-4px);
        }

        .qr {
            background: white;

            padding: 10px;

            border-radius: 14px;

            width: 150px;
        }


        /* ============================================================
           FOOTER
        ============================================================ */

        footer {
            position: relative;

            padding:
                80px 0 35px;

            text-align: center;

            overflow: hidden;

            color: var(--muted);
        }

        .wave {
            position: absolute;

            top: 0;
            left: 0;

            width: 200%;
            height: 55px;

            background:
                linear-gradient(
                    90deg,
                    transparent,
                    rgba(0,229,255,.17),
                    rgba(124,77,255,.18),
                    transparent
                );

            clip-path:
                polygon(
                    0 40%,
                    10% 60%,
                    20% 35%,
                    30% 65%,
                    40% 30%,
                    50% 60%,
                    60% 35%,
                    70% 65%,
                    80% 30%,
                    90% 55%,
                    100% 35%,
                    100% 100%,
                    0 100%
                );

            animation:
                waveMove 12s linear infinite;
        }

        @keyframes waveMove {

            from {
                transform:
                    translateX(0);
            }

            to {
                transform:
                    translateX(-50%);
            }
        }

        footer strong {
            color: white;
        }


        /* ============================================================
           REVEAL ANIMATIONS
        ============================================================ */

        .reveal {
            opacity: 0;

            transform:
                translateY(35px);

            transition:
                .8s cubic-bezier(.2,.7,.2,1);
        }

        .reveal.active {
            opacity: 1;

            transform:
                translateY(0);
        }


        /* ============================================================
           MOBILE
        ============================================================ */

        @media (max-width: 900px) {

            .hero-grid {
                grid-template-columns: 1fr;
            }

            .terminal {
                max-width: 620px;
            }

            .impact-grid {
                grid-template-columns:
                    repeat(2,1fr);
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .tech-groups {
                grid-template-columns: 1fr;
            }

            .github-images {
                grid-template-columns: 1fr;
            }

            .now-grid {
                grid-template-columns: 1fr;
            }

            .achievement-grid {
                grid-template-columns:
                    repeat(2,1fr);
            }

            .connect-box {
                grid-template-columns: 1fr;
            }

            .qr {
                width: 130px;
            }
        }

        @media (max-width: 600px) {

            section {
                padding: 65px 0;
            }

            .nav-links {
                display: none;
            }

            .hero h1 {
                letter-spacing: -2px;
            }

            .impact-grid {
                grid-template-columns: 1fr;
            }

            .achievement-grid {
                grid-template-columns:
                    repeat(2,1fr);
            }

            .connect-box {
                padding: 30px 22px;
            }
        }

    </style>
</head>


<body>

    <!-- ============================================================
         BACKGROUND PARTICLES
    ============================================================ -->

    <div id="particles"></div>


    <!-- ============================================================
         NAVBAR
    ============================================================ -->

    <nav>

        <div class="container nav-inner">

            <a
                href="#home"
                class="logo"
            >
                &lt;Srimanth /&gt;
            </a>

            <div class="nav-links">

                <a href="#about">
                    About
                </a>

                <a href="#projects">
                    Projects
                </a>

                <a href="#skills">
                    Arsenal
                </a>

                <a href="#github">
                    GitHub
                </a>

                <a href="#contact">
                    Contact
                </a>

            </div>

        </div>

    </nav>


    <!-- ============================================================
         HERO
    ============================================================ -->

    <section
        class="hero"
        id="home"
    >

        <div class="container hero-grid">

            <div>

                <div class="status">

                    <span class="status-dot"></span>

                    Open to Android / Kotlin opportunities

                </div>


                <h1>

                    Hi, I'm

                    <span class="gradient-text">
                        Srimanth.
                    </span>

                </h1>


                <div class="typing-container">

                    <span id="typing"></span>

                    <span class="cursor"></span>

                </div>


                <p class="hero-description">

                    Android Engineer building scalable,
                    production-ready applications using
                    Kotlin, Jetpack Compose and modern
                    architecture.

                    I work at the intersection of
                    Android, AI, Fintech, POS systems
                    and Kotlin Multiplatform.

                </p>


                <div class="hero-buttons">

                    <a
                        href="#projects"
                        class="btn btn-primary"
                    >
                        <i class="fa-solid fa-code"></i>

                        Explore My Work
                    </a>


                    <a
                        href="https://github.com/vasireddysrimanth"
                        target="_blank"
                        class="btn btn-outline"
                    >
                        <i class="fa-brands fa-github"></i>

                        GitHub
                    </a>


                    <a
                        href="https://www.linkedin.com/in/vasireddy-srimanth"
                        target="_blank"
                        class="btn btn-outline"
                    >
                        <i class="fa-brands fa-linkedin"></i>

                        LinkedIn
                    </a>

                </div>

            </div>


            <!-- TERMINAL -->

            <div class="terminal">

                <div class="terminal-header">

                    <span class="terminal-dot red"></span>

                    <span class="terminal-dot yellow"></span>

                    <span class="terminal-dot green"></span>

                </div>


                <div class="terminal-body">

                    <div>
                        <span class="term-green">
                            srimanth@android
                        </span>

                        <span class="term-muted">
                            :~$
                        </span>

                        whoami
                    </div>


                    <div>
                        <span class="term-blue">
                            Android Engineer
                        </span>
                    </div>


                    <br>


                    <div>
                        <span class="term-green">
                            srimanth@android
                        </span>

                        <span class="term-muted">
                            :~$
                        </span>

                        cat stack.json
                    </div>


                    <div class="term-purple">
                        {
                    </div>

                    <div>
                        &nbsp;&nbsp;"language":
                        <span class="term-green">
                            "Kotlin"
                        </span>,
                    </div>

                    <div>
                        &nbsp;&nbsp;"ui":
                        <span class="term-green">
                            "Jetpack Compose"
                        </span>,
                    </div>

                    <div>
                        &nbsp;&nbsp;"architecture":
                        <span class="term-green">
                            "Clean + MVVM"
                        </span>,
                    </div>

                    <div>
                        &nbsp;&nbsp;"ai":
                        <span class="term-green">
                            "Gemini + ML Kit"
                        </span>,
                    </div>

                    <div>
                        &nbsp;&nbsp;"domain":
                        <span class="term-green">
                            "Fintech / POS"
                        </span>,
                    </div>

                    <div>
                        &nbsp;&nbsp;"multiplatform":
                        <span class="term-green">
                            true
                        </span>
                    </div>

                    <div class="term-purple">
                        }
                    </div>


                    <br>


                    <div>
                        <span class="term-green">
                            srimanth@android
                        </span>

                        <span class="term-muted">
                            :~$
                        </span>

                        <span id="terminal-command">
                            build --future
                        </span>
                    </div>

                </div>

            </div>

        </div>

    </section>


    <!-- ============================================================
         IMPACT
    ============================================================ -->

    <section id="about">

        <div class="container">

            <div class="reveal">

                <div class="section-label">
                    &lt;impact /&gt;
                </div>

                <h2 class="section-title">
                    Engineering with measurable impact.
                </h2>

                <p class="section-description">

                    I focus on performance, reliability,
                    offline-first architecture and
                    production-quality Android engineering.

                </p>

            </div>


            <div class="impact-grid">

                <div class="impact-card reveal">

                    <div
                        class="impact-number counter"
                        data-target="40"
                    >
                        0
                    </div>

                    <p>
                        % Crash Rate Reduction
                    </p>

                </div>


                <div class="impact-card reveal">

                    <div
                        class="impact-number counter"
                        data-target="45"
                    >
                        0
                    </div>

                    <p>
                        % ANR Reduction
                    </p>

                </div>


                <div class="impact-card reveal">

                    <div
                        class="impact-number counter"
                        data-target="60"
                    >
                        0
                    </div>

                    <p>
                        % API Calls Reduced
                    </p>

                </div>


                <div class="impact-card reveal">

                    <div class="impact-number">
                        3+
                    </div>

                    <p>
                        Engineering Domains
                    </p>

                </div>

            </div>

        </div>

    </section>


    <!-- ============================================================
         EXPERIENCE
    ============================================================ -->

    <section>

        <div class="container">

            <div class="reveal">

                <div class="section-label">
                    &lt;experience /&gt;
                </div>

                <h2 class="section-title">
                    Building real-world fintech systems.
                </h2>

            </div>


            <div class="timeline reveal">

                <div class="timeline-item">

                    <div class="timeline-dot"></div>

                    <div class="timeline-date">
                        OCT 2024 — PRESENT
                    </div>

                    <h3>
                        Android Developer
                    </h3>

                    <h4>
                        ONEHUBPOS · Bengaluru, India
                    </h4>


                    <ul>

                        <li>
                            Developing enterprise-level POS
                            and fintech Android applications.
                        </li>

                        <li>
                            Integrating Dejavoo, PAX and
                            PhonePe payment systems.
                        </li>

                        <li>
                            Working with end-to-end transaction
                            workflows and POS hardware.
                        </li>

                        <li>
                            Designed offline-first architecture
                            using Room, Coroutines, Flow and
                            WorkManager.
                        </li>

                        <li>
                            Migrated application UI from
                            XML layouts to Jetpack Compose.
                        </li>

                        <li>
                            Reduced crash rates by 40% and
                            ANRs by 45% through performance
                            profiling and structured concurrency.
                        </li>

                    </ul>

                </div>

            </div>

        </div>

    </section>


    <!-- ============================================================
         PROJECTS
    ============================================================ -->

    <section id="projects">

        <div class="container">

            <div class="reveal">

                <div class="section-label">
                    &lt;featured_projects /&gt;
                </div>

                <h2 class="section-title">
                    Things I've built.
                </h2>

                <p class="section-description">

                    Android applications combining modern
                    architecture, AI, offline-first data,
                    backend systems and multiplatform
                    development.

                </p>

            </div>


            <div class="projects-grid">


                <!-- StudyGem -->

                <article class="project-card reveal">

                    <div class="project-visual">

                        <i class="fa-solid fa-brain"></i>

                    </div>


                    <div class="project-body">

                        <div class="project-number">
                            PROJECT_01
                        </div>

                        <h3 class="project-title">
                            StudyGem
                        </h3>

                        <p class="project-description">

                            AI-powered textbook study assistant
                            that scans pages using CameraX,
                            extracts text using on-device ML Kit
                            OCR and generates summaries,
                            quizzes and difficulty analysis
                            using Gemini AI.

                        </p>

                        <div class="tags">

                            <span class="tag">
                                Kotlin
                            </span>

                            <span class="tag">
                                Compose
                            </span>

                            <span class="tag">
                                CameraX
                            </span>

                            <span class="tag">
                                ML Kit
                            </span>

                            <span class="tag">
                                Gemini AI
                            </span>

                            <span class="tag">
                                Room
                            </span>

                        </div>

                    </div>

                </article>


                <!-- Store App -->

                <article class="project-card reveal">

                    <div class="project-visual">

                        <i class="fa-solid fa-cart-shopping"></i>

                    </div>


                    <div class="project-body">

                        <div class="project-number">
                            PROJECT_02
                        </div>

                        <h3 class="project-title">
                            StoreApp
                        </h3>

                        <p class="project-description">

                            Production-grade e-commerce Android
                            application built using Clean
                            Architecture, Room, Retrofit,
                            Firebase, Paging 3 and WorkManager
                            with offline-first intelligent caching.

                        </p>

                        <div class="tags">

                            <span class="tag">
                                Kotlin
                            </span>

                            <span class="tag">
                                MVVM
                            </span>

                            <span class="tag">
                                Room
                            </span>

                            <span class="tag">
                                Retrofit
                            </span>

                            <span class="tag">
                                Firebase
                            </span>

                            <span class="tag">
                                Paging 3
                            </span>

                        </div>

                    </div>

                </article>


                <!-- Travel -->

                <article class="project-card reveal">

                    <div class="project-visual">

                        <i class="fa-solid fa-plane"></i>

                    </div>


                    <div class="project-body">

                        <div class="project-number">
                            PROJECT_03
                        </div>

                        <h3 class="project-title">
                            Travel Marketplace
                        </h3>

                        <p class="project-description">

                            Full-stack travel marketplace
                            sharing domain and data layers
                            using Kotlin Multiplatform with
                            Compose Multiplatform and Ktor
                            backend APIs.

                        </p>

                        <div class="tags">

                            <span class="tag">
                                KMP
                            </span>

                            <span class="tag">
                                Compose Multiplatform
                            </span>

                            <span class="tag">
                                Ktor
                            </span>

                            <span class="tag">
                                MySQL
                            </span>

                            <span class="tag">
                                Koin
                            </span>

                            <span class="tag">
                                JWT
                            </span>

                        </div>

                    </div>

                </article>


                <!-- POS -->

                <article class="project-card reveal">

                    <div class="project-visual">

                        <i class="fa-solid fa-credit-card"></i>

                    </div>


                    <div class="project-body">

                        <div class="project-number">
                            PROFESSIONAL_WORK
                        </div>

                        <h3 class="project-title">
                            Enterprise POS Systems
                        </h3>

                        <p class="project-description">

                            Production Android POS applications
                            working with real-world payment
                            transactions, hardware communication,
                            Dejavoo terminals, PAX devices and
                            PhonePe payment integrations.

                        </p>

                        <div class="tags">

                            <span class="tag">
                                Fintech
                            </span>

                            <span class="tag">
                                PAX
                            </span>

                            <span class="tag">
                                Dejavoo
                            </span>

                            <span class="tag">
                                PhonePe
                            </span>

                            <span class="tag">
                                Offline-first
                            </span>

                            <span class="tag">
                                Compose
                            </span>

                        </div>

                    </div>

                </article>

            </div>

        </div>

    </section>


    <!-- ============================================================
         TECH ARSENAL
    ============================================================ -->

    <section id="skills">

        <div class="container">

            <div class="reveal">

                <div class="section-label">
                    &lt;tech_arsenal /&gt;
                </div>

                <h2 class="section-title">
                    Tools I use to build.
                </h2>

            </div>


            <div class="tech-groups">


                <div class="tech-card reveal">

                    <h3>
                        <i class="fa-brands fa-android"></i>
                        Android
                    </h3>

                    <div class="skills">

                        <span class="skill">Kotlin</span>
                        <span class="skill">Java</span>
                        <span class="skill">Jetpack Compose</span>
                        <span class="skill">MVVM</span>
                        <span class="skill">Clean Architecture</span>
                        <span class="skill">Coroutines</span>
                        <span class="skill">Flow</span>
                        <span class="skill">Hilt</span>
                        <span class="skill">Room</span>
                        <span class="skill">Retrofit</span>
                        <span class="skill">Paging 3</span>
                        <span class="skill">WorkManager</span>
                        <span class="skill">DataStore</span>

                    </div>

                </div>


                <div class="tech-card reveal">

                    <h3>
                        <i class="fa-solid fa-robot"></i>
                        AI / ML
                    </h3>

                    <div class="skills">

                        <span class="skill">Gemini AI</span>
                        <span class="skill">ML Kit</span>
                        <span class="skill">OCR</span>
                        <span class="skill">Firebase AI Logic</span>
                        <span class="skill">Vertex AI</span>
                        <span class="skill">LLM APIs</span>
                        <span class="skill">Streaming Responses</span>
                        <span class="skill">Python</span>

                    </div>

                </div>


                <div class="tech-card reveal">

                    <h3>
                        <i class="fa-solid fa-code-branch"></i>
                        Multiplatform / Backend
                    </h3>

                    <div class="skills">

                        <span class="skill">Kotlin Multiplatform</span>
                        <span class="skill">Compose Multiplatform</span>
                        <span class="skill">Ktor Client</span>
                        <span class="skill">Ktor Server</span>
                        <span class="skill">REST APIs</span>
                        <span class="skill">JWT</span>
                        <span class="skill">MySQL</span>
                        <span class="skill">SQL</span>
                        <span class="skill">Firebase</span>

                    </div>

                </div>


                <div class="tech-card reveal">

                    <h3>
                        <i class="fa-solid fa-flask"></i>
                        Testing / DevOps
                    </h3>

                    <div class="skills">

                        <span class="skill">JUnit 5</span>
                        <span class="skill">Espresso</span>
                        <span class="skill">Mockito</span>
                        <span class="skill">Turbine</span>
                        <span class="skill">Crashlytics</span>
                        <span class="skill">LeakCanary</span>
                        <span class="skill">Git</span>
                        <span class="skill">GitHub Actions</span>
                        <span class="skill">CI/CD</span>

                    </div>

                </div>

            </div>

        </div>

    </section>


    <!-- ============================================================
         CURRENT
    ============================================================ -->

    <section>

        <div class="container">

            <div class="reveal">

                <div class="section-label">
                    &lt;currently /&gt;
                </div>

                <h2 class="section-title">
                    What I'm up to.
                </h2>

            </div>


            <div class="now-grid">

                <div class="now-card reveal">

                    <div class="now-icon">
                        <i class="fa-solid fa-hammer"></i>
                    </div>

                    <h3>
                        Building
                    </h3>

                    <p>
                        AI-powered Android experiences,
                        scalable Compose applications and
                        production-grade mobile architecture.
                    </p>

                </div>


                <div class="now-card reveal">

                    <div class="now-icon">
                        <i class="fa-solid fa-book-open"></i>
                    </div>

                    <h3>
                        Learning
                    </h3>

                    <p>
                        Kotlin Multiplatform,
                        Compose Multiplatform,
                        on-device AI and advanced
                        LLM integrations.
                    </p>

                </div>


                <div class="now-card reveal">

                    <div class="now-icon">
                        <i class="fa-solid fa-bolt"></i>
                    </div>

                    <h3>
                        Exploring
                    </h3>

                    <p>
                        How AI can transform retail,
                        POS systems, developer productivity
                        and mobile user experiences.
                    </p>

                </div>

            </div>

        </div>

    </section>


    <!-- ============================================================
         GITHUB
    ============================================================ -->

    <section id="github">

        <div class="container">

            <div class="reveal">

                <div class="section-label">
                    &lt;github_activity /&gt;
                </div>

                <h2 class="section-title">
                    Code. Commit. Improve.
                </h2>

            </div>


            <div class="github-images reveal">

                <div class="github-image">

                    <img
                        src="https://github-readme-stats.vercel.app/api?username=vasireddysrimanth&show_icons=true&theme=tokyonight&hide_border=true&bg_color=00000000"
                        alt="Srimanth GitHub Stats"
                    >

                </div>


                <div class="github-image">

                    <img
                        src="https://github-readme-stats.vercel.app/api/top-langs/?username=vasireddysrimanth&layout=compact&theme=tokyonight&hide_border=true&bg_color=00000000"
                        alt="Top Languages"
                    >

                </div>

            </div>


            <div class="contribution reveal">

                <img
                    src="https://ghchart.rshah.org/00e5ff/vasireddysrimanth"
                    alt="Srimanth Vasireddy GitHub Contribution Chart"
                >

            </div>

        </div>

    </section>


    <!-- ============================================================
         ACHIEVEMENTS
    ============================================================ -->

    <section>

        <div class="container">

            <div class="reveal">

                <div class="section-label">
                    &lt;achievements /&gt;
                </div>

                <h2 class="section-title">
                    GitHub achievements.
                </h2>

                <p class="section-description">
                    Display these only if the corresponding
                    achievement exists on your GitHub profile.
                </p>

            </div>


            <div class="achievement-grid">

                <div class="achievement reveal">

                    <img
                        src="https://github.githubassets.com/images/modules/profile/achievements/pull-shark-default.png"
                        alt="Pull Shark"
                    >

                    <h3>
                        Pull Shark
                    </h3>

                </div>


                <div class="achievement reveal">

                    <img
                        src="https://github.githubassets.com/images/modules/profile/achievements/pair-extraordinaire-default.png"
                        alt="Pair Extraordinaire"
                    >

                    <h3>
                        Pair Extraordinaire
                    </h3>

                </div>


                <div class="achievement reveal">

                    <img
                        src="https://github.githubassets.com/images/modules/profile/achievements/yolo-default.png"
                        alt="YOLO"
                    >

                    <h3>
                        YOLO
                    </h3>

                </div>


                <div class="achievement reveal">

                    <img
                        src="https://github.githubassets.com/images/modules/profile/achievements/starstruck-default.png"
                        alt="Starstruck"
                    >

                    <h3>
                        Starstruck
                    </h3>

                </div>

            </div>

        </div>

    </section>


    <!-- ============================================================
         EDUCATION / OTHER
    ============================================================ -->

    <section>

        <div class="container">

            <div class="reveal">

                <div class="section-label">
                    &lt;beyond_code /&gt;
                </div>

                <h2 class="section-title">
                    Beyond engineering.
                </h2>

            </div>


            <div class="projects-grid">


                <div class="tech-card reveal">

                    <h3>
                        🎓 Education
                    </h3>

                    <p
                        style="
                            color:var(--muted);
                            line-height:1.8;
                        "
                    >
                        B.Tech in Computer Science
                        and Engineering

                        <br><br>

                        <strong style="color:white">
                            Bharat Institute of Engineering
                            and Technology
                        </strong>
                    </p>

                </div>


                <div class="tech-card reveal">

                    <h3>
                        🏆 UDGAM IIT Guwahati
                    </h3>

                    <p
                        style="
                            color:var(--muted);
                            line-height:1.8;
                        "
                    >
                        Ranked among the
                        <strong style="color:white">
                            Top 15 Campus Ambassadors
                            nationwide
                        </strong>,

                        contributing to campus outreach
                        and startup-student engagement
                        initiatives.
                    </p>

                </div>

            </div>

        </div>

    </section>


    <!-- ============================================================
         CONTACT
    ============================================================ -->

    <section id="contact">

        <div class="container">

            <div class="connect-box reveal">

                <div>

                    <div class="section-label">
                        &lt;connect /&gt;
                    </div>

                    <h2>
                        Let's build something
                        <span class="gradient-text">
                            impactful.
                        </span>
                    </h2>


                    <p>

                        Interested in Android,
                        Kotlin Multiplatform,
                        AI-powered applications,
                        fintech systems or building
                        something meaningful?

                        Let's connect.

                    </p>


                    <div class="socials">

                        <a
                            href="https://github.com/vasireddysrimanth"
                            target="_blank"
                            class="social"
                            aria-label="GitHub"
                        >
                            <i class="fa-brands fa-github"></i>
                        </a>


                        <a
                            href="https://www.linkedin.com/in/vasireddy-srimanth"
                            target="_blank"
                            class="social"
                            aria-label="LinkedIn"
                        >
                            <i class="fa-brands fa-linkedin-in"></i>
                        </a>


                        <a
                            href="mailto:vasireddysrimanth49@gmail.com"
                            class="social"
                            aria-label="Email"
                        >
                            <i class="fa-solid fa-envelope"></i>
                        </a>

                    </div>

                </div>


                <!-- Dynamic QR -->

                <div>

                    <img
                        id="qrCode"
                        class="qr"
                        alt="Portfolio QR Code"
                    >

                </div>

            </div>

        </div>

    </section>


    <!-- ============================================================
         FOOTER
    ============================================================ -->

    <footer>

        <div class="wave"></div>

        <div class="container">

            <p>
                Designed & built by
                <strong>
                    Srimanth Vasireddy
                </strong>
            </p>

            <p
                style="
                    margin-top:10px;
                    font-family:'Fira Code',monospace;
                    font-size:12px;
                "
            >
                Android × AI × Fintech × Kotlin
            </p>

        </div>

    </footer>


    <!-- ============================================================
         JAVASCRIPT
    ============================================================ -->

    <script>

        /* ==========================================================
           TYPING ANIMATION
        ========================================================== */

        const typingElement =
            document.getElementById("typing");


        const phrases = [

            "Android Engineer.",

            "Kotlin & Jetpack Compose Developer.",

            "AI-powered Mobile Developer.",

            "Fintech & POS Engineer.",

            "Kotlin Multiplatform Explorer.",

            "Building scalable mobile experiences."

        ];


        let phraseIndex = 0;
        let letterIndex = 0;

        let deleting = false;


        function typeText() {

            const current =
                phrases[phraseIndex];


            if (!deleting) {

                typingElement.textContent =
                    current.substring(
                        0,
                        letterIndex + 1
                    );

                letterIndex++;


                if (
                    letterIndex ===
                    current.length
                ) {

                    deleting = true;

                    setTimeout(
                        typeText,
                        1700
                    );

                    return;

                }

            } else {

                typingElement.textContent =
                    current.substring(
                        0,
                        letterIndex - 1
                    );

                letterIndex--;


                if (
                    letterIndex === 0
                ) {

                    deleting = false;

                    phraseIndex =
                        (
                            phraseIndex + 1
                        ) %
                        phrases.length;

                }

            }


            setTimeout(
                typeText,
                deleting
                    ? 35
                    : 70
            );

        }


        typeText();



        /* ==========================================================
           BACKGROUND PARTICLES
        ========================================================== */

        const particleContainer =
            document.getElementById(
                "particles"
            );


        function createParticles() {

            const count = 45;


            for (
                let i = 0;
                i < count;
                i++
            ) {

                const particle =
                    document.createElement(
                        "span"
                    );


                particle.classList.add(
                    "particle"
                );


                particle.style.left =
                    Math.random() *
                    100 +
                    "%";


                particle.style.animationDuration =
                    (
                        Math.random() *
                        10 +
                        10
                    ) +
                    "s";


                particle.style.animationDelay =
                    (
                        Math.random() *
                        -20
                    ) +
                    "s";


                const size =
                    Math.random() *
                    3 +
                    1;


                particle.style.width =
                    size +
                    "px";


                particle.style.height =
                    size +
                    "px";


                particleContainer.appendChild(
                    particle
                );

            }

        }


        createParticles();



        /* ==========================================================
           SCROLL REVEAL
        ========================================================== */

        const revealElements =
            document.querySelectorAll(
                ".reveal"
            );


        const revealObserver =
            new IntersectionObserver(

                entries => {

                    entries.forEach(
                        entry => {

                            if (
                                entry.isIntersecting
                            ) {

                                entry.target
                                    .classList
                                    .add(
                                        "active"
                                    );

                            }

                        }
                    );

                },

                {
                    threshold: 0.12
                }

            );


        revealElements.forEach(
            element =>
                revealObserver.observe(
                    element
                )
        );



        /* ==========================================================
           COUNTER ANIMATION
        ========================================================== */

        const counters =
            document.querySelectorAll(
                ".counter"
            );


        const counterObserver =
            new IntersectionObserver(

                entries => {

                    entries.forEach(
                        entry => {

                            if (
                                !entry.isIntersecting
                            )
                                return;


                            const element =
                                entry.target;


                            const target =
                                Number(
                                    element.dataset.target
                                );


                            let current = 0;


                            const increment =
                                Math.max(
                                    1,
                                    Math.ceil(
                                        target /
                                        40
                                    )
                                );


                            const update =
                                setInterval(
                                    () => {

                                        current +=
                                            increment;


                                        if (
                                            current >=
                                            target
                                        ) {

                                            current =
                                                target;

                                            clearInterval(
                                                update
                                            );

                                        }


                                        element.textContent =
                                            current +
                                            "%";

                                    },
                                    35
                                );


                            counterObserver
                                .unobserve(
                                    element
                                );

                        }
                    );

                },

                {
                    threshold: .7
                }

            );


        counters.forEach(
            counter =>
                counterObserver.observe(
                    counter
                )
        );



        /* ==========================================================
           QR CODE GENERATOR
        ========================================================== */

        /*
            Replace this URL with your deployed
            GitHub Pages or portfolio URL.
        */

        const portfolioUrl =
            "https://github.com/vasireddysrimanth";


        const qrCode =
            document.getElementById(
                "qrCode"
            );


        qrCode.src =
            "https://api.qrserver.com/v1/create-qr-code/" +
            "?size=220x220" +
            "&data=" +
            encodeURIComponent(
                portfolioUrl
            );



        /* ==========================================================
           TERMINAL COMMAND ANIMATION
        ========================================================== */

        const terminalCommand =
            document.getElementById(
                "terminal-command"
            );


        const commands = [

            "build --future",

            "compose --everything",

            "ai --integrate",

            "performance --optimize",

            "kotlin --multiplatform",

            "ship --production"

        ];


        let commandIndex = 0;


        setInterval(
            () => {

                commandIndex =
                    (
                        commandIndex + 1
                    ) %
                    commands.length;


                terminalCommand
                    .style
                    .opacity = 0;


                setTimeout(
                    () => {

                        terminalCommand
                            .textContent =
                            commands[
                                commandIndex
                            ];


                        terminalCommand
                            .style
                            .opacity = 1;

                    },
                    250
                );

            },
            2300
        );



        /* ==========================================================
           NAVBAR BACKGROUND ON SCROLL
        ========================================================== */

        window.addEventListener(
            "scroll",
            () => {

                const nav =
                    document.querySelector(
                        "nav"
                    );


                if (
                    window.scrollY > 50
                ) {

                    nav.style.background =
                        "rgba(5,8,16,.92)";

                } else {

                    nav.style.background =
                        "rgba(5,8,16,.65)";

                }

            }
        );



        /* ==========================================================
           CONSOLE EASTER EGG
        ========================================================== */

        console.log(
            "%cSrimanth Vasireddy",
            "font-size:25px;font-weight:bold;color:#00e5ff"
        );


        console.log(
            "%cAndroid × AI × Fintech × Kotlin",
            "font-size:14px;color:#b388ff"
        );


        console.log(
            "Thanks for checking out my portfolio 🚀"
        );

    </script>

</body>
</html>
