# Portfólio Pessoal - Diogo Rocha Pereira

## Nome do Aluno
Diogo Rocha Pereira

## Desenvolvimento de Sistemas I - Agenda 15

## Descrição do Portfólio
Este portfólio foi desenvolvido como evolução do projeto de sala de aula utilizando o framework Bootstrap. Ele apresenta de forma responsiva e moderna a minha trajetória acadêmica e profissional, minhas habilidades técnicas, links de contato e destaca meus principais projetos práticos desenvolvidos em lógica de programação.

## Tecnologias Utilizadas
- HTML5 e CSS3
- Bootstrap 5
- Python 3 (para os projetos apresentados)
- Git e GitHub Pages

## Link do Site Publicado
[Acesse o portfólio online aqui](https://diogocreator.github.io/diogorocha_ds_i_portfolio/)


## Explicação do Funcionamento do Projeto
O site foi construído sob o conceito de página única (*Single Page*) e conta com uma barra de navegação fixa no topo (`navbar`) que permite ao usuário alternar de forma fluida e suave entre as seções: **Perfil**, **Habilidades**, **Projetos** e **Contato**.

Os projetos desenvolvidos em Python estão organizados em formato de cartões interativos, contendo descrições específicas e botões de redirecionamento direto para os respectivos repositórios no GitHub.

## Descrição do Recurso Novo Adicionado
Como evolução do modelo padrão apresentado em aula, adicionei dois recursos visuais e interativos de destaque:
1. **Seção de Habilidades:** Uma nova área dedicada a apresentar visualmente o nível de domínio das principais tecnologias e linguagens que estudo (como Python, HTML/CSS e Bootstrap).
2. **Animações de Hover em Cards:** Efeito visual moderno implementado com transições em CSS, fazendo com que os cards dos projetos elevem-se sutilmente e ganhem sombras dinâmicas quando o cursor do mouse passa por cima.

## Explicação de Como Esse Recurso Foi Implementado
- **Para a Seção de Habilidades:** Utilizei os componentes nativos de barras de progresso do Bootstrap (`progress` e `progress-bar`), combinados com classes utilitárias de formatação e cores contextuais para mensurar graficamente a evolução técnica.
- **Para as Animações de Hover:** Criei uma classe CSS personalizada chamada `.card-hover`, aplicando as propriedades `transition` combinadas com `transform: translateY(-8px)` e `box-shadow`. Isso garante uma experiência de usuário (*UX*) muito mais fluida, interativa e profissional.

---

## Código Fonte do Projeto (`index.html`)

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfólio Pessoal - Diogo Rocha Pereira</title>
    <!-- Bootstrap 5 CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .card-hover {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .card-hover:hover {
            transform: translateY(-8px);
            box-shadow: 0 .5rem 1rem rgba(0,0,0,.15)!important;
        }
        .foto-perfil {
            width: 160px;
            height: 160px;
            object-fit: cover;
            border-radius: 50%;
            border: 4px solid #fff;
            box-shadow: 0 .5rem 1rem rgba(0,0,0,.15)!important;
        }
        .logo-nav {
            height: 38px;
            width: 38px;
            object-fit: cover;
            border-radius: 50%;
        }
        body {
            padding-top: 56px;
        }
    </style>
</head>
<body data-bs-spy="scroll" data-bs-target="#navbar-portfolio" data-bs-smooth-scroll="true">

    <!-- Barra de Navegação -->
    <nav id="navbar-portfolio" class="navbar navbar-expand-lg navbar-dark bg-dark fixed-top shadow-sm">
        <div class="container">
            <!-- Logo da Marca na Navbar -->
            <a class="navbar-brand fw-bold d-flex align-items-center gap-2" href="#perfil">
                <img src="img/diogocreator.jpg" alt="Logo DiogoCreator" class="logo-nav">
                <span>Diogo Rocha</span>
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="#perfil">Perfil</a></li>
                    <li class="nav-item"><a class="nav-link" href="#habilidades">Habilidades</a></li>
                    <li class="nav-item"><a class="nav-link" href="#projetos">Projetos</a></li>
                    <li class="nav-item"><a class="nav-link" href="#contato">Contato</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Seção Início / Perfil -->
    <header id="perfil" class="py-5 bg-light border-bottom">
        <div class="container py-5">
            <div class="row align-items-center justify-content-center text-center">
                <div class="col-lg-8">
                    <!-- Foto de Perfil -->
                    <img src="img/diogo7.jpeg" alt="Diogo Rocha Pereira" class="foto-perfil mb-4">
                    
                    <h1 class="display-5 fw-bold text-primary mb-3">Olá, eu sou Diogo Rocha Pereira</h1>
                    <p class="lead text-secondary mb-4">
                        Estudante de Bacharelado em TI e Técnico em Desenvolvimento de Sistemas, atualmente atuando como estagiário na área de TI. 
                        Meu objetivo é me tornar um desenvolvedor completo e dinâmico, dominando múltiplas ferramentas para criar soluções eficientes tanto para o setor privado quanto para o público, além de desenvolver meus próprios programas.
                    </p>
                    <a href="#projetos" class="btn btn-primary btn-lg shadow-sm">Ver Meus Projetos</a>
                </div>
            </div>
        </div>
    </header>

    <!-- Seção Habilidades -->
    <section id="habilidades" class="py-5">
        <div class="container py-4">
            <h2 class="text-center fw-bold mb-5">Minhas Habilidades & Aprendizado</h2>
            <div class="row justify-content-center">
                <div class="col-md-8">
                    <div class="mb-3">
                        <span class="fw-bold">Python (Lógica e Estruturas)</span>
                        <div class="progress mt-1" style="height: 12px;">
                            <div class="progress-bar bg-primary" role="progressbar" style="width: 85%;">85%</div>
                        </div>
                    </div>
                    <div class="mb-3">
                        <span class="fw-bold">HTML5 / CSS3 / Bootstrap</span>
                        <div class="progress mt-1" style="height: 12px;">
                            <div class="progress-bar bg-success" role="progressbar" style="width: 80%;">80%</div>
                        </div>
                    </div>
                    <div class="mb-3">
                        <span class="fw-bold">Git e GitHub</span>
                        <div class="progress mt-1" style="height: 12px;">
                            <div class="progress-bar bg-warning text-dark" role="progressbar" style="width: 75%;">75%</div>
                        </div>
                    </div>
                    <div class="mt-4 p-3 bg-light rounded border">
                        <p class="mb-0 text-muted text-center"><i class="fa-solid fa-graduation-cap me-2"></i>Em constante evolução: atualmente me dedicando também a estudos complementares em Banco de Dados.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Seção Projetos -->
    <section id="projetos" class="py-5 bg-light">
        <div class="container py-4">
            <h2 class="text-center fw-bold mb-5">Meus Projetos</h2>
            <div class="row g-4 justify-content-center">
                <!-- Projeto 1 -->
                <div class="col-md-6 col-lg-3">
                    <div class="card h-100 card-hover border-0 shadow-sm p-3">
                        <div class="card-body d-flex flex-column">
                            <h5 class="card-title fw-bold text-primary mb-3">📊 Pesquisa de Satisfação</h5>
                            <p class="card-text text-muted">Sistema em Python para coleta de dados de clientes, processamento de opiniões e geração de resumo estatístico completo.</p>
                            <span class="badge bg-secondary mb-3 align-self-start">Python 3</span>
                            <a href="https://github.com/diogocreator" target="_blank" class="btn btn-outline-primary mt-auto">Ver no GitHub</a>
                        </div>
                    </div>
                </div>
                <!-- Projeto 2 -->
                <div class="col-md-6 col-lg-3">
                    <div class="card h-100 card-hover border-0 shadow-sm p-3">
                        <div class="card-body d-flex flex-column">
                            <h5 class="card-title fw-bold text-primary mb-3">💧 Níveis de Água</h5>
                            <p class="card-text text-muted">Simulador de monitoramento de reservatório que utiliza códigos ANSI para exibir alertas coloridos no terminal.</p>
                            <span class="badge bg-secondary mb-3 align-self-start">Python / ANSI</span>
                            <a href="https://github.com/diogocreator/Controle-de-N-veis-de-gua" target="_blank" class="btn btn-outline-primary mt-auto">Ver no GitHub</a>
                        </div>
                    </div>
                </div>
                <!-- Projeto 3 -->
                <div class="col-md-6 col-lg-3">
                    <div class="card h-100 card-hover border-0 shadow-sm p-3">
                        <div class="card-body d-flex flex-column">
                            <h5 class="card-title fw-bold text-primary mb-3">🛒 Desconto Progressivo</h5>
                            <p class="card-text text-muted">Programa para cálculo de descontos em mercado online com tratamento de erros robusto via try/except.</p>
                            <span class="badge bg-secondary mb-3 align-self-start">Python 3</span>
                            <a href="https://github.com/diogocreator/DiogoRocha_Ag6_DS_-I" target="_blank" class="btn btn-outline-primary mt-auto">Ver no GitHub</a>
                        </div>
                    </div>
                </div>
                <!-- Projeto 4 -->
                <div class="col-md-6 col-lg-3">
                    <div class="card h-100 card-hover border-0 shadow-sm p-3">
                        <div class="card-body d-flex flex-column">
                            <h5 class="card-title fw-bold text-primary mb-3">⚡ Consumo Elétrico</h5>
                            <p class="card-text text-muted">Calculadora de consumo mensal de energia em kWh e estimativa de custo financeiro com base em tarifa média.</p>
                            <span class="badge bg-secondary mb-3 align-self-start">Python 3</span>
                            <a href="https://github.com/diogocreator" target="_blank" class="btn btn-outline-primary mt-auto">Ver no GitHub</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Seção Contato -->
    <section id="contato" class="py-5 text-white bg-dark">
        <div class="container py-4 text-center">
            <h2 class="fw-bold mb-3">Entre em Contato</h2>
            <p class="lead text-light mb-4">Tem interesse em conversar sobre tecnologia, oportunidades de estágio ou trocar ideias? Entre em contato comigo!</p>
            <div class="fs-5 mb-3">
                <p class="mb-2"><i class="fa-solid fa-phone me-2 text-primary"></i> Telefone: (12) 991232548</p>
                <p class="mb-2"><i class="fa-solid fa-envelope me-2 text-primary"></i> E-mail: <a href="mailto:diogorochailha8@gmail.com" class="text-white text-decoration-none">diogorochailha8@gmail.com</a></p>
                <p class="mb-2"><i class="fa-brands fa-github me-2 text-primary"></i> GitHub: <a href="https://github.com/diogocreator" target="_blank" class="text-white text-decoration-none">github.com/diogocreator</a></p>
                <p class="mb-0"><i class="fa-brands fa-linkedin me-2 text-primary"></i> LinkedIn: <a href="http://www.linkedin.com/in/diogo-rocha-pereira" target="_blank" class="text-white text-decoration-none">diogo-rocha-pereira</a></p>
            </div>
        </div>
    </section>

    <!-- Rodapé -->
    <footer class="py-3 bg-black text-white text-center">
        <div class="container">
            <small>© 2026 Diogo Rocha Pereira. Todos os direitos reservados.</small>
        </div>
    </footer>

    <!-- Bootstrap 5 JS Bundle -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
