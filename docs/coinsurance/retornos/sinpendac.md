# SINPENDAC — Retorno pendências (BMG)

> TODO: detalhar.

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SINPENDAC - Sinistro Pendente Aceito de Cosseguro</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism-tomorrow.min.css">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; line-height: 1.6; color: #333; background: #f5f5f5; }
        .container { max-width: 1200px; margin: 0 auto; padding: 20px; background: white; min-height: 100vh; }
        header { background: linear-gradient(135deg, #f39c12 0%, #e67e22 100%); color: white; padding: 30px 0; margin-bottom: 30px; box-shadow: 0 2px 10px rgba(0,0,0,0.1); }
        header h1 { font-size: 2.5em; margin-bottom: 10px; }
        header .subtitle { font-size: 1.2em; opacity: 0.9; }
        nav { background: #2d3748; padding: 15px 0; margin-bottom: 30px; position: sticky; top: 0; z-index: 100; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
        nav ul { list-style: none; display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; }
        nav a { color: white; text-decoration: none; padding: 8px 16px; border-radius: 5px; transition: background 0.3s; }
        nav a:hover { background: rgba(255,255,255,0.1); }
        nav a.active { background: #f39c12; }
        h2 { color: #f39c12; margin: 30px 0 15px 0; padding-bottom: 10px; border-bottom: 2px solid #f39c12; }
        h3 { color: #e67e22; margin: 25px 0 12px 0; }
        h4 { color: #4a5568; margin: 20px 0 10px 0; }
        table { width: 100%; border-collapse: collapse; margin: 20px 0; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
        th { background: #f39c12; color: white; padding: 12px; text-align: left; }
        td { padding: 12px; border-bottom: 1px solid #e2e8f0; }
        tr:hover { background: #f7fafc; }
        .code-block { background: #2d3748; color: #e2e8f0; padding: 20px; border-radius: 8px; overflow-x: auto; margin: 20px 0; font-family: 'Courier New', monospace; }
        .alert { padding: 15px; margin: 20px 0; border-radius: 5px; border-left: 4px solid; }
        .alert-info { background: #ebf8ff; border-color: #3182ce; color: #2c5282; }
        .alert-warning { background: #fffaf0; border-color: #dd6b20; color: #7c2d12; }
        .alert-success { background: #f0fff4; border-color: #38a169; color: #22543d; }
        .badge { display: inline-block; padding: 4px 8px; border-radius: 3px; font-size: 0.85em; font-weight: bold; }
        .badge-primary { background: #667eea; color: white; }
        .badge-success { background: #48bb78; color: white; }
        .badge-warning { background: #ed8936; color: white; }
        .card { background: white; border-radius: 8px; padding: 20px; margin: 20px 0; box-shadow: 0 2px 8px rgba(0,0,0,0.1); }
        footer { margin-top: 50px; padding: 20px 0; border-top: 2px solid #e2e8f0; text-align: center; color: #718096; }
        .breadcrumb { margin-bottom: 20px; color: #718096; }
        .breadcrumb a { color: #667eea; text-decoration: none; }
        code { background: #edf2f7; padding: 2px 6px; border-radius: 3px; font-family: 'Courier New', monospace; }
        pre code { background: none; padding: 0; }
        .highlight { background: #fff3cd; padding: 3px 6px; border-radius: 3px; font-weight: bold; }
        .formula { background: #e8f5e9; padding: 15px; border-radius: 5px; margin: 15px 0; font-family: monospace; font-size: 1.1em; text-align: center; }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>⏳ SINPENDAC</h1>
            <p class="subtitle">Sinistro Pendente Aceito de Cosseguro</p>
        </div>
    </header>

    <nav>
        <div class="container">
            <ul>
                <li><a href="../../index.html">🏠 Home</a></li>
                <li><a href="index.html">📋 Visão Geral</a></li>
                <li><a href="premac.html">PREMAC</a></li>
                <li><a href="premrecac.html">PREMRECAC</a></li>
                <li><a href="premrecebc.html">PREMRECEBC</a></li>
                <li><a href="respremc.html">RESPREMC</a></li>
                <li><a href="sinavac.html">SINAVAC</a></li>
                <li><a href="sinpagac.html">SINPAGAC</a></li>
                <li><a href="sinpendac.html" class="active">SINPENDAC</a></li>
            </ul>
        </div>
    </nav>

    <div class="container">
        <div class="breadcrumb">
            <a href="../../index.html">Home</a> / 
            <a href="index.html">Retornos</a> / 
            <span>SINPENDAC</span>
        </div>

        <h1>⏳ SINPENDAC - Sinistro Pendente Aceito de Cosseguro</h1>

        <div class="alert alert-info">
            <strong>ℹ️ Descrição:</strong> Sinistros pendentes com reservas técnicas, representando valores provisionados mas ainda não pagos (IBNR - Incurred But Not Reported).
        </div>

        <h2>🔧 Especificações Técnicas</h2>
        <table>
            <tr>
                <th>Propriedade</th>
                <th>Valor</th>
            </tr>
            <tr>
                <td><strong>Módulo</strong></td>
                <td>ClaimCase (Index) apenas</td>
            </tr>
            <tr>
                <td><strong>Filtros</strong></td>
                <td><code>BaseDate</code>, <code>owned_org_code=bmg</code></td>
            </tr>
            <tr>
                <td><strong>Total de Campos</strong></td>
                <td>15 campos</td>
            </tr>
            <tr>
                <td><strong>Complexidade</strong></td>
                <td><span class="badge badge-success">Baixa</span></td>
            </tr>
        </table>

        <h2>📋 Estrutura do Arquivo CSV</h2>
        <div class="code-block">
SEQUENCIA|COD_CIA|DT_BASE|TIPO_MOV|COD_RAMO|COD_COSS|NUM_SIN|NUM_APOL|NUM_END|DT_REG|DT_AVISO|DT_OCOR|VR_PENDENTE|VR_TOT|TP_SIN
0000000001|03417|202509|01|0553|05908|SIN123|POL123|END001|20250910|20250905|20250901|3000.00|7500.00|01
        </div>

        <h2>📝 Descrição dos Campos</h2>
        <table>
            <thead>
                <tr>
                    <th>Campo</th>
                    <th>Tipo</th>
                    <th>Descrição</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><code>SEQUENCIA</code></td>
                    <td>Numérico</td>
                    <td>Número sequencial do registro</td>
                </tr>
                <tr>
                    <td><code>COD_CIA</code></td>
                    <td>Texto</td>
                    <td>Código da companhia (03417)</td>
                </tr>
                <tr>
                    <td><code>DT_BASE</code></td>
                    <td>Texto</td>
                    <td>Data base (YYYYMM)</td>
                </tr>
                <tr>
                    <td><code>TIPO_MOV</code></td>
                    <td>Numérico</td>
                    <td>Tipo de movimento (convertido)</td>
                </tr>
                <tr>
                    <td><code>COD_RAMO</code></td>
                    <td>Texto</td>
                    <td>Código do ramo (<code>ExtBranchCode</code>)</td>
                </tr>
                <tr>
                    <td><code>COD_COSS</code></td>
                    <td>Texto</td>
                    <td>Código do cosseguro (05908)</td>
                </tr>
                <tr>
                    <td><code>NUM_SIN</code></td>
                    <td>Texto</td>
                    <td>Número do sinistro (<code>ExtClaimNo</code>)</td>
                </tr>
                <tr>
                    <td><code>NUM_APOL</code></td>
                    <td>Texto</td>
                    <td>Número da apólice (<code>ExtPolicyNo</code>)</td>
                </tr>
                <tr>
                    <td><code>NUM_END</code></td>
                    <td>Texto</td>
                    <td>Número do endosso (<code>ExtEndoNo</code>)</td>
                </tr>
                <tr>
                    <td><code>DT_REG</code></td>
                    <td>Data</td>
                    <td>Data de registro (<code>ExtRegistrationDate</code>)</td>
                </tr>
                <tr>
                    <td><code>DT_AVISO</code></td>
                    <td>Data</td>
                    <td>Data do aviso (<code>NoticeTime</code>)</td>
                </tr>
                <tr>
                    <td><code>DT_OCOR</code></td>
                    <td>Data</td>
                    <td>Data da ocorrência (<code>AccidentTime</code>)</td>
                </tr>
                <tr>
                    <td><code>VR_PENDENTE</code></td>
                    <td>Decimal</td>
                    <td><span class="highlight">Valor pendente cedido</span> (<code>ExtCededCoinsuranceAmount</code>)</td>
                </tr>
                <tr>
                    <td><code>VR_TOT</code></td>
                    <td>Decimal</td>
                    <td><span class="highlight">40% do valor total</span> (calculado)</td>
                </tr>
                <tr>
                    <td><code>TP_SIN</code></td>
                    <td>Texto</td>
                    <td>Tipo do sinistro (<code>ExtClaimType</code>)</td>
                </tr>
            </tbody>
        </table>

        <h2>🔄 Lógica de Negócio - Cálculo de Valores</h2>

        <div class="alert alert-warning">
            <strong>⚠️ Cálculo Especial:</strong> SINPENDAC possui um cálculo único para o campo <code>VR_TOT</code>, aplicando 40% sobre o valor total do movimento.
        </div>

        <h3>Fórmulas de Cálculo</h3>
        <div class="formula">
            VR_PENDENTE = ExtCededCoinsuranceAmount
        </div>

        <div class="formula">
            VR_TOT = ExtMovementAmount × 0.40
        </div>

        <h3>Implementação</h3>
        <pre><code class="language-groovy">// VR_PENDENTE: valor cedido ao cosseguro
BigDecimal vrPendente = claimDoc.ExtCededCoinsuranceAmount ?: 0.00

// VR_TOT: 40% do movimento total
BigDecimal movementAmount = claimDoc.ExtMovementAmount ?: 0.00
BigDecimal vrTot = movementAmount * 0.40

generateLine(
    vrPendente: vrPendente,
    vrTot: vrTot,
    // ... outros campos
)</code></pre>

        <h2>📊 Exemplo Numérico</h2>
        <div class="card">
            <h4>Cenário:</h4>
            <ul>
                <li><strong>ExtMovementAmount:</strong> R$ 10.000,00 (valor total do sinistro)</li>
                <li><strong>ExtCededCoinsuranceAmount:</strong> R$ 3.000,00 (valor cedido ao cosseguro)</li>
            </ul>

            <h4>Cálculo:</h4>
            <ul>
                <li><strong>VR_PENDENTE:</strong> R$ 3.000,00 (direto do campo)</li>
                <li><strong>VR_TOT:</strong> R$ 10.000,00 × 0.40 = <strong>R$ 4.000,00</strong></li>
            </ul>

            <h4>Resultado CSV:</h4>
            <div class="code-block">
...|VR_PENDENTE|VR_TOT|...
...|3000.00|4000.00|...
            </div>
        </div>

        <h2>🔢 Conversão de TipoMov (Completa)</h2>
        <table>
            <thead>
                <tr>
                    <th>Platform</th>
                    <th>SUSEP</th>
                    <th>Descrição</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><span class="badge badge-primary">201</span></td>
                    <td><span class="badge badge-success">01</span></td>
                    <td>Aviso</td>
                </tr>
                <tr>
                    <td><span class="badge badge-primary">204</span></td>
                    <td><span class="badge badge-success">04</span></td>
                    <td>Complementação</td>
                </tr>
                <tr>
                    <td><span class="badge badge-primary">207</span></td>
                    <td><span class="badge badge-success">07</span></td>
                    <td>Pagamento</td>
                </tr>
                <tr>
                    <td><span class="badge badge-primary">208</span></td>
                    <td><span class="badge badge-success">08</span></td>
                    <td>Pagamento complementar</td>
                </tr>
                <tr>
                    <td><span class="badge badge-primary">211</span></td>
                    <td><span class="badge badge-success">11</span></td>
                    <td>Recuperação</td>
                </tr>
                <tr>
                    <td><span class="badge badge-primary">214</span></td>
                    <td><span class="badge badge-success">14</span></td>
                    <td>Recuperação complementar</td>
                </tr>
                <tr>
                    <td>Outros</td>
                    <td><span class="badge badge-success">01</span></td>
                    <td>Default</td>
                </tr>
            </tbody>
        </table>

        <pre><code class="language-groovy">String resolveSusepMovType(String platformMovType) {
    switch (platformMovType) {
        case "201": return "01"
        case "204": return "04"
        case "207": return "07"
        case "208": return "08"
        case "211": return "11"
        case "214": return "14"
        default: return "01"
    }
}</code></pre>

        <h2>🗂️ Fonte de Dados</h2>
        <div class="card">
            <h4>Estrutura JSON (ClaimCase):</h4>
            <pre><code class="language-json">{
  "ClaimId": 67890,
  "ExtClaimNo": "SIN123",
  "ExtPolicyNo": "POL123",
  "ExtEndoNo": "END001",
  "ExtRegistrationDate": "2025-09-10",
  "NoticeTime": "2025-09-05T14:30:00",
  "AccidentTime": "2025-09-01T10:00:00",
  "ExtBranchCode": "0553",
  "ExtClaimType": "01",
  "ExtMovementType": "201",
  "ExtCededCoinsuranceAmount": 3000.00,
  "ExtMovementAmount": 7500.00
}</code></pre>
        </div>

        <h2>📊 Comparativo de Campos Especiais</h2>
        <table>
            <thead>
                <tr>
                    <th>Arquivo</th>
                    <th>Campo 1</th>
                    <th>Campo 2</th>
                    <th>Observação</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><strong>SINAVAC</strong></td>
                    <td>VR_MOV</td>
                    <td>-</td>
                    <td>Valor do movimento (direto)</td>
                </tr>
                <tr>
                    <td><strong>SINPAGAC</strong></td>
                    <td>VR_MOV</td>
                    <td>-</td>
                    <td>Valor pago (direto)</td>
                </tr>
                <tr>
                    <td><strong>SINPENDAC</strong></td>
                    <td>VR_PENDENTE</td>
                    <td><span class="highlight">VR_TOT</span></td>
                    <td>VR_TOT = valor × 0.40</td>
                </tr>
            </tbody>
        </table>

        <h2>📤 Saída do Arquivo</h2>
        <table>
            <tr>
                <th>Item</th>
                <th>Localização</th>
            </tr>
            <tr>
                <td><strong>CSV de Export</strong></td>
                <td><code>s3://bucket/export/SINPENDAC_202509_20260305_143022.csv</code></td>
            </tr>
            <tr>
                <td><strong>Log Detalhado</strong></td>
                <td><code>s3://bucket/logs/2026-03-05/SINPENDAC/SINPENDAC_DETAILED_202509_20260305_143022.log</code></td>
            </tr>
            <tr>
                <td><strong>Log de Erros</strong></td>
                <td><code>s3://bucket/logs/2026-03-05/SINPENDAC/error/LOG_SINPENDAC_202509_*.csv</code></td>
            </tr>
        </table>

        <h2>🚀 Exemplo de Uso</h2>
        <pre><code class="language-groovy">// Executar export para setembro/2025
process("202509")</code></pre>

        <div class="alert alert-success">
            <strong>✅ Resultado esperado:</strong>
            <ul>
                <li>15 sinistros pendentes → <strong>15 linhas</strong></li>
                <li>VR_TOT calculado automaticamente (40% do total)</li>
                <li>Processamento rápido (single module)</li>
            </ul>
        </div>

        <h2>💡 O que é IBNR?</h2>
        <div class="card">
            <h4>Incurred But Not Reported (IBNR)</h4>
            <p><strong>Definição:</strong> Reserva técnica para sinistros que já ocorreram mas ainda não foram reportados à seguradora.</p>
            
            <p><strong>Componentes do SINPENDAC:</strong></p>
            <ul>
                <li><strong>VR_PENDENTE:</strong> Valor conhecido e provisionado</li>
                <li><strong>VR_TOT:</strong> Estimativa total incluindo IBNR (40% rule)</li>
            </ul>
        </div>

        <footer>
            <p>&copy; 2026 BMG Seguros - Sistema de Exportação de Cosseguro</p>
            <p>Última atualização: 05/03/2026 | Versão: 1.0.0</p>
        </footer>
    </div>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/components/prism-groovy.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/components/prism-json.min.js"></script>
</body>
</html>
