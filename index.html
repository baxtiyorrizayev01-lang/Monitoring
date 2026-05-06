<!DOCTYPE html>
<html lang="uz">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>ExamPrep.AI — SAT · IELTS · Multilevel</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/react/18.2.0/umd/react.production.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/react-dom/18.2.0/umd/react-dom.production.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/babel-standalone/7.23.2/babel.min.js"></script>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@700;900&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet"/>
</head>
<body>
<div id="root"></div>
<script type="text/babel">
const { useState, useEffect, useRef, useCallback } = React;

// ════════════════════════════════════════════════════════════
// DATA & CONSTANTS
// ════════════════════════════════════════════════════════════
const ADMIN_PASS = "admin2025";

const ONBOARDING_SLIDES = [
  { icon: "🎯", title: "Maqsadingizga yeting", sub: "SAT, IELTS yoki Multilevel — qaysi imtihon bo'lmasin, biz siz bilan birga tayyorlanamiz.", accent: "#ff2d9e" },
  { icon: "🤖", title: "AI Tutor — 24/7", sub: "Har qanday savolingizga zudlik bilan javob. Tushuntirish, misollar, strategiyalar — hammasi bir joyda.", accent: "#7c3aed" },
  { icon: "📐", title: "SAT: Math + English", sub: "Easy → Medium → Hard darajali testlar. Desmos kalkulyator bilan real imtihon muhiti.", accent: "#ff6ec7" },
  { icon: "🎓", title: "IELTS: 4 Ko'nikma", sub: "Listening, Reading, Writing, Speaking — har birida amaliy testlar va AI tekshiruvi.", accent: "#00e5ff" },
  { icon: "🌍", title: "Multilevel A1→C2", sub: "Darajangizni aniqlang va o'z seviyangizga mos testlar ishlang. Progress real vaqtda ko'rinadi.", accent: "#00ff9d" },
  { icon: "🏆", title: "Tayyormisiz?", sub: "Hoziroq boshlang va birinchi testingizni ishlang. Sizning muvaffaqiyatingiz bizning g'ururumiz!", accent: "#ffe600" },
];

const SAMPLE_QUESTIONS = {
  sat: {
    math: {
      easy: [
        { id: "sm1", text: "If x + 5 = 12, what is the value of x?", options: ["5", "7", "8", "17"], correct: 1, explanation: "x = 12 - 5 = 7", desmos: true },
        { id: "sm2", text: "What is 15% of 200?", options: ["20", "25", "30", "35"], correct: 2, explanation: "200 × 0.15 = 30", desmos: true },
        { id: "sm3", text: "If a rectangle has length 8 and width 5, what is its area?", options: ["13", "26", "40", "45"], correct: 2, explanation: "Area = length × width = 8 × 5 = 40", desmos: true },
      ],
      medium: [
        { id: "sm4", text: "The equation y = 2x² - 8x + 6 has its vertex at x = ?", options: ["x = 1", "x = 2", "x = 3", "x = 4"], correct: 1, explanation: "Vertex x = -b/2a = 8/4 = 2", desmos: true },
        { id: "sm5", text: "If f(x) = 3x - 7, what is f(f(2))?", options: ["-16", "-10", "-4", "2"], correct: 0, explanation: "f(2) = 6-7 = -1, f(-1) = -3-7 = -10... wait: f(2)=-1, f(-1)=-10. Answer: -10", desmos: false },
        { id: "sm6", text: "A store sells shirts for $24 each. If a customer buys 3 and gets 1 free, what's the cost per shirt?", options: ["$16", "$18", "$20", "$24"], correct: 1, explanation: "3 × $24 = $72 for 4 shirts. $72 ÷ 4 = $18 each", desmos: false },
      ],
      hard: [
        { id: "sm7", text: "For all values of x, (2x + 3)² - (2x - 3)² = ?", options: ["12x", "24x", "4x² - 9", "8x"], correct: 1, explanation: "Using difference of squares: (a+b)(a-b) pattern. = [(2x+3)+(2x-3)][(2x+3)-(2x-3)] = (4x)(6) = 24x", desmos: true },
        { id: "sm8", text: "If log₂(x) + log₂(x-6) = 4, what is x?", options: ["2", "4", "8", "16"], correct: 2, explanation: "log₂(x(x-6)) = 4 → x(x-6) = 16 → x²-6x-16=0 → (x-8)(x+2)=0 → x=8 (positive)", desmos: false },
      ],
    },
    english: {
      easy: [
        { id: "se1", text: "Choose the correctly punctuated sentence:", options: ["Its a beautiful day.", "It's a beautiful day.", "Its' a beautiful day.", "It is, a beautiful day."], correct: 1, explanation: "It's = It is. The apostrophe shows contraction.", desmos: false },
        { id: "se2", text: "Which word means 'to make something larger'?", options: ["Reduce", "Expand", "Diminish", "Contract"], correct: 1, explanation: "'Expand' means to increase in size or extent.", desmos: false },
      ],
      medium: [
        { id: "se3", text: "The scientist _____ her findings at the conference, drawing widespread attention.", options: ["presented", "presents", "had presented", "will present"], correct: 0, explanation: "Past tense 'presented' is correct for completed action in context.", desmos: false },
        { id: "se4", text: "Which transition best connects: 'I studied all night. _____, I failed the exam.'", options: ["Therefore", "Nevertheless", "Furthermore", "Meanwhile"], correct: 1, explanation: "'Nevertheless' shows contrast — despite studying, the result was unexpected.", desmos: false },
      ],
      hard: [
        { id: "se5", text: "The author uses the word 'ephemeral' (line 23) most likely to emphasize that the peace was:", options: ["Deeply meaningful", "Widely celebrated", "Short-lived", "Internationally recognized"], correct: 2, explanation: "'Ephemeral' means lasting for a very short time — short-lived.", desmos: false },
      ],
    },
  },
  ielts: {
    reading: [
      { id: "ir1", text: "Read: 'The Amazon rainforest produces 20% of the world's oxygen supply.' Is this statement True, False, or Not Given according to current scientific consensus?", options: ["True", "False", "Not Given"], correct: 1, explanation: "FALSE — The Amazon actually recycles oxygen but does NOT produce a net 20% of Earth's oxygen. This is a common myth.", desmos: false },
      { id: "ir2", text: "The passage states that renewable energy sources currently supply approximately _____ of global electricity.", options: ["10%", "20%", "29%", "45%"], correct: 2, explanation: "According to IEA data referenced, renewables supply ~29% of global electricity.", desmos: false },
    ],
    listening: [
      { id: "il1", text: "🎧 [Audio simulation] A student asks about library hours. The librarian says opening time is _____ on weekdays.", options: ["8:00 AM", "8:30 AM", "9:00 AM", "9:30 AM"], correct: 2, explanation: "The correct answer is 9:00 AM. Key listening skill: numbers and times.", desmos: false },
      { id: "il2", text: "🎧 [Note completion] The conference is held in _____ Hall, on the _____ floor.", options: ["Newton / 3rd", "Darwin / 2nd", "Einstein / 4th", "Curie / 1st"], correct: 0, explanation: "Newton Hall, 3rd floor. Listen for proper nouns carefully.", desmos: false },
    ],
    writing: [
      { id: "iw1", text: "Task 1 — The chart shows CO₂ emissions from 2000-2020. Which sentence BEST describes an upward trend?", options: ["Emissions remained constant throughout the period.", "Emissions fluctuated wildly with no clear trend.", "Emissions showed an overall increase, rising from X to Y.", "Emissions decreased significantly after 2010."], correct: 2, explanation: "For upward trends, use: 'showed an overall increase' + specific data points.", desmos: false },
      { id: "iw2", text: "Task 2 — Which introduction is most appropriate for Band 7+?", options: ["In my essay I will discuss technology in education.", "Nowadays technology is very important everywhere.", "The integration of technology in education has become increasingly prevalent, sparking debate about its benefits and drawbacks.", "Technology is good. I think it helps students a lot."], correct: 2, explanation: "Band 7+ introductions paraphrase the question and state a clear position without using 'I will discuss' formula.", desmos: false },
    ],
    speaking: [
      { id: "isp1", text: "Part 1 — 'Do you enjoy cooking?' Which answer demonstrates Band 7+ language?", options: ["Yes, I like cooking.", "Yes, cooking is good.", "Absolutely! I'm quite passionate about cooking — I find it incredibly therapeutic after a long day.", "I cook sometimes when I have time."], correct: 2, explanation: "Band 7+ responses: extend answers, use varied vocabulary, show enthusiasm naturally.", desmos: false },
      { id: "isp2", text: "Part 2 (Cue Card) — You must talk about 'a memorable journey'. Which opening is most effective?", options: ["I want to talk about a journey.", "A journey I remember is...", "One journey that has stayed with me vividly is my trip to..., which I took about two years ago.", "My memorable journey was good."], correct: 2, explanation: "Effective Part 2 openings signal the topic clearly and set up the narrative with time reference.", desmos: false },
    ],
  },
  multilevel: {
    a1: [
      { id: "ml1", text: "Complete: 'My name _____ Sara.'", options: ["am", "is", "are", "be"], correct: 1, explanation: "'is' is used with he/she/it and names.", desmos: false },
      { id: "ml2", text: "Which word means the opposite of 'big'?", options: ["Large", "Tall", "Small", "Heavy"], correct: 2, explanation: "Small is the opposite of big.", desmos: false },
    ],
    a2: [
      { id: "ml3", text: "Choose the correct past tense: 'Yesterday I _____ to the market.'", options: ["go", "goes", "went", "gone"], correct: 2, explanation: "'went' is the irregular past tense of 'go'.", desmos: false },
    ],
    b1: [
      { id: "ml4", text: "Which sentence uses the present perfect correctly?", options: ["I have seen that film yesterday.", "I have already seen that film.", "I have saw that film.", "I seen that film."], correct: 1, explanation: "Present perfect with 'already' — no specific past time reference.", desmos: false },
    ],
    b2: [
      { id: "ml5", text: "Choose the correct conditional: 'If I _____ earlier, I wouldn't have missed the train.'", options: ["leave", "left", "had left", "have left"], correct: 2, explanation: "Third conditional (past unreal): If + past perfect, would have + past participle.", desmos: false },
    ],
    c1: [
      { id: "ml6", text: "Which word best completes: 'The politician gave an _____ speech that moved the audience to tears.'", options: ["eloquent", "talkative", "verbose", "chatty"], correct: 0, explanation: "'Eloquent' means fluent and persuasive in speaking — C1 level vocabulary.", desmos: false },
    ],
    c2: [
      { id: "ml7", text: "Identify the rhetorical device: 'Ask not what your country can do for you — ask what you can do for your country.'", options: ["Metaphor", "Chiasmus", "Alliteration", "Hyperbole"], correct: 1, explanation: "Chiasmus — reversed grammatical structure for emphasis. C2 literary analysis.", desmos: false },
    ],
  },
};

