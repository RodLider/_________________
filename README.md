
<html lang="pt-BR" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Grupo Rodlider - Soluções Financeiras</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        brand: {
                            light: '#3b82f6',
                            DEFAULT: '#1e40af', // Blue 800
                            dark: '#1e3a8a',   // Blue 900
                        },
                        accent: {
                            DEFAULT: '#f59e0b', // Amber 500
                            hover: '#d97706',   // Amber 600
                        }
                    }
                }
            }
        }
    </script>
    <style>
        .bank-logo {
            transition: all 0.3s ease;
            filter: grayscale(100%);
            opacity: 0.6;
            cursor: default;
        }
        .bank-logo:hover {
            filter: grayscale(0%);
            opacity: 1;
            transform: translateY(-3px);
        }
        .modal-enter {
            opacity: 0;
            transform: scale(0.9);
        }
        .modal-enter-active {
            opacity: 1;
            transform: scale(1);
            transition: all 0.3s ease-out;
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-800 font-sans antialiased flex flex-col min-h-screen">

    <!-- Navbar -->
    <nav class="bg-brand-dark text-white sticky top-0 z-50 shadow-lg">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-20 items-center">
                <div class="flex items-center gap-2">
                    <i data-lucide="gem" class="w-8 h-8 text-accent"></i>
                    <span class="font-bold text-2xl tracking-wider">GRUPO RODLIDER</span>
                </div>
                <div class="hidden md:flex space-x-8 font-medium">
                    <a href="#inicio" class="hover:text-accent transition">Início</a>
                    <a href="#servicos" class="hover:text-accent transition">Serviços</a>
                    <a href="#limites" class="hover:text-accent transition">Limites de Crédito</a>
                    <a href="#parceiros" class="hover:text-accent transition">Parceiros</a>
                </div>
                <div class="md:hidden">
                    <button id="mobile-menu-btn" class="text-white hover:text-accent focus:outline-none">
                        <i data-lucide="menu" class="w-6 h-6"></i>
                    </button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <header id="inicio" class="relative bg-brand-dark text-white overflow-hidden">
        <div class="absolute inset-0 bg-black opacity-50 z-0"></div>
        <!-- Abstract Background Pattern -->
        <div class="absolute inset-0 z-0 opacity-20" style="background-image: radial-gradient(#f59e0b 1px, transparent 1px); background-size: 30px 30px;"></div>
        
        <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-24 md:py-32 flex flex-col items-center text-center">
            <h1 class="text-4xl md:text-6xl font-extrabold tracking-tight mb-6">
                Crédito Inteligente para <br>
                <span class="text-accent">Seu Crescimento</span>
            </h1>
            <p class="mt-4 text-xl md:text-2xl max-w-4xl text-gray-200 mb-10 leading-relaxed">
                Capital de giro, financiamentos, consórcios e compra de bens. Trabalhamos com os maiores bancos do mercado para garantir a melhor taxa para você.
            </p>
            
            <div class="bg-white/10 backdrop-blur-md border border-white/20 p-8 rounded-2xl shadow-2xl max-w-2xl w-full">
                <h2 class="text-2xl font-bold mb-6">Qual modalidade você gostaria?</h2>
                <div class="flex flex-col sm:flex-row gap-4 justify-center">
                    <button onclick="openModal('Pessoa Física')" class="flex-1 bg-white text-brand-dark hover:bg-gray-100 font-bold py-4 px-6 rounded-xl flex items-center justify-center gap-3 transition transform hover:scale-105 shadow-lg">
                        <i data-lucide="user" class="w-6 h-6 text-brand"></i>
                        Sou Pessoa Física
                    </button>
                    <button onclick="openModal('Pessoa Jurídica')" class="flex-1 bg-accent hover:bg-accent-hover text-brand-dark font-bold py-4 px-6 rounded-xl flex items-center justify-center gap-3 transition transform hover:scale-105 shadow-lg">
                        <i data-lucide="building-2" class="w-6 h-6"></i>
                        Sou Pessoa Jurídica
                    </button>
                </div>
            </div>
        </div>
    </header>

    <!-- Serviços Section -->
    <section id="servicos" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-gray-900 sm:text-4xl">Nossas Soluções</h2>
                <div class="w-24 h-1 bg-accent mx-auto mt-4 rounded"></div>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <!-- Serviço 1 -->
                <div class="bg-gray-50 p-8 rounded-2xl border border-gray-100 shadow-sm hover:shadow-md transition group">
                    <div class="w-14 h-14 bg-brand/10 group-hover:bg-brand/20 transition rounded-xl flex items-center justify-center mb-6">
                        <i data-lucide="briefcase" class="w-8 h-8 text-brand"></i>
                    </div>
                    <h3 class="text-2xl font-bold text-gray-900 mb-4">Capital de Giro</h3>
                    <p class="text-gray-600 leading-relaxed">
                        Injete liquidez imediata no seu negócio. Ideal para cobrir despesas operacionais, pagar fornecedores, equilibrar o fluxo de caixa ou investir em expansão rápida. Liberação ágil e sem burocracia excessiva.
                    </p>
                </div>
                
                <!-- Serviço 2 -->
                <div class="bg-gray-50 p-8 rounded-2xl border border-gray-100 shadow-sm hover:shadow-md transition group">
                    <div class="w-14 h-14 bg-accent/10 group-hover:bg-accent/20 transition rounded-xl flex items-center justify-center mb-6">
                        <i data-lucide="car-front" class="w-8 h-8 text-accent"></i>
                    </div>
                    <h3 class="text-2xl font-bold text-gray-900 mb-4">Compra de Bens</h3>
                    <p class="text-gray-600 leading-relaxed">
                        Realize a aquisição de veículos, maquinários, equipamentos ou outros bens essenciais para você ou sua empresa, com linhas de crédito estruturadas diretamente com as melhores instituições.
                    </p>
                </div>

                <!-- Serviço 3 -->
                <div class="bg-gray-50 p-8 rounded-2xl border border-gray-100 shadow-sm hover:shadow-md transition group">
                    <div class="w-14 h-14 bg-green-500/10 group-hover:bg-green-500/20 transition rounded-xl flex items-center justify-center mb-6">
                        <i data-lucide="piggy-bank" class="w-8 h-8 text-green-600"></i>
                    </div>
                    <h3 class="text-2xl font-bold text-gray-900 mb-4">Consórcio</h3>
                    <p class="text-gray-600 leading-relaxed">
                        Planeje o seu futuro e aumente seu patrimônio de forma inteligente. Cartas de crédito para imóveis, veículos pesados e leves, com parcelas que cabem no seu orçamento e sem cobrança de juros.
                    </p>
                </div>

                <!-- Serviço 4 -->
                <div class="bg-gray-50 p-8 rounded-2xl border border-gray-100 shadow-sm hover:shadow-md transition group">
                    <div class="w-14 h-14 bg-purple-500/10 group-hover:bg-purple-500/20 transition rounded-xl flex items-center justify-center mb-6">
                        <i data-lucide="badge-dollar-sign" class="w-8 h-8 text-purple-600"></i>
                    </div>
                    <h3 class="text-2xl font-bold text-gray-900 mb-4">Financiamento</h3>
                    <p class="text-gray-600 leading-relaxed">
                        Crédito rápido e facilitado para você adquirir o que precisa agora. Trabalhamos com as melhores taxas do mercado para o financiamento de veículos, imóveis e capital para projetos estruturados.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Limites Section -->
    <section id="limites" class="py-20 bg-gray-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-gray-900 sm:text-4xl">Limites de Crédito</h2>
                <p class="mt-4 text-xl text-gray-600">Condições pré-aprovadas baseadas no seu perfil</p>
                <div class="w-24 h-1 bg-accent mx-auto mt-4 rounded"></div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-4xl mx-auto">
                <!-- Card PF -->
                <div class="bg-white rounded-3xl shadow-xl overflow-hidden border-t-4 border-brand">
                    <div class="p-8 text-center bg-gray-50 border-b border-gray-100">
                        <h3 class="text-2xl font-bold text-gray-900 uppercase tracking-wide">Pessoa Física</h3>
                        <p class="text-gray-500 mt-2">Crédito pessoal, consórcios e bens</p>
                    </div>
                    <div class="p-8 text-center">
                        <p class="text-sm text-gray-500 font-semibold uppercase mb-2">Linha de Crédito de</p>
                        <div class="flex items-center justify-center gap-2">
                            <span class="text-3xl font-bold text-gray-400">R$</span>
                            <span class="text-5xl font-extrabold text-brand">50 Mil</span>
                        </div>
                        <p class="my-4 text-gray-400 font-medium">até</p>
                        <div class="flex items-center justify-center gap-2 mb-8">
                            <span class="text-3xl font-bold text-gray-400">R$</span>
                            <span class="text-5xl font-extrabold text-brand">200 Mil</span>
                        </div>
                        <button onclick="openModal('Pessoa Física')" class="w-full bg-brand hover:bg-brand-dark text-white font-bold py-4 rounded-xl transition">
                            Simular Linha PF
                        </button>
                    </div>
                </div>

                <!-- Card PJ -->
                <div class="bg-white rounded-3xl shadow-xl overflow-hidden border-t-4 border-accent relative transform md:-translate-y-4">
                    <div class="absolute top-0 right-0 bg-accent text-brand-dark font-bold text-xs py-1 px-3 rounded-bl-lg">
                        MAIS BUSCADO
                    </div>
                    <div class="p-8 text-center bg-gray-50 border-b border-gray-100">
                        <h3 class="text-2xl font-bold text-gray-900 uppercase tracking-wide">Pessoa Jurídica</h3>
                        <p class="text-gray-500 mt-2">Capital de giro e investimentos</p>
                    </div>
                    <div class="p-8 text-center">
                        <p class="text-sm text-gray-500 font-semibold uppercase mb-2">Linha de Crédito de</p>
                        <div class="flex items-center justify-center gap-2">
                            <span class="text-3xl font-bold text-gray-400">R$</span>
                            <span class="text-5xl font-extrabold text-gray-900">100 Mil</span>
                        </div>
                        <p class="my-4 text-gray-400 font-medium">até</p>
                        <div class="flex items-center justify-center gap-2 mb-8">
                            <span class="text-3xl font-bold text-gray-400">R$</span>
                            <span class="text-5xl font-extrabold text-gray-900">1 Milhão</span>
                        </div>
                        <button onclick="openModal('Pessoa Jurídica')" class="w-full bg-accent hover:bg-accent-hover text-brand-dark font-bold py-4 rounded-xl transition shadow-lg shadow-accent/30">
                            Simular Linha PJ
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Parceiros Section -->
    <section id="parceiros" class="py-16 bg-white border-y border-gray-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <h3 class="text-sm font-bold text-gray-400 tracking-widest uppercase mb-12">Trabalhamos com as melhores instituições</h3>
            
            <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 gap-x-8 gap-y-12 items-center justify-items-center">
                
                <!-- Santander -->
                <div class="bank-logo flex items-center gap-1.5 font-sans font-bold text-2xl text-[#ec0000]">
                    <i data-lucide="flame" class="fill-current w-7 h-7"></i> Santander
                </div>

                <!-- Itaú -->
                <div class="bank-logo bg-[#ec7000] text-white font-black text-xl px-4 py-2 rounded-xl">
                    itaú
                </div>

                <!-- Bradesco -->
                <div class="bank-logo flex items-center gap-1.5 font-sans font-bold text-2xl text-[#cc092f]">
                    <div class="flex flex-col gap-0.5">
                        <div class="w-5 h-2 bg-[#cc092f] rounded-t-full"></div>
                        <div class="w-5 h-2 bg-[#cc092f] rounded-b-full"></div>
                    </div>
                    bradesco
                </div>

                <!-- Inter -->
                <div class="bank-logo flex items-center gap-1 font-black text-3xl text-[#ff7a00]">
                    <i data-lucide="sun-dim" class="w-7 h-7"></i> inter
                </div>

                <!-- C6 Bank -->
                <div class="bank-logo flex items-center gap-1 text-2xl text-gray-800">
                    <span class="font-black">C6</span><span class="font-light">BANK</span>
                </div>

                <!-- Banco Daycoval -->
                <div class="bank-logo font-serif font-bold text-xl text-gray-800 leading-tight text-left border-b-2 border-gray-800 pb-1">
                    Banco<br>Daycoval
                </div>

                <!-- Creditas -->
                <div class="bank-logo flex items-center gap-1.5 font-sans font-medium text-2xl text-gray-700">
                    <i data-lucide="infinity" class="w-8 h-8 text-[#00d084]"></i> creditas
                </div>

                <!-- BV -->
                <div class="bank-logo flex items-center gap-1.5 font-black text-[#00529b]">
                    <span class="text-4xl">BV</span> <span class="text-sm font-bold mt-2">banco</span>
                </div>

                <!-- Porto Bank -->
                <div class="bank-logo flex items-center gap-1.5 font-sans font-bold text-2xl text-[#004691]">
                    <i data-lucide="flag" class="fill-current w-6 h-6 text-[#00a1fc]"></i> PortoBank
                </div>

                <!-- Safra -->
                <div class="bank-logo font-serif font-bold text-2xl text-[#002f5d] tracking-widest border-b-2 border-[#d3a550]">
                    Safra
                </div>

                <!-- Caixa -->
                <div class="bank-logo flex items-center gap-1 font-black text-2xl text-[#005ca9] md:col-span-1 lg:col-span-2 xl:col-span-1">
                    <span class="text-[#f39200] text-3xl">X</span> CAIXA
                </div>

            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-brand-dark text-gray-300 py-12 mt-auto">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 grid grid-cols-1 md:grid-cols-3 gap-8">
            <div>
                <div class="flex items-center gap-2 mb-4 text-white">
                    <i data-lucide="gem" class="w-6 h-6 text-accent"></i>
                    <span class="font-bold text-xl tracking-wider">GRUPO RODLIDER</span>
                </div>
                <p class="text-sm">Soluções financeiras inteligentes, rápidas e seguras para alavancar seus projetos, seja você pessoa física ou jurídica.</p>
            </div>
            <div>
                <h4 class="text-white font-bold mb-4 uppercase">Links Rápidos</h4>
                <ul class="space-y-2 text-sm">
                    <li><a href="#inicio" class="hover:text-accent transition">Início</a></li>
                    <li><a href="#servicos" class="hover:text-accent transition">Serviços</a></li>
                    <li><a href="#limites" class="hover:text-accent transition">Limites de Crédito</a></li>
                </ul>
            </div>
            <div>
                <h4 class="text-white font-bold mb-4 uppercase">Contato</h4>
                <ul class="space-y-3 text-sm">
                    <li class="flex items-center gap-2"><a href="https://wa.me/5598984533013" target="_blank" class="hover:text-accent transition flex items-center gap-2"><i data-lucide="phone" class="w-4 h-4"></i> (98) 98453-3013</a></li>
                    <li class="flex items-center gap-2"><i data-lucide="mail" class="w-4 h-4"></i> contato@gruporodlider.com.br</li>
                    <li class="flex items-center gap-2"><i data-lucide="map-pin" class="w-4 h-4"></i> Atendimento Nacional</li>
                </ul>
            </div>
        </div>
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 mt-12 pt-8 border-t border-gray-700 text-sm text-center">
            &copy; 2024 Grupo Rodlider. Todos os direitos reservados.
        </div>
    </footer>

    <!-- Modal (Hidden by default) -->
    <div id="contactModal" class="fixed inset-0 z-[100] hidden items-center justify-center p-4">
        <div class="absolute inset-0 bg-brand-dark/80 backdrop-blur-sm transition-opacity" onclick="closeModal()"></div>
        
        <div id="modalContent" class="relative bg-white rounded-2xl shadow-2xl w-full max-w-md p-8 modal-enter">
            <button onclick="closeModal()" class="absolute top-4 right-4 text-gray-400 hover:text-gray-600">
                <i data-lucide="x" class="w-6 h-6"></i>
            </button>
            
            <div class="text-center mb-6">
                <div class="w-16 h-16 bg-[#25D366]/20 text-[#25D366] rounded-full flex items-center justify-center mx-auto mb-4">
                    <!-- WhatsApp Icon instead of check for context -->
                    <i data-lucide="message-circle" class="w-8 h-8"></i>
                </div>
                <h3 class="text-2xl font-bold text-gray-900" id="modalTitle">Simulação</h3>
                <p class="text-gray-500 mt-2 text-sm">Preencha seus dados para conversarmos pelo WhatsApp como <strong id="modalModality" class="text-brand"></strong>.</p>
            </div>

            <form onsubmit="submitToWhatsApp(event)" class="space-y-4">
                <input type="hidden" id="formModality" name="modalidade">
                
                <div>
                    <label class="block text-sm font-medium text-gray-700 mb-1">Nome Completo</label>
                    <input type="text" id="inputNome" required class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:ring-2 focus:ring-brand focus:border-brand outline-none transition" placeholder="Seu nome">
                </div>
                
                <div>
                    <label class="block text-sm font-medium text-gray-700 mb-1">Telefone / WhatsApp</label>
                    <input type="tel" id="inputTelefone" required class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:ring-2 focus:ring-brand focus:border-brand outline-none transition" placeholder="(00) 00000-0000">
                </div>

                <div>
                    <label class="block text-sm font-medium text-gray-700 mb-1">Serviço de Interesse</label>
                    <select id="inputServico" required class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:ring-2 focus:ring-brand focus:border-brand outline-none transition bg-white">
                        <option value="" disabled selected>Selecione uma opção...</option>
                        <option value="Capital de Giro">Capital de Giro</option>
                        <option value="Compra de Bens">Compra de Bens</option>
                        <option value="Consórcio">Consórcio</option>
                        <option value="Financiamento">Financiamento</option>
                    </select>
                </div>
                
                <div>
                    <label class="block text-sm font-medium text-gray-700 mb-1">Valor Desejado (R$)</label>
                    <select id="selectValorDesejado" required onchange="handleValorChange()" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:ring-2 focus:ring-brand focus:border-brand outline-none transition bg-white mb-2">
                        <!-- Populated by JS -->
                    </select>
                    
                    <input type="text" id="inputValorCustomizado" class="hidden w-full px-4 py-3 rounded-lg border border-gray-300 focus:ring-2 focus:ring-brand focus:border-brand outline-none transition" placeholder="Digite o valor (ex: 250.000)">
                </div>

                <button type="submit" class="w-full bg-[#25D366] hover:bg-[#1ebd5c] text-white font-bold py-4 rounded-xl transition mt-4 flex justify-center items-center gap-2 shadow-lg">
                    Chamar no WhatsApp <i data-lucide="arrow-right" class="w-5 h-5"></i>
                </button>
            </form>
        </div>
    </div>

    <!-- Scripts -->
    <script>
        // Initialize Lucide Icons
        lucide.createIcons();

        // Arrays com os valores desejados
        const valoresPF = [
            "50 Mil", "70 Mil", "90 Mil", "100 Mil", "120 Mil", 
            "150 Mil", "175 Mil", "190 Mil", "200 Mil", "Mais (digitar valor)"
        ];

        const valoresPJ = [
            "100 Mil", "200 Mil", "350 Mil", "400 Mil", "500 Mil", 
            "600 Mil", "700 Mil", "800 Mil", "900 Mil", "1 Milhão", "Mais (digitar valor)"
        ];

        // Modal Logic
        const modal = document.getElementById('contactModal');
        const modalContent = document.getElementById('modalContent');
        const modalModality = document.getElementById('modalModality');
        const formModality = document.getElementById('formModality');
        const selectValorDesejado = document.getElementById('selectValorDesejado');
        const inputValorCustomizado = document.getElementById('inputValorCustomizado');

        function openModal(modality) {
            // Define os textos de modalidade
            modalModality.textContent = modality;
            formModality.value = modality;
            
            // Popula o select de valores baseado na escolha (PF ou PJ)
            selectValorDesejado.innerHTML = '<option value="" disabled selected>Selecione um valor...</option>';
            const options = modality === 'Pessoa Física' ? valoresPF : valoresPJ;
            
            options.forEach(val => {
                const opt = document.createElement('option');
                opt.value = val === "Mais (digitar valor)" ? "custom" : val;
                opt.textContent = val;
                selectValorDesejado.appendChild(opt);
            });

            // Reseta e esconde o campo customizado toda vez que abre
            inputValorCustomizado.value = '';
            inputValorCustomizado.classList.add('hidden');
            inputValorCustomizado.required = false;
            
            modal.classList.remove('hidden');
            modal.classList.add('flex');
            
            // Trigger animation
            setTimeout(() => {
                modalContent.classList.add('modal-enter-active');
            }, 10);
        }

        function closeModal() {
            modalContent.classList.remove('modal-enter-active');
            
            setTimeout(() => {
                modal.classList.add('hidden');
                modal.classList.remove('flex');
            }, 300);
        }

        // Lida com a exibição do input customizado
        function handleValorChange() {
            if (selectValorDesejado.value === 'custom') {
                inputValorCustomizado.classList.remove('hidden');
                inputValorCustomizado.required = true;
                inputValorCustomizado.focus();
            } else {
                inputValorCustomizado.classList.add('hidden');
                inputValorCustomizado.required = false;
            }
        }

        // Envio para o WhatsApp
        function submitToWhatsApp(event) {
            event.preventDefault();
            
            // Pega as informações preenchidas
            const modalidade = document.getElementById('formModality').value;
            const nome = document.getElementById('inputNome').value;
            const telefone = document.getElementById('inputTelefone').value;
            const servico = document.getElementById('inputServico').value;
            
            // Verifica o valor desejado
            let valor = selectValorDesejado.value;
            if (valor === 'custom') {
                valor = "R$ " + inputValorCustomizado.value;
            }

            // Monta a mensagem que chegará no seu WhatsApp
            const mensagem = `*Nova Solicitação - Grupo Rodlider* 🚀
            
*Modalidade:* ${modalidade}
*Nome:* ${nome}
*Telefone:* ${telefone}
*Serviço:* ${servico}
*Valor Desejado:* ${valor}

Gostaria de dar andamento na minha simulação!`;

            // Número do WhatsApp que você forneceu
            const numeroWhatsApp = "5598984533013";
            
            // Codifica o texto para formato de URL (link)
            const textoCodificado = encodeURIComponent(mensagem);
            
            // Cria o link final
            const linkWhatsApp = `https://wa.me/${numeroWhatsApp}?text=${textoCodificado}`;
            
            // Abre o WhatsApp numa nova aba
            window.open(linkWhatsApp, '_blank');
            
            // Fecha e reseta o modal no site
            closeModal();
            event.target.reset();
        }

        // Mobile Menu Logic (Simple scroll to section for single page)
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>


