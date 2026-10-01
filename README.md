# TeachersDayCard
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Teacher's Day | Sir Randy Bello</title>

</head>

<body>
<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}


/* =========================
   VARIABLES
========================= */

:root {

    --red: #ff4655;
    --dark-red: #a90015;

    --black: #07090d;
    --dark: #0c0f15;
    --panel: #11151d;

    --white: #f4f4f4;
    --gray: #969ba7;

}


/* =========================
   BODY
========================= */

body {

    min-height: 100vh;

    background:
        radial-gradient(
            circle at 75% 35%,
            rgba(255, 70, 85, 0.12),
            transparent 30%
        ),

        radial-gradient(
            circle at 20% 80%,
            rgba(255, 70, 85, 0.08),
            transparent 30%
        ),

        var(--black);

    color: var(--white);

    font-family:
        Arial,
        Helvetica,
        sans-serif;

    overflow-x: hidden;

}


/* =========================
   GRID
========================= */

.grid {

    position: fixed;

    inset: 0;

    z-index: -5;

    opacity: 0.25;

    background-image:

        linear-gradient(
            rgba(255,255,255,0.035) 1px,
            transparent 1px
        ),

        linear-gradient(
            90deg,
            rgba(255,255,255,0.035) 1px,
            transparent 1px
        );

    background-size: 50px 50px;

}


/* =========================
   SCANLINES
========================= */

.scanlines {

    position: fixed;

    inset: 0;

    pointer-events: none;

    z-index: 50;

    opacity: 0.04;

    background:

        repeating-linear-gradient(
            to bottom,
            transparent 0px,
            transparent 3px,
            white 4px
        );

}


/* =========================
   PARTICLES
========================= */

#particles {

    position: fixed;

    inset: 0;

    pointer-events: none;

    overflow: hidden;

    z-index: -1;

}


.particle {

    position: absolute;

    width: 3px;

    height: 3px;

    background: var(--red);

    transform: rotate(45deg);

    opacity: 0.5;

    animation: floating linear infinite;

}


@keyframes floating {

    from {

        transform:
            translateY(110vh)
            rotate(45deg);

    }

    to {

        transform:
            translateY(-10vh)
            rotate(405deg);

    }

}


/* =========================
   MAIN CONTAINER
========================= */

.container {

    width: 90%;

    max-width: 1200px;

    min-height: 100vh;

    margin: auto;

}


/* =========================
   NAVBAR
========================= */

.navbar {

    height: 80px;

    display: flex;

    align-items: center;

    justify-content: space-between;

    border-bottom:
        1px solid
        rgba(255,255,255,0.12);

    animation:
        navbarIn
        0.8s
        ease;

}


@keyframes navbarIn {

    from {

        opacity: 0;

        transform:
            translateY(-20px);

    }

    to {

        opacity: 1;

        transform:
            translateY(0);

    }

}


.logo {

    font-size: 14px;

    font-weight: bold;

    letter-spacing: 2px;

}


.logo span {

    color: var(--red);

    margin-right: 8px;

    text-shadow:
        0 0 15px
        var(--red);

}


.status {

    color: var(--gray);

    font-size: 12px;

    letter-spacing: 2px;

}


.status-dot {

    display: inline-block;

    width: 7px;

    height: 7px;

    margin-right: 7px;

    border-radius: 50%;

    background: #55e69b;

    box-shadow:
        0 0 12px
        #55e69b;

}


/* =========================
   HERO
========================= */

.hero {

    min-height:
        calc(100vh - 80px);

    display: grid;

    grid-template-columns:
        1.1fr
        0.9fr;

    align-items: center;

    gap: 70px;

}


/* =========================
   HERO TEXT
========================= */

.hero-text {

    animation:
        heroIn
        1s
        ease;

}


@keyframes heroIn {

    from {

        opacity: 0;

        transform:
            translateX(-40px);

    }

    to {

        opacity: 1;

        transform:
            translateX(0);

    }

}


