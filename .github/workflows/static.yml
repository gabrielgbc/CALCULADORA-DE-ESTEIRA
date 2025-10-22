<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora de Esteira</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
        }
    </style>
</head>
<body class="min-h-screen bg-gradient-to-br from-blue-50 to-indigo-100 p-4">
    <div class="max-w-2xl mx-auto">
        <!-- Header -->
        <div class="bg-white rounded-2xl shadow-xl p-6 mb-6">
            <div class="flex items-center gap-3 mb-2">
                <svg class="w-8 h-8 text-indigo-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path>
                </svg>
                <h1 class="text-3xl font-bold text-gray-800">Calculadora de Esteira</h1>
            </div>
            <p class="text-gray-600">Calcule quantas calorias você queimou e quanto peso perdeu</p>
        </div>

        <!-- Formulário -->
        <div class="bg-white rounded-2xl shadow-xl p-6 mb-6">
            <h2 class="text-xl font-semibold text-gray-800 mb-4">Seus Dados</h2>
            
            <div class="space-y-4">
                <div>
                    <label class="block text-sm font-medium text-gray-700 mb-2">
                        Seu Peso (kg)
                    </label>
                    <input
                        type="number"
                        id="peso"
                        value="70"
                        class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indigo-500 focus:border-transparent"
                        placeholder="Ex: 70"
                    />
                </div>

                <div>
                    <label class="block text-sm font-medium text-gray-700 mb-2 flex items-center gap-2">
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <circle cx="12" cy="12" r="10"></circle>
                            <polyline points="12 6 12 12 16 14"></polyline>
                        </svg>
                        Tempo (minutos)
                    </label>
                    <input
                        type="number"
                        id="tempo"
                        value="30"
                        class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indigo-500 focus:border-transparent"
                        placeholder="Ex: 30"
                    />
                </div>

                <div>
                    <label class="block text-sm font-medium text-gray-700 mb-2 flex items-center gap-2">
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <circle cx="12" cy="12" r="10"></circle>
                            <polyline points="12 16 16 12 12 8"></polyline>
                            <line x1="8" y1="12" x2="12" y2="12"></line>
                        </svg>
                        Velocidade (mph)
                    </label>
                    <input
                        type="number"
                        step="0.1"
                        id="velocidade"
                        value="6"
                        class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indigo-500 focus:border-transparent"
                        placeholder="Ex: 6"
                    />
                </div>

                <div>
                    <label class="block text-sm font-medium text-gray-700 mb-2 flex items-center gap-2">
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <polyline points="4 15 12 9 20 15"></polyline>
                        </svg>
                        Inclinação (%)
                    </label>
                    <input
                        type="number"
                        step="0.5"
                        id="inclinacao"
                        value="15"
                        class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indigo-500 focus:border-transparent"
                        placeholder="Ex: 15"
                    />
                </div>
            </div>

            <button
                onclick="calcularCalorias()"
                class="w-full mt-6 bg-indigo-600 hover:bg-indigo-700 text-white font-semibold py-3 px-6 rounded-lg transition-colors duration-200 flex items-center justify-center gap-2"
            >
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 18.657A8 8 0 016.343 7.343S7 9 9 10c0-2 .5-5 2.986-7C14 5 16.09 5.777 17.656 7.343A7.975 7.975 0 0120 13a7.975 7.975 0 01-2.343 5.657z"></path>
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.879 16.121A3 3 0 1012.015 11L11 14H9c0 .768.293 1.536.879 2.121z"></path>
                </svg>
                Calcular Resultados
            </button>
        </div>

        <!-- Resultados -->
        <div id="resultados" class="bg-white rounded-2xl shadow-xl p-6 hidden">
            <h2 class="text-xl font-semibold text-gray-800 mb-4">Seus Resultados</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                <div class="bg-gradient-to-br from-orange-50 to-red-50 rounded-xl p-4 border border-orange-200">
                    <div class="flex items-center gap-2 mb-2">
                        <svg class="w-5 h-5 text-orange-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 18.657A8 8 0 016.343 7.343S7 9 9 10c0-2 .5-5 2.986-7C14 5 16.09 5.777 17.656 7.343A7.975 7.975 0 0120 13a7.975 7.975 0 01-2.343 5.657z"></path>
                        </svg>
                        <h3 class="font-semibold text-gray-800">Calorias Queimadas</h3>
                    </div>
                    <p class="text-3xl font-bold text-orange-600" id="calorias">0</p>
                    <p class="text-sm text-gray-600">kcal</p>
                </div>

                <div class="bg-gradient-to-br from-green-50 to-emerald-50 rounded-xl p-4 border border-green-200">
                    <div class="flex items-center gap-2 mb-2">
                        <svg class="w-5 h-5 text-green-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <polyline points="23 6 13.5 15.5 8.5 10.5 1 18"></polyline>
                            <polyline points="17 6 23 6 23 12"></polyline>
                        </svg>
                        <h3 class="font-semibold text-gray-800">Peso Perdido</h3>
                    </div>
                    <p class="text-3xl font-bold text-green-600" id="kgPerdidos">0</p>
                    <p class="text-sm text-gray-600">kg</p>
                </div>

                <div class="bg-gradient-to-br from-blue-50 to-indigo-50 rounded-xl p-4 border border-blue-200">
                    <div class="flex items-center gap-2 mb-2">
                        <svg class="w-5 h-5 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path>
                        </svg>
                        <h3 class="font-semibold text-gray-800">Intensidade (MET)</h3>
                    </div>
                    <p class="text-3xl font-bold text-blue-600" id="met">0</p>
                    <p class="text-sm text-gray-600">metabólico</p>
                </div>
                <div class="bg-gradient-to-br from-purple-50 to-pink-50 rounded-xl p-4 border border-purple-200">
                    <div class="flex items-center gap-2 mb-2">
                        <svg class="w-5 h-5 text-purple-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <circle cx="12" cy="12" r="10"></circle>
                            <polyline points="12 16 16 12 12 8"></polyline>
                        </svg>
                        <h3 class="font-semibold text-gray-800">Distância Percorrida</h3>
                    </div>
                    <p class="text-3xl font-bold text-purple-600" id="distancia">0</p>
                    <p class="text-sm text-gray-600">km</p>
                </div>
            </div>

            <div class="mt-6 p-4 bg-blue-50 rounded-lg border border-blue-200">
                <p class="text-sm text-gray-700">
                    <strong>💡 Nota:</strong> Para perder 1 kg de gordura, você precisa queimar aproximadamente 7.700 calorias através de exercícios e déficit calórico. Continue firme nos treinos! 💪
                </p>
            </div>
        </div>

        <!-- Exemplo -->
        <div class="mt-6 bg-white rounded-2xl shadow-xl p-6">
            <h3 class="font-semibold text-gray-800 mb-2">📝 Exemplo:</h3>
            <p class="text-gray-600 text-sm">
                Uma pessoa de 70 kg que caminha por 30 minutos na velocidade 6 mph (≈9.7 km/h) com inclinação de 15% queima aproximadamente <strong>350-400 calorias</strong>, o equivalente a cerca de <strong>0.05 kg</strong> de gordura por sessão.
            </p>
        </div>
    </div>

    <script>
        function calcularCalorias() {
            const peso = parseFloat(document.getElementById('peso').value);
            const tempo = parseFloat(document.getElementById('tempo').value);
            const velocidade = parseFloat(document.getElementById('velocidade').value);
            const inclinacao = parseFloat(document.getElementById('inclinacao').value);

            if (!peso || !tempo || !velocidade || peso <= 0 || tempo <= 0 || velocidade <= 0) {
                alert('Por favor, preencha todos os campos com valores válidos!');
                return;
            }

            // Cálculo do MET
            const velocidadeKmh = velocidade * 1.60934;
            
            let met;
            if (velocidadeKmh < 5) {
                met = 3.0;
            } else if (velocidadeKmh < 6.5) {
                met = 3.8;
            } else if (velocidadeKmh < 8) {
                met = 5.0;
            } else if (velocidadeKmh < 10) {
                met = 8.0;
            } else if (velocidadeKmh < 12) {
                met = 10.0;
            } else {
                met = 12.0;
            }

            const metAjustado = met + (inclinacao * 0.15);
            const tempoHoras = tempo / 60;
            const calorias = metAjustado * peso * tempoHoras;
            const kgPerdidos = calorias / 7700;
            const distancia = velocidadeKmh * tempoHoras;

            // Exibir resultados
            document.getElementById('calorias').textContent = Math.round(calorias);
            document.getElementById('kgPerdidos').textContent = kgPerdidos.toFixed(4);
            document.getElementById('met').textContent = metAjustado.toFixed(1);
            document.getElementById('distancia').textContent = distancia.toFixed(2);
            document.getElementById('resultados').classList.remove('hidden');

            // Scroll suave até os resultados
            document.getElementById('resultados').scrollIntoView({ behavior: 'smooth', block: 'nearest' });
        }
    </script>
</body>
</html>
