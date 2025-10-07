<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mint & Mango | AI-Powered Business Growth</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <!-- Chosen Palette: Fresh Growth (Mint, Mango, Neutrals) -->
    <!-- Application Structure Plan: A persuasive, single-page narrative flow designed to guide users through a marketing funnel. It begins with an interactive "Pain Point Diagnosis" to create personal relevance (Attention). It then explains the core problem as an "Operational Gap" (Interest). This is followed by showcasing the tangible benefits of AI with an interactive chart and explorable service cards (Desire). A new pricing tier section allows for direct purchase (Action). The journey concludes with a soft CTA to download a learning tool, capturing leads not ready to buy (Engagement). This structure shifts from a service-based to a product-based approach, offering immediate value and purchase options. -->
    <!-- Visualization & Content Choices: 
        1. Report Info: Business pain points. Goal: Engage/Inform. Method: Interactive clickable cards. Interaction: User clicks cards representing their issues. Justification: Personalizes the problem. Method: HTML/JS.
        2. Report Info: "Operational Gap" concept. Goal: Explain. Method: Simple visual diagram. Interaction: N/A. Justification: Simplifies an abstract concept. Method: HTML/Tailwind.
        3. Report Info: Benefits of AI. Goal: Persuade/Compare. Method: Interactive Bar Chart. Interaction: Buttons switch data views. Justification: Visually demonstrates a powerful "Before vs. After." Library: Chart.js.
        4. Report Info: On-demand services. Goal: Convert. Method: 3-tier pricing table. Interaction: Click to purchase via PayPal link. Justification: Provides clear, on-demand purchase options. Method: HTML/Tailwind.
        5. Report Info: Lead Magnet. Goal: Engage/Capture Leads. Method: Downloadable "learning tool" section. Interaction: Click to download. Justification: Offers value to users not yet ready to purchase. Method: HTML.
    -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
            height: 350px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 400px;
            }
        }
        .pain-point-card.selected {
            transform: translateY(-5px) scale(1.03);
            box-shadow: 0 10px 15px -3px rgba(16, 185, 129, 0.3), 0 4px 6px -2px rgba(16, 185, 129, 0.2);
            border-color: #10B981;
        }
        .chart-btn.active {
            background-color: #F97316;
            color: white;
        }
        .pricing-card {
            transition: all 0.3s ease;
        }
        .pricing-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1);
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800">

    <header class="bg-white shadow-sm sticky top-0 z-50">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <div class="text-2xl font-bold text-slate-800">
                <span class="text-emerald-500">Mint</span> & <span class="text-orange-500">Mango</span> 🥭
            </div>
            <a href="#services" class="bg-orange-500 text-white font-bold py-2 px-4 rounded-lg hover:bg-orange-600 transition-colors">
                View Services
            </a>
        </nav>
    </header>

    <main class="container mx-auto px-6 py-12 md:py-20">
        <!-- Section 1: The Hook -->
        <section class="text-center">
            <h1 class="text-3xl md:text-5xl font-bold leading-tight">Your Old Business Playbook is Obsolete.</h1>
            <p class="mt-4 text-lg md:text-xl text-slate-600 max-w-3xl mx-auto">You're working harder than ever, but something feels stuck. Does any of this sound familiar? Click on the challenges you're facing.</p>
            <div id="pain-points-grid" class="mt-12 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Pain points will be injected here by JS -->
            </div>
        </section>

        <!-- Section 2: The Revelation -->
        <section class="mt-20 md:mt-32 text-center">
            <h2 class="text-3xl md:text-4xl font-bold">You're Not Stuck. You Have an <span class="text-orange-500">Operational Gap</span>.</h2>
            <p class="mt-4 text-lg md:text-xl text-slate-600 max-w-3xl mx-auto">These aren't separate problems. They're symptoms of a single issue that's quietly costing you money, momentum, and morale every single day.</p>
            <div class="mt-12 max-w-4xl mx-auto bg-white p-8 rounded-xl shadow-lg flex flex-col md:flex-row items-center justify-center gap-8">
                <div class="text-center">
                    <div class="text-6xl">🏃‍♂️</div>
                    <h3 class="text-xl font-bold mt-2">Maximum Effort</h3>
                    <p class="text-slate-500">Long hours, busy teams.</p>
                </div>
                <div class="text-center text-red-500">
                    <div class="text-5xl font-mono animate-pulse">💸</div>
                    <h3 class="text-xl font-bold mt-2 text-slate-700">The Gap</h3>
                    <p class="text-slate-500">Inefficiency & Leaks</p>
                </div>
                <div class="text-center">
                    <div class="text-6xl">📉</div>
                    <h3 class="text-xl font-bold mt-2">Stalled Results</h3>
                    <p class="text-slate-500">Plateaued growth.</p>
                </div>
            </div>
        </section>

        <!-- Section 3: The Solution -->
        <section class="mt-20 md:mt-32">
            <div class="text-center">
                <h2 class="text-3xl md:text-4xl font-bold">Close The Gap. Unleash Your Growth with AI.</h2>
                <p class="mt-4 text-lg md:text-xl text-slate-600 max-w-3xl mx-auto">Stop trying to fix the symptoms. We use intelligent AI solutions to fix the cause, transforming how your business operates from the ground up.</p>
            </div>
            <div class="mt-12 bg-white p-6 md:p-8 rounded-xl shadow-lg">
                <div class="flex justify-center space-x-2 md:space-x-4 mb-6">
                    <button id="btn-ops" class="chart-btn active text-sm md:text-base font-semibold py-2 px-4 rounded-lg transition-colors border border-gray-200">Operations</button>
                    <button id="btn-rev" class="chart-btn text-sm md:text-base font-semibold py-2 px-4 rounded-lg transition-colors border border-gray-200">Revenue</button>
                    <button id="btn-growth" class="chart-btn text-sm md:text-base font-semibold py-2 px-4 rounded-lg transition-colors border border-gray-200">Growth</button>
                </div>
                <div class="chart-container">
                    <canvas id="impactChart"></canvas>
                </div>
            </div>
        </section>

        <!-- Section 4: The 'How' -->
        <section class="mt-20 md:mt-32">
            <div class="text-center">
                <h2 class="text-3xl md:text-4xl font-bold">Your New AI-Powered Playbook</h2>
                <p class="mt-4 text-lg md:text-xl text-slate-600 max-w-3xl mx-auto">This isn't about chasing trends. It's about building a smarter, more resilient, and ridiculously efficient business with a strategic partner.</p>
            </div>
            <div class="mt-12 grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-white p-8 rounded-xl shadow-md border-t-4 border-emerald-400">
                    <div class="text-4xl">⚡</div>
                    <h3 class="text-xl font-bold mt-4">Super-Powered Automation</h3>
                    <p class="mt-2 text-slate-600">We identify and eliminate repetitive, time-consuming tasks, freeing your team to focus on high-impact work.</p>
                </div>
                <div class="bg-white p-8 rounded-xl shadow-md border-t-4 border-orange-400">
                    <div class="text-4xl">💡</div>
                    <h3 class="text-xl font-bold mt-4">Hidden Revenue Streams</h3>
                    <p class="mt-2 text-slate-600">Our AI tools analyze your data to uncover profitable opportunities and customer insights you're currently missing.</p>
                </div>
                <div class="bg-white p-8 rounded-xl shadow-md border-t-4 border-sky-400">
                    <div class="text-4xl">🚀</div>
                    <h3 class="text-xl font-bold mt-4">Data-Driven Strategy</h3>
                    <p class="mt-2 text-slate-600">Stop guessing. We help you build a growth strategy based on real-time data and predictive analytics.</p>
                </div>
            </div>
        </section>

        <!-- Section 5: Service Tiers -->
        <section id="services" class="mt-20 md:mt-32">
            <div class="text-center">
                <h2 class="text-3xl md:text-4xl font-bold">On-Demand AI Automation Services</h2>
                <p class="mt-4 text-lg md:text-xl text-slate-600 max-w-3xl mx-auto">Choose the deliverable that best fits your immediate needs. Purchase instantly and we'll schedule a kickoff call to begin.</p>
            </div>
            <div class="mt-12 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 items-stretch">
                <!-- Tier 1 -->
                <div class="pricing-card bg-white p-8 rounded-xl shadow-lg border-t-4 border-slate-300 flex flex-col">
                    <h3 class="text-2xl font-bold">AI Audit & Roadmap</h3>
                    <p class="text-4xl font-bold mt-4">$499</p>
                    <p class="text-slate-500">One-time purchase</p>
                    <ul class="mt-6 space-y-4 text-slate-600 flex-grow">
                        <li class="flex items-start"><span class="text-emerald-500 mr-2">✔</span> Comprehensive analysis of your current operations.</li>
                        <li class="flex items-start"><span class="text-emerald-500 mr-2">✔</span> Identification of top 3 automation opportunities.</li>
                        <li class="flex items-start"><span class="text-emerald-500 mr-2">✔</span> A detailed, step-by-step implementation roadmap.</li>
                    </ul>
                    <a href="#" class="mt-8 w-full text-center bg-slate-600 text-white font-bold py-3 px-6 rounded-lg hover:bg-slate-700 transition-colors">Purchase via PayPal</a>
                </div>
                <!-- Tier 2 - Highlighted -->
                <div class="pricing-card bg-white p-8 rounded-xl shadow-2xl border-t-4 border-orange-500 flex flex-col ring-2 ring-orange-500">
                    <p class="text-orange-500 font-bold text-sm">MOST POPULAR</p>
                    <h3 class="text-2xl font-bold mt-2">Single Process Automation</h3>
                    <p class="text-4xl font-bold mt-4">$1,200</p>
                    <p class="text-slate-500">One-time purchase</p>
                    <ul class="mt-6 space-y-4 text-slate-600 flex-grow">
                        <li class="flex items-start"><span class="text-emerald-500 mr-2">✔</span> Includes everything in the AI Audit & Roadmap.</li>
                        <li class="flex items-start"><span class="text-emerald-500 mr-2">✔</span> Full development and deployment of one key process automation.</li>
                        <li class="flex items-start"><span class="text-emerald-500 mr-2">✔</span> Team training session & documentation.</li>
                    </ul>
                    <a href="#" class="mt-8 w-full text-center bg-orange-500 text-white font-bold py-3 px-6 rounded-lg hover:bg-orange-600 transition-colors">Purchase via PayPal</a>
                </div>
                <!-- Tier 3 -->
                <div class="pricing-card bg-white p-8 rounded-xl shadow-lg border-t-4 border-slate-300 flex flex-col">
                    <h3 class="text-2xl font-bold">Growth Partner Retainer</h3>
                    <p class="text-4xl font-bold mt-4">$2,500+</p>
                    <p class="text-slate-500">Per month</p>
                    <ul class="mt-6 space-y-4 text-slate-600 flex-grow">
                        <li class="flex items-start"><span class="text-emerald-500 mr-2">✔</span> Ongoing AI strategy and implementation.</li>
                        <li class="flex items-start"><span class="text-emerald-500 mr-2">✔</span> Unlimited process automations.</li>
                        <li class="flex items-start"><span class="text-emerald-500 mr-2">✔</span> Dedicated support & monthly performance reviews.</li>
                    </ul>
                    <a href="#cta" class="mt-8 w-full text-center bg-slate-600 text-white font-bold py-3 px-6 rounded-lg hover:bg-slate-700 transition-colors">Contact Us for Custom Quote</a>
                </div>
            </div>
        </section>

        <!-- Section 6: Call to Action -->
        <section id="cta" class="mt-20 md:mt-32 bg-emerald-600 text-white rounded-2xl p-10 md:p-16 flex flex-col md:flex-row items-center gap-8">
            <div class="text-center md:text-left flex-shrink-0">
                <div class="text-6xl bg-white text-emerald-600 rounded-xl inline-block p-4">🛠️</div>
            </div>
            <div>
                <h2 class="text-3xl md:text-4xl font-bold">Get Your Free AI Growth Kit</h2>
                <p class="mt-4 text-lg md:text-xl text-emerald-100 max-w-3xl">Not ready to commit? Download our free learning tool. It includes a self-assessment checklist and a guide to identifying your first automation opportunity.</p>
                <a href="growth_kit.html" class="mt-6 inline-block bg-white text-emerald-700 font-bold text-lg py-3 px-8 rounded-lg hover:bg-slate-100 transition-colors transform hover:scale-105">
                    Download for Free
                </a>
            </div>
        </section>
    </main>

    <footer class="bg-white mt-20 md:mt-32">
        <div class="container mx-auto px-6 py-8 text-center text-slate-500">
            <p>&copy; 2025 Mint & Mango. All Rights Reserved.</p>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const painPoints = [
                {
                    icon: '👥',
                    title: 'Team is Swamped',
                    desc: 'Your best people are bogged down with repetitive "busywork" instead of innovating.'
                },
                {
                    icon: '📈',
                    title: 'Growth Has Plateaued',
                    desc: 'What used to work isn\'t working anymore, and you\'re struggling to reach the next level.'
                },
                {
                    icon: '❓',
                    title: 'Can\'t Pinpoint the Bottleneck',
                    desc: 'You know something is holding you back, but it\'s impossible to see the root cause clearly.'
                },
            ];

            const painPointsGrid = document.getElementById('pain-points-grid');
            painPoints.forEach(point => {
                const card = document.createElement('div');
                card.className = 'pain-point-card bg-white p-8 rounded-xl shadow-md hover:shadow-xl border-2 border-transparent cursor-pointer transition-all duration-300';
                card.innerHTML = `
                    <div class="text-5xl">${point.icon}</div>
                    <h3 class="text-xl font-bold mt-4">${point.title}</h3>
                    <p class="mt-2 text-slate-600">${point.desc}</p>
                `;
                card.addEventListener('click', () => {
                    card.classList.toggle('selected');
                });
                painPointsGrid.appendChild(card);
            });

            const chartData = {
                operations: {
                    labels: ['Manual Tasks', 'Operational Errors', 'Team Efficiency'],
                    before: [85, 40, 50],
                    after: [15, 5, 95]
                },
                revenue: {
                    labels: ['Lead Conversion', 'Customer Churn', 'Untapped Opportunities'],
                    before: [60, 30, 20],
                    after: [85, 10, 80]
                },
                growth: {
                    labels: ['Speed to Market', 'Decision Accuracy', 'Scalability'],
                    before: [40, 65, 50],
                    after: [90, 95, 100]
                }
            };
            
            const ctx = document.getElementById('impactChart').getContext('2d');
            let impactChart = new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: chartData.operations.labels,
                    datasets: [
                        {
                            label: 'Before AI',
                            data: chartData.operations.before,
                            backgroundColor: 'rgba(100, 116, 139, 0.6)',
                            borderColor: 'rgba(100, 116, 139, 1)',
                            borderWidth: 1,
                            borderRadius: 4
                        },
                        {
                            label: 'With Mint & Mango AI',
                            data: chartData.operations.after,
                            backgroundColor: 'rgba(16, 185, 129, 0.6)',
                            borderColor: 'rgba(16, 185, 129, 1)',
                            borderWidth: 1,
                            borderRadius: 4
                        }
                    ]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    scales: {
                        y: {
                            beginAtZero: true,
                            max: 100,
                            ticks: {
                                callback: function(value) {
                                    return value + '%'
                                }
                            }
                        }
                    },
                    plugins: {
                        legend: {
                            position: 'top',
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    let label = context.dataset.label || '';
                                    if (label) {
                                        label += ': ';
                                    }
                                    if (context.parsed.y !== null) {
                                        label += context.parsed.y + '%';
                                    }
                                    return label;
                                }
                            }
                        }
                    }
                }
            });

            const chartBtns = document.querySelectorAll('.chart-btn');
            const btnOps = document.getElementById('btn-ops');
            const btnRev = document.getElementById('btn-rev');
            const btnGrowth = document.getElementById('btn-growth');

            function updateChart(dataType) {
                const newData = chartData[dataType];
                impactChart.data.labels = newData.labels;
                impactChart.data.datasets[0].data = newData.before;
                impactChart.data.datasets[1].data = newData.after;
                impactChart.update();

                chartBtns.forEach(btn => btn.classList.remove('active'));
                document.getElementById(`btn-${dataType.slice(0,3)}`).classList.add('active');
            }

            btnOps.addEventListener('click', () => updateChart('operations'));
            btnRev.addEventListener('click', () => updateChart('revenue'));
            btnGrowth.addEventListener('click', () => updateChart('growth'));

        });
    </script>
</body>
</html>


