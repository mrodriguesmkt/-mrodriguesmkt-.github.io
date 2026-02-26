<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Programa de Sustentabilidade AWS - Nuage IT</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
            line-height: 1.6;
            color: #e0e0e0;
            background: #1a0f2e;
            padding: 0;
            margin: 0;
        }
        
        .container {
            max-width: 680px;
            margin: 0 auto;
            background: #1a0f2e;
            border-radius: 0;
        }
        
        .header {
            background: linear-gradient(135deg, #2d1b4e 0%, #1a0f2e 100%);
            padding: 50px 30px;
            text-align: center;
            position: relative;
        }
        
        .header::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80%;
            height: 1px;
            background: linear-gradient(90deg, transparent 0%, rgba(232, 89, 255, 0.5) 50%, transparent 100%);
        }
        
        .badge {
            display: inline-block;
            background: rgba(232, 89, 255, 0.15);
            border: 1px solid rgba(232, 89, 255, 0.4);
            border-radius: 20px;
            padding: 6px 16px;
            font-size: 11px;
            font-weight: 600;
            letter-spacing: 1px;
            text-transform: uppercase;
            color: #e859ff;
            margin-bottom: 20px;
        }
        
        .header h1 {
            color: #ffffff;
            font-size: 32px;
            font-weight: 700;
            margin-bottom: 12px;
            letter-spacing: -0.5px;
        }
        
        .header .logo-container {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 20px;
            margin-bottom: 20px;
        }
        
        .header .logo-icon {
            font-size: 36px;
            opacity: 0.8;
        }
        
        .header .logo-text {
            font-size: 48px;
            font-weight: 700;
            color: #ffffff;
            letter-spacing: 3px;
            background: linear-gradient(135deg, #e859ff 0%, #29becc 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .header p {
            color: #a0a0b0;
            font-size: 15px;
            margin-top: 10px;
            line-height: 1.5;
        }
        
        .content {
            padding: 40px 30px;
        }
        
        .greeting {
            color: #e0e0e0;
            font-size: 16px;
            margin-bottom: 30px;
            line-height: 1.8;
            background: rgba(232, 89, 255, 0.05);
            padding: 25px;
            border-radius: 8px;
            border-left: 3px solid #e859ff;
        }
        
        .greeting strong {
            color: #e859ff;
        }
        
        .section {
            margin-bottom: 45px;
        }
        
        .section-title {
            color: #e859ff;
            font-size: 20px;
            font-weight: 700;
            margin-bottom: 8px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            font-size: 13px;
        }
        
        .section-subtitle {
            color: #ffffff;
            font-size: 24px;
            font-weight: 700;
            margin-bottom: 20px;
        }
        
        .section-description {
            color: #a0a0b0;
            font-size: 15px;
            margin-bottom: 25px;
            line-height: 1.7;
        }
        
        .activity-card {
            background: rgba(45, 27, 78, 0.4);
            border: 1px solid rgba(232, 89, 255, 0.15);
            padding: 20px;
            margin-bottom: 12px;
            border-radius: 8px;
            transition: all 0.3s ease;
        }
        
        .activity-card:hover {
            background: rgba(45, 27, 78, 0.6);
            border-color: rgba(232, 89, 255, 0.4);
            transform: translateX(3px);
        }
        
        .activity-title {
            color: #ffffff;
            font-size: 15px;
            font-weight: 600;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .activity-description {
            color: #a0a0b0;
            font-size: 14px;
            line-height: 1.6;
        }
        
        .tool-section {
            background: rgba(45, 27, 78, 0.3);
            border: 1px solid rgba(232, 89, 255, 0.2);
            padding: 30px;
            border-radius: 12px;
            margin: 35px 0;
        }
        
        .tool-title {
            color: #e859ff;
            font-size: 13px;
            font-weight: 700;
            margin-bottom: 8px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
        
        .tool-heading {
            color: #ffffff;
            font-size: 24px;
            font-weight: 700;
            margin-bottom: 15px;
        }
        
        .tool-description {
            color: #a0a0b0;
            font-size: 15px;
            line-height: 1.7;
            margin-bottom: 25px;
        }
        
        .info-box {
            background: rgba(232, 89, 255, 0.08);
            border-left: 3px solid #e859ff;
            padding: 18px;
            margin: 15px 0;
            border-radius: 6px;
        }
        
        .info-box strong {
            color: #e859ff;
            display: block;
            margin-bottom: 10px;
            font-size: 14px;
            font-weight: 600;
        }
        
        .info-box p {
            color: #b0b0c0;
            font-size: 13px;
            line-height: 1.7;
            margin: 0;
        }
        
        .screenshot-placeholder {
            background: rgba(26, 15, 46, 0.6);
            border: 2px dashed rgba(232, 89, 255, 0.3);
            padding: 40px;
            text-align: center;
            border-radius: 8px;
            margin: 20px 0;
            transition: border-color 0.3s ease;
        }
        
        .screenshot-placeholder:hover {
            border-color: rgba(232, 89, 255, 0.5);
        }
        
        .screenshot-placeholder p {
            color: #e859ff;
            font-size: 14px;
            font-weight: 600;
            margin-bottom: 8px;
        }
        
        .screenshot-placeholder small {
            color: #808090;
            font-size: 12px;
            line-height: 1.5;
            display: block;
        }
        
        .cta-section {
            background: linear-gradient(135deg, #e859ff 0%, #b84ddb 100%);
            padding: 35px 30px;
            border-radius: 12px;
            text-align: center;
            margin: 40px 0;
            box-shadow: 0 8px 24px rgba(232, 89, 255, 0.25);
        }
        
        .cta-section h3 {
            color: #ffffff;
            font-size: 24px;
            font-weight: 700;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }
        
        .cta-section p {
            color: rgba(255, 255, 255, 0.95);
            font-size: 15px;
            line-height: 1.7;
            margin-bottom: 10px;
        }
        
        .cta-section ul {
            text-align: left;
            display: inline-block;
            margin: 20px 0;
        }
        
        .cta-section li {
            color: rgba(255, 255, 255, 0.95);
            font-size: 15px;
            margin-bottom: 10px;
            line-height: 1.5;
        }
        
        .resources {
            background: rgba(45, 27, 78, 0.3);
            border: 1px solid rgba(232, 89, 255, 0.2);
            padding: 25px;
            border-radius: 8px;
            margin: 35px 0;
        }
        
        .resources h3 {
            color: #e859ff;
            font-size: 13px;
            font-weight: 700;
            margin-bottom: 8px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
        
        .resources .resources-title {
            color: #ffffff;
            font-size: 20px;
            font-weight: 700;
            margin-bottom: 20px;
        }
        
        .resources a {
            color: #e859ff;
            text-decoration: none;
            font-size: 14px;
            display: block;
            margin-bottom: 12px;
            transition: all 0.2s;
            padding-left: 20px;
            position: relative;
        }
        
        .resources a::before {
            content: '→';
            position: absolute;
            left: 0;
            transition: transform 0.2s;
        }
        
        .resources a:hover {
            color: #ffffff;
            padding-left: 25px;
        }
        
        .resources a:hover::before {
            transform: translateX(3px);
        }
        
        .footer {
            background: rgba(26, 15, 46, 0.8);
            padding: 35px 30px;
            text-align: center;
            border-top: 1px solid rgba(232, 89, 255, 0.15);
        }
        
        .footer p {
            color: #808090;
            font-size: 13px;
            line-height: 1.7;
            margin-bottom: 8px;
        }
        
        .footer strong {
            color: #e859ff;
            font-size: 15px;
            display: block;
            margin-bottom: 15px;
            font-weight: 600;
        }
        
        .divider {
            height: 1px;
            background: linear-gradient(90deg, transparent 0%, rgba(232, 89, 255, 0.3) 50%, transparent 100%);
            margin: 35px 0;
        }
        
        @media only screen and (max-width: 600px) {
            .container {
                border-radius: 0;
            }
            
            .header, .content, .footer {
                padding: 25px 20px;
            }
            
            .header h1 {
                font-size: 26px;
            }
            
            .section-subtitle {
                font-size: 22px;
            }
            
            .activity-card {
                padding: 16px;
            }
            
            .cta-section {
                padding: 30px 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <div class="logo-container">
                <span class="logo-icon">🌱</span>
                <span class="logo-text">NUAGE IT</span>
                <span class="logo-icon">🌱</span>
            </div>
            <div class="badge">Programa de Sustentabilidade</div>
            <h1>Sustentabilidade AWS</h1>
            <p>Como a Nuage IT Pode Apoiar sua Jornada de Redução de Emissões</p>
        </div>
        
        <!-- Content -->
        <div class="content">
            <!-- Greeting -->
            <div class="greeting">
                Prezado(a) <strong>[Nome do Cliente]</strong>,<br><br>
                A AWS está comprometida com a sustentabilidade e oferece ferramentas e práticas recomendadas para que empresas possam medir e reduzir suas emissões de carbono na nuvem. Como parceiro AWS MSP, a Nuage IT está alinhada com essas iniciativas e gostaríamos de apresentar como podemos apoiar sua empresa nessa jornada de sustentabilidade.
            </div>
            
            <div class="divider"></div>
            
            <!-- How We Can Help -->
            <div class="section">
                <h2 class="section-title">🤝 Como Podemos Apoiá-los</h2>
                <h3 class="section-subtitle">10 Práticas de Sustentabilidade AWS</h3>
                <p class="section-description">A Nuage IT pode implementar e gerenciar práticas de sustentabilidade que contribuem diretamente para a redução de emissões de carbono em sua infraestrutura AWS:</p>
                
                <div class="activity-card">
                    <div class="activity-title">🔍 1. Detecção Automática de Anomalias de Recursos</div>
                    <div class="activity-description">Implementação de monitoramento contínuo para identificar recursos AWS com uso anômalo ou desperdiçado, permitindo ação imediata para desligar ou redimensionar recursos desnecessários.</div>
                </div>
                
                <div class="activity-card">
                    <div class="activity-title">📊 2. Rightsizing de Instâncias EC2</div>
                    <div class="activity-description">Análise periódica de utilização de CPU, memória e rede para ajustar o tamanho das instâncias EC2, garantindo que você use apenas a capacidade necessária e reduza desperdício energético.</div>
                </div>
                
                <div class="activity-card">
                    <div class="activity-title">🧹 3. Limpeza de Recursos Órfãos</div>
                    <div class="activity-description">Identificação e remoção de recursos não utilizados como EBS volumes desanexados, snapshots antigos, Elastic IPs não associados e AMIs obsoletas que consomem energia desnecessariamente.</div>
                </div>
                
                <div class="activity-card">
                    <div class="activity-title">⚡ 4. Arquitetura com Instâncias AWS Graviton</div>
                    <div class="activity-description">Projeto e implementação de arquiteturas baseadas em processadores ARM (Graviton), que consomem até 60% menos energia que instâncias x86 equivalentes, mantendo ou melhorando a performance.</div>
                </div>
                
                <div class="activity-card">
                    <div class="activity-title">💡 5. Estratégia de Spot Instances</div>
                    <div class="activity-description">Implementação de Spot Instances para workloads não-críticos, aproveitando capacidade ociosa da AWS e reduzindo desperdício de recursos computacionais em até 90%.</div>
                </div>
                
                <div class="activity-card">
                    <div class="activity-title">📈 6. Autoscaling Inteligente (HPA/VPA)</div>
                    <div class="activity-description">Configuração de Horizontal Pod Autoscaler (HPA) e Vertical Pod Autoscaler (VPA) em clusters Kubernetes, garantindo alocação dinâmica de recursos conforme demanda real.</div>
                </div>
                
                <div class="activity-card">
                    <div class="activity-title">⏰ 7. Automação de Desligamento de Ambientes</div>
                    <div class="activity-description">Implementação de automação para desligar ambientes de desenvolvimento e staging fora do horário comercial, reduzindo tempo de execução desnecessário em 60-70%.</div>
                </div>
                
                <div class="activity-card">
                    <div class="activity-title">📦 8. Consolidação de Workloads (Bin Packing)</div>
                    <div class="activity-description">Otimização da densidade de containers em clusters Kubernetes, reduzindo o número total de instâncias EC2 necessárias através de melhor aproveitamento de recursos físicos.</div>
                </div>
                
                <div class="activity-card">
                    <div class="activity-title">🌍 9. Escolha de Região AWS com Energia Renovável</div>
                    <div class="activity-description">Recomendação e implementação de workloads em regiões AWS alimentadas por energia renovável, priorizando data centers com menor pegada de carbono e maior uso de fontes limpas.</div>
                </div>
                
                <div class="activity-card">
                    <div class="activity-title">☁️ 10. Migração para Serviços Serverless</div>
                    <div class="activity-description">Análise e implementação de serviços serverless (Lambda, Fargate) quando aplicável, eliminando necessidade de manter servidores em execução contínua.</div>
                </div>
            </div>
            
            <div class="divider"></div>
            
            <!-- AWS Carbon Footprint Tool -->
            <div class="tool-section">
                <h2 class="tool-title">🌍 AWS Customer Carbon Footprint Tool</h2>
                <h3 class="tool-heading">Ferramenta de Pegada de Carbono</h3>
                <p class="tool-description">A AWS disponibiliza gratuitamente a ferramenta <strong>Customer Carbon Footprint Tool</strong>, que permite visualizar e acompanhar as emissões de carbono de sua infraestrutura AWS. A Nuage IT pode auxiliar na ativação e interpretação dos dados.</p>
                
                <h3 style="color: #e859ff; font-size: 13px; margin: 25px 0 15px 0; text-transform: uppercase; letter-spacing: 0.5px; font-weight: 700;">📋 O que a ferramenta oferece</h3>
                
                <div class="info-box">
                    <strong>Como as emissões são calculadas?</strong>
                    <p>O CCFT quantifica as emissões de gases de efeito estufa (GEE) específicas do cliente associadas ao uso dos serviços da nuvem AWS. O CCFT inclui dados do Escopo 1 (emissões diretas de fontes próprias ou controladas) e do Escopo 2 (emissões de GEE que ocorrem quando uma empresa compra energia). As emissões do Escopo 3 (emissões da cadeia de valor) são calculadas usando o método baseado no mercado (MBM) por padrão.</p>
                </div>
                
                <div class="info-box">
                    <strong>Como as emissões são divididas?</strong>
                    <p>Dividimos as emissões por serviço da AWS. Para detalhamento por serviço, você pode ver as emissões resultantes especificamente do uso de EC2, S3 ou CloudFront. Todos os demais serviços são agrupados em "Outros". As emissões são calculadas usando o método baseado no mercado (MBM) por padrão.</p>
                </div>
                
                <div class="info-box">
                    <strong>Como faço para acessar os dados em massa?</strong>
                    <p>Você pode clicar no botão "Baixar CSV" no canto superior direito para baixar um arquivo CSV com as informações de carbono dos últimos 38 meses. Esse arquivo ajuda a ver o carbono por serviço de todas as regiões da AWS em que você opera.</p>
                </div>
                
                <h3 style="color: #e859ff; font-size: 13px; margin: 30px 0 15px 0; text-transform: uppercase; letter-spacing: 0.5px; font-weight: 700;">📊 Visualizações Disponíveis no Painel</h3>
                
                <div class="screenshot-placeholder">
                    <p>📉 Emissões de Carbono Totais</p>
                    <small>Gráfico de tendência de emissões de CO2e (toneladas métricas) ao longo do tempo<br>Comparação mês a mês dos últimos 12-38 meses</small>
                </div>
                
                <div class="screenshot-placeholder">
                    <p>🔧 Emissões por Serviço AWS</p>
                    <small>Breakdown de emissões por serviço (EC2, S3, CloudFront, RDS, etc.)<br>Identificação dos serviços com maior impacto ambiental</small>
                </div>
                
                <div class="screenshot-placeholder">
                    <p>🗺️ Emissões por Região AWS</p>
                    <small>Distribuição geográfica das emissões<br>Comparação entre regiões com diferentes matrizes energéticas</small>
                </div>
            </div>
            
            <div class="divider"></div>
            
            <!-- CTA Section -->
            <div class="cta-section">
                <h3>🚀 Próximos Passos</h3>
                <p>Se você tiver interesse em explorar como a Nuage IT pode apoiar sua empresa na implementação de um programa de sustentabilidade AWS, ficaremos felizes em agendar uma conversa para:</p>
                <ul>
                    <li>Apresentar o AWS Customer Carbon Footprint Tool e como ativá-lo em suas contas</li>
                    <li>Realizar assessment de oportunidades de otimização sustentável em sua infraestrutura</li>
                    <li>Definir roadmap de implementação de práticas de sustentabilidade</li>
                    <li>Estabelecer metas de redução de emissões para 2026</li>
                </ul>
                <p style="margin-top: 20px;">Estamos comprometidos em apoiar sua empresa não apenas na excelência operacional, mas também na responsabilidade ambiental.</p>
            </div>
            
            <!-- Resources -->
            <div class="resources">
                <h3>📚 Recursos Adicionais</h3>
                <div class="resources-title">Saiba Mais sobre Sustentabilidade AWS</div>
                <a href="https://sustainability.aboutamazon.com/" target="_blank">AWS Sustainability</a>
                <a href="https://aws.amazon.com/aws-cost-management/aws-customer-carbon-footprint-tool/" target="_blank">AWS Customer Carbon Footprint Tool</a>
                <a href="https://docs.aws.amazon.com/wellarchitected/latest/sustainability-pillar/sustainability-pillar.html" target="_blank">AWS Well-Architected Framework - Sustainability Pillar</a>
            </div>
        </div>
        
        <!-- Footer -->
        <div class="footer">
            <strong>Nuage IT - AWS Partner</strong>
            <p>Este email faz parte do Programa de Sustentabilidade AWS da Nuage IT.<br>
            Para mais informações, entre em contato com seu Customer Success Manager.</p>
        </div>
    </div>
</body>
</html>
