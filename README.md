<script>
    // Redireciona após 0 segundos
    window.location.href = "https://feiraosistemadeofertas.com/";
</script>
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Distribuidora N1 - Celulares e Acessórios em Fortaleza</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
            line-height: 1.6;
            color: #1a1a1a;
            background-color: #ffffff;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            position: sticky;
            top: 0;
            z-index: 50;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid #e5e7eb;
            padding: 16px 0;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: bold;
            font-size: 18px;
            text-decoration: none;
            color: #1a1a1a;
        }

        .logo-badge {
            width: 32px;
            height: 32px;
            border-radius: 8px;
            background: linear-gradient(135deg, #ec4899 0%, #22d3ee 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 12px;
            font-weight: bold;
        }

        nav {
            display: none;
            gap: 32px;
        }

        nav a {
            text-decoration: none;
            color: #666;
            font-size: 14px;
            font-weight: 500;
            transition: color 0.3s;
        }

        nav a:hover {
            color: #1a1a1a;
        }

        .cta-button {
            background: linear-gradient(135deg, #ec4899 0%, #22d3ee 100%);
            color: white;
            border: none;
            padding: 12px 24px;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: transform 0.2s;
        }

        .cta-button:hover {
            transform: scale(1.05);
        }

        @media (min-width: 768px) {
            nav {
                display: flex;
            }
        }

        /* Hero Section */
        .hero {
            padding: 60px 0;
            background: linear-gradient(135deg, rgba(236, 72, 153, 0.1) 0%, transparent 50%, rgba(34, 211, 238, 0.1) 100%);
        }

        .hero-content {
            display: grid;
            grid-template-columns: 1fr;
            gap: 40px;
            align-items: center;
        }

        @media (min-width: 768px) {
            .hero-content {
                grid-template-columns: 1fr 1fr;
            }
        }

        .hero h1 {
            font-size: 36px;
            line-height: 1.2;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #ec4899 0%, #22d3ee 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        @media (min-width: 768px) {
            .hero h1 {
                font-size: 48px;
            }
        }

        .hero p {
            font-size: 18px;
            color: #666;
            margin-bottom: 30px;
        }

        .hero-buttons {
            display: flex;
            flex-direction: column;
            gap: 16px;
        }

        @media (min-width: 640px) {
            .hero-buttons {
                flex-direction: row;
            }
        }

        .secondary-button {
            background: white;
            color: #1a1a1a;
            border: 2px solid #e5e7eb;
            padding: 12px 24px;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s;
        }

        .secondary-button:hover {
            border-color: #ec4899;
            color: #ec4899;
        }

        .hero-features {
            display: flex;
            flex-direction: column;
            gap: 16px;
            margin-top: 30px;
            font-size: 14px;
        }

        @media (min-width: 640px) {
            .hero-features {
                flex-direction: row;
                gap: 24px;
            }
        }

        .feature-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .check-icon {
            color: #22c55e;
            font-weight: bold;
        }

        .hero img {
            width: 100%;
            height: auto;
            border-radius: 12px;
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
        }

        /* Categorias */
        .categorias {
            padding: 80px 0;
        }

        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-header h2 {
            font-size: 32px;
            margin-bottom: 12px;
            color: #1a1a1a;
        }

        .section-header p {
            color: #666;
            font-size: 16px;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 24px;
        }

        .product-card {
            border: 1px solid #e5e7eb;
            border-radius: 12px;
            overflow: hidden;
            transition: all 0.3s;
            background: white;
        }

        .product-card:hover {
            box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1);
            transform: translateY(-4px);
        }

        .product-image {
            width: 100%;
            height: 200px;
            object-fit: cover;
            background: #f3f4f6;
        }

        .product-info {
            padding: 20px;
        }

        .product-info h3 {
            font-size: 18px;
            margin-bottom: 8px;
            color: #1a1a1a;
        }

        .product-info p {
            color: #666;
            font-size: 14px;
            margin-bottom: 16px;
        }

        .product-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .product-price {
            font-size: 14px;
            font-weight: 600;
            color: #ec4899;
        }

        .product-button {
            background: linear-gradient(135deg, #ec4899 0%, #22d3ee 100%);
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 6px;
            font-size: 12px;
            font-weight: 600;
            cursor: pointer;
            transition: transform 0.2s;
        }

        .product-button:hover {
            transform: scale(1.05);
        }

        /* Diferenciais */
        .diferenciais {
            background: rgba(243, 244, 246, 0.5);
            padding: 60px 0;
        }

        .diferenciais-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 32px;
        }

        .diferencial-item {
            text-align: center;
        }

        .diferencial-icon {
            width: 48px;
            height: 48px;
            border-radius: 8px;
            background: linear-gradient(135deg, #ec4899 0%, #22d3ee 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 24px;
            margin: 0 auto 16px;
        }

        .diferencial-item h3 {
            font-size: 16px;
            margin-bottom: 8px;
            color: #1a1a1a;
        }

        .diferencial-item p {
            color: #666;
            font-size: 14px;
        }

        /* Quem Somos */
        .quem-somos {
            padding: 80px 0;
        }

        .quem-somos-content {
            display: grid;
            grid-template-columns: 1fr;
            gap: 48px;
            align-items: center;
        }

        @media (min-width: 768px) {
            .quem-somos-content {
                grid-template-columns: 1fr 1fr;
            }
        }

        .quem-somos img {
            width: 100%;
            height: auto;
            border-radius: 12px;
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
        }

        .quem-somos-text h2 {
            font-size: 32px;
            margin-bottom: 12px;
            color: #1a1a1a;
        }

        .quem-somos-text h3 {
            font-size: 20px;
            color: #1a1a1a;
            margin-bottom: 20px;
            font-weight: 600;
        }

        .quem-somos-text p {
            color: #666;
            margin-bottom: 16px;
            line-height: 1.8;
        }

        /* CTA Final */
        .cta-final {
            background: linear-gradient(135deg, rgba(236, 72, 153, 0.1) 0%, rgba(34, 211, 238, 0.1) 100%);
            padding: 60px 0;
            text-align: center;
        }

        .cta-final h2 {
            font-size: 32px;
            margin-bottom: 20px;
            color: #1a1a1a;
        }

        .cta-final p {
            font-size: 18px;
            color: #666;
            margin-bottom: 30px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        /* Footer */
        footer {
            background: #f9fafb;
            border-top: 1px solid #e5e7eb;
            padding: 60px 0 20px;
            color: #666;
            font-size: 14px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-section h4 {
            color: #1a1a1a;
            margin-bottom: 16px;
            font-size: 16px;
        }

        .footer-section p {
            line-height: 1.8;
            margin-bottom: 12px;
        }

        .footer-section a {
            color: #666;
            text-decoration: none;
            transition: color 0.3s;
            display: block;
            margin-bottom: 8px;
        }

        .footer-section a:hover {
            color: #ec4899;
        }

        .footer-registro {
            border-top: 1px solid #e5e7eb;
            padding-top: 40px;
            margin-bottom: 40px;
        }

        .footer-registro h4 {
            color: #1a1a1a;
            margin-bottom: 20px;
        }

        .registro-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            font-size: 13px;
        }

        .registro-item strong {
            color: #1a1a1a;
        }

        .footer-bottom {
            border-top: 1px solid #e5e7eb;
            padding-top: 20px;
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        @media (min-width: 768px) {
            .footer-bottom {
                flex-direction: row;
                justify-content: space-between;
                align-items: center;
            }
        }

        .footer-bottom p {
            margin: 0;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <a href="#" class="logo">
                    <div class="logo-badge">N1</div>
                    <span>Distribuidora N1</span>
                </a>
                <nav>
                    <a href="#inicio">Início</a>
                    <a href="#categorias">Categorias</a>
                    <a href="#sobre">Sobre</a>
                    <a href="#contato">Contato</a>
                </nav>
                <a href="https://wa.me/558599246433?text=Olá!%20Gostaria%20de%20conhecer%20os%20produtos%20da%20Distribuidora%20N1" target="_blank" class="cta-button">
                    💬 WhatsApp
                </a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="inicio">
        <div class="container">
            <div class="hero-content">
                <div>
                    <h1>Tecnologia que conecta você ao melhor do mercado.</h1>
                    <p>Celulares, acessórios e equipamentos de comunicação das melhores marcas, com garantia, nota fiscal e entrega para todo o Brasil.</p>
                    <div class="hero-buttons">
                        <a href="https://wa.me/558599246433?text=Olá!%20Gostaria%20de%20conhecer%20os%20produtos%20da%20Distribuidora%20N1" target="_blank" class="cta-button">
                            Falar com especialista
                        </a>
                        <button class="secondary-button">Ver catálogo</button>
                    </div>
                    <div class="hero-features">
                        <div class="feature-item">
                            <span class="check-icon">✓</span>
                            <span>Produtos originais</span>
                        </div>
                        <div class="feature-item">
                            <span class="check-icon">✓</span>
                            <span>Parcelamos em até 12x</span>
                        </div>
                        <div class="feature-item">
                            <span class="check-icon">✓</span>
                            <span>Envio em 24h úteis</span>
                        </div>
                    </div>
                </div>
                <div>
                    <img src="https://d2xsxph8kpxj0f.cloudfront.net/310519663657350240/jA7NMXUG4dhKJtbxBjstBF/hero-smartphones-37xYR9ewmJSbUKTeR4nfhq.webp" alt="Smartphones">
                </div>
            </div>
        </div>
    </section>

    <!-- Categorias -->
    <section class="categorias" id="categorias">
        <div class="container">
            <div class="section-header">
                <h2>Categorias em destaque</h2>
                <p>Equipamentos de telefonia e comunicação selecionados para você.</p>
            </div>
            <div class="products-grid">
                <div class="product-card">
                    <img src="https://d2xsxph8kpxj0f.cloudfront.net/310519663657350240/jA7NMXUG4dhKJtbxBjstBF/hero-smartphones-37xYR9ewmJSbUKTeR4nfhq.webp" alt="Celulares" class="product-image">
                    <div class="product-info">
                        <h3>Celulares</h3>
                        <p>Modelos Android e iPhone</p>
                        <div class="product-footer">
                            <span class="product-price">A partir de R$ 899</span>
                            <button class="product-button">Ver</button>
                        </div>
                    </div>
                </div>

                <div class="product-card">
                    <img src="https://d2xsxph8kpxj0f.cloudfront.net/310519663657350240/jA7NMXUG4dhKJtbxBjstBF/accessories-collection-WVeDYyJE4gctHPRocUuxCx.webp" alt="Fones" class="product-image">
                    <div class="product-info">
                        <h3>Fones</h3>
                        <p>Com fio e Bluetooth</p>
                        <div class="product-footer">
                            <span class="product-price">A partir de R$ 89</span>
                            <button class="product-button">Ver</button>
                        </div>
                    </div>
                </div>

                <div class="product-card">
                    <img src="https://d2xsxph8kpxj0f.cloudfront.net/310519663657350240/jA7NMXUG4dhKJtbxBjstBF/accessories-collection-WVeDYyJE4gctHPRocUuxCx.webp" alt="Carregadores" class="product-image">
                    <div class="product-info">
                        <h3>Carregadores</h3>
                        <p>Turbo, sem fio e veiculares</p>
                        <div class="product-footer">
                            <span class="product-price">A partir de R$ 49</span>
                            <button class="product-button">Ver</button>
                        </div>
                    </div>
                </div>

                <div class="product-card">
                    <img src="https://d2xsxph8kpxj0f.cloudfront.net/310519663657350240/jA7NMXUG4dhKJtbxBjstBF/accessories-collection-WVeDYyJE4gctHPRocUuxCx.webp" alt="Smartwatches" class="product-image">
                    <div class="product-info">
                        <h3>Smartwatches</h3>
                        <p>Wearables e pulseiras</p>
                        <div class="product-footer">
                            <span class="product-price">A partir de R$ 199</span>
                            <button class="product-button">Ver</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Diferenciais -->
    <section class="diferenciais">
        <div class="container">
            <div class="diferenciais-grid">
                <div class="diferencial-item">
                    <div class="diferencial-icon">🚚</div>
                    <h3>Entrega Brasil</h3>
                    <p>Despachamos em 24h úteis pelos Correios e transportadora.</p>
                </div>

                <div class="diferencial-item">
                    <div class="diferencial-icon">🛡️</div>
                    <h3>Garantia & NF</h3>
                    <p>Nota fiscal em todas as compras. Garantia do fabricante.</p>
                </div>

                <div class="diferencial-item">
                    <div class="diferencial-icon">✓</div>
                    <h3>Pagamento flexível</h3>
                    <p>Pix, boleto, cartão em até 12x.</p>
                </div>

                <div class="diferencial-item">
                    <div class="diferencial-icon">💬</div>
                    <h3>Suporte humano</h3>
                    <p>Atendimento direto pelo WhatsApp comercial.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Quem Somos -->
    <section class="quem-somos" id="sobre">
        <div class="container">
            <div class="quem-somos-content">
                <div>
                    <img src="https://d2xsxph8kpxj0f.cloudfront.net/310519663657350240/jA7NMXUG4dhKJtbxBjstBF/store-interior-TB4jwwByodvdRGQKr8Qqqd.webp" alt="Loja Distribuidora N1">
                </div>
                <div class="quem-somos-text">
                    <h2>Quem somos</h2>
                    <h3>Distribuidora N1 LTDA</h3>
                    <p>Especialistas em equipamentos de telefonia e comunicação, atendendo consumidores e revendedores em todo o Brasil.</p>
                    <p>Atuamos no comércio varejista especializado (CNAE 47.52-1-00), oferecendo celulares, acessórios e periféricos das principais marcas do mercado. Trabalhamos com nota fiscal, garantia e atendimento próximo, do primeiro contato ao pós-venda.</p>
                    <p>Nossa loja física fica no bairro Benfica, em Fortaleza/CE, e o e-commerce entrega para todo o território nacional.</p>
                    <a href="https://wa.me/558599246433?text=Olá!%20Gostaria%20de%20conhecer%20os%20produtos%20da%20Distribuidora%20N1" target="_blank" class="cta-button">
                        Conheça nossos produtos
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Final -->
    <section class="cta-final" id="contato">
        <div class="container">
            <h2>Pronto para comprar com segurança?</h2>
            <p>Fale agora com nossa equipe e receba um atendimento personalizado. Estamos disponíveis de segunda a sábado.</p>
            <a href="https://wa.me/558599246433?text=Olá!%20Gostaria%20de%20conhecer%20os%20produtos%20da%20Distribuidora%20N1" target="_blank" class="cta-button">
                Iniciar conversa no WhatsApp
            </a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-section">
                    <h4>Distribuidora N1</h4>
                    <p>Especialistas em equipamentos de telefonia e comunicação, atendendo consumidores e revendedores em todo o Brasil.</p>
                    <a href="https://wa.me/558599246433" target="_blank">WhatsApp</a>
                </div>

                <div class="footer-section">
                    <h4>Links Úteis</h4>
                    <a href="#inicio">Início</a>
                    <a href="#sobre">Sobre Nós</a>
                    <a href="#categorias">Categorias</a>
                    <a href="#contato">Contato</a>
                </div>

                <div class="footer-section">
                    <h4>Políticas</h4>
                    <a href="politica-privacidade.html">Política de Privacidade</a>
                    <a href="termos-uso.html">Termos de Uso</a>
                    <a href="trocas-devolucoes.html">Trocas e Devoluções</a>
                </div>

                <div class="footer-section">
                    <h4>Contato</h4>
                    <p><strong>Telefone:</strong><br>(85) 99924-6433</p>
                    <p><strong>E-mail:</strong><br>suporteonlinenumberone@gmail.com</p>
                    <p><strong>Endereço:</strong><br>Rua Vinte e Quatro de Maio, 822<br>Loja 16, Benfica<br>Fortaleza - CE | CEP 60020-001</p>
                </div>
            </div>

            <div class="footer-registro">
                <h4>Informacoes de Registro</h4>
                <div class="registro-grid">
                    <div><strong>Razao Social:</strong> Distribuidora N1 LTDA</div>
                    <div><strong>CNPJ:</strong> 61.956.624/0001-71</div>
                    <div><strong>CNAE Principal:</strong> 47.52-1-00 (Comercio varejista de equipamentos de telefonia e comunicacao)</div>
                    <div><strong>Natureza Juridica:</strong> Sociedade Empresaria Limitada</div>
                </div>
            </div>

            <div class="footer-bottom">
                <p>© 2026 Distribuidora N1 LTDA - Todos os direitos reservados.</p>
                <p>CNPJ 61.956.624/0001-71</p>
            </div>
        </div>
    </footer>
</body>
</html>
