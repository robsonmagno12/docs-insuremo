# SINAVAC — Retorno de sinistro (BMG)

> TODO: detalhar.
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SINAVAC - Sinistro Aviso Aceito de Cosseguro</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism-tomorrow.min.css">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; line-height: 1.6; color: #333; background: #f5f5f5; }
        .container { max-width: 1200px; margin: 0 auto; padding: 20px; background: white; min-height: 100vh; }
        header { background: linear-gradient(135deg, #e74c3c 0%, #c0392b 100%); color: white; padding: 30px 0; margin-bottom: 30px; box-shadow: 0 2px 10px rgba(0,0,0,0.1); }
        header h1 { font-size: 2.5em; margin-bottom: 10px; }
        header .subtitle { font-size: 1.2em; opacity: 0.9; }
        nav { background: #2d3748; padding: 15px 0; margin-bottom: 30px; position: sticky; top: 0; z-index: 100; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
        nav ul { list-style: none; display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; }
        nav a { color: white; text-decoration: none; padding: 8px 16px; border-radius: 5px; transition: background 0.3s; }
        nav a:hover { background: rgba(255,255,255,0.1); }
        nav a.active { background: #e74c3c; }
        h2 { color: #e74c3c; margin: 30px 0 15px 0; padding-bottom: 10px; border-bottom: 2px solid #e74c3c; }
        h3 { color: #c0392b; margin: 25px 0 12px 0; }
        h4 { color: #4a5568; margin: 20px 0 10px 0; }
        table { width: 100%; border-collapse: collapse; margin: 20px 0; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
        th { background: #e74c3c; color: white; padding: 12px; text-align: left; }
        td { padding: 12px; border-bottom: 1px solid #e2e8f0; }
        tr:hover { background: #f7fafc; }
        .code-block { background: #2d3748; color: #e2e8f0; padding: 20px; border-radius: 8px; overflow-x: auto; margin: 20px 0; font-family: 'Courier New', monospace; font-size: 0.9em; }
        .alert { padding: 15px; margin: 20px 0; border-radius: 5px; border-left: 4px solid; }
        .alert-info { background: #ebf8ff; border-color: #3182ce; color: #2c5282; }
        .alert-warning { background: #fffaf0; border-color: #dd6b20; color: #7c2d12; }
        .alert-success { background: #f0fff4; border-color: #38a169; color: #22543d; }
        .alert-danger { background: #fff5f5; border-color: #e53e3e; color: #742a2a; }
        .badge { display: inline-block; padding: 4px 8px; border-radius: 3px; font-size: 0.85em; font-weight: bold; }
        .badge-primary { background: #667eea; color: white; }
        .badge-success { background: #48bb78; color: white; }
        .badge-warning { background: #ed8936; color: white; }
        .badge-danger { background: #f56565; color: white; }
        .card { background: white; border-radius: 8px; padding: 20px; margin: 20px 0; box-shadow: 0 2px 8px rgba(0,0,0,0.1); }
        footer { margin-top: 50px; padding: 20px 0; border-top: 2px solid #e2e8f0; text-align: center; color: #718096; }
        .breadcrumb { margin-bottom: 20px; color: #718096; }
        .breadcrumb a { color: #667eea; text-decoration: none; }
        code { background: #edf2f7; padding: 2px 6px; border-radius: 3px; font-family: 'Courier New', monospace; }
        pre code { background: none; padding: 0; }
        .highlight { background: #fef5e7; padding: 3px 6px; border-radius: 3px; font-weight: bold; }
        .complexity-high { background: #fee; padding: 10px; border-left: 4px solid #e53e3e; border-radius: 5px; margin: 20px 0; }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>🚨 SINAVAC</h1>
            <p class="subtitle">Sinistro Aviso Aceito de Cosseguro</p>
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
                <li><a href="sinavac.html" class="active">SINAVAC</a></li>
                <li><a href="sinpagac.html">SINPAGAC</a></li>
                <li><a href="sinpendac.html">SINPENDAC</a></li>
            </ul>
        </div>
    </nav>

    <div class="container">
        <div class="breadcrumb">
            <a href="../../index.html">Home</a> / 
            <a href="index.html">Retornos</a> / 
            <span>SINAVAC</span>
        </div>

        <h1>🚨 SINAVAC - Sinistro Aviso Aceito de Cosseguro</h1>

        <div class="alert alert-info">
            <strong>ℹ️ Descrição:</strong> Avisos de sinistro com histórico completo de transações, utilizando estratégia de busca dual (ClaimCase + ARAP) para capturar todos os movimentos.
        </div>

        <div class="complexity-high">
            <strong>⚠️ COMPLEXIDADE ALTA:</strong> Este é o arquivo mais complexo do sistema, utilizando <strong>dois módulos</strong> (ClaimCase + BCP ARAP) com paginação e histórico completo.
        </div>

        <h2>🔧 Especificações Técnicas</h2>
        <table>
            <tr>
                <th>Propriedade</th>
                <th>Valor</th>
            </tr>
            <tr>
                <td><strong>Módulo Primário</strong></td>
                <td>ClaimCase (Index)</td>
            </tr>
            <tr>
                <td><strong>Módulo Secundário</strong></td>
                <td>BCP ARAP (Transaction)</td>
            </tr>
            <tr>
                <td><strong>Filtros</strong></td>
                <td><code>BaseDate</code>, <code>owned_org_code=bmg</code></td>
            </tr>
            <tr>
                <td><strong>Total de Campos</strong></td>
                <td>16 campos</td>
            </tr>
            <tr>
                <td><strong>Complexidade</strong></td>
                <td><span class="badge badge-danger">Alta</span></td>
            </tr>
        </table>

        <h2>📋 Estrutura do Arquivo CSV</h2>
        <div class="code-block">
SEQUENCIA|COD_CIA|DT_BASE|TIPO_MOV|COD_RAMO|COD_COSS|NUM_SIN|NUM_APOL|NUM_END|DT_REG|DT_AVISO|DT_OCOR|VR_MOV|DT_SIN|TP_SIN|UF_RISCO
0000000001|03417|202509|01|0553|05908|SIN123|POL123|END001|20250910|20250905|20250901|5000.00|20250901|01|SP
        </div>

        <h2>📝 Descrição dos Campos</h2>
        <table>
            <thead>
                <tr>
                    <th>Campo</th>
                    <th>Fonte</th>
                    <th>Descrição</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><code>SEQUENCIA</code></td>
                    <td>-</td>
                    <td>Número sequencial do registro</td>
                </tr>
                <tr>
                    <td><code>COD_CIA</code></td>
                    <td>-</td>
                    <td>Código da companhia (03417)</td>
                </tr>
                <tr>
                    <td><code>DT_BASE</code></td>
                    <td>-</td>
                    <td>Data base (YYYYMM)</td>
                </tr>
                <tr>
                    <td><code>TIPO_MOV</code></td>
                    <td><span class="badge badge-danger">ARAP</span></td>
                    <td>Tipo de movimento SUSEP (convertido)</td>
                </tr>
                <tr>
                    <td><code>COD_RAMO</code></td>
                    <td><span class="badge badge-primary">ClaimCase</span></td>
                    <td>Código do ramo (<code>ExtBranchCode</code>)</td>
                </tr>
                <tr>
                    <td><code>COD_COSS</code></td>
                    <td>-</td>
                    <td>Código do cosseguro (05908)</td>
                </tr>
                <tr>
                    <td><code>NUM_SIN</code></td>
                    <td><span class="badge badge-primary">ClaimCase</span></td>
                    <td>Número do sinistro (<code>ExtClaimNo</code>)</td>
                </tr>
                <tr>
                    <td><code>NUM_APOL</code></td>
                    <td><span class="badge badge-primary">ClaimCase</span></td>
                    <td>Número da apólice (<code>ExtPolicyNo</code>)</td>
                </tr>
                <tr>
                    <td><code>NUM_END</code></td>
                    <td><span class="badge badge-primary">ClaimCase</span></td>
                    <td>Número do endosso (<code>ExtEndoNo</code>)</td>
                </tr>
                <tr>
                    <td><code>DT_REG</code></td>
                    <td><span class="badge badge-primary">ClaimCase</span></td>
                    <td>Data de registro (<code>ExtRegistrationDate</code>)</td>
                </tr>
                <tr>
                    <td><code>DT_AVISO</code></td>
                    <td><span class="badge badge-primary">ClaimCase</span></td>
                    <td>Data do aviso (<code>NoticeTime</code>)</td>
                </tr>
                <tr>
                    <td><code>DT_OCOR</code></td>
                    <td><span class="badge badge-primary">ClaimCase</span></td>
                    <td>Data da ocorrência (<code>AccidentTime</code>)</td>
                </tr>
                <tr>
                    <td><code>VR_MOV</code></td>
                    <td><span class="badge badge-danger">ARAP</span></td>
                    <td>Valor do movimento (<code>ExtCededCoinsuranceAmount</code>)</td>
                </tr>
                <tr>
                    <td><code>DT_SIN</code></td>
                    <td><span class="badge badge-primary">ClaimCase</span></td>
                    <td>Data do sinistro (mesmo que DT_OCOR)</td>
                </tr>
                <tr>
                    <td><code>TP_SIN</code></td>
                    <td><span class="badge badge-primary">ClaimCase</span></td>
                    <td>Tipo do sinistro (<code>ExtClaimType</code>)</td>
                </tr>
                <tr>
                    <td><code>UF_RISCO</code></td>
                    <td><span class="badge badge-primary">ClaimCase</span></td>
                    <td>UF do risco (<code>RiskState</code>)</td>
                </tr>
            </tbody>
        </table>

        <h2>🔄 Lógica de Negócio - Estratégia Dual Module</h2>

        <div class="alert alert-warning">
            <strong>⚠️ Estratégia:</strong> SINAVAC combina dados de <strong>ClaimCase</strong> (dados base do sinistro) com <strong>ARAP</strong> (histórico de transações financeiras).
        </div>

        <h3>Fluxo de Processamento</h3>
        <div class="card">
            <ol>
                <li><strong>Query ClaimCase Index</strong> por BaseDate</li>
                <li><strong>Load ClaimCase Data</strong> completo</li>
                <li><strong>Extract ClaimNo</strong> do ClaimCase</li>
                <li><strong>Query ARAP</strong> por ClaimNo (com paginação)</li>
                <li>Se ARAP encontrado: <strong>Para cada Transaction</strong>, gera linha combinando ClaimCase + ARAP</li>
                <li>Se ARAP não encontrado: Gera linha com dados do ClaimCase apenas (fallback)</li>
            </ol>
        </div>

        <h3>Código de Implementação</h3>
        <pre><code class="language-groovy">// 1. Busca ClaimCase
List&lt;Map&gt; claimDocs = fetchClaimsCaseBatch(baseDate, cursorId)

claimDocs.each { claimDoc ->
    String claimNo = claimDoc.ExtClaimNo
    
    // 2. Busca TODOS os ARAP para este ClaimNo
    List&lt;Map&gt; arapHistorico = fetchAllArapDataByClaimNo(claimNo)
    
    if (arapHistorico.isEmpty()) {
        // Fallback: usa dados do ClaimCase
        detailedLogger.log("  Sem ARAP - usando dados do ClaimCase")
        generateLine(
            claimCase: claimDoc,
            arap: null
        )
    } else {
        // Para cada ARAP Transaction, gera uma linha
        detailedLogger.log("  ${arapHistorico.size()} transacoes ARAP encontradas")
        arapHistorico.each { arapData ->
            generateLine(
                claimCase: claimDoc,  // Campos base
                arap: arapData         // TipoMov e VrMov
            )
        }
    }
}</code></pre>

        <h3>Paginação do ARAP</h3>
        <pre><code class="language-groovy">List fetchAllArapDataByClaimNo(String claimNo) {
    List allArapData = []
    int pageNo = 1
    boolean hasMorePages = true
    
    while (hasMorePages) {
        // Query ARAP com BizTransType=CLAIM
        PagedResultArap response = bcpSdkClient.arapApi()
            .newAdvanceQueryArapRequestBuilder()
            .searchConditionRequest([
                conditions: [
                    ClaimNo: claimNo,
                    BizTransType: "CLAIM"
                ],
                pageNo: pageNo,
                pageSize: 100
            ])
            .doRequest()
            .getBody()
        
        if (response.totalElements > 0) {
            response.elementsInCurrentPage.each { arap ->
                // Extrai Transaction de cada ARAP
                Map transaction = arap.Transaction
                allArapData.add(transaction)
            }
            
            hasMorePages = (response.elementsInCurrentPage.size() == 100)
            pageNo++
        } else {
            hasMorePages = false
        }
    }
    
    return allArapData
}</code></pre>

        <h2>🔢 Conversão de TipoMov (Platform → SUSEP)</h2>
        <table>
            <thead>
                <tr>
                    <th>Platform (ARAP)</th>
                    <th>SUSEP</th>
                    <th>Descrição</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><span class="badge badge-primary">201</span></td>
                    <td><span class="badge badge-success">01</span></td>
                    <td>Aviso inicial</td>
                </tr>
                <tr>
                    <td><span class="badge badge-primary">204</span></td>
                    <td><span class="badge badge-success">04</span></td>
                    <td>Complementação de aviso</td>
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
                    <td>Default (fallback)</td>
                </tr>
            </tbody>
        </table>

        <pre><code class="language-groovy">String resolveSusepMovType(String platformMovType) {
    switch (platformMovType) {
        case "201": return "01"
        case "204": return "04"
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
  "RiskState": "SP"
}</code></pre>

            <h4>Estrutura JSON (ARAP Transaction):</h4>
            <pre><code class="language-json">{
  "Transaction": {
    "ExtMovementType": "201",
    "ExtCededCoinsuranceAmount": 5000.00,
    "TransactionDate": "2025-09-05"
  }
}</code></pre>
        </div>

        <h2>📊 Exemplo de Resultado</h2>
        <div class="alert alert-success">
            <strong>✅ Cenário:</strong> Um sinistro com 3 transações ARAP
            <ul>
                <li><strong>Input:</strong> 1 ClaimCase com ClaimNo = SIN123</li>
                <li><strong>ARAP Query:</strong> Retorna 3 transactions (201, 204, 211)</li>
                <li><strong>Output:</strong> 3 linhas CSV (uma para cada transaction)</li>
            </ul>
        </div>

        <table>
            <thead>
                <tr>
                    <th>Linha</th>
                    <th>NUM_SIN</th>
                    <th>TIPO_MOV</th>
                    <th>VR_MOV</th>
                    <th>Origem</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>1</td>
                    <td>SIN123</td>
                    <td>01</td>
                    <td>5000.00</td>
                    <td>ClaimCase + ARAP Transaction 1 (201)</td>
                </tr>
                <tr>
                    <td>2</td>
                    <td>SIN123</td>
                    <td>04</td>
                    <td>2000.00</td>
                    <td>ClaimCase + ARAP Transaction 2 (204)</td>
                </tr>
                <tr>
                    <td>3</td>
                    <td>SIN123</td>
                    <td>11</td>
                    <td>-1000.00</td>
                    <td>ClaimCase + ARAP Transaction 3 (211)</td>
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
                <td><code>s3://bucket/export/SINAVAC_202509_20260305_143022.csv</code></td>
            </tr>
            <tr>
                <td><strong>Log Detalhado</strong></td>
                <td><code>s3://bucket/logs/2026-03-05/SINAVAC/SINAVAC_DETAILED_202509_20260305_143022.log</code></td>
            </tr>
            <tr>
                <td><strong>Log de Erros</strong></td>
                <td><code>s3://bucket/logs/2026-03-05/SINAVAC/error/LOG_SINAVAC_202509_*.csv</code></td>
            </tr>
        </table>

        <h2>⚠️ Considerações de Performance</h2>
        <div class="alert alert-danger">
            <strong>⚠️ Performance:</strong>
            <ul>
                <li>Processamento mais lento devido à busca dual de módulos</li>
                <li>Paginação do ARAP pode gerar múltiplas chamadas API</li>
                <li>~20 registros/segundo (vs ~50 em arquivos simples)</li>
                <li>Tempo médio para 10k sinistros: ~8 minutos</li>
            </ul>
        </div>

        <h2>🚀 Exemplo de Uso</h2>
        <pre><code class="language-groovy">// Executar export para setembro/2025
process("202509")</code></pre>

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