const SYSTEM_PROMPTS = {
  sat_math: `You are an elite SAT Math tutor. Help with algebra, geometry, advanced math, data analysis, problem-solving. Give step-by-step solutions. When relevant, suggest using Desmos graphing calculator. Be concise and precise. Respond in user's language (Uzbek or English).`,
  sat_english: `You are an expert SAT English (Reading & Writing) tutor. Help with grammar, reading comprehension, vocabulary in context, writing conventions. Explain rules clearly with examples. Respond in user's language.`,
  ielts_listening: `You are a certified IELTS examiner specializing in Listening. Teach strategies for note completion, multiple choice, maps, and diagrams. Focus on predicting answers, recognizing paraphrases. Respond in user's language.`,
  ielts_reading: `You are a certified IELTS examiner specializing in Reading. Teach skimming, scanning, True/False/Not Given, matching headings, sentence completion. Provide practice passages. Respond in user's language.`,
  ielts_writing: `You are a certified IELTS examiner specializing in Writing. Help with Task 1 (graphs, charts, diagrams) and Task 2 (essays). Score responses using band criteria. Provide model answers. Respond in user's language.`,
  ielts_speaking: `You are a certified IELTS examiner specializing in Speaking. Help with all 3 parts. Provide model answers, vocabulary, pronunciation tips, fluency strategies. Respond in user's language.`,
  multilevel: `You are an expert English teacher for all CEFR levels (A1-C2). Adapt language and complexity to the student's level. Provide level-appropriate activities, explanations, and corrections. Respond in user's language.`,
};

async function callClaude(messages, systemKey) {
  const res = await fetch("https://api.anthropic.com/v1/messages", {
    method: "POST",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify({
      model: "claude-sonnet-4-20250514",
      max_tokens: 1000,
      system: SYSTEM_PROMPTS[systemKey] || SYSTEM_PROMPTS.multilevel,
      messages,
    }),
  });
  const data = await res.json();
  return data.content?.[0]?.text || "Xatolik. Qaytadan urinib ko'ring.";
}