.small-title {

    color: var(--red);

    font-size: 13px;

    font-weight: bold;

    letter-spacing: 3px;

    margin-bottom: 20px;

}


h1 {

    font-size:
        clamp(
            55px,
            8vw,
            110px
        );

    line-height: 0.85;

    margin-bottom: 30px;

    font-weight: 900;

    letter-spacing: -4px;

}


h1 span {

    color: transparent;

    -webkit-text-stroke:
        1px
        white;

}


.description {

    max-width: 520px;

    color: var(--gray);

    font-size: 17px;

    line-height: 1.6;

    margin-bottom: 35px;

}


/* =========================
   BUTTON
========================= */

.open-button {

    border: none;

    background: var(--red);

    color: white;

    padding:
        17px
        28px;

    font-weight: bold;

    letter-spacing: 1.5px;

    cursor: pointer;

    display: inline-flex;

    align-items: center;

    gap: 12px;

    clip-path:
        polygon(
            0 0,
            94% 0,
            100% 25%,
            100% 100%,
            6% 100%,
            0 75%
        );

    transition:
        0.25s ease;

}


.open-button:hover {

    transform:
        translateY(-4px);

    box-shadow:
        0 15px 35px
        rgba(255,70,85,0.35);

    background:
        #ff5b68;

}


.open-button:active {

    transform:
        translateY(0);

}


.play-icon {

    font-size: 11px;

}


.hint {

    margin-top: 12px;

    color: #555b67;

    font-size: 10px;

    letter-spacing: 2px;

}


/* =========================
   PHOTO
========================= */

.photo-section {

    display: flex;

    justify-content: center;

    animation:
        photoIn
        1.1s
        0.15s
        ease both;

}


@keyframes photoIn {

    from {

        opacity: 0;

        transform:
            translateX(40px)
            scale(0.95);

    }

    to {

        opacity: 1;

        transform:
            translateX(0)
            scale(1);

    }

}


.photo-frame {

    width:
        min(
            390px,
            80vw
        );

    aspect-ratio:
        4 / 5;

    position: relative;

    padding: 12px;

    background: #11151b;

    border:
        1px solid
        rgba(255,255,255,0.2);

    box-shadow:
        20px
        20px
        0
        rgba(255,70,85,0.08);

}


.photo-frame::before {

    content: "";

    position: absolute;

    inset: -8px;

    border:
        1px solid
        rgba(255,70,85,0.35);

}


.photo-frame img {

    width: 100%;

    height: 100%;

    object-fit: cover;

    display: block;

    filter:
        saturate(0.9)
        contrast(1.08);

}


/* =========================
   PHOTO CORNERS
========================= */

.corner {

    position: absolute;

    width: 28px;

    height: 28px;

    border-color:
        var(--red);

    z-index: 2;

}


.top-left {

    left: -14px;

    top: -14px;

    border-left: 2px solid;

    border-top: 2px solid;

}


.top-right {

    right: -14px;

    top: -14px;

    border-right: 2px solid;

    border-top: 2px solid;

}


.bottom-left {

    left: -14px;

    bottom: -14px;

    border-left: 2px solid;

    border-bottom: 2px solid;

}


.bottom-right {

    right: -14px;

    bottom: -14px;

    border-right: 2px solid;

    border-bottom: 2px solid;

}


/* =========================
   PHOTO LABEL
========================= */

.photo-label {

    position: absolute;

    left: 25px;

    bottom: 25px;

    background:
        rgba(5,7,10,0.9);

    border-left:
        3px solid
        var(--red);

    padding:
        10px
        15px;

    font-size: 13px;

    font-weight: bold;

    letter-spacing: 2px;

}


/* =========================
   PHOTO SCAN
========================= */

.scan {

    position: absolute;

    left: 12px;

    right: 12px;

    top: 10%;

    height: 2px;

    background:
        var(--red);

    box-shadow:
        0 0 15px
        var(--red);

    animation:
        scanAnimation
        4s
        infinite;

}


