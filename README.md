<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fluxograma - Estrutura do Manual CEPE</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: white;
            padding: 20px;
            color: #1a3a32;
            width: 210mm; /* Tamanho A4 */
            min-height: 297mm;
            margin: 0 auto;
        }
        
        .container {
            width: 100%;
            max-width: 100%;
        }
        
        header {
            text-align: center;
            margin-bottom: 25px;
            padding: 20px;
            background: linear-gradient(135deg, #1a3a32 0%, #2a5a4f 100%);
            color: white;
            border-radius: 8px;
        }
        
        h1 {
            font-size: 24px;
            margin-bottom: 8px;
            font-weight: 700;
        }
        
        .subtitle {
            font-size: 16px;
            opacity: 0.9;
            font-weight: 300;
        }
        
        .flowchart {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .section {
            background-color: white;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 2px 8px rgba(26, 58, 50, 0.1);
            position: relative;
            border-left: 5px solid;
            page-break-inside: avoid;
        }
        
        .section-title {
            font-size: 18px;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        .section-title .icon {
            width: 32px;
            height: 32px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            font-size: 16px;
        }
        
        .subsection {
            margin-left: 20px;
            margin-bottom: 15px;
            position: relative;
        }
        
        .subsection::before {
            content: '';
            position: absolute;
            left: -15px;
            top: 10px;
            width: 8px;
            height: 8px;
            border-radius: 50%;
            background-color: currentColor;
            opacity: 0.7;
        }
        
        .subsection-title {
            font-weight: 600;
            margin-bottom: 8px;
            font-size: 16px;
        }
        
        .subsection-content {
            margin-left: 25px;
            font-size: 14px;
            line-height: 1.5;
            color: #2a4a42;
        }
        
        .subsection-content ul {
            margin-left: 15px;
        }
        
        .subsection-content li {
            margin-bottom: 6px;
            position: relative;
            padding-left: 8px;
        }
        
        .subsection-content li::before {
            content: '•';
            position: absolute;
            left: -8px;
            color: currentColor;
            font-weight: bold;
        }
        
        .example-box {
            background-color: #f0f7f5;
            border-left: 3px solid #4a9a85;
            padding: 10px 12px;
            margin: 8px 0;
            border-radius: 0 6px 6px 0;
            font-size: 13px;
        }
        
        .example-title {
            font-weight: 600;
            margin-bottom: 4px;
            color: #2a5a4f;
        }
        
        /* Tons de verde */
        .pre-textual { border-left-color: #1a3a32; color: #1a3a32; }
        .pre-textual .icon { background: linear-gradient(135deg, #1a3a32 0%, #2a5a4f 100%); }
        
        .apresentacao { border-left-color: #2a5a4f; color: #2a5a4f; }
        .apresentacao .icon { background: linear-gradient(135deg, #2a5a4f 0%, #3a7a6a 100%); }
        
        .miolo { border-left-color: #3a7a6a; color: #3a7a6a; }
        .miolo .icon { background: linear-gradient(135deg, #3a7a6a 0%, #4a9a85 100%); }
        
        .plus { border-left-color: #4a9a85; color: #4a9a85; }
        .plus .icon { background: linear-gradient(135deg, #4a9a85 0%, #5abaa0 100%); }
        
        .conclusao { border-left-color: #5abaa0; color: #5abaa0; }
        .conclusao .icon { background: linear-gradient(135deg, #5abaa0 0%, #6adabb 100%); }
        
        .bibliografia { border-left-color: #6adabb; color: #6adabb; }
        .bibliografia .icon { background: linear-gradient(135deg, #6adabb 0%, #7afad6 100%); }
        
        .download-btn {
            display: block;
            width: 200px;
            margin: 30px auto;
            padding: 12px 24px;
            background: linear-gradient(135deg, #2a5a4f 0%, #3a7a6a 100%);
            color: white;
            text-align: center;
            text-decoration: none;
            border-radius: 6px;
            font-weight: bold;
            font-size: 16px;
            border: none;
            cursor: pointer;
        }
        
        @media print {
            body {
                width: 100%;
                padding: 10px;
                box-shadow: none;
            }
            
            .download-btn {
                display: none;
            }
            
            .section {
                box-shadow: none;
                border: 1px solid #e0e0e0;
            }
        }
    </style>
</head>
<body>
    <div class="container" id="contentToPrint">
        <header>
            <h1>PROPOSTA ESTRUTURA MANUAL CEPE</h1>
            <p class="subtitle">Fluxograma Visual - Número de páginas: 25 a 30</p>
        </header>
        
        <div class="flowchart">
            <div class="section pre-textual">
                <div class="section-title">
                    <div class="icon">1</div>
                    <h2>Elementos Pré-textuais</h2>
                </div>
                <div class="subsection">
                    <div class="subsection-title">Carta para o mestre</div>
                </div>
                <div class="subsection">
                    <div class="subsection-title">Índice</div>
                </div>
            </div>
            
            <div class="section apresentacao">
                <div class="section-title">
                    <div class="icon">2</div>
                    <h2>Apresentação</h2>
                </div>
                <div class="subsection-content">
                    Explicação do manual, apresentando todos os tópicos - uma espécie de cartografia. Extensão máxima.
                </div>
            </div>
            
            <div class="section miolo">
                <div class="section-title">
                    <div class="icon">3</div>
                    <h2>Conteúdo Principal do Manual</h2>
                </div>
                
                <div class="subsection">
                    <div class="subsection-title">I. Tópico introdutório por formato/idade:</div>
                    <div class="subsection-content">
                        <ul>
                            <li><strong>A. Infantil:</strong> O brincante como elemento pedagógico (MEC + MINC têm uma proposta de ensino integral, baseado nas artes e literatura)</li>
                            <li><strong>B. Infantojuvenil:</strong>
                                <ul>
                                    <li>Ficção: construção de pensamento crítico</li>
                                    <li>Histórico: múltiplos olhares sobre fatos históricos</li>
                                </ul>
                            </li>
                            <li><strong>C. Literatura Ficcional outras idades:</strong>
                                <ul>
                                    <li>A formulação de um pensamento crítico, incluindo também a adesão de conceitos mais complexos no próprio desenvolvimento do texto</li>
                                    <li>Histórico: a importância de múltiplos olhares e saberes sobre um fato histórico, incluindo também a adesão de conceitos mais complexos no próprio desenvolvimento do texto</li>
                                    <li>Suporte para professor e livros acadêmicos: Diálogos entre os conceitos do livro + outros conceitos próximos</li>
                                </ul>
                                <div class="example-box">
                                    <div class="example-title">ATENÇÃO: Diferente do tópico Discussão temática</div>
                                    <strong>Exemplo:</strong> Miró - performance - elemento fundamental para entender sua obra.<br>
                                    <strong>Discussão temática:</strong> Cultura popular e rua.
                                </div>
                            </li>
                        </ul>
                    </div>
                </div>
                
                <div class="subsection">
                    <div class="subsection-title">II. Discussão temática do livro</div>
                </div>
                
                <div class="subsection">
                    <div class="subsection-title">III. Contextualização da obra</div>
                    <div class="subsection-content">
                        <ul>
                            <li>Autoria</li>
                            <li>Relação com fatos históricos (quando aplicável)</li>
                        </ul>
                    </div>
                </div>
                
                <div class="subsection">
                    <div class="subsection-title">IV. Uso da obra na etapa Pedagógica</div>
                    <div class="subsection-content">
                        Vinculada à noção de projetos (ideia de Giane): Infantil, Fundamental 1 e 2, Médio, EJA, suporte para professor e/ou obras interseccionais.
                    </div>
                </div>
                
                <div class="subsection">
                    <div class="subsection-title">V. Análise da obra</div>
                    <div class="subsection-content">
                        Partes da obra + imagens com determinados direcionamentos.
                    </div>
                </div>
                
                <div class="subsection">
                    <div class="subsection-title">VI. Sugestão de atividades</div>
                </div>
            </div>
            
            <div class="section plus">
                <div class="section-title">
                    <div class="icon">4</div>
                    <h2>Plus Surpresa</h2>
                </div>
                <div class="subsection-content">
                    <div class="example-box">
                        <div class="example-title">EXEMPLO 1: Temática sobre autismo</div>
                        Carta de pessoas autistas expondo suas experiências
                    </div>
                    <div class="example-box">
                        <div class="example-title">EXEMPLO 2: Fontes do Acervo Digital CEPE para uso</div>
                        Documentos históricos complementares
                    </div>
                </div>
            </div>
            
            <div class="section conclusao">
                <div class="section-title">
                    <div class="icon">5</div>
                    <h2>Conclusão</h2>
                </div>
            </div>
            
            <div class="section bibliografia">
                <div class="section-title">
                    <div class="icon">6</div>
                    <h2>Bibliografia</h2>
                </div>
                <div class="subsection">
                    <div class="subsection-title">Sugestão de bibliografias complementares</div>
                    <div class="subsection-content">
                        Apresentação de outros livros, incluindo os da própria CEPE, que complementem o conteúdo.
                    </div>
                </div>
                <div class="subsection">
                    <div class="subsection-title">Bibliografia utilizada comentada</div>
                </div>
            </div>
        </div>
        
        <button class="download-btn" onclick="generatePDF()">Baixar como PDF</button>
    </div>

    <script>
        function generatePDF() {
            const element = document.getElementById('contentToPrint');
            const opt = {
                margin: 10,
                filename: 'fluxograma_manual_cepe.pdf',
                image: { type: 'jpeg', quality: 0.98 },
                html2canvas: { scale: 2, useCORS: true },
                jsPDF: { unit: 'mm', format: 'a4', orientation: 'portrait' }
            };
            
            // Mostrar mensagem de processamento
            const originalText = document.querySelector('.download-btn').textContent;
            document.querySelector('.download-btn').textContent = 'Gerando PDF...';
            document.querySelector('.download-btn').disabled = true;
            
            html2pdf().set(opt).from(element).save().then(() => {
                // Restaurar texto do botão após conclusão
                document.querySelector('.download-btn').textContent = originalText;
                document.querySelector('.download-btn').disabled = false;
            });
        }
        
        // Também permite impressão direta com Ctrl+P
        document.addEventListener('keydown', function(e) {
            if (e.ctrlKey && e.key === 'p') {
                e.preventDefault();
                generatePDF();
            }
        });
    </script>
</body>
</html>