// ════════════════════════════════════════════════════════════
// STYLES
// ════════════════════════════════════════════════════════════
const CSS = `
@import url('https://fonts.googleapis.com/css2?family=Clash+Display:wght@400;500;600;700&family=DM+Sans:wght@300;400;500;600&family=Orbitron:wght@700;900&display=swap');

*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#060010;--bg1:#0a0018;--bg2:#0f001f;
  --s1:rgba(255,255,255,0.04);--s2:rgba(255,255,255,0.07);--s3:rgba(255,255,255,0.11);
  --b:rgba(255,50,180,0.18);--b2:rgba(255,50,180,0.35);
  --pink:#ff2d9e;--pink2:#ff6ec7;--pink3:rgba(255,45,158,0.15);
  --pur:#9333ea;--pur2:#c084fc;
  --cyan:#00e5ff;--cyan2:rgba(0,229,255,0.15);
  --green:#00ff9d;--green2:rgba(0,255,157,0.15);
  --gold:#ffe600;--gold2:rgba(255,230,0,0.15);
  --red:#ff4d6d;
  --tx:#f0e6ff;--muted:rgba(240,230,255,0.45);--muted2:rgba(240,230,255,0.25);
  --r:16px;--r2:12px;--r3:8px;
  --font:'DM Sans',sans-serif;--font2:'Clash Display',sans-serif;--font3:'Orbitron',monospace;
}
body{background:var(--bg);color:var(--tx);font-family:var(--font);min-height:100vh;overflow-x:hidden}

/* ── BG ── */
.bg-wrap{position:fixed;inset:0;z-index:0;pointer-events:none;overflow:hidden}
.bg-grid{position:absolute;inset:0;background-image:linear-gradient(rgba(255,45,158,.03)1px,transparent 1px),linear-gradient(90deg,rgba(255,45,158,.03)1px,transparent 1px);background-size:48px 48px}
.bg-glow{position:absolute;border-radius:50%;filter:blur(100px);opacity:.12}
.bg-glow.g1{width:600px;height:600px;background:var(--pink);top:-200px;left:-200px;animation:drift 10s ease-in-out infinite}
.bg-glow.g2{width:400px;height:400px;background:var(--pur);bottom:-100px;right:-100px;animation:drift 13s ease-in-out infinite reverse}
.bg-glow.g3{width:250px;height:250px;background:var(--cyan);top:45%;left:50%;animation:drift 8s ease-in-out infinite 3s}
@keyframes drift{0%,100%{transform:translate(0,0)}33%{transform:translate(40px,-30px)}66%{transform:translate(-25px,40px)}}

.app{position:relative;z-index:1;min-height:100vh;display:flex;flex-direction:column}

/* ── ONBOARDING ── */
.onb-wrap{min-height:100vh;display:flex;flex-direction:column;align-items:center;justify-content:center;padding:20px;text-align:center}
.onb-logo{font-family:var(--font3);font-size:1.1rem;font-weight:900;letter-spacing:3px;margin-bottom:48px;opacity:.7}
.onb-logo span{color:var(--pink);text-shadow:0 0 20px var(--pink)}
.onb-slide{max-width:500px;animation:slideUp .5s ease}
@keyframes slideUp{from{opacity:0;transform:translateY(24px)}to{opacity:1;transform:translateY(0)}}
.onb-icon{font-size:4.5rem;margin-bottom:24px;filter:drop-shadow(0 0 20px currentColor)}
.onb-title{font-family:var(--font2);font-size:clamp(1.7rem,5vw,2.4rem);font-weight:700;line-height:1.15;margin-bottom:14px}
.onb-sub{color:var(--muted);font-size:1rem;line-height:1.7;max-width:420px;margin:0 auto 36px}
.onb-dots{display:flex;gap:8px;justify-content:center;margin-bottom:32px}
.onb-dot{width:8px;height:8px;border-radius:50%;background:var(--s3);transition:all .3s}
.onb-dot.active{width:24px;border-radius:4px;background:var(--pink);box-shadow:0 0 12px var(--pink)}
.onb-btns{display:flex;gap:12px;justify-content:center}
.onb-btn{padding:12px 28px;border-radius:30px;border:1px solid var(--b2);background:var(--s2);color:var(--tx);cursor:pointer;font-family:var(--font);font-size:.9rem;font-weight:500;transition:all .2s}
.onb-btn:hover{background:var(--s3)}
.onb-btn.primary{background:linear-gradient(135deg,var(--pink),var(--pur));border-color:transparent;color:#fff;box-shadow:0 0 24px rgba(255,45,158,.4)}
.onb-btn.primary:hover{transform:translateY(-2px);box-shadow:0 0 40px rgba(255,45,158,.6)}
.onb-skip{margin-top:16px;font-size:.8rem;color:var(--muted2);cursor:pointer;text-decoration:underline;text-underline-offset:3px}
.onb-skip:hover{color:var(--muted)}

/* ── HEADER ── */
.hdr{padding:13px 20px;display:flex;align-items:center;justify-content:space-between;background:rgba(6,0,16,.85);backdrop-filter:blur(20px);border-bottom:1px solid var(--b);position:sticky;top:0;z-index:200;gap:12px}
.hdr-logo{font-family:var(--font3);font-weight:900;font-size:1rem;letter-spacing:2px;white-space:nowrap;flex-shrink:0}
.hdr-logo em{color:var(--pink);font-style:normal;text-shadow:0 0 16px var(--pink)}
.hdr-nav{display:flex;gap:6px;flex-wrap:wrap;justify-content:flex-end}
.hnav{padding:6px 12px;border-radius:20px;border:1px solid var(--b);background:var(--s1);color:var(--muted);cursor:pointer;font-family:var(--font);font-size:.78rem;font-weight:500;transition:all .2s;white-space:nowrap}
.hnav:hover{color:var(--tx);border-color:rgba(255,45,158,.4)}
.hnav.on{color:#fff;border-color:transparent}
.hnav.on.p{background:linear-gradient(135deg,var(--pink),var(--pur));box-shadow:0 0 14px rgba(255,45,158,.4)}
.hnav.on.c{background:var(--cyan);color:#000}
.hnav.on.g{background:var(--green);color:#000}
.hnav.on.y{background:var(--gold);color:#000}

/* ── HOME ── */
.home{padding:48px 20px;max-width:1100px;margin:0 auto;width:100%}
.home-hero{text-align:center;margin-bottom:56px}
.hero-badge{display:inline-flex;align-items:center;gap:6px;padding:5px 14px;border-radius:20px;border:1px solid rgba(255,45,158,.3);background:rgba(255,45,158,.07);color:var(--pink2);font-size:.72rem;font-weight:600;letter-spacing:2px;text-transform:uppercase;margin-bottom:20px}
.hero-h1{font-family:var(--font2);font-size:clamp(2rem,5.5vw,3.8rem);font-weight:700;line-height:1.08;margin-bottom:16px}
.hero-h1 .pk{color:var(--pink);text-shadow:0 0 50px rgba(255,45,158,.5)}
.hero-h1 .cy{color:var(--cyan);text-shadow:0 0 50px rgba(0,229,255,.4)}
.hero-p{color:var(--muted);font-size:1.05rem;max-width:580px;margin:0 auto 36px;line-height:1.75}
.hero-actions{display:flex;gap:12px;justify-content:center;flex-wrap:wrap}
.ha-btn{padding:13px 28px;border-radius:30px;font-family:var(--font);font-weight:600;font-size:.95rem;cursor:pointer;transition:all .25s;border:1px solid}
.ha-btn.main{background:linear-gradient(135deg,var(--pink),var(--pur));border-color:transparent;color:#fff;box-shadow:0 0 28px rgba(255,45,158,.4)}
.ha-btn.main:hover{transform:translateY(-2px);box-shadow:0 0 44px rgba(255,45,158,.6)}
.ha-btn.sec{background:var(--s2);border-color:var(--b);color:var(--tx)}
.ha-btn.sec:hover{background:var(--s3);border-color:var(--b2)}

.section-lbl{font-family:var(--font3);font-size:.72rem;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:var(--muted);margin-bottom:20px}
.exam-cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));gap:18px;margin-bottom:48px}
.ec{border-radius:20px;border:1px solid var(--b);background:var(--s1);padding:26px;cursor:pointer;transition:all .3s;position:relative;overflow:hidden}
.ec::after{content:'';position:absolute;inset:0;border-radius:20px;opacity:0;transition:opacity .3s}
.ec.sat::after{background:radial-gradient(circle at 20% 20%,rgba(255,110,199,.1),transparent 65%)}
.ec.ielts::after{background:radial-gradient(circle at 20% 20%,rgba(0,229,255,.1),transparent 65%)}
.ec.multi::after{background:radial-gradient(circle at 20% 20%,rgba(0,255,157,.1),transparent 65%)}
.ec:hover::after{opacity:1}
.ec:hover{transform:translateY(-5px)}
.ec.sat:hover{border-color:var(--pink2);box-shadow:0 10px 40px rgba(255,45,158,.2)}
.ec.ielts:hover{border-color:var(--cyan);box-shadow:0 10px 40px rgba(0,229,255,.2)}
.ec.multi:hover{border-color:var(--green);box-shadow:0 10px 40px rgba(0,255,157,.2)}
.ec-icon{font-size:2.2rem;margin-bottom:12px}
.ec-name{font-family:var(--font2);font-size:1.3rem;font-weight:700;margin-bottom:6px}
.ec-name.pk{color:var(--pink2)}
.ec-name.cy{color:var(--cyan)}
.ec-name.gr{color:var(--green)}
.ec-desc{color:var(--muted);font-size:.85rem;line-height:1.6;margin-bottom:16px}
.ec-pills{display:flex;flex-wrap:wrap;gap:6px}
.pill{padding:3px 10px;border-radius:20px;font-size:.7rem;font-weight:600;border:1px solid}
.pill.pk{color:var(--pink2);border-color:rgba(255,110,199,.3);background:rgba(255,110,199,.08)}
.pill.cy{color:var(--cyan);border-color:rgba(0,229,255,.3);background:rgba(0,229,255,.08)}
.pill.gr{color:var(--green);border-color:rgba(0,255,157,.3);background:rgba(0,255,157,.08)}
.ec-arrow{position:absolute;top:24px;right:24px;color:var(--muted2);font-size:1.2rem;transition:all .3s}
.ec:hover .ec-arrow{color:var(--pink);transform:translateX(4px)}

/* ── SAT PAGE ── */
.page-wrap{padding:28px 20px;max-width:1100px;margin:0 auto;width:100%}
.page-title{font-family:var(--font2);font-size:1.6rem;font-weight:700;margin-bottom:6px}
.page-sub{color:var(--muted);font-size:.85rem;margin-bottom:28px}

.subject-tabs{display:flex;gap:10px;margin-bottom:24px}
.stab{padding:9px 20px;border-radius:24px;border:1px solid var(--b);background:var(--s1);color:var(--muted);cursor:pointer;font-family:var(--font);font-size:.85rem;font-weight:500;transition:all .2s;display:flex;align-items:center;gap:6px}
.stab.on.math{background:rgba(255,110,199,.15);color:var(--pink2);border-color:rgba(255,110,199,.4)}
.stab.on.eng{background:rgba(156,110,255,.15);color:var(--pur2);border-color:rgba(156,110,255,.4)}
.stab.on.list{background:rgba(0,229,255,.15);color:var(--cyan);border-color:rgba(0,229,255,.4)}
.stab.on.read{background:rgba(0,229,255,.15);color:var(--cyan);border-color:rgba(0,229,255,.4)}
.stab.on.writ{background:rgba(255,230,0,.15);color:var(--gold);border-color:rgba(255,230,0,.4)}
.stab.on.spea{background:rgba(0,255,157,.15);color:var(--green);border-color:rgba(0,255,157,.4)}

.diff-tabs{display:flex;gap:8px;margin-bottom:24px;flex-wrap:wrap}
.dtab{padding:7px 16px;border-radius:20px;border:1px solid var(--b);background:var(--s1);color:var(--muted);cursor:pointer;font-size:.78rem;font-weight:600;transition:all .2s;font-family:var(--font)}
.dtab.on.easy{background:rgba(0,255,157,.12);color:var(--green);border-color:rgba(0,255,157,.4);box-shadow:0 0 12px rgba(0,255,157,.15)}
.dtab.on.medium{background:rgba(255,230,0,.12);color:var(--gold);border-color:rgba(255,230,0,.4);box-shadow:0 0 12px rgba(255,230,0,.15)}
.dtab.on.hard{background:rgba(255,77,109,.12);color:var(--red);border-color:rgba(255,77,109,.4);box-shadow:0 0 12px rgba(255,77,109,.15)}

.mode-toggle{display:flex;gap:8px;margin-bottom:24px}
.mtog{padding:8px 18px;border-radius:20px;border:1px solid var(--b);background:var(--s1);color:var(--muted);cursor:pointer;font-size:.82rem;font-weight:500;transition:all .2s;font-family:var(--font)}
.mtog.on{background:var(--s3);color:var(--tx);border-color:var(--b2)}

/* ── TEST MODE ── */
.test-wrap{animation:fadeIn .3s ease}
@keyframes fadeIn{from{opacity:0;transform:translateY(12px)}to{opacity:1;transform:translateY(0)}}
.test-hdr{display:flex;align-items:center;justify-content:space-between;margin-bottom:20px;flex-wrap:wrap;gap:12px}
.test-prog-info{font-size:.82rem;color:var(--muted)}
.test-prog-bar{height:4px;border-radius:2px;background:var(--s3);margin-bottom:20px;overflow:hidden}
.test-prog-fill{height:100%;border-radius:2px;background:linear-gradient(90deg,var(--pink),var(--pur));transition:width .4s ease;box-shadow:0 0 8px rgba(255,45,158,.4)}
.q-card{padding:28px;border-radius:20px;border:1px solid var(--b);background:var(--s1);margin-bottom:16px}
.q-num{font-size:.72rem;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:var(--muted);margin-bottom:12px}
.q-text{font-size:1rem;line-height:1.7;margin-bottom:24px;font-weight:400}
.q-opts{display:flex;flex-direction:column;gap:10px}
.q-opt{padding:13px 18px;border-radius:12px;border:1px solid var(--b);background:var(--s1);cursor:pointer;font-size:.9rem;transition:all .2s;text-align:left;color:var(--tx);font-family:var(--font);display:flex;align-items:center;gap:10px}
.q-opt:hover{background:var(--s2);border-color:var(--b2)}
.q-opt.selected{background:rgba(147,51,234,.15);border-color:rgba(147,51,234,.5);color:var(--pur2)}
.q-opt.correct{background:rgba(0,255,157,.12);border-color:var(--green);color:var(--green)}
.q-opt.wrong{background:rgba(255,77,109,.1);border-color:var(--red);color:var(--red)}
.q-opt-letter{width:26px;height:26px;border-radius:50%;background:var(--s3);display:flex;align-items:center;justify-content:center;font-size:.72rem;font-weight:700;flex-shrink:0;font-family:var(--font3)}
.q-explain{margin-top:16px;padding:14px 18px;border-radius:12px;background:rgba(147,51,234,.1);border:1px solid rgba(147,51,234,.3);font-size:.85rem;line-height:1.65;color:var(--pur2)}
.q-actions{display:flex;gap:10px;margin-top:20px;flex-wrap:wrap}
.qa-btn{padding:10px 22px;border-radius:24px;border:1px solid;cursor:pointer;font-family:var(--font);font-size:.85rem;font-weight:500;transition:all .2s}
.qa-btn.next{background:linear-gradient(135deg,var(--pink),var(--pur));border-color:transparent;color:#fff;box-shadow:0 0 16px rgba(255,45,158,.3)}
.qa-btn.next:hover{transform:translateY(-1px);box-shadow:0 0 28px rgba(255,45,158,.5)}
.qa-btn.des{background:var(--s2);border-color:var(--b);color:var(--tx)}
.qa-btn.des:hover{background:var(--s3)}

/* DESMOS */
.desmos-panel{margin-top:16px;border-radius:14px;overflow:hidden;border:1px solid var(--b)}
.desmos-hdr{padding:10px 16px;background:var(--s2);border-bottom:1px solid var(--b);display:flex;align-items:center;gap:8px;font-size:.8rem;color:var(--muted);font-weight:600}
.desmos-hdr span{color:var(--green)}
.desmos-frame{width:100%;height:340px;border:none;background:#fff}

/* RESULT */
.result-card{padding:36px;border-radius:24px;border:1px solid var(--b);background:var(--s1);text-align:center;animation:fadeIn .5s ease}
.result-score{font-family:var(--font3);font-size:3.5rem;font-weight:900;margin:16px 0 8px}
.result-label{color:var(--muted);font-size:.9rem;margin-bottom:24px}
.result-breakdown{display:grid;grid-template-columns:repeat(auto-fit,minmax(120px,1fr));gap:12px;margin-bottom:28px}
.rb-item{padding:14px;border-radius:12px;background:var(--s2);border:1px solid var(--b)}
.rb-val{font-family:var(--font3);font-size:1.4rem;font-weight:700;margin-bottom:4px}
.rb-lbl{font-size:.72rem;color:var(--muted);text-transform:uppercase;letter-spacing:.5px}

/* ── AI CHAT ── */
.chat-wrap{display:flex;flex-direction:column;height:calc(100vh - 64px)}
.chat-hdr{padding:20px;border-bottom:1px solid var(--b);flex-shrink:0}
.chat-title{font-family:var(--font2);font-size:1.3rem;font-weight:700}
.chat-sub{color:var(--muted);font-size:.82rem;margin-top:3px}
.quick-chips{display:flex;gap:7px;flex-wrap:wrap;padding:14px 20px;border-bottom:1px solid var(--b);flex-shrink:0}
.chip{padding:6px 13px;border-radius:16px;border:1px solid var(--b);background:var(--s1);color:var(--muted);cursor:pointer;font-size:.75rem;font-family:var(--font);transition:all .2s;white-space:nowrap}
.chip:hover{border-color:var(--b2);color:var(--tx);background:var(--s2)}
.msgs{flex:1;overflow-y:auto;padding:20px;display:flex;flex-direction:column;gap:14px}
.msgs::-webkit-scrollbar{width:3px}
.msgs::-webkit-scrollbar-thumb{background:rgba(255,45,158,.3);border-radius:2px}
.msg-row{display:flex;gap:10px;animation:fadeIn .3s ease}
.msg-row.u{flex-direction:row-reverse}
.msg-av{width:34px;height:34px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:.95rem;flex-shrink:0;border:1px solid var(--b)}
.msg-av.ai{background:linear-gradient(135deg,rgba(255,45,158,.2),rgba(147,51,234,.2))}
.msg-av.u{background:linear-gradient(135deg,rgba(0,229,255,.2),rgba(0,255,157,.2))}
.msg-bub{max-width:74%;padding:11px 15px;border-radius:14px;font-size:.875rem;line-height:1.65;white-space:pre-wrap;word-break:break-word}
.msg-bub.ai{background:var(--s2);border:1px solid var(--b);border-top-left-radius:4px}
.msg-bub.u{background:linear-gradient(135deg,rgba(255,45,158,.18),rgba(147,51,234,.18));border:1px solid rgba(255,45,158,.3);border-top-right-radius:4px}
.typing{display:flex;gap:5px;align-items:center;padding:3px 0}
.typing i{width:6px;height:6px;border-radius:50%;background:var(--pink);animation:blink 1.1s ease infinite}
.typing i:nth-child(2){animation-delay:.18s}
.typing i:nth-child(3){animation-delay:.36s}
@keyframes blink{0%,80%,100%{transform:translateY(0);opacity:.35}40%{transform:translateY(-5px);opacity:1}}
.inp-area{padding:14px 20px 18px;border-top:1px solid var(--b);flex-shrink:0}
.inp-row{display:flex;gap:10px;align-items:flex-end}
.inp-ta{flex:1;background:var(--s2);border:1px solid var(--b);border-radius:14px;padding:11px 15px;color:var(--tx);font-family:var(--font);font-size:.88rem;resize:none;outline:none;transition:border-color .2s;min-height:44px;max-height:110px}
.inp-ta:focus{border-color:var(--pink)}
.inp-ta::placeholder{color:var(--muted2)}
.send{width:44px;height:44px;border-radius:50%;border:none;cursor:pointer;background:linear-gradient(135deg,var(--pink),var(--pur));color:#fff;font-size:1rem;display:flex;align-items:center;justify-content:center;box-shadow:0 0 14px rgba(255,45,158,.4);transition:all .2s;flex-shrink:0}
.send:hover{transform:scale(1.08);box-shadow:0 0 24px rgba(255,45,158,.6)}
.send:disabled{opacity:.4;cursor:not-allowed;transform:none}

/* ── STATS ── */
.stats-wrap{padding:28px 20px;max-width:1000px;margin:0 auto;width:100%}
.snum{font-family:var(--font3);font-size:2rem;font-weight:900}
.snum.pk{color:var(--pink);text-shadow:0 0 16px rgba(255,45,158,.4)}
.snum.cy{color:var(--cyan);text-shadow:0 0 16px rgba(0,229,255,.4)}
.snum.gr{color:var(--green);text-shadow:0 0 16px rgba(0,255,157,.4)}
.snum.gd{color:var(--gold);text-shadow:0 0 16px rgba(255,230,0,.4)}
.sg{display:grid;grid-template-columns:repeat(auto-fit,minmax(160px,1fr));gap:14px;margin-bottom:28px}
.sc{padding:20px;border-radius:16px;border:1px solid var(--b);background:var(--s1);text-align:center}
.slbl{font-size:.72rem;text-transform:uppercase;letter-spacing:1px;color:var(--muted);margin-top:6px}
.pbar{height:5px;border-radius:3px;background:var(--s3);overflow:hidden;margin-top:6px}
.pfill{height:100%;border-radius:3px;transition:width 1s ease}
.pfill.pk{background:linear-gradient(90deg,var(--pink),var(--pur));box-shadow:0 0 6px rgba(255,45,158,.4)}
.pfill.cy{background:linear-gradient(90deg,var(--cyan),var(--pur));box-shadow:0 0 6px rgba(0,229,255,.4)}
.pfill.gr{background:linear-gradient(90deg,var(--green),var(--cyan));box-shadow:0 0 6px rgba(0,255,157,.4)}
.prog-card{padding:22px;border-radius:16px;border:1px solid var(--b);background:var(--s1);margin-bottom:14px}
.prog-row{margin-bottom:11px}
.prog-top{display:flex;justify-content:space-between;font-size:.8rem;color:var(--muted);margin-bottom:6px}

/* ── ADMIN ── */
.adm-wrap{padding:28px 20px;max-width:1100px;margin:0 auto;width:100%}
.adm-login{max-width:360px;margin:80px auto;text-align:center}
.adm-title{font-family:var(--font2);font-size:1.6rem;font-weight:700;margin-bottom:8px}
.adm-title.gd{color:var(--gold);text-shadow:0 0 20px rgba(255,230,0,.4)}
.ai-field{width:100%;padding:11px 14px;border-radius:12px;background:var(--s2);border:1px solid var(--b);color:var(--tx);font-family:var(--font);font-size:.88rem;outline:none;transition:border-color .2s;margin-bottom:10px}
.ai-field:focus{border-color:var(--gold)}
.ai-btn{width:100%;padding:11px;border-radius:12px;border:none;cursor:pointer;background:linear-gradient(135deg,var(--gold),#ff9500);color:#000;font-family:var(--font);font-weight:700;font-size:.9rem;transition:all .2s}
.ai-btn:hover{transform:translateY(-1px);box-shadow:0 0 20px rgba(255,230,0,.4)}
.adm-tabs{display:flex;gap:8px;margin-bottom:24px;flex-wrap:wrap}
.atab{padding:8px 16px;border-radius:20px;border:1px solid rgba(255,230,0,.2);background:var(--s1);color:var(--muted);cursor:pointer;font-size:.8rem;font-family:var(--font);transition:all .2s}
.atab.on{background:var(--gold);color:#000;border-color:var(--gold);font-weight:700}
.form-box{padding:22px;border-radius:16px;border:1px solid rgba(255,230,0,.2);background:var(--s1);margin-bottom:20px}
.form-row{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-bottom:10px}
.fsel{padding:9px 12px;border-radius:10px;background:var(--s2);border:1px solid var(--b);color:var(--tx);font-family:var(--font);font-size:.83rem;outline:none;width:100%}
.fsel:focus{border-color:var(--gold)}
.fta{width:100%;padding:10px 13px;border-radius:10px;background:var(--s2);border:1px solid var(--b);color:var(--tx);font-family:var(--font);font-size:.83rem;resize:vertical;outline:none;margin-bottom:10px;min-height:70px}
.fta:focus{border-color:var(--gold)}
.opts-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-bottom:10px}
.opt-in{padding:8px 12px;border-radius:8px;background:var(--s2);border:1px solid var(--b);color:var(--tx);font-family:var(--font);font-size:.82rem;outline:none;width:100%}
.opt-in:focus{border-color:var(--gold)}
.correct-row{display:flex;gap:7px;margin-bottom:12px}
.cr-btn{padding:6px 14px;border-radius:8px;cursor:pointer;border:1px solid var(--b);background:var(--s2);color:var(--muted);font-family:var(--font3);font-size:.78rem;transition:all .2s}
.cr-btn.on{background:rgba(0,255,157,.15);color:var(--green);border-color:rgba(0,255,157,.5)}
.sv-btn{padding:9px 22px;border-radius:10px;border:none;cursor:pointer;background:linear-gradient(135deg,var(--gold),#ff9500);color:#000;font-family:var(--font);font-weight:700;font-size:.85rem;transition:all .2s}
.sv-btn:hover{transform:translateY(-1px);box-shadow:0 0 16px rgba(255,230,0,.3)}
.q-list{display:flex;flex-direction:column;gap:10px}
.qi{padding:16px;border-radius:14px;border:1px solid var(--b);background:var(--s1)}
.qi-meta{display:flex;gap:6px;flex-wrap:wrap;margin-bottom:8px}
.qbadge{padding:2px 9px;border-radius:10px;font-size:.68rem;font-weight:700;border:1px solid}
.qbadge.sat{color:var(--pink2);border-color:rgba(255,110,199,.3);background:rgba(255,110,199,.08)}
.qbadge.ielts{color:var(--cyan);border-color:rgba(0,229,255,.3);background:rgba(0,229,255,.08)}
.qbadge.multi{color:var(--green);border-color:rgba(0,255,157,.3);background:rgba(0,255,157,.08)}
.qbadge.diff{color:var(--gold);border-color:rgba(255,230,0,.3);background:rgba(255,230,0,.08)}
.qi-text{font-size:.84rem;margin-bottom:8px;line-height:1.5}
.qi-del{padding:4px 11px;border-radius:7px;font-size:.73rem;cursor:pointer;border:1px solid rgba(255,77,109,.3);color:var(--red);background:rgba(255,77,109,.07);font-family:var(--font);transition:all .2s}
.qi-del:hover{background:rgba(255,77,109,.15)}
.bulk-zone{border:2px dashed rgba(255,230,0,.3);border-radius:14px;padding:32px;text-align:center;margin-bottom:16px;transition:all .2s;cursor:pointer}
.bulk-zone:hover,.bulk-zone.drag{border-color:var(--gold);background:rgba(255,230,0,.05)}
.bulk-ico{font-size:2.5rem;margin-bottom:12px}
.bulk-hint{color:var(--muted);font-size:.83rem;line-height:1.6;margin-top:8px}
code{background:rgba(255,230,0,.1);color:var(--gold);padding:1px 5px;border-radius:4px;font-size:.85em}
.err{color:var(--red);font-size:.8rem;margin-bottom:8px}
.ok-msg{color:var(--green);font-size:.8rem;margin-bottom:8px}

/* ── EMPTY ── */
.empty{flex:1;display:flex;flex-direction:column;align-items:center;justify-content:center;padding:40px;text-align:center}
.empty-ico{font-size:3rem;margin-bottom:14px;opacity:.5}
.empty-t{font-size:1rem;font-weight:600;margin-bottom:7px}
.empty-s{color:var(--muted);font-size:.83rem;max-width:360px;line-height:1.6}

@media(max-width:600px){
  .hdr{padding:10px 14px}.hero-h1{font-size:1.9rem}
  .form-row,.opts-grid{grid-template-columns:1fr}
  .subject-tabs{flex-wrap:wrap}
}
`;