@keyframes scanAnimation {

    0% {

        top: 10%;

        opacity: 0;

    }

    20% {

        opacity: 1;

    }

    50% {

        top: 90%;

        opacity: 0.8;

    }

    70% {

        opacity: 0;

    }

    100% {

        top: 10%;

        opacity: 0;

    }

}


/* =========================
   LETTER OVERLAY
========================= */

.letter-overlay {

    position: fixed;

    inset: 0;

    z-index: 100;

    display: flex;

    align-items: center;

    justify-content: center;

    padding: 20px;

    background:
        rgba(2,3,6,0.86);

    backdrop-filter:
        blur(12px);

    opacity: 0;

    visibility: hidden;

    transition:
        opacity 0.5s ease,
        visibility 0.5s ease;

}


.letter-overlay.active {

    opacity: 1;

    visibility: visible;

}


/* =========================
   LETTER
========================= */

.letter {

    width:
        min(
            780px,
            100%
        );

    max-height:
        90vh;

    overflow-y: auto;

    background:
        linear-gradient(
            135deg,
            rgba(255,70,85,0.07),
            transparent 30%
        ),
        var(--panel);

    border:
        1px solid
        rgba(255,70,85,0.55);

    box-shadow:

        0 30px 100px
        rgba(0,0,0,0.8),

        0 0 60px
        rgba(255,70,85,0.15);

    transform:
        translateY(50px)
        scale(0.88)
        rotateX(8deg);

    opacity: 0;

    transition:
        transform 0.7s
        cubic-bezier(.2,.8,.2,1),

        opacity 0.5s ease;

}


.letter-overlay.active .letter {

    transform:
        translateY(0)
        scale(1)
        rotateX(0);

    opacity: 1;

}


/* =========================
   CLOSE
========================= */

.close-button {

    position: absolute;

    right: 25px;

    top: 20px;

    width: 40px;

    height: 40px;

    border:
        1px solid
        rgba(255,255,255,0.15);

    background:
        rgba(0,0,0,0.25);

    color: white;

    font-size: 25px;

    cursor: pointer;

    z-index: 5;

    transition:
        0.2s ease;

}


.close-button:hover {

    background:
        var(--red);

    border-color:
        var(--red);

}


/* =========================
   LETTER HEADER
========================= */

.letter-header {

    padding:
        35px
        45px
        28px;

    border-bottom:
        1px solid
        rgba(255,255,255,0.1);

    display: flex;

    justify-content: space-between;

    align-items: center;

}


.letter-tag {

    color:
        var(--red);

    font-size: 11px;

    font-weight: bold;

    letter-spacing: 2px;

    margin-bottom: 10px;

}


.letter-header h2 {

    font-size:
        clamp(
            30px,
            5vw,
            45px
        );

}


/* =========================
   SEAL
========================= */

.thank-you-seal {

    width: 65px;

    height: 65px;

    border:
        1px solid
        var(--red);

    color:
        var(--red);

    display: flex;

    justify-content: center;

    align-items: center;

    flex-direction: column;

    transform:
        rotate(45deg);

}


.thank-you-seal small {

    transform:
        rotate(-45deg);

    color: white;

    font-size: 7px;

    text-align: center;

    letter-spacing: 1px;

}


/* =========================
   LETTER BODY
========================= */

.letter-body {

    padding:
        35px
        45px;

    color:
        #d4d6dc;

    font-size:
        16px;

    line-height:
        1.8;

}


.letter-body p {

    margin-bottom:
        20px;

}


.salutation {

    color: white;

    font-weight: bold;

}


.final-message {

    color: white;

}


.signature {

    color:
        #aeb3bd;

}


/* =========================
   LETTER FOOTER
========================= */

