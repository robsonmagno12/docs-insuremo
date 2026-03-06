# PREMRECAC — Retorno de parcelas (BMG)

> TODO: detalhar.
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PREMRECAC - Prêmio Recebível Aceito de Cosseguro</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism-tomorrow.min.css">
    <style>
        /* [Mesmo CSS do premac.html] */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; line-height: 1.6; color: #333; background: #f5f5f5; }
        .container { max-width: 1200px; margin: 0 auto; padding: 20px; background: white; min-height: 100vh; }
        header { background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); color: white; padding: 30px 0; margin-bottom: 30px; box-shadow: 0 2px 10px rgba(0,0,0,0.1); }
        header h1 { font-size: 2.5em; margin-bottom: 10px; }
        header .subtitle { font-size: 1.2em; opacity: 0.9; }
        nav { background: #2d3748; padding: 15px 0; margin-bottom: 30px; position: sticky; top: 0; z-index: 100; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
        nav ul { list-style: none; display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; }
        nav a { color: white; text-decoration: none; padding: 8px 16px; border-radius: 5px; transition: background 0.3s; }
        nav a:hover { background: rgba(255,255,255,0.1); }
        nav a.active { background: #667eea; }
        h2 { color: #667eea; margin: 30px 0 15px 0; padding-bottom: 10px; border-bottom: 2px solid #667eea; }
        h3 { color: #764ba2; margin: 25px 0 12px 0; }
        h4 { color: #4a5568; margin: 20px 0 10px 0; }
        table { width: 100%; border-collapse: collapse; margin: 20px 0; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
        th { background: #667eea; color: white; padding: 12px; text-align: left; }
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
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>📅 PREMRECAC</h1>
            <p class="subtitle">Prêmio Recebível Aceito de Cosseguro</p>
        </div>
    </header>

    <nav>
        <div class="container">
            <ul>
                <li><a href="../../index.html">🏠 Home</a></li>
                <li><a href="index.html">📋 Visão Geral</a></li>
                <li><a href="premac.html">PREMAC</a></li>
                <li><a href="premrecac.html" class="active">PREMRECAC</a></li>
                <li><a href="premrecebc.html">PREMRECEBC</a></li>
                <li><a href="respremc.html">RESPREMC</a></li>
                <li><a href="sinavac.html">SINAVAC</a></li>
                <li><a href="sinpagac.html">SINPAGAC</a></li>
                <li><a href="sinpendac.html">SINPENDAC</a></li>
            </ul>
        </div>
    </nav>

    <div class="container">
        <div class="breadcrumb">
            <a href="../../index.html">Home</a> / 
            <a href="index.html">Retornos</a> / 
            <span>PREMRECAC</span>
        </div>

        <h1>📅 PREMRECAC - Prêmio Recebível Aceito de Cosseguro</h1>

        <div class="alert alert-info">
            <strong>ℹ️ Descrição:</strong> Detalhamento de prêmios por prestação (parcela), mostrando o cronograma de recebimento com valores por ramo e parcela.
        </div>

        <h2>🔧 Especificações Técnicas</h2>
        <table>
            <tr>
                <th>Propriedade</th>
                <th>Valor</th>
            </tr>
            <tr>
                <td><strong>Módulo</strong></td>
                <td>Policy (PolicyCore)</td>
            </tr>
            <tr>
                <td><strong>Filtros</strong></td>
                <td><code>BaseDate</code>, <code>CodCoss=05908</code></td>
            </tr>
            <tr>
                <td><strong>Total de Campos</strong></td>
                <td>20 campos</td>
            </tr>
            <tr>
                <td><strong>Agregação</strong></td>
                <td>Por Ramo + Prestação</td>
            </tr>
            <tr>
                <td><strong>Delimitador</strong></td>
                <td>Pipe (<code>|</code>)</td>
            </tr>
        </table>

        <h2>📋 Estrutura do Arquivo CSV</h2>
        <div class="code-block">
SEQUENCIA|COD_CIA|DT_BASE|TIPO_MOV|COD_RAMO|NUM_APOL|NUM_END|COD_COSS|PRESTACAO|QTDE_PREST|DT_EMIS_PRE|DT_VEN_PRE|DT_INI_VIG|DT_FIM_VIG|PR_COSS_AC|COM_COS_AC|COFEE|PRO_LAB|NUM_PROP|DT_PROP
0000000001|03417|202509|101|0553|POL123|00000000000000000000|05908|1|12|20250901|20251001|20250901|20260901|125.00|12.50|4.17|2.50|PROP123|20250815
0000000002|03417|202509|101|0553|POL123|00000000000000000000|05908|2|12|20251001|20251101|20250901|20260901|125.00|12.50|4.17|2.50|PROP123|20250815
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
                    <td>Tipo de movimento (101, 102, 105)</td>
                </tr>
                <tr>
                    <td><code>COD_RAMO</code></td>
                    <td>Texto</td>
                    <td>Código do ramo SUSEP</td>
                </tr>
                <tr>
                    <td><code>NUM_APOL</code></td>
                    <td>Texto</td>
                    <td>Número da apólice líder</td>
                </tr>
                <tr>
                    <td><code>NUM_END</code></td>
                    <td>Texto</td>
                    <td>Número do endosso líder</td>
                </tr>
                <tr>
                    <td><code>COD_COSS</code></td>
                    <td>Texto</td>
                    <td>Código do cosseguro (05908)</td>
                </tr>
                <tr>
                    <td><code>PRESTACAO</code></td>
                    <td>Numérico</td>
                    <td><strong>Número da prestação/parcela</strong></td>
                </tr>
                <tr>
                    <td><code>QTDE_PREST</code></td>
                    <td>Numérico</td>
                    <td><strong>Quantidade total de prestações</strong></td>
                </tr>
                <tr>
                    <td><code>DT_EMIS_PRE</code></td>
                    <td>Data</td>
                    <td><strong>Data emissão da prestação</strong></td>
                </tr>
                <tr>
                    <td><code>DT_VEN_PRE</code></td>
                    <td>Data</td>
                    <td><strong>Data vencimento da prestação</strong></td>
                </tr>
                <tr>
                    <td><code>DT_INI_VIG</code></td>
                    <td>Data</td>
                    <td>Data início vigência da apólice</td>
                </tr>
                <tr>
                    <td><code>DT_FIM_VIG</code></td>
                    <td>Data</td>
                    <td>Data fim vigência da apólice</td>
                </tr>
                <tr>
                    <td><code>PR_COSS_AC</code></td>
                    <td>Decimal</td>
                    <td>Prêmio cosseguro aceito (da prestação)</td>
                </tr>
                <tr>
                    <td><code>COM_COS_AC</code></td>
                    <td>Decimal</td>
                    <td>Comissão cosseguro aceito</td>
                </tr>
                <tr>
                    <td><code>COFEE</code></td>
                    <td>Decimal</td>
                    <td>COFEE</td>
                </tr>
                <tr>
                    <td><code>PRO_LAB</code></td>
                    <td>Decimal</td>
                    <td>Pro labore</td>
                </tr>
                <tr>
                    <td><code>NUM_PROP</code></td>
                    <td>Texto</td>
                    <td>Número da proposta líder</td>
                </tr>
                <tr>
                    <td><code>DT_PROP</code></td>
                    <td>Data</td>
                    <td>Data da proposta</td>
                </tr>
            </tbody>
        </table>

        <h2>🔄 Lógica de Negócio</h2>

        <h3>1. Extração de Prestações</h3>
        <div class="alert alert-info">
            <strong>ℹ️ Importante:</strong> O PREMRECAC gera <strong>uma linha por ramo × prestação</strong>, criando múltiplas linhas para apólices parceladas.
        </div>

        <pre><code class="language-groovy">// 1. Busca lista de parcelas
List installments = policy.PolicyPaymentInfoList[0].InstallmentList

// 2. Para cada parcela
installments.each { inst ->
    String prestacao = inst.InstallmentNo
    String dtEmisPresta = inst.IssueDate
    String dtVencPresta = inst.DueDate
    Integer qtdePrestacoes = installments.size()
    
    // 3. Gera linhas por Ramo × Prestação
    ramoTotals.each { codRamo, totals ->
        generateLine(
            codRamo: codRamo,
            prestacao: prestacao,
            qtdePrestacoes: qtdePrestacoes,
            dtEmisPresta: dtEmisPresta,
            dtVencPresta: dtVencPresta,
            valores: totals
        )
    }
}</code></pre>

        <h3>2. Mapeamento de TipoMov</h3>
        <table>
            <thead>
                <tr>
                    <th>TipoMov</th>
                    <th>Campo PR_COSS_AC</th>
                    <th>Descrição</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><span class="badge badge-primary">101</span></td>
                    <td><code>PrCossAc</code></td>
                    <td>Emissão original</td>
                </tr>
                <tr>
                    <td><span class="badge badge-warning">102</span></td>
                    <td><code>PrCossAc</code></td>
                    <td>OldPolicy - Prêmio aceito</td>
                </tr>
                <tr>
                    <td><span class="badge badge-warning">105</span></td>
                    <td><code>PrCosCed</code></td>
                    <td>NewPolicy - Prêmio cedido ⚠️</td>
                </tr>
            </tbody>
        </table>

        <h2>📊 Diferenças vs PREMAC</h2>
        <table>
            <thead>
                <tr>
                    <th>Aspecto</th>
                    <th>PREMAC</th>
                    <th>PREMRECAC</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><strong>Granularidade</strong></td>
                    <td>Por Ramo</td>
                    <td>Por Ramo + Prestação</td>
                </tr>
                <tr>
                    <td><strong>Total de Campos</strong></td>
                    <td>26</td>
                    <td>20</td>
                </tr>
                <tr>
                    <td><strong>Linhas por Apólice</strong></td>
                    <td>N ramos</td>
                    <td>N ramos × M prestações</td>
                </tr>
                <tr>
                    <td><strong>Foco</strong></td>
                    <td>Valores consolidados</td>
                    <td>Cronograma de recebimento</td>
                </tr>
                <tr>
                    <td><strong>Fonte Prestações</strong></td>
                    <td>N/A</td>
                    <td><code>InstallmentList</code></td>
                </tr>
            </tbody>
        </table>

        <h2>🗂️ Fonte de Dados</h2>
        <div class="card">
            <h4>Estrutura JSON (InstallmentList):</h4>
            <pre><code class="language-json">{
  "PolicyPaymentInfoList": [{
    "InstallmentList": [
      {
        "InstallmentNo": "1",
        "IssueDate": "2025-09-01",
        "DueDate": "2025-10-01"
      },
      {
        "InstallmentNo": "2",
        "IssueDate": "2025-10-01",
        "DueDate": "2025-11-01"
      }
    ]
  }]
}</code></pre>
        </div>

        <h2>📤 Saída do Arquivo</h2>
        <table>
            <tr>
                <th>Item</th>
                <th>Localização</th>
            </tr>
            <tr>
                <td><strong>CSV de Export</strong></td>
                <td><code>s3://bucket/export/PREMRECAC_202509_20260305_143022.csv</code></td>
            </tr>
            <tr>
                <td><strong>Log Detalhado</strong></td>
                <td><code>s3://bucket/logs/2026-03-05/PREMRECAC/PREMRECAC_DETAILED_202509_20260305_143022.log</code></td>
            </tr>
            <tr>
                <td><strong>Log de Erros</strong></td>
                <td><code>s3://bucket/logs/2026-03-05/PREMRECAC/error/LOG_PREMRECAC_202509_*.csv</code></td>
            </tr>
        </table>

        <h2>🚀 Exemplo de Uso</h2>
        <pre><code class="language-groovy">// Executar export para setembro/2025
process("202509")</code></pre>

        <div class="alert alert-success">
            <strong>✅ Resultado esperado:</strong>
            <ul>
                <li>Apólice parcelada em 12x com 2 ramos → <strong>24 linhas</strong> (12 × 2)</li>
                <li>Apólice à vista com 1 ramo → <strong>1 linha</strong></li>
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