// ════════════════════════════════════════════════════════════
// DESMOS COMPONENT
// ════════════════════════════════════════════════════════════
function DesmosPanel() {
  const [show, setShow] = useState(false);
  return (
    <div className="desmos-panel">
      <div className="desmos-hdr" style={{ cursor: "pointer", justifyContent: "space-between" }} onClick={() => setShow(p => !p)}>
        <span>📊 <span>Desmos</span> Graphing Calculator</span>
        <span style={{ fontSize: ".75rem" }}>{show ? "▲ Yopish" : "▼ Ochish"}</span>
      </div>
      {show && (
        <iframe
          className="desmos-frame"
          src="https://www.desmos.com/calculator"
          title="Desmos Calculator"
          allow="fullscreen"
        />
      )}
    </div>
  );
}

// ════════════════════════════════════════════════════════════
// TEST ENGINE
// ════════════════════════════════════════════════════════════
function TestEngine({ questions, color, showDesmos, onFinish }) {
  const [idx, setIdx] = useState(0);
  const [answers, setAnswers] = useState({});
  const [revealed, setRevealed] = useState({});
  const [done, setDone] = useState(false);

  const q = questions[idx];
  const total = questions.length;
  const pct = Math.round(((idx + (answers[q?.id] !== undefined ? 1 : 0)) / total) * 100);
  const letters = ["A", "B", "C", "D"];

  const select = (optIdx) => {
    if (revealed[q.id]) return;
    setAnswers(p => ({ ...p, [q.id]: optIdx }));
    setRevealed(p => ({ ...p, [q.id]: true }));
  };

  const next = () => {
    if (idx < total - 1) { setIdx(p => p + 1); }
    else { setDone(true); if (onFinish) onFinish(answers, questions); }
  };

  if (done) {
    const correct = questions.filter(q => answers[q.id] === q.correct).length;
    const pctScore = Math.round((correct / total) * 100);
    return (
      <div className="result-card">
        <div style={{ fontSize: "2.5rem", marginBottom: "8px" }}>
          {pctScore >= 80 ? "🏆" : pctScore >= 60 ? "👍" : "📚"}
        </div>
        <div className="result-score" style={{ color: pctScore >= 80 ? "#00ff9d" : pctScore >= 60 ? "#ffe600" : "#ff6ec7" }}>
          {pctScore}%
        </div>
        <div className="result-label">{correct}/{total} to'g'ri javob</div>
        <div className="result-breakdown">
          <div className="rb-item"><div className="rb-val" style={{ color: "#00ff9d" }}>{correct}</div><div className="rb-lbl">To'g'ri</div></div>
          <div className="rb-item"><div className="rb-val" style={{ color: "#ff4d6d" }}>{total - correct}</div><div className="rb-lbl">Noto'g'ri</div></div>
          <div className="rb-item"><div className="rb-val" style={{ color: "#ffe600" }}>{pctScore}%</div><div className="rb-lbl">Natija</div></div>
        </div>
        <div style={{ display: "flex", gap: "10px", justifyContent: "center", flexWrap: "wrap" }}>
          <button className="qa-btn next" onClick={() => { setIdx(0); setAnswers({}); setRevealed({}); setDone(false); }}>
            🔄 Qaytadan
          </button>
          <button className="qa-btn des" onClick={onFinish}>← Orqaga</button>
        </div>
      </div>
    );
  }

  if (!q) return null;
  const sel = answers[q.id];
  const rev = revealed[q.id];

  return (
    <div className="test-wrap">
      <div className="test-hdr">
        <span className="test-prog-info">Savol {idx + 1} / {total}</span>
        <span className="test-prog-info">{q.subject || ""}</span>
      </div>
      <div className="test-prog-bar">
        <div className="test-prog-fill" style={{ width: `${((idx) / total) * 100}%` }} />
      </div>
      <div className="q-card">
        <div className="q-num">Savol {idx + 1}</div>
        <div className="q-text">{q.text}</div>
        <div className="q-opts">
          {q.options.map((opt, i) => {
            let cls = "q-opt";
            if (rev) {
              if (i === q.correct) cls += " correct";
              else if (i === sel && i !== q.correct) cls += " wrong";
            } else if (sel === i) cls += " selected";
            return (
              <button key={i} className={cls} onClick={() => select(i)}>
                <span className="q-opt-letter">{letters[i]}</span>
                {opt}
              </button>
            );
          })}
        </div>
        {rev && q.explanation && (
          <div className="q-explain">💡 {q.explanation}</div>
        )}
        <div className="q-actions">
          {rev && (
            <button className="qa-btn next" onClick={next}>
              {idx < total - 1 ? "Keyingi →" : "Natijani ko'rish 🏁"}
            </button>
          )}
          {showDesmos && q.desmos && <button className="qa-btn des">📊 Desmos</button>}
        </div>
      </div>
      {showDesmos && q.desmos && <DesmosPanel />}
    </div>
  );
}