.letter-footer {

    padding:
        18px
        45px;

    border-top:
        1px solid
        rgba(255,255,255,0.1);

    display: flex;

    justify-content:
        space-between;

    align-items: center;

    color:
        var(--red);

    font-size: 11px;

    font-weight: bold;

    letter-spacing: 2px;

}


#readAgain {

    padding:
        9px
        13px;

    background:
        transparent;

    color:
        #aaa;

    border:
        1px solid
        rgba(255,255,255,0.15);

    cursor: pointer;

}


#readAgain:hover {

    color: white;

    border-color:
        var(--red);

}


/* =========================
   MOBILE
========================= */

@media(max-width: 850px) {

    .hero {

        grid-template-columns: 1fr;

        padding:
            60px 0;

        gap: 60px;

    }


    .hero-text {

        text-align: center;

    }


    .description {

        margin-left: auto;

        margin-right: auto;

    }


    .photo-section {

        order: -1;

    }


    .photo-frame {

        width:
            min(
                300px,
                75vw
            );

    }

}


@media(max-width: 550px) {

    .container {

        width: 88%;

    }


    .navbar {

        height: 65px;

    }


    .status {

        display: none;

    }


    h1 {

        font-size: 58px;

    }


    .letter {

        max-height:
            94vh;

    }


    .letter-header {

        padding:
            30px
            25px;

    }


    .letter-body {

        padding:
            30px
            25px;

        font-size:
            15px;

    }


    .letter-footer {

        padding:
            15px
            25px;

    }


    .thank-you-seal {

        width: 48px;

        height: 48px;

    }

}
    </style>

    <!-- Background Effects -->
    <div class="grid"></div>
    <div class="scanlines"></div>

    <div id="particles"></div>

    <!-- Main Website -->
    <div class="container">

        <!-- Navigation -->
        <header class="navbar">

            <div class="logo">
                <span>◆</span>
                TEACHER'S DAY
            </div>

            <div class="status">
                <span class="status-dot"></span>
                MESSAGE READY
            </div>

        </header>


        <!-- Hero Section -->
        <main class="hero">

            <!-- Left Side -->
            <section class="hero-text">

                <p class="small-title">
                    MISSION: APPRECIATION
                </p>

                <h1>
                    HAPPY
                    <br>
                    <span>TEACHER'S DAY</span>
                </h1>

                <p class="description">
                    A special message prepared with respect and
                    gratitude for a teacher who continues to guide,
                    teach, and inspire.
                </p>

                <button class="open-button" id="openLetter">

                    <span class="play-icon">▶</span>

                    OPEN THE LETTER

                </button>

                <p class="hint">
                    CLICK TO DEPLOY MESSAGE
                </p>

            </section>


            <!-- Right Side -->
            <section class="photo-section">

                <div class="photo-frame">

                    <div class="corner top-left"></div>
                    <div class="corner top-right"></div>
                    <div class="corner bottom-left"></div>
                    <div class="corner bottom-right"></div>

                    <img
                        src="images/sir-randy-bello.png"
                        alt="Randy Bello"
                    >

                    <div class="photo-label">
                        SIR RANDY BELLO
                    </div>

                    <div class="scan"></div>

                </div>

            </section>

        </main>

    </div>


    <!-- LETTER -->
    <div class="letter-overlay" id="letterOverlay">

        <div class="letter">

            <!-- Close Button -->
            <button
                class="close-button"
                id="closeLetter"
            >
                ×
            </button>


            <!-- Letter Header -->
            <div class="letter-header">

                <div>

                    <p class="letter-tag">
                        CONFIDENTIAL // TEACHER'S DAY
                    </p>

                    <h2>
                        To Sir Randy Bello
                    </h2>

                </div>


                <div class="thank-you-seal">

                    ◆

                    <small>
                        THANK
                        <br>
                        YOU
                    </small>

                </div>

            </div>


            <!-- Letter Body -->
            <div class="letter-body">

                <p class="salutation">
                    Dear Sir Randy,
                </p>


                <p>
                    Happy Teacher's Day, Sir Randy Bello!
                </p>


                <p>
                    Today, we want to take a moment to thank you
                    for the time, patience, and effort you give to
                    your students. Your lessons are not only about
                    what we learn inside the classroom, but also
                    about the values, discipline, and confidence
                    we carry with us beyond it.
                </p>


                <p>
                    Thank you for sharing your knowledge, for
                    guiding us when things become difficult, and
                    for continuing to encourage us to improve.
                    Every explanation, reminder, and challenge
                    helps us become better students and better
                    people.
                </p>


                <p>
                    Just like a good teammate who stays until
                    the mission is complete, your guidance
                    reminds us to keep moving forward, learn
                    from our mistakes, and never stop trying.
                </p>


                <p>
                    We truly appreciate everything you do for us.
                    May you continue to inspire many more students
                    and make a positive difference through your
                    dedication as a teacher.
                </p>


                <p class="final-message">
                    Happy Teacher's Day, Sir Randy!
                    <br><br>

                    Thank you for being one of the people who
                    helps us level up not only in school,
                    but also in life.
                </p>


                <p class="signature">

                    With respect and gratitude,

                    <br>

                    <strong>
                        Your Students
                    </strong>

                </p>

            </div>


            <!-- Letter Footer -->
            <div class="letter-footer">

                <span>
                    MISSION COMPLETE
                </span>

                <button id="readAgain">
                    ↻ READ AGAIN
                </button>

            </div>

        </div>

    </div>

    <script>
