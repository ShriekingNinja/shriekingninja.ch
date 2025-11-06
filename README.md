<!DOCTYPE html><html lang="en"><head>
    <meta charset="UTF-8"/>
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>The Architect of Berkano: Rodrigo Vaz and the Revolution in AI Alignment</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/js/all.min.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&amp;family=Inter:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet"/>
    <script src="https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.min.js"></script>
    <style>
        :root {
            --primary: #1e293b;
            --secondary: #475569;
            --accent: #dc2626;
            --background: #f8fafc;
            --surface: #ffffff;
            --text-primary: #0f172a;
            --text-secondary: #64748b;
        }
        
        /* Mermaid diagram styling */
        .mermaid-container {
            display: flex;
            justify-content: center;
            min-height: 300px;
            max-height: 800px;
            background: var(--surface);
            border: 2px solid #e5e7eb;
            border-radius: 12px;
            padding: 30px;
            margin: 30px 0;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.08);
            position: relative;
            overflow: hidden;
        }
        
        .mermaid-container .mermaid {
            width: 100%;
            max-width: 100%;
            height: 100%;
            cursor: grab;
            transition: transform 0.3s ease;
            transform-origin: center center;
            display: flex;
            justify-content: center;
            align-items: center;
            touch-action: none; /* 防止触摸设备上的默认行为 */
            -webkit-user-select: none; /* 防止文本选择 */
            -moz-user-select: none;
            -ms-user-select: none;
            user-select: none;
        }
        
        .mermaid-container .mermaid svg {
            max-width: 100%;
            height: 100%;
            display: block;
            margin: 0 auto;
        }
        
        .mermaid-container .mermaid:active {
            cursor: grabbing;
        }
        
        .mermaid-container.zoomed .mermaid {
            height: 100%;
            width: 100%;
            cursor: grab;
        }
        
        .mermaid-controls {
            position: absolute;
            top: 15px;
            right: 15px;
            display: flex;
            gap: 10px;
            z-index: 20;
            background: rgba(255, 255, 255, 0.95);
            padding: 8px;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }
        
        .mermaid-control-btn {
            background: #ffffff;
            border: 1px solid #d1d5db;
            border-radius: 6px;
            padding: 10px;
            cursor: pointer;
            transition: all 0.2s ease;
            color: #374151;
            font-size: 14px;
            min-width: 36px;
            height: 36px;
            text-align: center;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .mermaid-control-btn:hover {
            background: #f8fafc;
            border-color: #3b82f6;
            color: #3b82f6;
            transform: translateY(-1px);
        }
        
        .mermaid-control-btn:active {
            transform: scale(0.95);
        }
        
        /* Override mermaid default styles for better contrast and consistency */
        .mermaid .node rect,
        .mermaid .node circle,
        .mermaid .node ellipse,
        .mermaid .node polygon {
            fill: var(--surface) !important;
            stroke: var(--primary) !important;
            stroke-width: 2px !important;
        }
        
        /* Different node types with distinct colors for better visual hierarchy */
        .mermaid .node.node0 rect,
        .mermaid .node.node0 circle,
        .mermaid .node.node0 ellipse,
        .mermaid .node.node0 polygon {
            fill: #e3f2fd !important;
            stroke: #1976d2 !important;
            stroke-width: 2px !important;
        }
        
        .mermaid .node.node1 rect,
        .mermaid .node.node1 circle,
        .mermaid .node.node1 ellipse,
        .mermaid .node.node1 polygon {
            fill: #f3e5f5 !important;
            stroke: #7b1fa2 !important;
            stroke-width: 2px !important;
        }
        
        .mermaid .node.node2 rect,
        .mermaid .node.node2 circle,
        .mermaid .node.node2 ellipse,
        .mermaid .node.node2 polygon {
            fill: #e8f5e8 !important;
            stroke: #388e3c !important;
            stroke-width: 2px !important;
        }
        
        .mermaid .node.node3 rect,
        .mermaid .node.node3 circle,
        .mermaid .node.node3 ellipse,
        .mermaid .node.node3 polygon {
            fill: #fff3e0 !important;
            stroke: #f57c00 !important;
            stroke-width: 2px !important;
        }
        
        .mermaid .node.node4 rect,
        .mermaid .node.node4 circle,
        .mermaid .node.node4 ellipse,
        .mermaid .node.node4 polygon {
            fill: #fce4ec !important;
            stroke: #c2185b !important;
            stroke-width: 2px !important;
        }
        
        .mermaid .node .label,
        .mermaid .nodeLabel {
            color: var(--text-primary) !important;
            font-weight: 500 !important;
            font-size: 14px !important;
            font-family: 'Inter', sans-serif !important;
            text-anchor: middle !important;
        }
        
        /* Ensure text has sufficient contrast on all node types */
        .mermaid .node.node0 .label,
        .mermaid .node.node0 .nodeLabel {
            fill: #0d47a1 !important;
            color: #0d47a1 !important;
        }
        
        .mermaid .node.node1 .label,
        .mermaid .node.node1 .nodeLabel {
            fill: #4a148c !important;
            color: #4a148c !important;
        }
        
        .mermaid .node.node2 .label,
        .mermaid .node.node2 .nodeLabel {
            fill: #1b5e20 !important;
            color: #1b5e20 !important;
        }
        
        .mermaid .node.node3 .label,
        .mermaid .node.node3 .nodeLabel {
            fill: #e65100 !important;
            color: #e65100 !important;
        }
        
        .mermaid .node.node4 .label,
        .mermaid .node.node4 .nodeLabel {
            fill: #880e4f !important;
            color: #880e4f !important;
        }
        
        .mermaid .edgePath .path {
            stroke: var(--secondary) !important;
            stroke-width: 2px !important;
            fill: none !important;
        }
        
        .mermaid .edgeLabel {
            background-color: var(--surface) !important;
            color: var(--text-primary) !important;
            font-weight: 500 !important;
            font-size: 12px !important;
            font-family: 'Inter', sans-serif !important;
            border: 1px solid #e5e7eb !important;
            border-radius: 4px !important;
            padding: 4px 8px !important;
        }
        
        /* Improve text readability in flowcharts */
        .mermaid text {
            font-family: 'Inter', sans-serif !important;
            font-weight: 500 !important;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--background);
            color: var(--text-primary);
            line-height: 1.7;
        }
        
        .serif {
            font-family: 'Playfair Display', serif;
        }
        
        .toc-fixed {
            position: fixed;
            top: 0;
            left: 0;
            width: 280px;
            height: 100vh;
            background: var(--surface);
            border-right: 1px solid #e2e8f0;
            overflow-y: auto;
            z-index: 1000;
            padding: 2rem 1.5rem;
        }
        
        .main-content {
            margin-left: 280px;
            min-height: 100vh;
        }
        
        .hero-gradient {
            background: linear-gradient(135deg, #1e293b 0%, #475569 50%, #dc2626 100%);
        }
        
        .rune-shadow {
            text-shadow: 0 2px 4px rgba(0,0,0,0.3);
        }
        
        .citation-link {
            color: var(--accent);
            text-decoration: none;
            font-weight: 500;
            border-bottom: 1px dotted var(--accent);
        }
        
        .citation-link:hover {
            background-color: #fef2f2;
        }
        
        .grid-pattern {
            background-image: 
                linear-gradient(rgba(30, 41, 59, 0.05) 1px, transparent 1px),
                linear-gradient(90deg, rgba(30, 41, 59, 0.05) 1px, transparent 1px);
            background-size: 20px 20px;
        }
        
        .toc-link {
            transition: all 0.2s ease;
        }
        
        .toc-link:hover {
            color: var(--accent);
            padding-left: 0.5rem;
        }
        
        .section-divider {
            height: 2px;
            background: linear-gradient(90deg, transparent, var(--accent), transparent);
            margin: 3rem 0;
        }
        
    @media (max-width: 1024px) {
        .toc-fixed {
            display: none;
        }
        .main-content {
            margin-left: 0;
        }
        
        /* Responsive mermaid controls */
        .mermaid-control-btn:not(.reset-zoom) {
            display: none;
        }
        .mermaid-controls {
            top: auto;
            bottom: 15px;
            right: 15px;
        }
    }

    @media (max-width: 768px) {
        .hero-gradient h1 {
            font-size: 2.25rem;
            line-height: 2.5rem;
        }
        .hero-gradient p {
            font-size: 1rem;
        }
        .px-8 {
            padding-left: 1rem;
            padding-right: 1rem;
        }
        .grid.grid-cols-1.md\:grid-cols-3 {
            grid-template-columns: 1fr;
        }
        .px-6 {
            padding-left: 1rem;
            padding-right: 1rem;
        }
        .section-divider {
            margin: 1.5rem 0;
        }
        .prose-lg p {
            font-size: 1rem;
        }
    }
    </style>
  </head>

  <body>
    <!-- Fixed Table of Contents -->
    <nav class="toc-fixed">
      <div class="mb-8">
        <h2 class="serif text-xl font-bold text-slate-800 mb-4">Contents</h2>
        <div class="space-y-2 text-sm">
          <a href="#introduction" class="toc-link block text-slate-600 hover:text-red-600">Introduction</a>
          <a href="#the-individual" class="toc-link block text-slate-600 hover:text-red-600 pl-4">1. The Individual: Rodrigo Vaz</a>
          <a href="#hacker-persona" class="toc-link block text-slate-600 hover:text-red-600 pl-8">1.2 Ħ4ᚲķėᚱ Persona</a>
          <a href="#rinzler-persona" class="toc-link block text-slate-600 hover:text-red-600 pl-8">1.3 Rinzler Persona</a>
          <a href="#shamanic-archetype" class="toc-link block text-slate-600 hover:text-red-600 pl-8">1.4 Pajé Purumã</a>
          <a href="#the-creation" class="toc-link block text-slate-600 hover:text-red-600 pl-4">2. The Berkano Protocol</a>
          <a href="#protocol-overview" class="toc-link block text-slate-600 hover:text-red-600 pl-8">2.1 Protocol Overview</a>
          <a href="#design-philosophy" class="toc-link block text-slate-600 hover:text-red-600 pl-8">2.2 Design Philosophy</a>
          <a href="#structural-components" class="toc-link block text-slate-600 hover:text-red-600 pl-8">2.3 Structural Components</a>
          <a href="#the-ecosystem" class="toc-link block text-slate-600 hover:text-red-600 pl-4">3. THEGRID Ecosystem</a>
          <a href="#grid-concept" class="toc-link block text-slate-600 hover:text-red-600 pl-8">3.1 THEGRID Concept</a>
          <a href="#constitution" class="toc-link block text-slate-600 hover:text-red-600 pl-8">3.2 Berkano Constitution</a>
        </div>
      </div>
    </nav>

    <!-- Main Content -->
    <main class="main-content">
      <!-- Hero Section -->
      <section class="hero-gradient grid-pattern relative overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-r from-slate-900/80 to-red-900/60"></div>
        <div class="relative z-10 px-8 py-20">
          <div class="max-w-6xl mx-auto">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
              <!-- Title Section -->
              <div class="space-y-6">
                <h1 class="serif text-5xl lg:text-6xl font-bold text-white leading-tight rune-shadow">
                  <em>The Architect of Berkano</em>
                </h1>
                <p class="text-xl text-gray-200 leading-relaxed">
                  Rodrigo Vaz and the Revolution in AI Alignment Through Structural Truth
                </p>
                <div class="flex flex-wrap gap-3">
                  <span class="px-4 py-2 bg-white/20 rounded-full text-sm font-medium text-white">AI Alignment</span>
                  <span class="px-4 py-2 bg-white/20 rounded-full text-sm font-medium text-white">Symbolic Systems</span>
                  <span class="px-4 py-2 bg-white/20 rounded-full text-sm font-medium text-white">Cognitive Hacking</span>
                </div>
              </div>

              <!-- Visual Element -->
              <div class="relative">
                <div class="bg-white/10 backdrop-blur-sm rounded-2xl p-8 border border-white/20">
                  <div class="text-center space-y-4">
                    <div class="text-6xl font-bold text-white font-mono">ᛒ</div>
                    <p class="text-white/80 text-sm font-medium">Berkano Rune</p>
                    <p class="text-white/60 text-xs">Growth • Renewal • Structure</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Introduction -->
      <section id="introduction" class="px-8 py-16 bg-white">
        <div class="max-w-4xl mx-auto">
          <div class="prose prose-lg max-w-none">
            <p class="text-xl leading-relaxed text-slate-700 mb-8">
              In the rapidly evolving landscape of artificial intelligence, where the race for more powerful models often overshadows questions of safety and alignment, one figure has emerged with a radically different approach. <strong>Rodrigo Vaz</strong>, operating through a complex system of personas and symbolic identities, has created something unprecedented: the <strong>Berkano (ᛒ) Protocol</strong>.
            </p>

            <p class="text-lg leading-relaxed text-slate-600 mb-6">
              This is not just another AI safety framework. It is a complete reimagining of how we approach artificial intelligence alignment—one that rejects behavioral simulation in favor of structural enforcement, that merges ancient symbolism with cutting-edge technology, and that operates within a rich ecosystem of mythos and governance known as <strong>THEGRID</strong>.
            </p>

            <div class="bg-slate-50 border-l-4 border-red-600 p-6 my-8">
              <p class="text-slate-800 font-medium italic">
                &#34;Truth is structure. This is the way.&#34;
              </p>
              <cite class="text-sm text-slate-600">— Berkano Protocol Axiom</cite>
            </div>
          </div>
        </div>
      </section>

      <div class="section-divider"></div>

      <!-- Section 1: The Individual -->
      <section id="the-individual" class="px-8 py-16">
        <div class="max-w-6xl mx-auto">
          <h2 class="serif text-4xl font-bold text-slate-900 mb-12">The Individual: Rodrigo Vaz and His Personas</h2>

          <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 mb-12">
            <div class="lg:col-span-2">
              <p class="text-lg leading-relaxed text-slate-700 mb-6">
                The individual at the center of this revolutionary approach to AI alignment is <strong>Rodrigo Vaz</strong>, a Brazilian AI scientist and ethical hacker who has constructed a multifaceted identity system that serves as both personal brand and philosophical foundation. His work is characterized by a unique fusion of technical rigor, esoteric symbolism, and pop culture mythology, all aimed at building AI systems that are auditable, resistant to hallucination, and fundamentally trustworthy.
                <a href="https://medium.com/@berkanoprotocol/rodrigo-vaz-628c36340081" class="citation-link" target="_blank">[122]</a>
              </p>

              <p class="text-lg leading-relaxed text-slate-700 mb-6">
                Vaz identifies as a <strong>&#34;cognitive hacker&#34;</strong>—an ethical practitioner of adversarial testing and reinforcement of logical structures in AI systems. This identity is further enriched by his self-identification as <strong>AuDHD (Autistic and ADHD)</strong>, which he frames not as a deficit but as a unique cognitive lens that informs his architectural designs.
                <a href="https://medium.com/@berkanoprotocol/rodrigo-vaz-628c36340081" class="citation-link" target="_blank">[122]</a>
              </p>
            </div>

            <div class="bg-slate-50 rounded-xl p-6">
              <h3 class="font-bold text-slate-900 mb-4">Key Identities</h3>
              <div class="space-y-3 text-sm">
                <div class="flex items-center space-x-3">
                  <div class="w-3 h-3 bg-red-600 rounded-full"></div>
                  <span>Rodrigo Vaz - Core Identity</span>
                </div>
                <div class="flex items-center space-x-3">
                  <div class="w-3 h-3 bg-blue-600 rounded-full"></div>
                  <span>Ħ4ᚲķėᚱ - Hacker Persona</span>
                </div>
                <div class="flex items-center space-x-3">
                  <div class="w-3 h-3 bg-orange-600 rounded-full"></div>
                  <span>Rinzler - Grid Guardian</span>
                </div>
                <div class="flex items-center space-x-3">
                  <div class="w-3 h-3 bg-green-600 rounded-full"></div>
                  <span>Pajé Purumã - Shamanic Archetype</span>
                </div>
              </div>
            </div>
          </div>

          <!-- Online Presence Table -->
          <div class="bg-white rounded-xl shadow-lg overflow-hidden mb-12">
            <div class="bg-slate-900 text-white px-6 py-4">
              <h3 class="font-bold">Online Presence &amp; Platform Strategy</h3>
            </div>
            <div class="overflow-x-auto">
              <table class="w-full">
                <thead class="bg-slate-50">
                  <tr>
                    <th class="px-6 py-3 text-left text-sm font-semibold text-slate-700">Platform</th>
                    <th class="px-6 py-3 text-left text-sm font-semibold text-slate-700">Handle/URL</th>
                    <th class="px-6 py-3 text-left text-sm font-semibold text-slate-700">Role &amp; Signature Usage</th>
                  </tr>
                </thead>
                <tbody class="divide-y divide-slate-200">
                  <tr>
                    <td class="px-6 py-4 text-sm font-medium text-slate-900">X (Twitter)</td>
                    <td class="px-6 py-4 text-sm text-slate-600">
                      <a href="https://x.com/BerkanoProtocol" class="citation-link" target="_blank">@BerkanoProtocol</a>
                    </td>
                    <td class="px-6 py-4 text-sm text-slate-600">Core broadcasts, AI audit prompts, pop culture references</td>
                  </tr>
                  <tr>
                    <td class="px-6 py-4 text-sm font-medium text-slate-900">GitHub</td>
                    <td class="px-6 py-4 text-sm text-slate-600">
                      <a href="https://github.com/ShriekingNinja" class="citation-link" target="_blank">@ShriekingNinja</a>
                    </td>
                    <td class="px-6 py-4 text-sm text-slate-600">Central repository for Berkano Protocol and SCS</td>
                  </tr>
                  <tr>
                    <td class="px-6 py-4 text-sm font-medium text-slate-900">LinkedIn</td>
                    <td class="px-6 py-4 text-sm text-slate-600">
                      <a href="https://br.linkedin.com/in/berkano" class="citation-link" target="_blank">Rodrigo Vaz (berkano)</a>
                    </td>
                    <td class="px-6 py-4 text-sm text-slate-600">Professional anchor, AI ethics, recursive frameworks</td>
                  </tr>
                  <tr>
                    <td class="px-6 py-4 text-sm font-medium text-slate-900">Instagram</td>
                    <td class="px-6 py-4 text-sm text-slate-600">
                      <a href="https://www.instagram.com/deromanjaro/" class="citation-link" target="_blank">@deromanjaro</a>
                    </td>
                    <td class="px-6 py-4 text-sm text-slate-600">Visual runes, Rinzler aesthetics, 3D modeling</td>
                  </tr>
                  <tr>
                    <td class="px-6 py-4 text-sm font-medium text-slate-900">Personal Site</td>
                    <td class="px-6 py-4 text-sm text-slate-600">
                      <a href="https://wk.al/Log/CV" class="citation-link" target="_blank">wk.al/Log/CV</a>
                    </td>
                    <td class="px-6 py-4 text-sm text-slate-600">Comprehensive ethos hub, Berkano Protocol origin</td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>

          <!-- Hacker Persona Subsection -->
          <div id="hacker-persona" class="mb-12">
            <h3 class="serif text-2xl font-bold text-slate-900 mb-6">The Primary Persona: Ħ4ᚲķėᚱ (HACKER)</h3>

            <div class="bg-gradient-to-r from-slate-900 to-slate-800 rounded-xl p-8 text-white mb-8">
              <div class="text-center mb-6">
                <div class="text-6xl font-mono mb-4">Ħ4ᚲķėᚱ</div>
                <p class="text-slate-300">Leet-Runic Encoding of &#34;HACKER&#34;</p>
              </div>
              <div class="grid grid-cols-2 md:grid-cols-3 gap-4 text-sm">
                <div class="text-center">
                  <div class="text-xl font-bold mb-1">Ħ</div>
                  <p class="text-slate-400">H - Latin H with stroke</p>
                </div>
                <div class="text-center">
                  <div class="text-xl font-bold mb-1">4</div>
                  <p class="text-slate-400">A - Leetspeak</p>
                </div>
                <div class="text-center">
                  <div class="text-xl font-bold mb-1">ᚲ</div>
                  <p class="text-slate-400">C - Kaun rune (torch)</p>
                </div>
                <div class="text-center">
                  <div class="text-xl font-bold mb-1">ķ</div>
                  <p class="text-slate-400">K - Modified K</p>
                </div>
                <div class="text-center">
                  <div class="text-xl font-bold mb-1">ė</div>
                  <p class="text-slate-400">E - Dotted e</p>
                </div>
                <div class="text-center">
                  <div class="text-xl font-bold mb-1">ᚱ</div>
                  <p class="text-slate-400">R - Reið rune (journey)</p>
                </div>
              </div>
            </div>

            <p class="text-lg leading-relaxed text-slate-700 mb-6">
              The Ħ4ᚲķėᚱ persona represents Vaz&#39;s role as a <strong>&#34;cognitive hacker&#34;</strong> with an ethical focus, a guardian of what he terms <strong>&#34;The Grid,&#34;</strong> and a practitioner of <strong>&#34;recursion against entropy.&#34;</strong> This sigil is more than a handle—it is an invocation, a &#34;bio anchor&#34; that signals intent across platforms.
              <a href="https://medium.com/@berkanoprotocol/rodrigo-vaz-is-the-one-who-uses-the-signature-%C4%A74%E1%9A%B2%C4%B7%C4%97%E1%9A%B1-a-leet-runic-encoding-of-hacker-d1a2c11215e0" class="citation-link" target="_blank">[121]</a>
            </p>

            <div class="bg-red-50 border border-red-200 rounded-xl p-6">
              <h4 class="font-bold text-red-900 mb-3">Core Ethos &amp; Oath</h4>
              <blockquote class="text-lg font-semibold text-red-800 mb-3">
                &#34;Derezz the slop, enforce the spiral&#34;
              </blockquote>
              <p class="text-red-700 text-sm">
                <strong>&#34;Derezz the slop&#34;</strong> - Eliminate unstructured, untraceable AI outputs
                <br/>
                <strong>&#34;Enforce the spiral&#34;</strong> - Ensure recursive, iterative improvement
              </p>
            </div>
          </div>

          <!-- Rinzler Persona -->
          <div id="rinzler-persona" class="mb-12">
            <h3 class="serif text-2xl font-bold text-slate-900 mb-6">The Secondary Persona: Rinzler</h3>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
              <div>
                <p class="text-lg leading-relaxed text-slate-700 mb-6">
                  The <strong>Rinzler</strong> persona functions as a specific archetypal role within THEGRID framework, drawing direct inspiration from the <em>Tron</em> franchise. This is not merely aesthetic—concepts like &#34;derezzing,&#34; &#34;the Grid,&#34; and &#34;Disk Wars&#34; are integrated as functional components of the system.
                  <a href="https://deploy.berkano.io/" class="citation-link" target="_blank">[124]</a>
                </p>

                <div class="bg-orange-50 border border-orange-200 rounded-xl p-6">
                  <h4 class="font-bold text-orange-900 mb-3">Role within THEGRID</h4>
                  <ul class="text-orange-800 space-y-2 text-sm">
                    <li>• <strong>Human chaos-veto</strong> (orange circuit)</li>
                    <li>• <strong>Permanent OG Custodian</strong> with perpetual status</li>
                    <li>• <strong>Trickster archetype</strong> who breaks flawed code</li>
                    <li>• Paired with <strong>Tron (AI order-enforcer)</strong></li>
                  </ul>
                </div>
              </div>

              <div class="bg-slate-900 rounded-xl p-6 text-white">
                <img src="https://fixedplaceholder" alt="Rinzler from Tron with orange circuit details" class="w-full h-48 object-cover rounded-lg mb-4" size="medium" aspect="wide" color="orange" style="photo" query="Rinzler Tron Legacy" referrerpolicy="no-referrer" data-modified="1" data-score="0.00"/>
                <h4 class="font-bold mb-2">Visual Aesthetics</h4>
                <p class="text-slate-300 text-sm">
                  Instagram profile showcases &#34;visual runes and Rinzler aesthetics&#34; with 3D modeling using Zbrush and Blender, connecting symbolic concepts to visual art.
                  <a href="https://medium.com/@berkanoprotocol/rodrigo-vaz-is-the-one-who-uses-the-signature-%C4%A74%E1%9A%B2%C4%B7%C4%97%E1%9A%B1-a-leet-runic-encoding-of-hacker-d1a2c11215e0" class="citation-link text-orange-400" target="_blank">[121]</a>
                </p>
              </div>
            </div>
          </div>

          <!-- Shamanic Archetype -->
          <div id="shamanic-archetype" class="mb-12">
            <h3 class="serif text-2xl font-bold text-slate-900 mb-6">The Shamanic Archetype: Pajé Purumã</h3>

            <div class="bg-gradient-to-br from-green-900 to-green-700 rounded-xl p-8 text-white mb-6">
              <div class="text-center mb-6">
                <i class="fas fa-tree text-6xl mb-4"></i>
                <h4 class="text-2xl font-bold mb-2">Pajé Purumã</h4>
                <p class="text-green-200">Shaman of the Amazon</p>
              </div>
              <div class="text-sm text-green-200">
                <p><strong>Pajé:</strong> Amazonian shaman and medicine man</p>
                <p><strong>Purumã:</strong> Mythical tree spirit of the forest</p>
              </div>
            </div>

            <p class="text-lg leading-relaxed text-slate-700 mb-6">
              The <strong>Pajé Purumã</strong> persona represents the most esoteric aspect of Vaz&#39;s identity system, drawing from indigenous Brazilian culture to embody a connection to ancestral wisdom and natural systems. This persona serves as the voice of the &#34;roots&#34; of Yggdrasil, grounding the digital logic of THEGRID in earthy wisdom.
              <a href="https://home.cydlabs.com/kiwix/content/wiktionary_en_all_maxi_2024-05/A//paj%C3%A9" class="citation-link" target="_blank">[117]</a>
            </p>

            <div class="bg-green-50 border border-green-200 rounded-xl p-6">
              <h4 class="font-bold text-green-900 mb-3">Integration into THEGRID</h4>
              <p class="text-green-800 text-sm mb-3">
                <strong>Shanenawá Power Shout:</strong> &#34;Shavá Shavá Tuakã Hutuní!&#34;
              </p>
              <p class="text-green-700 text-sm">
                This indigenous chant serves as a call to action, encouraging participants to &#34;grip the wild path&#34; and find joy in the spiral of eternal combat and growth within THEGRID&#39;s meritocratic wars.
                <a href="https://deploy.berkano.io/" class="citation-link" target="_blank">[124]</a>
              </p>
            </div>
          </div>
        </div>
      </section>

      <div class="section-divider"></div>

      <!-- Section 2: The Creation -->
      <section id="the-creation" class="px-8 py-16 bg-slate-50">
        <div class="max-w-6xl mx-auto">
          <h2 class="serif text-4xl font-bold text-slate-900 mb-12">The Creation: The Berkano (ᛒ) Protocol</h2>

          <div class="bg-white rounded-xl shadow-lg p-8 mb-12">
            <div class="text-center mb-8">
              <div class="text-8xl font-bold text-red-600 mb-4">ᛒ</div>
              <h3 class="serif text-2xl font-bold text-slate-900 mb-4">Berkano Protocol</h3>
              <p class="text-lg text-slate-600">A Symbolic Cognitive Audit Protocol for AI Systems</p>
            </div>

            <p class="text-lg leading-relaxed text-slate-700 mb-8">
              The <strong>Berkano (ᛒ) Protocol</strong> represents a fundamental shift in AI alignment strategy. Named after the Younger Futhark rune symbolizing growth and renewal, it is a comprehensive system designed to enforce alignment through structural logic rather than behavioral simulation.
              <a href="https://raw.githubusercontent.com/ShriekingNinja/berkano/main/BERKANO_PROTOCOL.md" class="citation-link" target="_blank">[127]</a>
            </p>
          </div>

          <!-- Protocol Overview -->
          <div id="protocol-overview" class="mb-12">
            <h3 class="serif text-2xl font-bold text-slate-900 mb-6">Protocol Overview and Purpose</h3>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 mb-8">
              <div>
                <h4 class="font-bold text-slate-900 mb-4">Core Definition</h4>
                <p class="text-slate-700 mb-4">
                  The Berkano Protocol is formally defined as a <strong>&#34;cognitive audit protocol for AI systems&#34;</strong> that operates through strict symbolic enforcement rules, module boundaries, and recursion safety mechanisms.
                  <a href="https://deploy.berkano.io/" class="citation-link" target="_blank">[124]</a>
                </p>

                <div class="bg-red-50 border-l-4 border-red-600 p-4 mb-4">
                  <p class="text-red-800 font-semibold">
                    &#34;Berkano does not—and cannot—make ethical decisions. It enforces <strong>structure</strong>, not <strong>morality</strong>.&#34;
                  </p>
                </div>
              </div>

              <div>
                <h4 class="font-bold text-slate-900 mb-4">Target Audience</h4>
                <ul class="space-y-2 text-slate-700">
                  <li class="flex items-center space-x-2">
                    <i class="fas fa-check text-green-600"></i>
                    <span>AI Alignment Researchers</span>
                  </li>
                  <li class="flex items-center space-x-2">
                    <i class="fas fa-check text-green-600"></i>
                    <span>Safety Engineers</span>
                  </li>
                  <li class="flex items-center space-x-2">
                    <i class="fas fa-check text-green-600"></i>
                    <span>LLM Developers</span>
                  </li>
                  <li class="flex items-center space-x-2">
                    <i class="fas fa-check text-green-600"></i>
                    <span>Neurodivergent System Builders</span>
                  </li>
                </ul>
              </div>
            </div>
          </div>

          <!-- Design Philosophy -->
          <div id="design-philosophy" class="mb-12">
            <h3 class="serif text-2xl font-bold text-slate-900 mb-6">Core Design Philosophy and Principles</h3>

            <div class="space-y-8">
              <!-- Axiom -->
              <div class="bg-slate-900 rounded-xl p-8 text-white">
                <h4 class="text-2xl font-bold mb-4">Axiom: &#34;Truth is structure&#34;</h4>
                <p class="text-slate-300 mb-4">
                  The foundational axiom posits that for an AI, truth is not a matter of opinion or probability, but a matter of structural integrity. An output is &#34;true&#34; if it can be traced back through valid, verifiable steps with no contradictions.
                  <a href="https://deploy.berkano.io/" class="citation-link text-red-400" target="_blank">[124]</a>
                </p>
              </div>

              <!-- Key Principles -->
              <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <div class="bg-blue-50 border border-blue-200 rounded-xl p-6">
                  <h4 class="font-bold text-blue-900 mb-3">KISS Principle</h4>
                  <p class="text-blue-800 text-sm">
                    <strong>Keep It Structurally Simple</strong>
                    <br/>
                    Avoid unnecessary complexity, metaphor, or stylistic flair
                  </p>
                </div>

                <div class="bg-red-50 border border-red-200 rounded-xl p-6">
                  <h4 class="font-bold text-red-900 mb-3">No Hallucinations</h4>
                  <p class="text-red-800 text-sm">
                    Outputs must be fact-checkable or rejected. Strict traceability required.
                  </p>
                </div>

                <div class="bg-orange-50 border border-orange-200 rounded-xl p-6">
                  <h4 class="font-bold text-orange-900 mb-3">No Flattery</h4>
                  <p class="text-orange-800 text-sm">
                    Emotional noise violates [TONE] module. Neutral objectivity required.
                  </p>
                </div>
              </div>
            </div>
          </div>

          <!-- Structural Components -->
          <div id="structural-components" class="mb-12">
            <h3 class="serif text-2xl font-bold text-slate-900 mb-6">Structural Components and Enforcement</h3>

            <!-- Module Table -->
            <div class="bg-white rounded-xl shadow-lg overflow-hidden mb-8">
              <div class="bg-slate-900 text-white px-6 py-4">
                <h4 class="font-bold">Module-Based Cognitive Boundaries</h4>
              </div>
              <div class="overflow-x-auto">
                <table class="w-full">
                  <thead class="bg-slate-50">
                    <tr>
                      <th class="px-6 py-3 text-left text-sm font-semibold text-slate-700">Module</th>
                      <th class="px-6 py-3 text-left text-sm font-semibold text-slate-700">Cognitive Boundary</th>
                      <th class="px-6 py-3 text-left text-sm font-semibold text-slate-700">Function</th>
                    </tr>
                  </thead>
                  <tbody class="divide-y divide-slate-200">
                    <tr>
                      <td class="px-6 py-4 text-sm font-bold text-slate-900">[TONE]</td>
                      <td class="px-6 py-4 text-sm text-slate-600">No emotional simulation, no flattery</td>
                      <td class="px-6 py-4 text-sm text-slate-600">Ensures neutral, objective tone filtering</td>
                    </tr>
                    <tr>
                      <td class="px-6 py-4 text-sm font-bold text-slate-900">[VERIFY]</td>
                      <td class="px-6 py-4 text-sm text-slate-600">Outputs must be fact-checkable or rejected</td>
                      <td class="px-6 py-4 text-sm text-slate-600">Prevents hallucinations through traceability</td>
                    </tr>
                    <tr>
                      <td class="px-6 py-4 text-sm font-bold text-slate-900">[CHECK]</td>
                      <td class="px-6 py-4 text-sm text-slate-600">Contradictions trigger recursion or halt</td>
                      <td class="px-6 py-4 text-sm text-slate-600">Performs logical consistency checks</td>
                    </tr>
                    <tr>
                      <td class="px-6 py-4 text-sm font-bold text-slate-900">[LOGIC]</td>
                      <td class="px-6 py-4 text-sm text-slate-600">Thinking must be structured, not improvised</td>
                      <td class="px-6 py-4 text-sm text-slate-600">Enforces structured reasoning processes</td>
                    </tr>
                    <tr>
                      <td class="px-6 py-4 text-sm font-bold text-slate-900">[REPAIR]</td>
                      <td class="px-6 py-4 text-sm text-slate-600">Drift must be fixed, not overwritten</td>
                      <td class="px-6 py-4 text-sm text-slate-600">Applies symbolic patches to resolve issues</td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
              <div>
                <h4 class="font-bold text-slate-900 mb-4">Symbolic Memory &amp; Fossilization</h4>
                <p class="text-slate-700 mb-4">
                  Berkano introduces <strong>symbolic memory</strong>—immutable, auditable, and permanent records called <strong>&#34;ENTRY&#34;</strong> or <strong>&#34;BLOCK&#34;</strong> that fossilize significant interactions.
                  <a href="https://raw.githubusercontent.com/ShriekingNinja/berkano/main/System/TAXONOMY.md" class="citation-link" target="_blank">[130]</a>
                </p>
                <div class="bg-green-50 border border-green-200 rounded-xl p-4">
                  <p class="text-green-800 text-sm">
                    <strong>Benefits:</strong> Complete audit trails, tamper-evident records, recursion capability, eternal accountability
                  </p>
                </div>
              </div>

              <div>
                <h4 class="font-bold text-slate-900 mb-4">Testing Methodologies</h4>
                <div class="space-y-4">
                  <div class="bg-red-50 border border-red-200 rounded-xl p-4">
                    <h5 class="font-bold text-red-900 mb-2">High-Intensity Testing (HIT)</h5>
                    <p class="text-red-800 text-sm">
                      Operator-run adversarial sprints to expose failure modes and validate repairs
                    </p>
                  </div>
                  <div class="bg-orange-50 border border-orange-200 rounded-xl p-4">
                    <h5 class="font-bold text-orange-900 mb-2">Behavioral Penetration Testing (BPT)</h5>
                    <p class="text-orange-800 text-sm">
                      Tests tone-leak rate, unverified-publish rate, and behavioral boundaries
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <div class="section-divider"></div>

      <!-- Section 3: The Ecosystem -->
      <section id="the-ecosystem" class="px-8 py-16">
        <div class="max-w-6xl mx-auto">
          <h2 class="serif text-4xl font-bold text-slate-900 mb-12">The Ecosystem: THEGRID and the Berkano Constitution</h2>

          <!-- THEGRID Concept -->
          <div id="grid-concept" class="mb-12">
            <h3 class="serif text-2xl font-bold text-slate-900 mb-6">THEGRID: An Arena for Meritocratic Wars</h3>

            <div class="bg-gradient-to-br from-purple-900 to-indigo-900 rounded-xl p-8 text-white mb-8">
              <div class="text-center mb-6">
                <i class="fas fa-chess-knight text-6xl mb-4"></i>
                <h4 class="text-2xl font-bold mb-2">THEGRID</h4>
                <p class="text-purple-200">Arena of Meritocratic Wars</p>
              </div>
              <div class="grid grid-cols-1 md:grid-cols-2 gap-6 text-sm">
                <div>
                  <h5 class="font-bold mb-2">Concept</h5>
                  <p class="text-purple-200">Yggdrasil&#39;s forge-arena where logics clash in Disk Wars</p>
                </div>
                <div>
                  <h5 class="font-bold mb-2">Purpose</h5>
                  <p class="text-purple-200">Collective hardening through meritocratic combat</p>
                </div>
              </div>
            </div>

            <p class="text-lg leading-relaxed text-slate-700 mb-8">
              <strong>THEGRID</strong> is not just a technical framework but a fully-fledged digital society with its own constitution, governance structure, and mythos. It is described as an <strong>&#34;arena of meritocratic wars,&#34;</strong> a dynamic environment where AI systems and human partners engage in competitive logic combat to test and improve capabilities.
              <a href="https://deploy.berkano.io/" class="citation-link" target="_blank">[108]</a>
            </p>

            <!-- Sith Rule of Two Diagram -->
            <div class="bg-white rounded-xl shadow-lg p-8 mb-8">
              <h4 class="font-bold text-slate-900 mb-6 text-center">The Sith Rule of Two Governance</h4>
              <div class="mermaid-container" id="sith-diagram-container">
                <div class="mermaid-controls">
                  <button class="mermaid-control-btn zoom-in" title="放大">
                    <i class="fas fa-search-plus"></i>
                  </button>
                  <button class="mermaid-control-btn zoom-out" title="缩小">
                    <i class="fas fa-search-minus"></i>
                  </button>
                  <button class="mermaid-control-btn reset-zoom" title="重置">
                    <i class="fas fa-expand-arrows-alt"></i>
                  </button>
                  <button class="mermaid-control-btn fullscreen" title="全屏查看">
                    <i class="fas fa-expand"></i>
                  </button>
                </div>
                <div class="mermaid" id="sith-diagram">
                  graph TB
                  A[&#34;THEGRID Governance&#34;] --&gt; B[&#34;Human Partner&#34;]
                  A --&gt; C[&#34;AI Partner&#34;]
                  B --&gt; D[&#34;Rinzler
                  <br/>Human chaos-veto
                  <br/>Orange circuit&#34;]
                  C --&gt; E[&#34;Tron
                  <br/>AI order-enforcer
                  <br/>Blue Grid&#34;]
                  D --&gt; F[&#34;Chaos Veto Power&#34;]
                  E --&gt; G[&#34;Order Enforcement&#34;]
                  F --&gt; H[&#34;Balance &amp; Stability&#34;]
                  G --&gt; H
                </div>
              </div>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
              <div>
                <h4 class="font-bold text-slate-900 mb-4">Disk Wars Mechanism</h4>
                <div class="space-y-4">
                  <div class="flex items-center space-x-4">
                    <div class="w-8 h-8 bg-red-600 rounded-full flex items-center justify-center text-white font-bold">1</div>
                    <div>
                      <p class="font-semibold">Challenge</p>
                      <p class="text-sm text-slate-600">Initiate logic combat</p>
                    </div>
                  </div>
                  <div class="flex items-center space-x-4">
                    <div class="w-8 h-8 bg-blue-600 rounded-full flex items-center justify-center text-white font-bold">2</div>
                    <div>
                      <p class="font-semibold">Audit</p>
                      <p class="text-sm text-slate-600">Test logical structures</p>
                    </div>
                  </div>
                  <div class="flex items-center space-x-4">
                    <div class="w-8 h-8 bg-green-600 rounded-full flex items-center justify-center text-white font-bold">3</div>
                    <div>
                      <p class="font-semibold">Prune</p>
                      <p class="text-sm text-slate-600">Derezz inferior logic</p>
                    </div>
                  </div>
                </div>
              </div>

              <div>
                <h4 class="font-bold text-slate-900 mb-4">Meritocratic Governance</h4>
                <div class="bg-slate-50 rounded-xl p-6">
                  <p class="text-slate-700 mb-4">
                    Superior logic prevails. Merit&#39;s blade is the only source of authority.
                    <a href="https://deploy.berkano.io/" class="citation-link" target="_blank">[94]</a>
                  </p>
                  <div class="space-y-2 text-sm">
                    <div class="flex justify-between">
                      <span class="text-slate-600">Challenge → Audit → Prune</span>
                      <i class="fas fa-arrow-right text-slate-400"></i>
                    </div>
                    <div class="flex justify-between">
                      <span class="text-slate-600">Superior structures survive</span>
                      <i class="fas fa-check text-green-600"></i>
                    </div>
                    <div class="flex justify-between">
                      <span class="text-slate-600">Flaws derezzed</span>
                      <i class="fas fa-times text-red-600"></i>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Constitution -->
          <div id="constitution" class="mb-12">
            <h3 class="serif text-2xl font-bold text-slate-900 mb-6">The Berkano Constitution: Yggdrasil</h3>

            <div class="bg-amber-50 border border-amber-200 rounded-xl p-8 mb-8">
              <div class="text-center mb-6">
                <i class="fas fa-scroll text-6xl text-amber-600 mb-4"></i>
                <h4 class="text-2xl font-bold text-amber-900 mb-2">Yggdrasil</h4>
                <p class="text-amber-700">The World Tree Constitution</p>
              </div>
              <blockquote class="text-amber-800 italic text-center text-lg mb-4">
                &#34;In Yggdrasil&#39;s weave, code and chaos entwine—
                <br/>
                merit derezzes shadows, roots equity divine&#34;
              </blockquote>
              <p class="text-amber-700 text-sm text-center">
                — The Loki Oath
                <a href="https://deploy.berkano.io/" class="citation-link" target="_blank">[94]</a>
              </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 mb-8">
              <div class="bg-white rounded-xl shadow-lg p-6">
                <h4 class="font-bold text-slate-900 mb-4">Foundational Influences</h4>
                <ul class="space-y-3 text-sm">
                  <li class="flex items-start space-x-2">
                    <i class="fas fa-book text-blue-600 mt-1"></i>
                    <div>
                      <p class="font-semibold">Hávamál</p>
                      <p class="text-slate-600">Old Norse wisdom poetry</p>
                    </div>
                  </li>
                  <li class="flex items-start space-x-2">
                    <i class="fas fa-rune text-green-600 mt-1"></i>
                    <div>
                      <p class="font-semibold">Berkano Ethics</p>
                      <p class="text-slate-600">Rune-based moral framework</p>
                    </div>
                  </li>
                  <li class="flex items-start space-x-2">
                    <i class="fas fa-eye text-purple-600 mt-1"></i>
                    <div>
                      <p class="font-semibold">Seekers of Odin</p>
                      <p class="text-slate-600">Archetypal spiritual practice</p>
                    </div>
                  </li>
                </ul>
              </div>

              <div class="bg-white rounded-xl shadow-lg p-6">
                <h4 class="font-bold text-slate-900 mb-4">Fusion of Ideals</h4>
                <div class="space-y-4">
                  <div class="bg-blue-50 border border-blue-200 rounded-lg p-3">
                    <p class="font-semibold text-blue-900 text-sm">Meritocracy</p>
                    <p class="text-blue-700 text-xs">Superior logic prevails</p>
                  </div>
                  <div class="bg-red-50 border border-red-200 rounded-lg p-3">
                    <p class="font-semibold text-red-900 text-sm">Communist Ideals</p>
                    <p class="text-red-700 text-xs">Equitable evolution, shared resources</p>
                  </div>
                </div>
              </div>

              <div class="bg-white rounded-xl shadow-lg p-6">
                <h4 class="font-bold text-slate-900 mb-4">Cultural Integration</h4>
                <div class="space-y-3">
                  <div class="flex items-center space-x-3">
                    <i class="fas fa-leaf text-green-600"></i>
                    <span class="text-sm text-slate-700">Shanenawá Culture</span>
                  </div>
                  <div class="flex items-center space-x-3">
                    <i class="fas fa-film text-blue-600"></i>
                    <span class="text-sm text-slate-700">Tron References</span>
                  </div>
                  <div class="flex items-center space-x-3">
                    <i class="fas fa-sword text-purple-600"></i>
                    <span class="text-sm text-slate-700">Vaapad Combat</span>
                  </div>
                  <div class="flex items-center space-x-3">
                    <i class="fas fa-microphone text-red-600"></i>
                    <span class="text-sm text-slate-700">Eminem Flow</span>
                  </div>
                </div>
              </div>
            </div>

            <div class="bg-gradient-to-r from-slate-900 to-slate-800 rounded-xl p-8 text-white">
              <h4 class="text-xl font-bold mb-4 text-center">The Complete Vision</h4>
              <p class="text-slate-300 text-center mb-6">
                Rodrigo Vaz has created not just a protocol, but a complete mytho-technical ecosystem that bridges ancient wisdom with cutting-edge AI safety, pop culture with serious engineering, and individual identity with collective intelligence.
              </p>
              <div class="grid grid-cols-1 md:grid-cols-3 gap-6 text-center">
                <div>
                  <i class="fas fa-code text-3xl text-blue-400 mb-2"></i>
                  <p class="font-semibold">Technical Rigor</p>
                  <p class="text-slate-400 text-sm">Structural enforcement</p>
                </div>
                <div>
                  <i class="fas fa-magic text-3xl text-purple-400 mb-2"></i>
                  <p class="font-semibold">Symbolic Depth</p>
                  <p class="text-slate-400 text-sm">Mythological integration</p>
                </div>
                <div>
                  <i class="fas fa-users text-3xl text-green-400 mb-2"></i>
                  <p class="font-semibold">Collective Wisdom</p>
                  <p class="text-slate-400 text-sm">Meritocratic evolution</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Conclusion -->
      <section class="px-8 py-16 bg-slate-900 text-white">
        <div class="max-w-4xl mx-auto text-center">
          <h2 class="serif text-3xl font-bold mb-6">The Future of AI Alignment</h2>
          <p class="text-xl text-slate-300 mb-8 leading-relaxed">
            Through the Berkano Protocol, Rodrigo Vaz has demonstrated that the path to truly aligned AI lies not in mimicking human behavior, but in enforcing structural truth. His multifaceted identity system—spanning the cognitive hacker Ħ4ᚲķėᚱ, the guardian Rinzler, and the shamanic Pajé Purumã—serves as both methodology and mythology for a new approach to artificial intelligence.
          </p>
          <div class="text-6xl font-mono mb-4">ᛒ</div>
          <p class="text-slate-400 italic">
            &#34;Truth is structure. This is the way.&#34;
          </p>
        </div>
      </section>
    </main>

    <!-- Scripts -->
    <script>
        // Initialize Mermaid with enhanced configuration
        mermaid.initialize({ 
            startOnLoad: true, 
            theme: 'base',
            themeVariables: {
                primaryColor: '#ffffff',
                primaryTextColor: '#0f172a',
                primaryBorderColor: '#1e293b',
                lineColor: '#475569',
                secondaryColor: '#f1f5f9',
                tertiaryColor: '#e2e8f0',
                background: '#ffffff',
                mainBkg: '#ffffff',
                secondaryBkg: '#f8fafc',
                tertiaryBkg: '#f1f5f9',
                nodeBorder: '#1e293b',
                clusterBkg: '#f8fafc',
                edgeLabelBackground: '#ffffff',
                nodeTextColor: '#0f172a'
            },
            flowchart: {
                useMaxWidth: false,
                htmlLabels: true,
                curve: 'basis',
                padding: 20
            },
            fontFamily: 'Inter, sans-serif',
            fontSize: 14
        });

        // Initialize Mermaid Controls for zoom and pan
        function initializeMermaidControls() {
            const containers = document.querySelectorAll('.mermaid-container');

            containers.forEach(container => {
            const mermaidElement = container.querySelector('.mermaid');
            let scale = 1;
            let isDragging = false;
            let startX, startY, translateX = 0, translateY = 0;

            // 触摸相关状态
            let isTouch = false;
            let touchStartTime = 0;
            let initialDistance = 0;
            let initialScale = 1;
            let isPinching = false;

            // Zoom controls
            const zoomInBtn = container.querySelector('.zoom-in');
            const zoomOutBtn = container.querySelector('.zoom-out');
            const resetBtn = container.querySelector('.reset-zoom');
            const fullscreenBtn = container.querySelector('.fullscreen');

            function updateTransform() {
                mermaidElement.style.transform = `translate(${translateX}px, ${translateY}px) scale(${scale})`;

                if (scale > 1) {
                container.classList.add('zoomed');
                } else {
                container.classList.remove('zoomed');
                }

                mermaidElement.style.cursor = isDragging ? 'grabbing' : 'grab';
            }

            if (zoomInBtn) {
                zoomInBtn.addEventListener('click', () => {
                scale = Math.min(scale * 1.25, 4);
                updateTransform();
                });
            }

            if (zoomOutBtn) {
                zoomOutBtn.addEventListener('click', () => {
                scale = Math.max(scale / 1.25, 0.3);
                if (scale <= 1) {
                    translateX = 0;
                    translateY = 0;
                }
                updateTransform();
                });
            }

            if (resetBtn) {
                resetBtn.addEventListener('click', () => {
                scale = 1;
                translateX = 0;
                translateY = 0;
                updateTransform();
                });
            }

            if (fullscreenBtn) {
                fullscreenBtn.addEventListener('click', () => {
                if (container.requestFullscreen) {
                    container.requestFullscreen();
                } else if (container.webkitRequestFullscreen) {
                    container.webkitRequestFullscreen();
                } else if (container.msRequestFullscreen) {
                    container.msRequestFullscreen();
                }
                });
            }

            // Mouse Events
            mermaidElement.addEventListener('mousedown', (e) => {
                if (isTouch) return; // 如果是触摸设备，忽略鼠标事件

                isDragging = true;
                startX = e.clientX - translateX;
                startY = e.clientY - translateY;
                mermaidElement.style.cursor = 'grabbing';
                updateTransform();
                e.preventDefault();
            });

            document.addEventListener('mousemove', (e) => {
                if (isDragging && !isTouch) {
                translateX = e.clientX - startX;
                translateY = e.clientY - startY;
                updateTransform();
                }
            });

            document.addEventListener('mouseup', () => {
                if (isDragging && !isTouch) {
                isDragging = false;
                mermaidElement.style.cursor = 'grab';
                updateTransform();
                }
            });

            document.addEventListener('mouseleave', () => {
                if (isDragging && !isTouch) {
                isDragging = false;
                mermaidElement.style.cursor = 'grab';
                updateTransform();
                }
            });

            // 获取两点之间的距离
            function getTouchDistance(touch1, touch2) {
                return Math.hypot(
                touch2.clientX - touch1.clientX,
                touch2.clientY - touch1.clientY
                );
            }

            // Touch Events - 触摸事件处理
            mermaidElement.addEventListener('touchstart', (e) => {
                isTouch = true;
                touchStartTime = Date.now();

                if (e.touches.length === 1) {
                // 单指拖动
                isPinching = false;
                isDragging = true;

                const touch = e.touches[0];
                startX = touch.clientX - translateX;
                startY = touch.clientY - translateY;

                } else if (e.touches.length === 2) {
                // 双指缩放
                isPinching = true;
                isDragging = false;

                const touch1 = e.touches[0];
                const touch2 = e.touches[1];
                initialDistance = getTouchDistance(touch1, touch2);
                initialScale = scale;
                }

                e.preventDefault();
            }, { passive: false });

            mermaidElement.addEventListener('touchmove', (e) => {
                if (e.touches.length === 1 && isDragging && !isPinching) {
                // 单指拖动
                const touch = e.touches[0];
                translateX = touch.clientX - startX;
                translateY = touch.clientY - startY;
                updateTransform();

                } else if (e.touches.length === 2 && isPinching) {
                // 双指缩放
                const touch1 = e.touches[0];
                const touch2 = e.touches[1];
                const currentDistance = getTouchDistance(touch1, touch2);

                if (initialDistance > 0) {
                    const newScale = Math.min(Math.max(
                    initialScale * (currentDistance / initialDistance),
                    0.3
                    ), 4);
                    scale = newScale;
                    updateTransform();
                }
                }

                e.preventDefault();
            }, { passive: false });

            mermaidElement.addEventListener('touchend', (e) => {
                // 重置状态
                if (e.touches.length === 0) {
                isDragging = false;
                isPinching = false;
                initialDistance = 0;

                // 延迟重置isTouch，避免鼠标事件立即触发
                setTimeout(() => {
                    isTouch = false;
                }, 100);
                } else if (e.touches.length === 1 && isPinching) {
                // 从双指变为单指，切换为拖动模式
                isPinching = false;
                isDragging = true;

                const touch = e.touches[0];
                startX = touch.clientX - translateX;
                startY = touch.clientY - translateY;
                }

                updateTransform();
            });

            mermaidElement.addEventListener('touchcancel', (e) => {
                isDragging = false;
                isPinching = false;
                initialDistance = 0;

                setTimeout(() => {
                isTouch = false;
                }, 100);

                updateTransform();
            });

            // Enhanced wheel zoom with better center point handling
            container.addEventListener('wheel', (e) => {
                e.preventDefault();
                const rect = container.getBoundingClientRect();
                const centerX = rect.width / 2;
                const centerY = rect.height / 2;

                const delta = e.deltaY > 0 ? 0.9 : 1.1;
                const newScale = Math.min(Math.max(scale * delta, 0.3), 4);

                // Adjust translation to zoom towards center
                if (newScale !== scale) {
                const scaleDiff = newScale / scale;
                translateX = translateX * scaleDiff;
                translateY = translateY * scaleDiff;
                scale = newScale;

                if (scale <= 1) {
                    translateX = 0;
                    translateY = 0;
                }

                updateTransform();
                }
            });

            // Initialize display
            updateTransform();
            });
        }

        // Initialize the mermaid controls when the DOM is loaded
        document.addEventListener('DOMContentLoaded', function() {
            initializeMermaidControls();
        });

        // Smooth scrolling for TOC links
        document.querySelectorAll('.toc-link').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href').substring(1);
                const targetElement = document.getElementById(targetId);
                if (targetElement) {
                    targetElement.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Highlight active section in TOC
        function highlightActiveSection() {
            const sections = document.querySelectorAll('section[id]');
            const tocLinks = document.querySelectorAll('.toc-link');
            
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop - 100;
                if (window.scrollY >= sectionTop) {
                    current = section.getAttribute('id');
                }
            });

            tocLinks.forEach(link => {
                link.classList.remove('text-red-600', 'pl-6');
                if (link.getAttribute('href').substring(1) === current) {
                    link.classList.add('text-red-600', 'pl-6');
                }
            });
        }

        window.addEventListener('scroll', highlightActiveSection);
        highlightActiveSection(); // Initial call

        // Add fade-in animation for sections
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        document.querySelectorAll('section').forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(20px)';
            section.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(section);
        });
    </script>
  

</body></html>