// ════════════════════════════════════════════════════════════
// AI CHAT
// ════════════════════════════════════════════════════════════
function AIChat({ title, subtitle, icon, systemKey, accentColor, chips }) {
  const [msgs, setMsgs] = useState([]);
  const [inp, setInp] = useState("");
  const [loading, setLoading] = useState(false);
  const btm = useRef(null);

  useEffect(() => { btm.current?.scrollIntoView({ behavior: "smooth" }); }, [msgs, loading]);

  const send = async (text) => {
    if (!text.trim() || loading) return;
    const newMsgs = [...msgs, { role: "user", content: text.trim() }];
    setMsgs(newMsgs);
    setInp("");
    setLoading(true);
    try {
      const reply = await callClaude(newMsgs, systemKey);
      setMsgs(p => [...p, { role: "assistant", content: reply }]);
    } catch {
      setMsgs(p => [...p, { role: "assistant", content: "❌ Xatolik. Qaytadan urinib ko'ring." }]);
    }
    setLoading(false);
  };

  return (
    <div className="chat-wrap">
      <div className="chat-hdr">
        <div className="chat-title" style={{ color: accentColor }}>{icon} {title}</div>
        <div className="chat-sub">{subtitle}</div>
      </div>
      <div className="quick-chips">
        {chips.map((c, i) => (
          <button key={i} className="chip" onClick={() => send(c.prompt)}>{c.label}</button>
        ))}
      </div>
      <div className="msgs">
        {msgs.length === 0 && !loading && (
          <div className="empty">
            <div className="empty-ico">{icon}</div>
            <div className="empty-t">AI Tutor tayyor!</div>
            <div className="empty-s">Yuqoridagi tugmalardan birini bosing yoki savolingizni yozing.</div>
          </div>
        )}
        {msgs.map((m, i) => (
          <div key={i} className={`msg-row ${m.role === "user" ? "u" : ""}`}>
            <div className={`msg-av ${m.role === "user" ? "u" : "ai"}`}>{m.role === "user" ? "👤" : icon}</div>
            <div className={`msg-bub ${m.role === "user" ? "u" : "ai"}`}>{m.content}</div>
          </div>
        ))}
        {loading && (
          <div className="msg-row">
            <div className="msg-av ai">{icon}</div>
            <div className="msg-bub ai"><div className="typing"><i /><i /><i /></div></div>
          </div>
        )}
        <div ref={btm} />
      </div>
      <div className="inp-area">
        <div className="inp-row">
          <textarea className="inp-ta" value={inp} onChange={e => setInp(e.target.value)}
            onKeyDown={e => { if (e.key === "Enter" && !e.shiftKey) { e.preventDefault(); send(inp); } }}
            placeholder="Savolingizni yozing... (Enter = yuborish)" rows={1} />
          <button className="send" onClick={() => send(inp)} disabled={loading || !inp.trim()}>➤</button>
        </div>
      </div>
    </div>
  );
}

// ════════════════════════════════════════════════════════════
// SAT SECTION
// ════════════════════════════════════════════════════════════
function SATSection({ extraQuestions }) {
  const [subject, setSubject] = useState("math");
  const [diff, setDiff] = useState("easy");
  const [mode, setMode] = useState("test");
  const [testKey, setTestKey] = useState(0);

  const baseQ = SAMPLE_QUESTIONS.sat;
  const mathQ = {
    easy: [...baseQ.math.easy, ...extraQuestions.filter(q => q.exam === "SAT" && q.subject?.toLowerCase().includes("math") && q.difficulty === "Easy")],
    medium: [...baseQ.math.medium, ...extraQuestions.filter(q => q.exam === "SAT" && q.subject?.toLowerCase().includes("math") && q.difficulty === "Medium")],
    hard: [...baseQ.math.hard, ...extraQuestions.filter(q => q.exam === "SAT" && q.subject?.toLowerCase().includes("math") && q.difficulty === "Hard")],
  };
  const engQ = {
    easy: [...baseQ.english.easy, ...extraQuestions.filter(q => q.exam === "SAT" && !q.subject?.toLowerCase().includes("math") && q.difficulty === "Easy")],
    medium: [...baseQ.english.medium, ...extraQuestions.filter(q => q.exam === "SAT" && !q.subject?.toLowerCase().includes("math") && q.difficulty === "Medium")],
    hard: [...baseQ.english.hard, ...extraQuestions.filter(q => q.exam === "SAT" && !q.subject?.toLowerCase().includes("math") && q.difficulty === "Hard")],
  };
  const questions = subject === "math" ? (mathQ[diff] || []) : (engQ[diff] || []);

  const MATH_CHIPS = [
    { label: "📐 Algebra help", prompt: "SAT Math Algebra bo'yicha eng muhim tushunchalar va misollar." },
    { label: "📈 Quadratic tips", prompt: "Quadratic equations ni SAT da qanday tez yechish mumkin?" },
    { label: "📊 Data analysis", prompt: "SAT Math Data Analysis bo'limida qanday xatolar ko'p uchraydi?" },
    { label: "⏱ Speed tips", prompt: "SAT Math da vaqtni tejash uchun 5 ta effektiv strategiya." },
  ];
  const ENG_CHIPS = [
    { label: "✍️ Grammar rules", prompt: "SAT English da eng ko'p uchraydigan grammar qoidalar." },
    { label: "📖 Reading strategy", prompt: "SAT Reading bo'limida tez va to'g'ri javob topish strategiyasi." },
    { label: "🔤 Vocab tips", prompt: "SAT Vocabulary in Context savollarini qanday yechish kerak?" },
  ];

  return (
    <div className="page-wrap">
      <div className="page-title" style={{ color: "var(--pink2)" }}>📐 SAT Tayyorgarlik</div>
      <div className="page-sub">Math va English · Easy → Medium → Hard</div>
      <div className="subject-tabs">
        <button className={`stab ${subject === "math" ? "on math" : ""}`} onClick={() => { setSubject("math"); setTestKey(p => p + 1); }}>📐 Math</button>
        <button className={`stab ${subject === "english" ? "on eng" : ""}`} onClick={() => { setSubject("english"); setTestKey(p => p + 1); }}>📝 English</button>
      </div>
      <div className="mode-toggle">
        <button className={`mtog ${mode === "test" ? "on" : ""}`} onClick={() => setMode("test")}>🧪 Test rejimi</button>
        <button className={`mtog ${mode === "ai" ? "on" : ""}`} onClick={() => setMode("ai")}>🤖 AI Tutor</button>
      </div>

      {mode === "test" && (
        <>
          <div className="diff-tabs">
            {["easy", "medium", "hard"].map(d => (
              <button key={d} className={`dtab ${diff === d ? `on ${d}` : ""}`}
                onClick={() => { setDiff(d); setTestKey(p => p + 1); }}>
                {d === "easy" ? "🟢 Easy" : d === "medium" ? "🟡 Medium" : "🔴 Hard"}
                {" "}({(subject === "math" ? mathQ : engQ)[d]?.length || 0})
              </button>
            ))}
          </div>
          {questions.length > 0
            ? <TestEngine key={`${subject}-${diff}-${testKey}`} questions={questions} showDesmos={subject === "math"} />
            : <div className="empty"><div className="empty-ico">📭</div><div className="empty-t">Savollar yo'q</div><div className="empty-s">Admin paneldan savollar qo'shing.</div></div>
          }
        </>
      )}
      {mode === "ai" && (
        <div style={{ height: "calc(100vh - 300px)", display: "flex", flexDirection: "column", borderRadius: "16px", border: "1px solid var(--b)", overflow: "hidden" }}>
          <AIChat title={subject === "math" ? "SAT Math Tutor" : "SAT English Tutor"}
            subtitle={subject === "math" ? "Algebra · Geometry · Data Analysis" : "Reading · Grammar · Vocabulary"}
            icon={subject === "math" ? "📐" : "📝"} systemKey={subject === "math" ? "sat_math" : "sat_english"}
            accentColor="var(--pink2)" chips={subject === "math" ? MATH_CHIPS : ENG_CHIPS} />
        </div>
      )}
    </div>
  );
}

