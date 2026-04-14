<!DOCTYPE html>
<html lang="sq">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PD Vlorë - Faqja Zyrtare</title>
    
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --pd-blue: #0056b3;
            --pd-dark-blue: #003d80;
            --pd-white: #ffffff;
        }
        body { font-family: 'Open Sans', sans-serif; background-color: #f4f7f9; }
        h1, h2, h3, .navbar-brand { font-family: 'Montserrat', sans-serif; font-weight: 700; }

        /* Navigation */
        .navbar { background-color: var(--pd-blue) !important; border-bottom: 3px solid #f8d11d; } /* Added yellow accent line */
        .nav-link { color: white !important; font-weight: 600; text-transform: uppercase; font-size: 0.9rem; }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 86, 179, 0.7), rgba(0, 61, 128, 0.8)), 
                        url('https://images.unsplash.com/photo-1563911302283-d2bc129e7570?q=80&w=2000');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 120px 0;
            text-align: center;
        }

        /* Feature Cards */
        .info-card {
            border: none;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.08);
            transition: 0.3s;
        }
        .info-card:hover { transform: translateY(-10px); }
        .icon-box { color: var(--pd-blue); font-size: 2.5rem; margin-bottom: 15px; }

        /* Footer */
        footer { background: #1a1a1a; color: #ccc; padding: 50px 0 20px; }
        .footer-brand { color: white; font-size: 1.5rem; margin-bottom: 20px; }
    </style>
</head>
<body>

    <nav class="navbar navbar-expand-lg navbar-dark sticky-top">
        <div class="container">
            <a class="navbar-brand" href="#">PD VLORË</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="#ballina">Ballina</a></li>
                    <li class="nav-item"><a class="nav-link" href="#kryetarja">Kryesia</a></li>
                    <li class="nav-item"><a class="nav-link" href="#lajme">Lajmet</a></li>
                    <li class="nav-item"><a class="nav-link" href="#kontakt">Kontakt</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <header class="hero" id="ballina">
        <div class="container">
            <h1 class="display-2 mb-3">PËR VLORËN, PËR SHQIPËRINË</h1>
            <p class="fs-4 mb-5">Partia Demokratike - Dega Vlorë | Opozita në Aksion</p>
            <div class="d-flex justify-content-center gap-3">
                <a href="#lajme" class="btn btn-warning btn-lg px-4 fw-bold text-dark">Lajmet e fundit</a>
                <a href="#kontakt" class="btn btn-outline-light btn-lg px-4">Anëtarësohu</a>
            </div>
        </div>
    </header>

    <section class="container my-5 py-5" id="kryetarja">
        <div class="row align-items-center">
            <div class="col-md-6 mb-4 mb-md-0">
                <h2 class="mb-4">Mesazhi i Kryetares</h2>
                <p class="lead text-muted">"Vlora meriton një qeverisje që punon për qytetarët, jo për interesat e ngushta. Bashkë do të kthejmë shpresën në çdo lagje të qytetit tonë."</p>
                <h5 class="fw-bold mt-4">Nadire Meçorapaj</h5>
                <p class="text-primary">Kryetare e PD Dega Vlorë</p>
            </div>
            <div class="col-md-6">
                <div class="p-5 bg-white shadow rounded-4 text-center">
                    <h3 class="text-primary mb-3">Vlerat tona</h3>
                    <ul class="list-unstyled fs-5">
                        <li class="mb-2">✓ Liria dhe Demokracia</li>
                        <li class="mb-2">✓ Prona Private</li>
                        <li class="mb-2">✓ Familja Tradicionale</li>
                        <li class="mb-2">✓ Integrimi Evropian</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <section class="bg-light py-5" id="lajme">
        <div class="container">
            <h2 class="text-center mb-5">Aktivitetet dhe Njoftimet</h2>
            <div class="row g-4">
                <div class="col-md-4">
                    <div class="card h-100 info-card p-4">
                        <span class="text-primary fw-bold mb-2">Prill 2026</span>
                        <h4>Mbledhja e Këshillit Kombëtar</h4>
                        <p>Diskutimet mbi strategjinë e re politike dhe mobilizimin e strukturave në Vlorë.</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="card h-100 info-card p-4 border-primary">
                        <span class="text-primary fw-bold mb-2">Live</span>
                        <h4>Protesta dhe Qëndresa</h4>
                        <p>Vazhdon aksioni opozitar në shesh për mbrojtjen e interesit publik.</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="card h-100 info-card p-4">
                        <span class="text-primary fw-bold mb-2">Sociale</span>
                        <h4>Takimet me qytetarët</h4>
                        <p>Dëgjojmë shqetësimet e biznesit të vogël në zonën e Skelës dhe Lungomares.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer id="kontakt">
        <div class="container">
            <div class="row">
                <div class="col-md-6">
                    <div class="footer-brand fw-bold">PD VLORË</div>
                    <p>Adresa: Zyrat e PD, Vlorë, Shqipëri</p>
                    <p>Email: vlora@pd.al</p>
                </div>
                <div class="col-md-6 text-md-end">
                    <h5>Na ndiqni</h5>
                    <p>Facebook | Instagram | Twitter</p>
                </div>
            </div>
            <hr class="mt-4 border-secondary">
            <p class="text-center mb-0 small">&copy; 2026 Partia Demokratike e Shqipërisë - Dega Vlorë.</p>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
