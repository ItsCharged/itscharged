<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ItsCharged - GitHub Profil</title>
    <!-- Tailwind CSS für responsives Layout -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Basis-Styling und Dark-Theme */
        body {
            background-color: #0d1117; /* GitHub Dark Mode Hintergrund */
            color: #c9d1d9;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
            overflow-x: hidden;
        }

        /* Smoothe Neon-Glühen Animation für den Namen */
        @keyframes neonPulse {
            0%, 100% {
                text-shadow: 0 0 5px #F7DF1E, 0 0 10px #F7DF1E, 0 0 20px #F7DF1E;
            }
            50% {
                text-shadow: 0 0 2px #F7DF1E, 0 0 5px #F7DF1E, 0 0 10px #ffaa00;
            }
        }
        .neon-text {
            color: #ffffff;
            animation: neonPulse 3s infinite alternate;
        }

        /* Ladebalken-Animation */
        @keyframes chargeUp {
            0% { width: 0%; background-color: #ef4444; box-shadow: 0 0 10px #ef4444; }
            50% { background-color: #eab308; box-shadow: 0 0 15px #eab308; }
            100% { width: 100%; background-color: #22c55e; box-shadow: 0 0 20px #22c55e; }
        }
        .battery-level {
            animation: chargeUp 4s ease-out forwards;
        }

        /* Schwebe-Animation für Karten */
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-5px); }
            100% { transform: translateY(0px); }
        }
        .floating-card {
            transition: all 0.3s ease;
        }
        .floating-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px -5px rgba(247, 223, 30, 0.2);
            border-color: #F7DF1E;
        }

        /* Lokale Stats Nummern Animation (Fade in & Scale) */
        @keyframes popIn {
            0% { opacity: 0; transform: scale(0.5); }
            100% { opacity: 1; transform: scale(1); }
        }
        .stat-number {
            animation: popIn 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
        }
    </style>
</head>
<body class="min-h-screen flex flex-col items-center py-12 px-4 sm:px-6 lg:px-8">

    <!-- Header Bereich -->
    <header class="text-center w-full max-w-3xl flex flex-col items-center animate-[popIn_1s_ease-out]">
        <!-- Profilbild (zieht automatisch das aktuelle GitHub Bild) -->
        <div class="relative w-32 h-32 mb-6">
            <div class="absolute inset-0 rounded-full border-4 border-[#F7DF1E] opacity-50 animate-ping"></div>
            <img src="https://github.com/ItsCharged.png" alt="ItsCharged Profilbild" class="relative rounded-full w-32 h-32 object-cover border-4 border-[#F7DF1E] shadow-[0_0_15px_#F7DF1E]">
        </div>

        <h1 class="text-5xl md:text-6xl font-bold tracking-tight mb-2 neon-text font-mono">
            itscharged
        </h1>
        <p class="text-xl md:text-2xl text-yellow-400 font-semibold mb-8 tracking-wider">
            ⚡ charged Up to 2000V ⚡
        </p>

        <!-- Animierter Batterie-Ladebalken -->
        <div class="w-full max-w-md bg-gray-800 rounded-full h-4 sm:h-6 mb-2 border border-gray-600 relative overflow-hidden p-0.5">
            <div class="battery-level h-full rounded-full w-0"></div>
        </div>
        <p class="text-xs text-gray-400 mb-12 font-mono">System Status: Fully Charged</p>
    </header>

    <!-- Hauptinhalt Grid -->
    <main class="w-full max-w-4xl grid grid-cols-1 md:grid-cols-2 gap-8">
        
        <!-- Info / Bio Sektion -->
        <section class="bg-[#161b22] border border-gray-700 rounded-2xl p-6 md:p-8 floating-card">
            <h2 class="text-2xl font-bold mb-6 flex items-center text-white border-b border-gray-700 pb-2">
                <span class="mr-3">🔌</span> Was mache ich?
            </h2>
            <ul class="space-y-4 text-gray-300">
                <li class="flex items-start">
                    <span class="text-yellow-400 mr-3">⚡</span>
                    <span>Ich versuche, bei anderen Repositories zu helfen und zu kollaborieren.</span>
                </li>
                <li class="flex items-start">
                    <span class="text-yellow-400 mr-3">⚡</span>
                    <span>Höchstwahrscheinlich versuche ich, Schul-Einschränkungen zu umgehen (weil sie ziemlich dumm sind).</span>
                </li>
                <li class="flex items-start">
                    <span class="text-yellow-400 mr-3">⚡</span>
                    <span>Ich programmiere mit Gemini und der Gemini CLI. Ich habe jedoch Grundkenntnisse und kann den Code normalerweise verstehen.</span>
                </li>
            </ul>
        </section>

        <!-- Lokale Stats Sektion -->
        <section class="bg-[#161b22] border border-gray-700 rounded-2xl p-6 md:p-8 floating-card flex flex-col justify-between">
            <div>
                <h2 class="text-2xl font-bold mb-2 flex items-center text-white border-b border-gray-700 pb-2">
                    <span class="mr-3">📊</span> Lokale Statistiken
                </h2>
                <p class="text-xs text-gray-400 mb-6 italic">Statistiken sind lokal gespeichert für maximale Geschwindigkeit.</p>
            </div>
            
            <div class="grid grid-cols-3 gap-4 text-center mt-auto">
                <!-- Stat: Contributions -->
                <div class="bg-[#0d1117] p-4 rounded-xl border border-gray-700 flex flex-col items-center justify-center group hover:border-[#F7DF1E] transition-colors">
                    <span class="text-xs text-gray-400 uppercase tracking-wider mb-1">Beiträge</span>
                    <span class="text-3xl font-bold text-white stat-number group-hover:text-[#F7DF1E] transition-colors" style="animation-delay: 0.2s;">88</span>
                </div>
                
                <!-- Stat: Current Streak -->
                <div class="bg-[#0d1117] p-4 rounded-xl border border-gray-700 flex flex-col items-center justify-center group hover:border-blue-400 transition-colors relative overflow-hidden">
                    <div class="absolute inset-0 bg-blue-500 opacity-5 group-hover:opacity-10 transition-opacity"></div>
                    <span class="text-xs text-gray-400 uppercase tracking-wider mb-1">Akt. Streak</span>
                    <span class="text-3xl font-bold text-blue-400 stat-number" style="animation-delay: 0.4s;">1</span>
                    <span class="text-[10px] text-gray-500 mt-1">Tag</span>
                </div>

                <!-- Stat: Longest Streak -->
                <div class="bg-[#0d1117] p-4 rounded-xl border border-gray-700 flex flex-col items-center justify-center group hover:border-purple-400 transition-colors">
                    <span class="text-xs text-gray-400 uppercase tracking-wider mb-1">Max Streak</span>
                    <span class="text-3xl font-bold text-purple-400 stat-number" style="animation-delay: 0.6s;">3</span>
                    <span class="text-[10px] text-gray-500 mt-1">Tage</span>
                </div>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer class="mt-16 text-center text-gray-500 text-sm">
        <p>⚡ Powered by HTML & CSS | Lokal gehostet ⚡</p>
    </footer>

</body>
</html>