// ════════════════════════════════════════════════════════════
// IELTS SECTION
// ════════════════════════════════════════════════════════════
function IELTSSection({ extraQuestions }) {
  const [skill, setSkill] = useState("listening");
  const [mode, setMode] = useState("test");
  const [testKey, setTestKey] = useState(0);

  const skills = ["listening", "reading", "writing", "speaking"];
  const icons = { listening: "🎧", reading: "📚", writing: "✍️", speaking: "🎤" };
  const tabClass = { listening: "list", reading: "read", writing: "writ", speaking: "spea" };

  const baseQ = SAMPLE_QUESTIONS.ielts;
  const getQ = (sk) => [
    ...(baseQ[sk] || []),
    ...extraQuestions.filter(q => q.exam === "IELTS" && q.subject?.toLowerCase().includes(sk))
  ];

  const CHIPS = {
    listening: [
      { label: "🎧 Note completion", prompt: "IELTS Listening note completion savollarini qanday yechish kerak?" },
      { label: "🗺 Map labeling", prompt: "IELTS Listening map labeling topshiriqlarida nimalarga e'tibor berish kerak?" },
      { label: "📝 Prediction tips", prompt: "IELTS Listening da oldindan savol o'qish strategiyasini tushuntir." },
    ],
    reading: [
      { label: "T/F/NG strategy", prompt: "IELTS Reading True/False/Not Given savollarini qanday farqlash kerak?" },
      { label: "🔍 Matching headings", prompt: "IELTS Reading matching headings uchun eng samarali strategiya." },
      { label: "⏱ 60 min plan", prompt: "IELTS Reading uchun 60 daqiqani qanday rejalashtirish kerak?" },
    ],
    writing: [
      { label: "✍️ Task 1 template", prompt: "IELTS Writing Task 1 uchun Band 7+ shablon ber." },
      { label: "📝 Task 2 essay", prompt: "IELTS Writing Task 2 opinion essay uchun to'liq shablon va misol." },
      { label: "📊 Describe chart", prompt: "Line chart va bar chart ni qanday tasvirlash kerak? Misol bilan." },
    ],
    speaking: [
      { label: "🗣 Part 1 tips", prompt: "IELTS Speaking Part 1 uchun yuqori band olish strategiyasi." },
      { label: "📋 Cue card", prompt: "IELTS Speaking Part 2 cue card ga tayyorlanish va shablon." },
      { label: "💬 Part 3 vocab", prompt: "IELTS Speaking Part 3 uchun abstract topics da ishlatiladigan iboralar." },
    ],
  };

  const questions = getQ(skill);

  return (
    <div className="page-wrap">
      <div className="page-title" style={{ color: "var(--cyan)" }}>🎓 IELTS Tayyorgarlik</div>
      <div className="page-sub">Listening · Reading · Writing · Speaking</div>
      <div className="subject-tabs" style={{ flexWrap: "wrap" }}>
        {skills.map(s => (
          <button key={s} className={`stab ${skill === s ? `on ${tabClass[s]}` : ""}`}
            onClick={() => { setSkill(s); setTestKey(p => p + 1); }}>
            {icons[s]} {s.charAt(0).toUpperCase() + s.slice(1)}
          </button>
        ))}
      </div>
      <div className="mode-toggle">
        <button className={`mtog ${mode === "test" ? "on" : ""}`} onClick={() => setMode("test")}>🧪 Test</button>
        <button className={`mtog ${mode === "ai" ? "on" : ""}`} onClick={() => setMode("ai")}>🤖 AI Tutor</button>
      </div>
      {mode === "test" && (
        questions.length > 0
          ? <TestEngine key={`${skill}-${testKey}`} questions={questions} showDesmos={false} />
          : <div className="empty"><div className="empty-ico">📭</div><div className="empty-t">Savollar yo'q</div><div className="empty-s">Admin paneldan IELTS savollarini qo'shing.</div></div>
      )}
      {mode === "ai" && (
        <div style={{ height: "calc(100vh - 280px)", display: "flex", flexDirection: "column", borderRadius: "16px", border: "1px solid var(--b)", overflow: "hidden" }}>
          <AIChat title={`IELTS ${skill.charAt(0).toUpperCase() + skill.slice(1)} Tutor`}
            subtitle="Certified IELTS Examiner darajasida yordam" icon={icons[skill]}
            systemKey={`ielts_${skill}`} accentColor="var(--cyan)" chips={CHIPS[skill]} />
        </div>
      )}
    </div>
  );
}

// ════════════════════════════════════════════════════════════
// MULTILEVEL SECTION
// ════════════════════════════════════════════════════════════
function MultiSection({ extraQuestions }) {
  const [lvl, setLvl] = useState("b1");
  const [mode, setMode] = useState("test");
  const [testKey, setTestKey] = useState(0);
  const levels = ["a1", "a2", "b1", "b2", "c1", "c2"];
  const lvlColors = { a1: "#00ff9d", a2: "#00d4ff", b1: "#ffe600", b2: "#ff9500", c1: "#ff6ec7", c2: "#ff2d9e" };

  const getQ = (l) => [
    ...(SAMPLE_QUESTIONS.multilevel[l] || []),
    ...extraQuestions.filter(q => q.exam === "Multilevel" && q.difficulty?.toLowerCase() === l)
  ];
  const questions = getQ(lvl);

  const CHIPS = [
    { label: "🔍 Darajamni aniqlash", prompt: `Men ${lvl.toUpperCase()} darajasidaman. Placement test o'tka — 8 ta savol.` },
    { label: "📖 Reading text", prompt: `${lvl.toUpperCase()} uchun qisqa matn va 4 ta comprehension savoli ber.` },
    { label: "✍️ Writing task", prompt: `${lvl.toUpperCase()} darajasi uchun yozma topshiriq va model javob ber.` },
    { label: "💬 Speaking practice", prompt: `${lvl.toUpperCase()} uchun speaking practice topshirig'i va foydali iboralar.` },
    { label: "📝 Grammar focus", prompt: `${lvl.toUpperCase()} darajasida eng muhim grammar mavzularini tushuntir.` },
  ];

  return (
    <div className="page-wrap">
      <div className="page-title" style={{ color: "var(--green)" }}>🌍 Multilevel English</div>
      <div className="page-sub">CEFR darajasi: A1 → A2 → B1 → B2 → C1 → C2</div>
      <div className="subject-tabs" style={{ flexWrap: "wrap" }}>
        {levels.map(l => (
          <button key={l} className={`stab ${lvl === l ? "on" : ""}`}
            style={lvl === l ? { background: `${lvlColors[l]}22`, color: lvlColors[l], borderColor: lvlColors[l] } : {}}
            onClick={() => { setLvl(l); setTestKey(p => p + 1); }}>
            {l.toUpperCase()} ({getQ(l).length})
          </button>
        ))}
      </div>
      <div className="mode-toggle">
        <button className={`mtog ${mode === "test" ? "on" : ""}`} onClick={() => setMode("test")}>🧪 Test</button>
        <button className={`mtog ${mode === "ai" ? "on" : ""}`} onClick={() => setMode("ai")}>🤖 AI Tutor</button>
      </div>
      {mode === "test" && (
        questions.length > 0
          ? <TestEngine key={`${lvl}-${testKey}`} questions={questions} showDesmos={false} />
          : <div className="empty"><div className="empty-ico">📭</div><div className="empty-t">Savollar yo'q</div><div className="empty-s">Admin paneldan {lvl.toUpperCase()} darajasi uchun savollar qo'shing.</div></div>
      )}
      {mode === "ai" && (
        <div style={{ height: "calc(100vh - 280px)", display: "flex", flexDirection: "column", borderRadius: "16px", border: "1px solid var(--b)", overflow: "hidden" }}>
          <AIChat title={`${lvl.toUpperCase()} Level Tutor`} subtitle="Listening · Reading · Writing · Speaking"
            icon="🌍" systemKey="multilevel" accentColor={lvlColors[lvl]} chips={CHIPS} />
        </div>
      )}
    </div>
  );
}

// ════════════════════════════════════════════════════════════
// STATS
// ════════════════════════════════════════════════════════════
function StatsPage() {
  return (
    <div className="stats-wrap">
      <div className="page-title" style={{ color: "var(--pink)" }}>📊 Statistika</div>
      <div className="page-sub" style={{ marginBottom: "28px" }}>Umumiy o'quv natijalari</div>
      <div className="sg">
        <div className="sc"><div className="snum pk">47</div><div className="slbl">Jami sessiya</div></div>
        <div className="sc"><div className="snum cy">1240</div><div className="slbl">SAT ball</div></div>
        <div className="sc"><div className="snum gr">6.5</div><div className="slbl">IELTS Band</div></div>
        <div className="sc"><div className="snum gd">B2</div><div className="slbl">Daraja</div></div>
      </div>
      {[
        { title: "📐 SAT Progress", color: "pk", topics: { "Math": 72, "Reading": 68, "Writing": 75 } },
        { title: "🎓 IELTS Progress", color: "cy", topics: { "Listening": 70, "Reading": 65, "Writing": 60, "Speaking": 68 } },
        { title: "🌍 Multilevel Progress", color: "gr", topics: { "Listening": 78, "Reading": 80, "Writing": 65, "Speaking": 72 } },
      ].map(s => (
        <div key={s.title}>
          <div className="section-lbl" style={{ marginBottom: "12px" }}>{s.title}</div>
          <div className="prog-card">
            {Object.entries(s.topics).map(([t, v]) => (
              <div className="prog-row" key={t}>
                <div className="prog-top"><span>{t}</span><span>{v}%</span></div>
                <div className="pbar"><div className={`pfill ${s.color}`} style={{ width: `${v}%` }} /></div>
              </div>
            ))}
          </div>
        </div>
      ))}
    </div>
  );
}

