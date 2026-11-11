<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Bug Builder: Drag &amp; Drop Traits</title>
  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&amp;family=Fraunces:wght@600;700&amp;display=swap" rel="stylesheet">
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com/3.4.17" type="text/javascript"></script>
  <!-- Lucide Icons -->
  <script src="https://cdn.jsdelivr.net/npm/lucide@0.577.0/dist/umd/lucide.min.js" type="text/javascript"></script>
  <!-- Custom Stylesheet -->
  <link rel="stylesheet" href="style.css">
</head>
<body class="bg-[#f7f3e8]">
  <div class="page-shell w-full">
    <header class="w-full border-b border-[#d8dccd] bg-[#f7f3e8]/95">
      <div class="max-w-7xl mx-auto px-5 sm:px-8 py-5 flex flex-wrap items-center justify-between gap-4">
        <div>
          <p class="uppercase tracking-[.2em] font-bold mb-1 text-[12px] text-[#287866]">CLASSROOM GENETICS LAB</p>
          <h1 class="display font-bold leading-tight text-[32px] text-[#233b35]">Build-a-Bug</h1>
        </div>
        <div class="flex gap-2" role="group" aria-label="Choose XX or XY">
          <button type="button" data-gender="XX" aria-pressed="true" class="gender-button rounded-full px-4 py-2 border border-[#b8cbb9] bg-white font-semibold text-[13px] text-[#233b35]">Parent 1 · XX</button>
          <button type="button" data-gender="XY" aria-pressed="false" class="gender-button rounded-full px-4 py-2 border border-[#b8cbb9] bg-white font-semibold text-[13px] text-[#233b35]">Parent 2 · XY</button>
        </div>
      </div>
    </header>
    
    <main class="max-w-7xl mx-auto px-5 sm:px-8 py-7 lg:py-10">
      <div class="mb-7 max-w-3xl">
        <h2 class="display font-semibold mb-2 text-[24px] text-[#233b35]">Mix traits. Meet your new bug.</h2>
        <p class="leading-relaxed text-[16px] text-[#53665d]">Choose one version of each trait. Drag a colourful block to its matching slot, or click a block to snap it in. Watch your bug change!</p>
      </div>

      <div class="grid lg:grid-cols-[minmax(0,1.1fr)_minmax(360px,.9fr)] gap-7 lg:gap-9 items-start">
        <section aria-labelledby="traits-title">
          <div class="flex flex-wrap items-end justify-between gap-2 mb-4">
            <h2 id="traits-title" class="display font-semibold text-[24px] text-[#233b35]">Choose your traits</h2>
            <span class="text-[12px] text-[#67796d]">Allele examples: uppercase / lowercase</span>
          </div>
          
          <div class="grid sm:grid-cols-2 gap-4">
            <!-- Antennae -->
            <section class="rounded-2xl border border-[#d8dccd] p-4 bg-[#fffefa]">
              <h3 class="font-bold mb-4 text-[19px] text-[#233b35]">01 / Antennae</h3>
              <div class="grid grid-cols-2 gap-3">
                <button type="button" draggable="true" data-trait="antennae" data-value="straight" aria-pressed="true" class="block-choice tone-antennae">
                  <span class="block font-semibold text-[16px] text-white">Straight</span>
                  <span class="allele block mt-1 text-[12px] text-white/80">A_ example</span>
                </button>
                <button type="button" draggable="true" data-trait="antennae" data-value="curly" aria-pressed="false" class="block-choice tone-antennae">
                  <span class="block font-semibold text-[16px] text-white">Curly</span>
                  <span class="allele block mt-1 text-[12px] text-white/80">aa example</span>
                </button>
              </div>
            </section>

            <!-- Wings -->
            <section class="rounded-2xl border border-[#d8dccd] p-4 bg-[#fffefa]">
              <h3 class="font-bold mb-4 text-[19px] text-[#233b35]">02 / Wings</h3>
              <div class="grid grid-cols-2 gap-3">
                <button type="button" draggable="true" data-trait="wings" data-value="1" aria-pressed="true" class="block-choice tone-wings">
                  <span class="block font-semibold text-[16px] text-white">1 pair</span>
                  <span class="allele block mt-1 text-[12px] text-white/80">ww example</span>
                </button>
                <button type="button" draggable="true" data-trait="wings" data-value="2" aria-pressed="false" class="block-choice tone-wings">
                  <span class="block font-semibold text-[16px] text-white">2 pairs</span>
                  <span class="allele block mt-1 text-[12px] text-white/80">W_ example</span>
                </button>
              </div>
            </section>

            <!-- Legs -->
            <section class="rounded-2xl border border-[#d8dccd] p-4 bg-[#fffefa]">
              <h3 class="font-bold mb-4 text-[19px] text-[#233b35]">03 / Legs</h3>
              <div class="grid grid-cols-2 gap-3">
                <button type="button" draggable="true" data-trait="legs" data-value="2" aria-pressed="true" class="block-choice tone-legs">
                  <span class="block font-semibold text-[16px] text-white">2 pairs</span>
                  <span class="allele block mt-1 text-[12px] text-white/80">ll example</span>
                </button>
                <button type="button" draggable="true" data-trait="legs" data-value="3" aria-pressed="false" class="block-choice tone-legs">
                  <span class="block font-semibold text-[16px] text-white">3 pairs</span>
                  <span class="allele block mt-1 text-[12px] text-white/80">L_ example</span>
                </button>
              </div>
            </section>

            <!-- Body Pattern / Style -->
            <section class="rounded-2xl border border-[#d8dccd] p-4 bg-[#fffefa]">
              <h3 class="font-bold mb-4 text-[19px] text-[#233b35]">04 / Body Pattern</h3>
              <div class="grid grid-cols-2 gap-3">
                <button type="button" draggable="true" data-trait="body" data-value="solid" aria-pressed="true" class="block-choice tone-body">
                  <span class="block font-semibold text-[16px] text-white">Solid</span>
                  <span class="allele block mt-1 text-[12px] text-white/80">Bb example</span>
                </button>
                <button type="button" draggable="true" data-trait="body" data-value="striped" aria-pressed="false" class="block-choice tone-body">
                  <span class="block font-semibold text-[16px] text-white">Striped</span>
                  <span class="allele block mt-1 text-[12px] text-white/80">bb example</span>
                </button>
              </div>
            </section>
          </div>
        </section>

        <!-- Right Column / Bug Preview & Active Slots -->
        <section class="rounded-2xl border border-[#d8dccd] p-6 bg-[#fffefa] sticky top-6">
          <h2 class="display font-semibold mb-4 text-[20px] text-[#233b35]">Your Bug Assembly</h2>
          <div class="w-full h-48 bg-[#f0ede1] rounded-xl flex items-center justify-center mb-6 border border-[#d8dccd] relative overflow-hidden">
            <!-- Simple SVG placeholder visual representing the bug -->
            <svg class="w-32 h-32 text-[#287866]" viewBox="0 0 100 100" fill="currentColor">
              <circle cx="50" cy="50" r="25" />
              <circle cx="50" cy="25" r="15" />
            </svg>
          </div>
          
          <div class="space-y-3">
            <div class="stack-slot tone-antennae">
              <span class="slot-number">01</span>
              <span class="slot-value">Straight Antennae</span>
              <span class="slot-name">Antennae Trait</span>
            </div>
            <div class="stack-slot tone-wings">
              <span class="slot-number">02</span>
              <span class="slot-value">1 Pair Wings</span>
              <span class="slot-name">Wing Trait</span>
            </div>
          </div>
        </section>
      </div>
    </main>
  </div>
  <!-- Optional interaction script -->
  <script src="script.js"></script>
</body>
</html>
