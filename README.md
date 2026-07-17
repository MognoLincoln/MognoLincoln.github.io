<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Relatório de Medição</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
</head>
<body class="bg-gray-100 min-h-screen py-8 flex flex-col">
    <div id="conteudo-pdf" class="max-w-3xl mx-auto bg-white p-4 md:p-8 shadow-md w-full">
        <div class="border-b-2 border-gray-800 pb-4 mb-6 flex flex-col md:flex-row items-center justify-between gap-4">
            <div class="flex-shrink-0">
                <img src="https://wsrv.nl/?url=mognodesign.com.br/wp-content/themes/mognodesign/assets/img/logo-footer.png" crossorigin="anonymous" alt="Mogno Home Design" class="h-14 object-contain">
            </div>
            <div class="text-center md:text-right">
                <h1 class="text-xl md:text-2xl font-bold text-gray-800 uppercase tracking-wide">Relatório de Medição Técnica</h1>
                <p class="text-gray-500 text-sm mt-1">Comprovação de visita e validação de medidas</p>
            </div>
        </div>
        <form class="space-y-4">
            <div class="bg-gray-50 p-2 font-bold border-l-4 border-blue-500 text-gray-700 mb-2 text-sm">1. Dados do Cliente e do Projeto</div>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-3">
                <div class="col-span-1 md:col-span-2">
                    <label class="block text-xs font-bold text-gray-700 mb-1">Cliente:</label>
                    <input type="text" class="w-full border-b border-gray-400 bg-transparent focus:outline-none focus:border-blue-500 py-1 text-sm" placeholder="Nome do cliente ou empresa">
                </div>
                <div>
                    <label class="block text-xs font-bold text-gray-700 mb-1">Data da Medição:</label>
                    <input type="date" class="w-full border-b border-gray-400 bg-transparent focus:outline-none focus:border-blue-500 py-1 text-sm">
                </div>
                <div>
                    <label class="block text-xs font-bold text-gray-700 mb-1">Ambiente(s) (ex: Hall):</label>
                    <input type="text" class="w-full border-b border-gray-400 bg-transparent focus:outline-none focus:border-blue-500 py-1 text-sm" placeholder="Quarto, Cozinha, Sala...">
                </div>
            </div>
            <div class="bg-gray-50 p-2 font-bold border-l-4 border-blue-500 text-gray-700 mt-4 mb-2 text-sm">2. Equipe e Responsáveis</div>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-3">
                <div>
                    <label class="block text-xs font-bold text-gray-700 mb-1">Responsável pela Obra no Local:</label>
                    <input type="text" class="w-full border-b border-gray-400 bg-transparent focus:outline-none focus:border-blue-500 py-1 text-sm">
                </div>
                <div>
                    <label class="block text-xs font-bold text-gray-700 mb-1">Medidor (Técnico):</label>
                    <input type="text" class="w-full border-b border-gray-400 bg-transparent focus:outline-none focus:border-blue-500 py-1 text-sm">
                </div>
                <div class="col-span-1 md:col-span-2">
                    <label class="block text-xs font-bold text-gray-700 mb-1">Supervisor:</label>
                    <input type="text" class="w-full border-b border-gray-400 bg-transparent focus:outline-none focus:border-blue-500 py-1 text-sm">
                </div>
            </div>
            <div class="bg-gray-50 p-2 font-bold border-l-4 border-blue-500 text-gray-700 mt-4 mb-2 text-sm">3. Status da Visita</div>
            <div class="space-y-2">
                <label class="flex items-start space-x-2 cursor-pointer">
                    <input type="radio" name="status" class="mt-1 h-4 w-4 text-blue-600">
                    <span class="text-xs text-gray-800"><strong>Medição Concluída e Aprovada:</strong> Todas as medidas foram conferidas com sucesso, sem impedimentos, e validadas pelo responsável no local.</span>
                </label>
                <label class="flex items-start space-x-2 cursor-pointer">
                    <input type="radio" name="status" class="mt-1 h-4 w-4 text-blue-600">
                    <span class="text-xs text-gray-800"><strong>Tentativa de Medição (Impedimento):</strong> A equipe compareceu ao local, mas a medição não pôde ser realizada/concluída.</span>
                </label>
            </div>
            <div class="bg-gray-50 p-2 font-bold border-l-4 border-blue-500 text-gray-700 mt-6 mb-2 text-sm">4. Observações / Motivo de Impedimento</div>
            <div>
                <textarea class="w-full border border-gray-300 rounded p-2 focus:outline-none focus:border-blue-500 text-sm" rows="5" placeholder="Descreva aqui os detalhes, se houver muitos..."></textarea>
            </div>
            <div style="page-break-before: always; break-before: page; page-break-inside: avoid;" class="pt-6">
                <div class="text-[11px] text-gray-600 text-justify bg-gray-50 p-3 rounded border border-gray-200 leading-snug">
                    <strong class="text-gray-800 text-xs">Termo de Aceite / Ciência de Visita:</strong><br>
                    Declaro para os devidos fins que acompanhei a visita técnica da equipe no ambiente supracitado. Em caso de <strong>medição concluída</strong>, atesto que o ambiente encontra-se liberado e aprovo as marcações realizadas, autorizando a sequência do projeto. Em caso de <strong>tentativa de medição (impedimento)</strong>, reconheço a presença da equipe na data informada, estando ciente de que o serviço não ocorreu por motivos descritos nas observações (ex: obra não finalizada, local trancado, ausência de responsável, etc.), podendo acarretar reagendamento ou custos adicionais de deslocamento.
                </div>
                <div class="mt-6 pt-6 border-t border-gray-200">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <div class="flex flex-col items-center">
                            <label class="block text-sm font-bold text-gray-700 mb-2">Assinatura do Cliente / Responsável</label>
                            <canvas id="assinatura-canvas" class="border-2 border-gray-300 rounded bg-gray-50 cursor-crosshair w-full" height="120"></canvas>
                            <span class="text-xs text-gray-500 mt-1">Atesta o acompanhamento da visita</span>
                        </div>
                        <div class="flex flex-col items-center">
                            <label class="block text-sm font-bold text-gray-700 mb-2">Assinatura do Medidor</label>
                            <canvas id="assinatura-medidor-canvas" class="border-2 border-gray-300 rounded bg-gray-50 cursor-crosshair w-full" height="120"></canvas>
                            <span class="text-xs text-gray-500 mt-1">Responsável técnico</span>
                        </div>
                    </div>
                </div>
            </div>
            <div style="page-break-before: always; break-before: page; page-break-inside: auto;" class="pt-6">
                <div class="bg-gray-50 p-2 font-bold border-l-4 border-blue-500 text-gray-700 mb-4 text-sm flex justify-between items-center">
                    <span>5. Registro Fotográfico (Anexos)</span>
                    <label class="btn-ocultar-pdf cursor-pointer bg-blue-200 hover:bg-blue-300 text-blue-800 py-1 px-3 rounded text-xs font-bold transition-colors">
                        + Adicionar Foto
                        <input type="file" accept="image/*" multiple class="hidden" onchange="adicionarFotos(event)">
                    </label>
                </div>                
                <div id="galeria-fotos" class="grid grid-cols-1 sm:grid-cols-1 gap-4">
                </div>
                <p id="texto-sem-foto" class="text-xs text-gray-400 italic text-center mt-4">Nenhuma foto anexada até o momento.</p>
            </div>
        </form>
    </div>
    <div class="max-w-3xl mx-auto w-full px-4 mt-8 mb-8 flex flex-col sm:flex-row justify-center gap-4">
        <button onclick="limparAssinatura()" class="bg-gray-500 hover:bg-gray-600 text-white font-bold py-3 px-6 rounded-lg transition-colors text-sm w-full sm:w-auto shadow-md">
            Limpar Assinaturas
        </button>
        <button onclick="gerarPDF()" class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 px-8 rounded-lg shadow-lg transition-colors flex items-center justify-center gap-2 w-full sm:w-auto text-lg">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4" />
            </svg>
            Salvar e Gerar PDF
        </button>
    </div>
    <script>
        // Lógica de inicialização para múltiplos Canvas de Assinatura
        function initSignatureCanvas(canvasId) {
            const canvas = document.getElementById(canvasId);
            const ctx = canvas.getContext('2d');
            let isDrawing = false;
            // Ajusta a resolução interna do canvas para evitar borrado
            function resizeCanvas() {
                // 1. Salva o desenho atual (se existir) antes de redimensionar
                let imageData = null;
                if (canvas.width > 0 && canvas.height > 0) {
                    imageData = ctx.getImageData(0, 0, canvas.width, canvas.height);
                }
                const rect = canvas.getBoundingClientRect();
                canvas.width = rect.width;
                canvas.height = rect.height;                
                // Configurações do traço da caneta
                ctx.lineWidth = 2;
                ctx.lineCap = 'round';
                ctx.strokeStyle = '#000000';
                // 2. Restaura o desenho no canvas após o redimensionamento
                if (imageData) {
                    ctx.putImageData(imageData, 0, 0);
                }
            }
            window.addEventListener('resize', resizeCanvas);
            resizeCanvas();
            // Eventos para Mouse (Computador)
            canvas.addEventListener('mousedown', startDrawing);
            canvas.addEventListener('mousemove', draw);
            canvas.addEventListener('mouseup', stopDrawing);
            canvas.addEventListener('mouseout', stopDrawing);
            // Eventos para Touch (Celular/Tablet)
            canvas.addEventListener('touchstart', handleTouchStart, { passive: false });
            canvas.addEventListener('touchmove', handleTouchMove, { passive: false });
            canvas.addEventListener('touchend', stopDrawing);
            function startDrawing(e) {
                isDrawing = true;
                draw(e);
            }
            function draw(e) {
                if (!isDrawing) return;
                e.preventDefault(); // Evita que a tela role no celular enquanto assina                
                const rect = canvas.getBoundingClientRect();
                let clientX, clientY;
                if (e.type.includes('touch')) {
                    clientX = e.touches[0].clientX;
                    clientY = e.touches[0].clientY;
                } else {
                    clientX = e.clientX;
                    clientY = e.clientY;
                }
                const x = clientX - rect.left;
                const y = clientY - rect.top;
                ctx.lineTo(x, y);
                ctx.stroke();
                ctx.beginPath();
                ctx.moveTo(x, y);
            }
            function handleTouchStart(e) {
                e.preventDefault();
                isDrawing = true;
                const touch = e.touches[0];
                const mouseEvent = new MouseEvent("mousedown", {
                    clientX: touch.clientX,
                    clientY: touch.clientY
                });
                canvas.dispatchEvent(mouseEvent);
            }
            function handleTouchMove(e) {
                e.preventDefault();
                const touch = e.touches[0];
                const mouseEvent = new MouseEvent("mousemove", {
                    clientX: touch.clientX,
                    clientY: touch.clientY
                });
                canvas.dispatchEvent(mouseEvent);
            }
            function stopDrawing() {
                isDrawing = false;
                ctx.beginPath();
            }
            return {
                clear: function() {
                    ctx.clearRect(0, 0, canvas.width, canvas.height);
                },
                resize: resizeCanvas // Exposto para usarmos na geração do PDF
            };
        }
        // Inicializa os dois quadros de assinatura
        const sigCliente = initSignatureCanvas('assinatura-canvas');
        const sigMedidor = initSignatureCanvas('assinatura-medidor-canvas');
        function limparAssinatura() {
            sigCliente.clear();
            sigMedidor.clear();
        }
        function adicionarFotos(event) {
            const files = event.target.files;
            const galeria = document.getElementById('galeria-fotos');
            const textoSemFoto = document.getElementById('texto-sem-foto');
            if (files.length > 0) {
                textoSemFoto.style.display = 'none'; // Esconde o aviso de "nenhuma foto"
            }
            for (let i = 0; i < files.length; i++) {
                const file = files[i];                
                // Valida se é imagem
                if (!file.type.startsWith('image/')) continue;
                const reader = new FileReader();
                reader.onload = function(e) {
                    const div = document.createElement('div');
                    // "page-break-inside: avoid" impede que a foto seja cortada no meio durante a paginação
                    div.style.pageBreakInside = 'avoid';
                    div.className = 'relative border-2 border-gray-200 p-2 rounded bg-white shadow-sm flex justify-center items-center';                    
                    div.innerHTML = `
                        <img src="${e.target.result}" class="max-w-full h-auto max-h-[400px] object-contain rounded">
                        <button type="button" onclick="this.parentElement.remove(); verificarGaleriaVazia();" class="btn-remover-foto absolute top-2 right-2 bg-red-600 text-white rounded-full w-8 h-8 flex items-center justify-center font-bold shadow-md hover:bg-red-700">X</button>
                    `;
                    galeria.appendChild(div);
                };
                reader.readAsDataURL(file);
            }
            // Limpa o input para permitir selecionar a mesma foto novamente, se necessário
            event.target.value = '';
        }
        function verificarGaleriaVazia() {
            const galeria = document.getElementById('galeria-fotos');
            const textoSemFoto = document.getElementById('texto-sem-foto');
            if (galeria.children.length === 0) {
                textoSemFoto.style.display = 'block';
            }
        }
        // Lógica de Geração de PDF (html2pdf)
        function gerarPDF() {
            const elemento = document.getElementById('conteudo-pdf');            
            // Pega o nome do cliente para usar no nome do arquivo
            const nomeCliente = document.querySelector('input[placeholder="Nome do cliente ou empresa"]').value || 'Cliente_Sem_Nome';
            const dataHoje = new Date().toISOString().split('T')[0];
            const nomeArquivo = `Medicao_${nomeCliente}_${dataHoje}.pdf`;
            // Muda o cursor para "carregando"
            document.body.style.cursor = 'wait';
            // Forçamos o navegador a setar os valores no HTML para a foto não sair em branco
            const inputs = elemento.querySelectorAll('input, textarea');
            inputs.forEach(input => {
                if (input.tagName.toLowerCase() === 'textarea') {
                    input.innerHTML = input.value;
                } else if (input.type === 'radio' || input.type === 'checkbox') {
                    if (input.checked) input.setAttribute('checked', 'checked');
                    else input.removeAttribute('checked');
                } else {
                    input.setAttribute('value', input.value);
                }
            });
            // Esconde os botões de "Excluir Foto" e "Adicionar Foto" para não saírem impressos no PDF
            const elementosOcultos = elemento.querySelectorAll('.btn-remover-foto, .btn-ocultar-pdf');
            elementosOcultos.forEach(el => el.style.display = 'none');
            // Configurações do PDF (Com scrollY: 0 para corrigir o gap gigante no topo)
            const opt = {
                margin:       [10, 10, 10, 10], // Margem de 10mm
                filename:     nomeArquivo,
                image:        { type: 'jpeg', quality: 0.98 },
                html2canvas:  { scale: 2, useCORS: true, scrollY: 0 }, 
                jsPDF:        { unit: 'mm', format: 'a4', orientation: 'portrait' },
                pagebreak:    { mode: ['css', 'legacy'] } // Permite quebra de página dinâmica e segura
            };            
            // Geração do arquivo (sem alterar as dimensões da página)
            html2pdf().set(opt).from(elemento).save().then(() => {
                document.body.style.cursor = 'default';                
                // Restaura os botões de "Excluir Foto" e "Adicionar Foto" na tela após terminar de baixar o PDF
                elementosOcultos.forEach(el => el.style.display = '');
            });
        }
    </script>
</body>
</html>