// ════════════════════════════════════════════════════════════
// ADMIN
// ════════════════════════════════════════════════════════════
function AdminPage({ questions, setQuestions }) {
  const [authed, setAuthed] = useState(false);
  const [pass, setPass] = useState("");
  const [err, setErr] = useState("");
  const [tab, setTab] = useState("list");
  const [bulkMsg, setBulkMsg] = useState("");
  const [bulkErr, setBulkErr] = useState("");
  const [dragging, setDragging] = useState(false);

  const [form, setForm] = useState({
    exam: "SAT", subject: "Math", difficulty: "Easy",
    text: "", opts: ["", "", "", ""], correctIdx: 0, explanation: ""
  });

  const login = () => {
    if (pass === ADMIN_PASS) { setAuthed(true); setErr(""); }
    else setErr("Noto'g'ri parol!");
  };

  const saveQ = () => {
    if (!form.text.trim() || form.opts.some(o => !o.trim())) return;
    const newQ = {
      id: `admin_${Date.now()}`, exam: form.exam, subject: form.subject, difficulty: form.difficulty,
      text: form.text, options: form.opts, correct: form.correctIdx, answer: ["A", "B", "C", "D"][form.correctIdx],
      explanation: form.explanation, desmos: form.exam === "SAT" && form.subject === "Math"
    };
    setQuestions(p => [newQ, ...p]);
    setForm({ exam: "SAT", subject: "Math", difficulty: "Easy", text: "", opts: ["", "", "", ""], correctIdx: 0, explanation: "" });
    setTab("list");
    setBulkMsg("");
  };

  const parseAndLoad = (text) => {
    try {
      setBulkErr(""); setBulkMsg("");
      const parsed = JSON.parse(text);
      const arr = Array.isArray(parsed) ? parsed : [parsed];
      const valid = arr.filter(q => q.text && q.options && q.correct !== undefined);
      if (!valid.length) throw new Error("Hech qanday to'g'ri savol topilmadi.");
      const withIds = valid.map((q, i) => ({ ...q, id: `bulk_${Date.now()}_${i}`, desmos: q.exam === "SAT" && q.subject?.includes("Math") }));
      setQuestions(p => [...withIds, ...p]);
      setBulkMsg(`✅ ${withIds.length} ta savol yuklandi!`);
    } catch (e) {
      setBulkErr("❌ JSON xato: " + (e.message || "Noto'g'ri format"));
    }
  };

  const handleFile = (file) => {
    const r = new FileReader();
    r.onload = e => parseAndLoad(e.target.result);
    r.readAsText(file);
  };

  const handleDrop = (e) => {
    e.preventDefault(); setDragging(false);
    const file = e.dataTransfer.files[0];
    if (file) handleFile(file);
  };

  if (!authed) return (
    <div className="adm-wrap">
      <div className="adm-login">
        <div style={{ fontSize: "2.8rem", marginBottom: "16px" }}>🔐</div>
        <div className="adm-title gd">Admin Panel</div>
        <p style={{ color: "var(--muted)", fontSize: ".83rem", marginBottom: "24px", lineHeight: "1.6" }}>
          Test tuzuvchi paneliga kirish uchun parolni kiriting
        </p>
        {err && <div className="err">⚠ {err}</div>}
        <input className="ai-field" type="password" placeholder="Parol..." value={pass}
          onChange={e => setPass(e.target.value)} onKeyDown={e => e.key === "Enter" && login()} />
        <button className="ai-btn" onClick={login}>Kirish →</button>
        <div style={{ marginTop: "10px", fontSize: ".73rem", color: "var(--muted2)" }}>Demo: admin2025</div>
      </div>
    </div>
  );

  return (
    <div className="adm-wrap">
      <div className="adm-title gd" style={{ marginBottom: "20px" }}>⚙️ Test Tuzuvchi Paneli</div>
      <div className="adm-tabs">
        {[["list", `📋 Savollar (${questions.length})`], ["add", "➕ Qo'shish"], ["bulk", "📦 Bulk Yuklash"], ["stats", "📊 Stats"]].map(([id, lbl]) => (
          <button key={id} className={`atab ${tab === id ? "on" : ""}`} onClick={() => setTab(id)}>{lbl}</button>
        ))}
        <button className="atab" style={{ marginLeft: "auto", borderColor: "rgba(255,77,109,.3)", color: "var(--red)" }}
          onClick={() => setAuthed(false)}>🚪 Chiqish</button>
      </div>

      {/* LIST */}
      {tab === "list" && (
        <div className="q-list">
          {questions.length === 0 && <div className="empty"><div className="empty-ico">📭</div><div className="empty-t">Savollar yo'q</div></div>}
          {questions.map(q => (
            <div key={q.id} className="qi">
              <div className="qi-meta">
                <span className={`qbadge ${q.exam?.toLowerCase() === "sat" ? "sat" : q.exam?.toLowerCase() === "ielts" ? "ielts" : "multi"}`}>{q.exam}</span>
                <span className="qbadge diff">{q.difficulty}</span>
                <span style={{ fontSize: ".72rem", color: "var(--muted)", padding: "2px 0" }}>{q.subject}</span>
              </div>
              <div className="qi-text">{q.text.length > 110 ? q.text.slice(0, 110) + "..." : q.text}</div>
              <div style={{ display: "flex", gap: "6px", flexWrap: "wrap", marginBottom: "8px" }}>
                {(q.options || []).map((opt, i) => (
                  <span key={i} style={{
                    fontSize: ".72rem", padding: "2px 8px", borderRadius: "6px",
                    background: i === q.correct ? "rgba(0,255,157,.1)" : "var(--s2)",
                    color: i === q.correct ? "var(--green)" : "var(--muted)",
                    border: `1px solid ${i === q.correct ? "rgba(0,255,157,.3)" : "var(--b)"}`,
                  }}>{i === q.correct ? "✓ " : ""}{typeof opt === "string" ? opt : opt}</span>
                ))}
              </div>
              <button className="qi-del" onClick={() => setQuestions(p => p.filter(x => x.id !== q.id))}>🗑 O'chirish</button>
            </div>
          ))}
        </div>
      )}

      {/* ADD */}
      {tab === "add" && (
        <div className="form-box">
          <div style={{ fontWeight: 600, color: "var(--gold)", marginBottom: "16px", fontSize: ".9rem" }}>➕ Yangi savol qo'shish</div>
          <div className="form-row">
            <select className="fsel" value={form.exam} onChange={e => setForm(p => ({ ...p, exam: e.target.value }))}>
              <option>SAT</option><option>IELTS</option><option>Multilevel</option>
            </select>
            <select className="fsel" value={form.difficulty} onChange={e => setForm(p => ({ ...p, difficulty: e.target.value }))}>
              {form.exam === "SAT" ? <><option>Easy</option><option>Medium</option><option>Hard</option></> :
               form.exam === "IELTS" ? <><option>listening</option><option>reading</option><option>writing</option><option>speaking</option></> :
               <><option>a1</option><option>a2</option><option>b1</option><option>b2</option><option>c1</option><option>c2</option></>}
            </select>
          </div>
          <input className="ai-field" style={{ marginBottom: "10px" }} placeholder="Fan / mavzu (Math, Reading, B2 Grammar...)"
            value={form.subject} onChange={e => setForm(p => ({ ...p, subject: e.target.value }))} />
          <textarea className="fta" placeholder="Savol matnini kiriting..." rows={3}
            value={form.text} onChange={e => setForm(p => ({ ...p, text: e.target.value }))} />
          <div className="opts-grid">
            {["A", "B", "C", "D"].map((l, i) => (
              <input key={i} className="opt-in" placeholder={`${l} variant...`}
                value={form.opts[i]} onChange={e => { const o = [...form.opts]; o[i] = e.target.value; setForm(p => ({ ...p, opts: o })); }} />
            ))}
          </div>
          <div style={{ fontSize: ".78rem", color: "var(--muted)", marginBottom: "8px" }}>To'g'ri javob:</div>
          <div className="correct-row">
            {["A", "B", "C", "D"].map((l, i) => (
              <button key={i} className={`cr-btn ${form.correctIdx === i ? "on" : ""}`}
                onClick={() => setForm(p => ({ ...p, correctIdx: i }))}>{l}</button>
            ))}
          </div>
          <textarea className="fta" placeholder="Tushuntirish (ixtiyoriy)..." rows={2}
            value={form.explanation} onChange={e => setForm(p => ({ ...p, explanation: e.target.value }))} />
          <button className="sv-btn" onClick={saveQ}>💾 Saqlash</button>
        </div>
      )}

      {/* BULK */}
      {tab === "bulk" && (
        <div>
          <div className="form-box" style={{ marginBottom: "16px" }}>
            <div style={{ fontWeight: 600, color: "var(--gold)", marginBottom: "12px", fontSize: ".9rem" }}>📦 JSON orqali toplu yuklash</div>
            <div
              className={`bulk-zone ${dragging ? "drag" : ""}`}
              onDragOver={e => { e.preventDefault(); setDragging(true); }}
              onDragLeave={() => setDragging(false)}
              onDrop={handleDrop}
              onClick={() => document.getElementById("bulk-file").click()}
            >
              <div className="bulk-ico">📂</div>
              <div style={{ fontWeight: 600, marginBottom: "6px" }}>JSON faylni shu yerga tashlang</div>
              <div style={{ color: "var(--muted)", fontSize: ".78rem" }}>yoki bosing</div>
              <input id="bulk-file" type="file" accept=".json" style={{ display: "none" }}
                onChange={e => { if (e.target.files[0]) handleFile(e.target.files[0]); }} />
            </div>
            {bulkErr && <div className="err">{bulkErr}</div>}
            {bulkMsg && <div className="ok-msg">{bulkMsg}</div>}
          </div>
          <div className="form-box">
            <div style={{ fontWeight: 600, color: "var(--gold)", marginBottom: "12px", fontSize: ".9rem" }}>📋 JSON format namunasi</div>
            <div style={{ fontSize: ".78rem", color: "var(--muted)", lineHeight: 1.8, fontFamily: "monospace", background: "rgba(0,0,0,.3)", padding: "14px", borderRadius: "10px", overflowX: "auto" }}>
{`[
  {
    "exam": "SAT",
    "subject": "Math",
    "difficulty": "Medium",
    "text": "If 2x + 4 = 10, find x",
    "options": ["1", "3", "5", "7"],
    "correct": 1,
    "explanation": "2x = 6, x = 3"
  },
  {
    "exam": "IELTS",
    "subject": "reading",
    "difficulty": "reading",
    "text": "T/F/NG: ...",
    "options": ["True","False","Not Given"],
    "correct": 0,
    "explanation": "..."
  }
]`}
            </div>
            <div className="bulk-hint">
              <strong>exam:</strong> <code>SAT</code> | <code>IELTS</code> | <code>Multilevel</code><br />
              <strong>difficulty (SAT):</strong> <code>Easy</code> | <code>Medium</code> | <code>Hard</code><br />
              <strong>difficulty (IELTS):</strong> <code>listening</code> | <code>reading</code> | <code>writing</code> | <code>speaking</code><br />
              <strong>difficulty (Multilevel):</strong> <code>a1</code> | <code>a2</code> | <code>b1</code> | <code>b2</code> | <code>c1</code> | <code>c2</code>
            </div>
          </div>
          <div className="form-box" style={{ marginTop: "0" }}>
            <div style={{ fontWeight: 600, color: "var(--gold)", marginBottom: "10px", fontSize: ".9rem" }}>📝 JSON matnini to'g'ridan kiritish</div>
            <textarea className="fta" rows={8} placeholder='[{"exam":"SAT","subject":"Math",...}]'
              id="bulk-text-input" style={{ fontFamily: "monospace", fontSize: ".78rem" }} />
            <button className="sv-btn" onClick={() => {
              const val = document.getElementById("bulk-text-input")?.value;
              if (val) parseAndLoad(val);
            }}>📥 Yuklash</button>
          </div>
        </div>
      )}

      {/* STATS */}
      {tab === "stats" && (
        <div>
          <div className="sg">
            <div className="sc"><div className="snum gd">{questions.length}</div><div className="slbl">Jami savollar</div></div>
            <div className="sc"><div className="snum pk">{questions.filter(q => q.exam === "SAT").length}</div><div className="slbl">SAT</div></div>
            <div className="sc"><div className="snum cy">{questions.filter(q => q.exam === "IELTS").length}</div><div className="slbl">IELTS</div></div>
            <div className="sc"><div className="snum gr">{questions.filter(q => q.exam === "Multilevel").length}</div><div className="slbl">Multilevel</div></div>
          </div>
          <div className="prog-card">
            <div style={{ fontFamily: "var(--font3)", fontSize: ".72rem", color: "var(--muted)", marginBottom: "14px", letterSpacing: "1px" }}>IMTIHON BO'YICHA</div>
            {[["SAT", "pk"], ["IELTS", "cy"], ["Multilevel", "gr"]].map(([exam, col]) => {
              const cnt = questions.filter(q => q.exam === exam).length;
              const pct = questions.length ? Math.round(cnt / questions.length * 100) : 0;
              return (
                <div className="prog-row" key={exam}>
                  <div className="prog-top"><span>{exam}</span><span>{cnt} ta ({pct}%)</span></div>
                  <div className="pbar"><div className={`pfill ${col}`} style={{ width: `${pct}%` }} /></div>
                </div>
              );
            })}
          </div>
        </div>
      )}
    </div>
  );
}

// ════════════════════════════════════════════════════════════
// ONBOARDING
// ════════════════════════════════════════════════════════════
function Onboarding({ onDone }) {
  const [slide, setSlide] = useState(0);
  const total = ONBOARDING_SLIDES.length;
  const s = ONBOARDING_SLIDES[slide];

  return (
    <div className="onb-wrap">
      <div className="onb-logo">EXAM<span>PREP</span>.AI</div>
      <div className="onb-slide" key={slide}>
        <div className="onb-icon" style={{ color: s.accent }}>{s.icon}</div>
        <div className="onb-title" style={{ color: s.accent }}>{s.title}</div>
        <div className="onb-sub">{s.sub}</div>
      </div>
      <div className="onb-dots">
        {ONBOARDING_SLIDES.map((_, i) => (
          <div key={i} className={`onb-dot ${i === slide ? "active" : ""}`} onClick={() => setSlide(i)} />
        ))}
      </div>
      <div className="onb-btns">
        {slide > 0 && <button className="onb-btn" onClick={() => setSlide(p => p - 1)}>← Orqaga</button>}
        {slide < total - 1
          ? <button className="onb-btn primary" onClick={() => setSlide(p => p + 1)}>Keyingi →</button>
          : <button className="onb-btn primary" onClick={onDone}>🚀 Boshlash!</button>
        }
      </div>
      <div className="onb-skip" onClick={onDone}>O'tkazib yuborish</div>
    </div>
  );
}

// ════════════════════════════════════════════════════════════
// HOME
// ════════════════════════════════════════════════════════════
function HomePage({ nav }) {
  return (
    <div className="home">
      <div className="home-hero">
        <div className="hero-badge">🚀 AI-Powered · Interaktiv · Sertifikatlash</div>
        <h1 className="hero-h1">
          <span className="pk">SAT · IELTS</span><br />
          <span className="cy">Multilevel</span> ga Tayyorlik
        </h1>
        <p className="hero-p">
          Sun'iy intellekt asosidagi shaxsiy tutor bilan imtihonlarga professional darajada tayyorlaning.
          Diagnostik testlar, mock imtihonlar, AI-tutor va ekspert maslahatlari — hammasi bir joyda.
        </p>
        <div className="hero-actions">
          <button className="ha-btn main" onClick={() => nav("sat")}>📐 SAT boshlash</button>
          <button className="ha-btn sec" onClick={() => nav("ielts")}>🎓 IELTS boshlash</button>
        </div>
      </div>
      <div className="section-lbl">Imtihon bo'limlari</div>
      <div className="exam-cards">
        <div className="ec sat" onClick={() => nav("sat")}>
          <span className="ec-arrow">→</span>
          <div className="ec-icon">📐</div>
          <div className="ec-name pk">SAT</div>
          <div className="ec-desc">Math (Algebra, Geometry, Data Analysis) va English (Reading, Grammar, Vocabulary) bo'yicha Easy → Hard darajali testlar. Desmos kalkulyator bilan real imtihon muhiti.</div>
          <div className="ec-pills">
            <span className="pill pk">Math Easy/Med/Hard</span>
            <span className="pill pk">English E/M/H</span>
            <span className="pill pk">Desmos</span>
            <span className="pill pk">AI Tutor</span>
          </div>
        </div>
        <div className="ec ielts" onClick={() => nav("ielts")}>
          <span className="ec-arrow">→</span>
          <div className="ec-icon">🎓</div>
          <div className="ec-name cy">IELTS</div>
          <div className="ec-desc">4 ko'nikma bo'yicha professional tayyorgarlik. Listening strategies, Reading techniques, Writing Task 1&2 va Speaking band improvement.</div>
          <div className="ec-pills">
            <span className="pill cy">Listening</span>
            <span className="pill cy">Reading</span>
            <span className="pill cy">Writing</span>
            <span className="pill cy">Speaking</span>
          </div>
        </div>
        <div className="ec multi" onClick={() => nav("multi")}>
          <span className="ec-arrow">→</span>
          <div className="ec-icon">🌍</div>
          <div className="ec-name gr">Multilevel</div>
          <div className="ec-desc">CEFR A1 dan C2 gacha barcha darajalar. Placement test, daraja aniqlash va har bir darajaga mos testlar hamda AI tutor.</div>
          <div className="ec-pills">
            <span className="pill gr">A1 · A2</span>
            <span className="pill gr">B1 · B2</span>
            <span className="pill gr">C1 · C2</span>
            <span className="pill gr">CEFR</span>
          </div>
        </div>
      </div>
      <div className="section-lbl" style={{ marginTop: "8px" }}>💡 Ekspert maslahatlari</div>
      <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fill,minmax(260px,1fr))", gap: "12px" }}>
        {[
          { exam: "SAT", icon: "📐", text: "Math bo'limida formula sheet beriladi — ammo tezkor hisoblash uchun formulalarni yod oling." },
          { exam: "SAT", icon: "📖", text: "Reading da avval savollarni o'qing, keyin matnni skanerlang. Vaqtni tejaysiz!" },
          { exam: "IELTS", icon: "✍️", text: "Writing Task 2: Intro → Body 1 → Body 2 → Conclusion. Har qismni 4-5 jumlada yozing." },
          { exam: "IELTS", icon: "🎧", text: "Listening da audio boshlanmasdan savolni oldindan o'qib, keywords belgilang." },
          { exam: "Multilevel", icon: "📚", text: "Har kuni 20 ta yangi so'z o'rganing va ularni jumlalarda ishlating." },
          { exam: "SAT", icon: "✅", text: "SAT da noto'g'ri javob uchun minus ball yo'q — hamma savolga javob bering!" },
        ].map((t, i) => (
          <div key={i} style={{ padding: "16px", borderRadius: "14px", border: "1px solid var(--b)", background: "var(--s1)", display: "flex", gap: "12px" }}>
            <span style={{ fontSize: "1.3rem", flexShrink: 0 }}>{t.icon}</span>
            <div>
              <div style={{ fontSize: ".68rem", fontWeight: 700, letterSpacing: "1px", textTransform: "uppercase", marginBottom: "4px", color: t.exam === "SAT" ? "var(--pink2)" : t.exam === "IELTS" ? "var(--cyan)" : "var(--green)" }}>{t.exam}</div>
              <div style={{ fontSize: ".8rem", color: "var(--muted)", lineHeight: "1.55" }}>{t.text}</div>
            </div>
          </div>
        ))}
      </div>
    </div>
  );
}