// ========================================
// ELEMENTS
// ========================================

const openLetter =
    document.getElementById("openLetter");

const closeLetter =
    document.getElementById("closeLetter");

const letterOverlay =
    document.getElementById("letterOverlay");

const readAgain =
    document.getElementById("readAgain");

const particles =
    document.getElementById("particles");


// ========================================
// OPEN LETTER
// ========================================

openLetter.addEventListener("click", () => {

    letterOverlay.classList.add("active");

    document.body.style.overflow = "hidden";

});


// ========================================
// CLOSE LETTER
// ========================================

function closeTheLetter() {

    letterOverlay.classList.remove("active");

    document.body.style.overflow = "";

}


closeLetter.addEventListener(
    "click",
    closeTheLetter
);


// ========================================
// CLICK OUTSIDE LETTER
// ========================================

letterOverlay.addEventListener(
    "click",
    (event) => {

        if (
            event.target ===
            letterOverlay
        ) {

            closeTheLetter();

        }

    }
);


// ========================================
// ESC KEY
// ========================================

document.addEventListener(
    "keydown",
    (event) => {

        if (
            event.key === "Escape" &&
            letterOverlay.classList.contains("active")
        ) {

            closeTheLetter();

        }

    }
);


// ========================================
// READ AGAIN
// ========================================

readAgain.addEventListener(
    "click",
    () => {

        const letter =
            document.querySelector(".letter");

        letter.animate(

            [

                {
                    transform:
                        "translateY(0) scale(1)"
                },

                {
                    transform:
                        "translateY(10px) scale(0.98)"
                },

                {
                    transform:
                        "translateY(0) scale(1)"
                }

            ],

            {

                duration: 600,

                easing:
                    "cubic-bezier(.2,.8,.2,1)"

            }

        );

    }
);


// ========================================
// BACKGROUND PARTICLES
// ========================================

for (
    let i = 0;
    i < 35;
    i++
) {

    const particle =
        document.createElement("div");

    particle.classList.add(
        "particle"
    );


    particle.style.left =
        Math.random() * 100 + "%";


    particle.style.animationDuration =
        (5 + Math.random() * 8) + "s";


    particle.style.animationDelay =
        (Math.random() * -10) + "s";


    particle.style.opacity =
        0.15 + Math.random() * 0.5;


    particles.appendChild(
        particle
    );

}
</script>

</body>
</html>
