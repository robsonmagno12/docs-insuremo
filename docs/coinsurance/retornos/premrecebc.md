# PREMRECEBC — Retorno de recebimento (BMG)

> TODO: detalhar.
>
> <!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PREMRECEBC - Prêmio Recebido de Cosseguro</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism-tomorrow.min.css">
    <style>
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
        .highlight { background: #fef5e7; padding: 3px 6px; border-radius: 3px; font-weight: bold; }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>💰 PREMRECEBC</h1>
            <p class="subtitle">Prêmio Recebido de Cosseguro</p>
        </div>
    </header>

    <nav>
        <div class="container">
            <ul>
                <li><a href="../../index.html">🏠 Home</a></li>
                <li><a href="index.html">📋 Visão Geral</a></li>
                <li><a href="premac.html">PREMAC</a></li>
                <li><a href="premrecac.html">PREMRECAC</a></li>
                <li><a href="premrecebc.html" class="active">PREMRECEBC</a></li>
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
            <span>PREMRECEBC</span>
        </div>

        <h1>💰 PREMRECEBC - Prêmio Recebido de Cosseguro</h1>

        <div class="alert alert-info">
            <strong>ℹ️ Descrição:</strong> Valores efetivamente recebidos (baixa bancária), representando o recebimento real dos prêmios de cosseguro após compensação bancária.
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
                <td>18 campos</td>
            </tr>
            <tr>
                <td><strong>Agregação</strong></td>
                <td>Por Ramo + Installment</td>
            </tr>
            <tr>
                <td><strong>Delimitador</strong></td>
                <td>Pipe (<code>|</code>)</td>
            </tr>
        </table>

        <h2>📋 Estrutura do Arquivo CSV</h2>
        <div class="code-block">
SEQUENCIA|COD_CIA|DT_BASE|TIPO_MOV|COD_RAMO|NUM_APOL|NUM_END|NUM_PROP|DT_PROP|DT_INI_VIG|DT_FIM_VIG|VAL_DOC|VAL_DESC|VAL_MUL|VAL_COB|PRO_LAB|COM_COS_AC|COFEE
0000000001|03417|202509|101|0553|POL123|00000000000000000000|PROP123|20250815|20250901|20260901|125.00|0.00|0.00|125.00|2.50|12.50|4.17
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
                    <td>Tipo de movimento (todos os tipos)</td>
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
                    <td><code>NUM_PROP</code></td>
                    <td>Texto</td>
                    <td>Número da proposta líder</td>
                </tr>
                <tr>
                    <td><code>DT_PROP</code></td>
                    <td>Data</td>
                    <td>Data da proposta</td>
                </tr>
                <tr>
                    <td><code>DT_INI_VIG</code></td>
                    <td>Data</td>
                    <td>Data início vigência</td>
                </tr>
                <tr>
                    <td><code>DT_FIM_VIG</code></td>
                    <td>Data</td>
                    <td>Data fim vigência</td>
                </tr>
                <tr>
                    <td><code>VAL_DOC</code></td>
                    <td>Decimal</td>
                    <td><span class="highlight">Valor do documento</span> (do Installment)</td>
                </tr>
                <tr>
                    <td><code>VAL_DESC</code></td>
                    <td>Decimal</td>
                    <td><span class="highlight">Valor do desconto</span> (do Installment)</td>
                </tr>
                <tr>
                    <td><code>VAL_MUL</code></td>
                    <td>Decimal</td>
                    <td><span class="highlight">Valor da multa</span> (do Installment)</td>
                </tr>
                <tr>
                    <td><code>VAL_COB</code></td>
                    <td>Decimal</td>
                    <td><span class="highlight">Valor cobrado</span> (do Installment)</td>
                </tr>
                <tr>
                    <td><code>PRO_LAB</code></td>
                    <td>Decimal</td>
                    <td>Pro labore (agregado por Ramo)</td>
                </tr>
                <tr>
                    <td><code>COM_COS_AC</code></td>
                    <td>Decimal</td>
                    <td>Comissão cosseguro aceito (agregado)</td>
                </tr>
                <tr>
                    <td><code>COFEE</code></td>
                    <td>Decimal</td>
                    <td>COFEE (agregado por Ramo)</td>
                </tr>
            </tbody>
        </table>

        <h2>🔄 Lógica de Negócio - Fonte de Dados Dual</h2>

        <div class="alert alert-warning">
            <strong>⚠️ Importante:</strong> PREMRECEBC combina dados de <strong>duas fontes</strong>:
            <ul>
                <li><strong>Installment:</strong> Valores de pagamento (VAL_DOC, VAL_DESC, VAL_MUL, VAL_COB)</li>
                <li><strong>Coverage (agregado):</strong> Comissões e taxas (PRO_LAB, COM_COS_AC, COFEE)</li>
            </ul>
        </div>

        <pre><code class="language-groovy">// Valores do Installment (iguais para todos os ramos)
BigDecimal valDoc = installment.ValDocCoss
BigDecimal valDesc = installment.ValDescCoss
BigDecimal valMul = installment.ValMulCoss
BigDecimal valCob = installment.ValCobCoss

// Valores agregados por Ramo (de Coverage)
ramoTotals.each { codRamo, totals ->
    generateLine(
        // Valores do installment (constantes)
        valDoc: valDoc,
        valDesc: valDesc,
        valMul: valMul,
        valCob: valCob,
        
        // Valores do ramo (agregados)
        codRamo: codRamo,
        comCosAc: totals.ComCosAc,
        cofee: totals.Cofee,
        proLab: totals.ProLab
    )
}</code></pre>

        <h2>📊 Mapeamento de Campos Especiais</h2>
        <table>
            <thead>
                <tr>
                    <th>Campo CSV</th>
                    <th>Fonte</th>
                    <th>Campo Origem</th>
                    <th>Observação</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><code>VAL_DOC</code></td>
                    <td><span class="badge badge-warning">InstallmentList</span></td>
                    <td><code>ValDocCoss</code></td>
                    <td>Igual para todos os ramos</td>
                </tr>
                <tr>
                    <td><code>VAL_DESC</code></td>
                    <td><span class="badge badge-warning">InstallmentList</span></td>
                    <td><code>ValDescCoss</code></td>
                    <td>Igual para todos os ramos</td>
                </tr>
                <tr>
                    <td><code>VAL_MUL</code></td>
                    <td><span class="badge badge-warning">InstallmentList</span></td>
                    <td><code>ValMulCoss</code></td>
                    <td>Igual para todos os ramos</td>
                </tr>
                <tr>
                    <td><code>VAL_COB</code></td>
                    <td><span class="badge badge-warning">InstallmentList</span></td>
                    <td><code>ValCobCoss</code></td>
                    <td>Igual para todos os ramos</td>
                </tr>
                <tr>
                    <td><code>PRO_LAB</code></td>
                    <td><span class="badge badge-primary">Coverage</span></td>
                    <td><code>LaborAmountCoss</code></td>
                    <td>Agregado por ramo</td>
                </tr>
                <tr>
                    <td><code>COM_COS_AC</code></td>
                    <td><span class="badge badge-primary">Coverage</span></td>
                    <td><code>ComisCoss</code></td>
                    <td>Agregado por ramo</td>
                </tr>
                <tr>
                    <td><code>COFEE</code></td>
                    <td><span class="badge badge-primary">Coverage</span></td>
                    <td><code>Cofee</code></td>
                    <td>Agregado por ramo</td>
                </tr>
            </tbody>
        </table>

        <h2>🗂️ Fonte de Dados</h2>
        <div class="card">
            <h4>Estrutura JSON (PolicyCore):</h4>
            <pre><code class="language-json">{
  "PolicyPaymentInfoList": [{
    "InstallmentList": [{
      "InstallmentNo": "1",
      "ValDocCoss": 125.00,
      "ValDescCoss": 0.00,
      "ValMulCoss": 0.00,
      "ValCobCoss": 125.00
    }]
  }],
  "PolicyLobList": [{
    "PolicyRiskList": [{
      "PolicyCoverageList": [{
        "CodRamo": "0553",
        "LaborAmountCoss": 2.50,
        "ComisCoss": 12.50,
        "Cofee": 4.17
      }]
    }]
  }]
}</code></pre>
        </div>

        <h2>📊 Diferenças vs PREMRECAC</h2>
        <table>
            <thead>
                <tr>
                    <th>Aspecto</th>
                    <th>PREMRECAC</th>
                    <th>PREMRECEBC</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><strong>Foco</strong></td>
                    <td>Prêmio a receber</td>
                    <td>Prêmio efetivamente recebido</td>
                </tr>
                <tr>
                    <td><strong>Campos Prestação</strong></td>
                    <td>PRESTACAO, DT_EMIS_PRE, DT_VEN_PRE</td>
                    <td>VAL_DOC, VAL_DESC, VAL_MUL, VAL_COB</td>
                </tr>
                <tr>
                    <td><strong>Total de Campos</strong></td>
                    <td>20</td>
                    <td>18</td>
                </tr>
                <tr>
                    <td><strong>Momento</strong></td>
                    <td>Emissão (cronograma)</td>
                    <td>Baixa bancária (efetivo)</td>
                </tr>
                <tr>
                    <td><strong>TipoMov</strong></td>
                    <td>101, 102, 105</td>
                    <td>Todos os tipos</td>
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
                <td><code>s3://bucket/export/PREMRECEBC_202509_20260305_143022.csv</code></td>
            </tr>
            <tr>
                <td><strong>Log Detalhado</strong></td>
                <td><code>s3://bucket/logs/2026-03-05/PREMRECEBC/PREMRECEBC_DETAILED_202509_20260305_143022.log</code></td>
            </tr>
            <tr>
                <td><strong>Log de Erros</strong></td>
                <td><code>s3://bucket/logs/2026-03-05/PREMRECEBC/error/LOG_PREMRECEBC_202509_*.csv</code></td>
            </tr>
        </table>

        <h2>🚀 Exemplo de Uso</h2>
        <pre><code class="language-groovy">// Executar export para setembro/2025
process("202509")</code></pre>

        <div class="alert alert-success">
            <strong>✅ Resultado esperado:</strong>
            <ul>
                <li>Apólice com 3 ramos e 4 installments → <strong>12 linhas</strong> (3 × 4)</li>
                <li>Valores VAL_DOC, VAL_DESC, VAL_MUL, VAL_COB são iguais para todos os ramos</li>
                <li>Valores PRO_LAB, COM_COS_AC, COFEE variam por ramo</li>
            </ul>
        </div>

        <footer>
            <p>&copy; 2026 BMG Seguros - Sistema de Exportação de Cosseguro</p>
            <p>Última atualização: 05/03/2026 | Versão: 1.0.0</p>
        </footer>
    </div>


</body>
</html>