// ════════════════════════════════════════════════════════════
// ROOT APP
// ════════════════════════════════════════════════════════════
function App() {
  const [page, setPage] = useState("onboarding");
  const [extraQ, setExtraQ] = useState([]);

  const nav = (p) => setPage(p);

  const navItems = [
    { id: "home", label: "🏠 Bosh sahifa", cls: "p" },
    { id: "sat", label: "📐 SAT", cls: "p" },
    { id: "ielts", label: "🎓 IELTS", cls: "c" },
    { id: "multi", label: "🌍 Multilevel", cls: "g" },
    { id: "stats", label: "📊 Statistika", cls: "p" },
    { id: "admin", label: "⚙️ Admin", cls: "y" },
  ];

  if (page === "onboarding") return (
    <>
      <style>{CSS}</style>
      <div className="bg-wrap"><div className="bg-grid" /><div className="bg-glow g1" /><div className="bg-glow g2" /><div className="bg-glow g3" /></div>
      <div style={{ position: "relative", zIndex: 1 }}>
        <Onboarding onDone={() => nav("home")} />
      </div>
    </>
  );

  return (
    <>
      <style>{CSS}</style>
      <div className="bg-wrap"><div className="bg-grid" /><div className="bg-glow g1" /><div className="bg-glow g2" /><div className="bg-glow g3" /></div>
      <div className="app">
        <header className="hdr">
          <div className="hdr-logo">EXAM<em>PREP</em>.AI</div>
          <nav className="hdr-nav">
            {navItems.map(n => (
              <button key={n.id} className={`hnav ${page === n.id ? `on ${n.cls}` : ""}`} onClick={() => nav(n.id)}>
                {n.label}
              </button>
            ))}
          </nav>
        </header>
        <main style={{ flex: 1 }}>
          {page === "home" && <HomePage nav={nav} />}
          {page === "sat" && <SATSection extraQuestions={extraQ} />}
          {page === "ielts" && <IELTSSection extraQuestions={extraQ} />}
          {page === "multi" && <MultiSection extraQuestions={extraQ} />}
          {page === "stats" && <StatsPage />}
          {page === "admin" && <AdminPage questions={extraQ} setQuestions={setExtraQ} />}
        </main>
      </div>
    </>
  );
}


ReactDOM.createRoot(document.getElementById('root')).render(React.createElement(App));
</script>
</body>
</html>