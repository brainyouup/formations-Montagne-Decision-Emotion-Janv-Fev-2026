<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formations Décision en Montagne - Guillaume Pellet-Bourgeois</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
        }
    </style>
</head>
<body class="bg-gradient-to-br from-slate-50 to-blue-50">
    <div id="app"></div>

    <script src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
    <script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>

    <script type="text/babel">
        const { useState } = React;

        const formations = {
            keynote: {
                title: "KEYNOTE",
                subtitle: "Décider sous incertitude : leçons de la montagne",
                color: "bg-blue-600",
                price: "39€",
                duration: "1h30",
                content: {
                    description: "Une conférence qui révèle les mécanismes émotionnels de vos décisions face au risque. À travers le prisme de la montagne et les résultats d'une étude scientifique unique menée auprès de 70 guides de haute montagne, vous découvrirez comment vos émotions biaisent vos choix... sans que vous vous en rendiez compte.",
                    objectifs: [
                        "Identifier les 3 pièges émotionnels",
                        "Comprendre pourquoi l'expertise peut devenir un piège (paradoxe compétence-vulnérabilité)",
                        "Découvrir les parallèles concrets entre la gestion du risque en montagne et en entreprise",
                        "Acquérir des outils pratiques pour améliorer votre prise de décision"
                    ],
                    programme: [
                        {
                            time: "18h00 - 19h00",
                            title: "Conférence « Le piège invisible »",
                            details: [
                                "Le jour blanc émotionnel : quand vos émotions déforment la réalité",
                                "Les 3 pièges émotionnels",
                                "Présentation de l'étude scientifique publiée en 2025 dans Psychology of Sport and Exercise",
                                "70 guides testés : mesures physiologiques, tâches de laboratoire, tests psychologiques",
                                "Avalanche vs décision sous risque : même mécanisme émotionnel"
                            ]
                        },
                        {
                            time: "19h00 - 19h30",
                            title: "Session Questions/Réponses",
                            details: [
                                "Échanges sur vos situations professionnelles ou personnelles",
                                "Application concrète des concepts à vos contextes de décision"
                            ]
                        },
                        {
                            time: "19h30 - 20h00",
                            title: "Networking informel",
                            details: [
                                "Échanges avec les autres participants",
                                "Discussions approfondies avec Guillaume"
                            ]
                        }
                    ],
                    publicCible: [
                        { categorie: "Pratiquants de montagne", description: "Skieurs de randonnée, hors-piste, alpinistes souhaitant améliorer leur gestion du risque" },
                        { categorie: "Professionnels de la montagne", description: "Guides, moniteurs, pisteurs, gestionnaires de domaines skiables" },
                        { categorie: "Dirigeants et décideurs", description: "Managers, entrepreneurs, chefs de projet confrontés à des décisions sous incertitude" },
                        { categorie: "Curieux de neurosciences", description: "Toute personne intéressée par la compréhension des mécanismes de décision" }
                    ],
                    takeway: [
                        "Document PDF de synthèse reprenant les concepts clés",
                        "Exercices pratiques applicables immédiatement en montagne et en entreprise",
                        "Bibliographie scientifique pour aller plus loin"
                    ],
                    infos: {
                        date: "Vendredi 30 janvier 2026",
                        horaire: "18h00 - 20h00",
                        lieu: "Chamonix (lieu communiqué aux inscrits)",
                        places: "Nombre de places limité",
                        reservation: "Pré-réservation jusqu'au 15 janvier 2026 via MP Instagram @avalanche_decision_lab"
                    }
                }
            },
            rando: {
                title: "JOURNÉE SKI DE RANDONNÉE",
                subtitle: "Décider en conditions réelles",
                color: "bg-green-600",
                price: "125-700€",
                duration: "Journée complète",
                content: {
                    description: "Une journée d'immersion totale en ski de randonnée. Au-delà de la pratique technique, nous pourrons échanger ensemble sur des situations réelles de prise de décision et vous découvrirez les pièges émotionnels les plus fréquents lors du débriefing.",
                    objectifs: [
                        "Identifier les pièges émotionnels en situation réelle",
                        "Comprendre l'anatomie de vos décisions sous risque",
                        "Découvrir une méthode complète de gestion du risque qui intègre le facteur humain",
                        "Pratiquer le ski de randonnée dans un cadre sécurisé et formateur"
                    ],
                    programme: [
                        {
                            time: "8h30 - 9h00",
                            title: "Accueil & Briefing personnalisé",
                            details: [
                                "Rappel des objectifs définis lors de la prise de contact",
                                "Présentation du terrain et analyse des conditions du jour",
                                "Briefing sécurité et check du matériel (DVA, pelle, sonde)"
                            ]
                        },
                        {
                            time: "9h00 - 12h30",
                            title: "Terrain - Ski de randonnée",
                            details: ["Situations réelles : choix d'itinéraire, lecture du terrain, gestion du groupe"]
                        },
                        {
                            time: "12h30 - 14h00",
                            title: "Pause déjeuner",
                            details: [
                                "Refuge, restaurant ou pique-nique selon la course (à votre charge)",
                                "Moment d'échange informel sur le ressenti de la matinée"
                            ]
                        },
                        {
                            time: "14h00 - 16h00",
                            title: "Débriefing",
                            details: [
                                "Retour sur les décisions clés de la matinée",
                                "Identification des 3 pièges émotionnels",
                                "Liens avec l'étude neurosciences",
                                "Exercices pratiques pour vos prochaines sorties"
                            ]
                        }
                    ],
                    formules: [
                        {
                            nom: "FORMULE PREMIUM",
                            tarif: "700€ (1 à 3 personnes)",
                            description: "Expérience ultra-personnalisée avec attention totale sur vos patterns de décision.",
                            avantages: ["Débriefing approfondi individuel", "Flexibilité totale sur le terrain choisi"]
                        },
                        {
                            nom: "FORMULE GROUPE",
                            tarif: "125€/personne (4 à 6 personnes)",
                            description: "Dynamique collective enrichissante pour observer comment vous ET les autres décidez sous risque.",
                            avantages: ["Diversité des profils et échanges riches", "Observation des dynamiques de groupe", "Excellent rapport qualité/prix"]
                        }
                    ],
                    publicCible: [
                        { categorie: "Niveau technique requis", description: "Bonne maîtrise du ski toutes neiges + expérience ski de randonnée souhaitée. En cas de doute sur votre niveau, contactez Guillaume pour évaluation." },
                        { categorie: "Profil idéal", description: "Pratiquants réguliers cherchant à gagner en autonomie et en lucidité dans leur gestion du risque. Personnes prêtes à questionner leurs certitudes et à travailler sur leur intelligence émotionnelle." }
                    ],
                    inclus: [
                        "Encadrement professionnel journée complète (Guillaume, moniteur diplômé d'État)",
                        "Débriefing (2h)",
                        "Document de synthèse personnalisé",
                        "Plan d'action adapté à votre profil envoyé quelques jours après la sortie"
                    ],
                    nonInclus: [
                        "Matériel de ski de randonnée",
                        "Matériel de sécurité DVA/pelle/sonde",
                        "Repas",
                        "Assurance personnelle couvrant ski de randonnée",
                        "Transport"
                    ],
                    infos: {
                        dates: "Tous les jours du samedi 21 au samedi 28 février 2026",
                        lieu: "Haute-Savoie (Vallée de Chamonix ou Chablais selon conditions et préférences)",
                        reservation: "MP Instagram @avalanche_decision_lab avec : date + formule + nombre de personnes",
                        paiement: "50% à la réservation, solde 7 jours avant la sortie"
                    }
                }
            },
            horspiste: {
                title: "JOURNÉE HORS-PISTE",
                subtitle: "Décider en terrain non sécurisé",
                color: "bg-orange-600",
                price: "125-700€",
                duration: "Journée complète",
                content: {
                    description: "Une journée hors-piste qui va au-delà de la descente technique. Nous pourrons échanger ensemble sur des situations réelles de prise de décision et vous découvrirez les pièges émotionnels les plus fréquents lors du débriefing.",
                    objectifs: [
                        "Développer votre lecture du terrain hors-piste",
                        "Identifier les réactions émotionnelles face au risque avalanche",
                        "Comprendre vos biais décisionnels en contexte adrénaline",
                        "Découvrir une méthode complète de gestion du risque qui intègre le facteur humain",
                        "Progresser techniquement en ski toutes neiges"
                    ],
                    programme: [
                        {
                            time: "8h30 - 9h00",
                            title: "Accueil & Briefing personnalisé",
                            details: [
                                "Rappel des objectifs définis lors de la prise de contact",
                                "Analyse bulletin avalanche (BERA) et conditions nivologiques",
                                "Check matériel de sécurité (DVA, pelle, sonde)",
                                "Définition du terrain de jeu selon niveau groupe"
                            ]
                        },
                        {
                            time: "9h00 - 12h30",
                            title: "Session hors-piste matin",
                            details: [
                                "Accès via remontées mécaniques",
                                "3-4 descentes avec niveaux progressifs d'exposition",
                                "À chaque descente : briefing terrain + analyse collective",
                                "Travail technique ski toutes neiges"
                            ]
                        },
                        {
                            time: "12h30 - 14h00",
                            title: "Pause déjeuner",
                            details: [
                                "Restaurant d'altitude ou pique-nique (à votre charge)",
                                "Échange informel sur les sensations de la matinée"
                            ]
                        },
                        {
                            time: "14h00 - 16h00",
                            title: "Débriefing",
                            details: [
                                "Retour sur les 3-4 situations clés de la matinée",
                                "Analyse : qu'avez-vous vu ? Qu'avez-vous ressenti ? Qu'avez-vous décidé ?",
                                "Identification des 3 pièges émotionnels",
                                "Lien avec l'étude sur les guides",
                                "Outils pratiques pour vos prochaines sorties hors-piste"
                            ]
                        }
                    ],
                    formules: [
                        {
                            nom: "FORMULE PREMIUM",
                            tarif: "700€ (1 à 3 personnes)",
                            description: "Attention maximale sur votre progression technique ET décisionnelle.",
                            avantages: ["Débriefing individuel approfondi", "Choix du domaine skiable optimal"]
                        },
                        {
                            nom: "FORMULE GROUPE",
                            tarif: "125€/personne (4 à 6 personnes)",
                            description: "Dynamique de groupe enrichissante. Observation croisée des comportements.",
                            avantages: ["Apprentissage par les pairs", "Cohésion et sécurité collective", "Rapport qualité/prix optimal"]
                        }
                    ],
                    publicCible: [
                        { categorie: "Niveau technique requis", description: "Très bonne maîtrise du ski sur piste (à l'aise sur pistes noires). Capacité à skier toutes neiges souhaitée mais pas obligatoire." },
                        { categorie: "Profil idéal", description: "Skieurs confirmés cherchant à sortir du domaine sécurisé avec lucidité." }
                    ],
                    inclus: [
                        "Encadrement professionnel journée complète (Guillaume, moniteur diplômé d'État)",
                        "Débriefing (2h)",
                        "Document de synthèse personnalisé",
                        "Plan d'action adapté à votre profil décisionnel envoyé quelques jours après la sortie",
                        "Conseils techniques ski personnalisés"
                    ],
                    nonInclus: [
                        "Forfait remontées mécaniques (Chamonix Le Pass minimum recommandé)",
                        "Matériel de ski",
                        "Matériel de sécurité DVA/pelle/sonde",
                        "Repas",
                        "Assurance personnelle",
                        "Transport"
                    ],
                    infos: {
                        dates: "Tous les jours du samedi 21 au samedi 28 février 2026",
                        lieu: "Domaine skiable Chamonix Mont-Blanc",
                        reservation: "MP Instagram @avalanche_decision_lab avec : date + formule + nombre de personnes",
                        paiement: "50% à la réservation, solde 7 jours avant"
                    }
                }
            },
            secu: {
                title: "FORMATION SÉCURITÉ AVALANCHE",
                subtitle: "Option SECU+ Week-end Chalet",
                color: "bg-red-600",
                price: "70-80€",
                duration: "3h (9h-12h)",
                content: {
                    description: "Formation complémentaire au week-end chalet, axée sur les compétences techniques de sauvetage et la gestion pratique du risque avalanche.",
                    objectifs: [
                        "Maîtriser l'utilisation du DVA (recherche mono et multi-victimes)",
                        "Acquérir les techniques de sondage et pelletage efficaces",
                        "Savoir passer une alerte claire et complète",
                        "Intégrer une routine de sécurité pré-sortie"
                    ],
                    programme: [
                        {
                            time: "Avant la formation",
                            title: "Préparation théorique",
                            details: [
                                "Envoi d'un document écrit de préparation",
                                "Lecture du bulletin avalanche (BERA)",
                                "Base du matériel de sécurité",
                                "Protocoles de sauvetage"
                            ]
                        },
                        {
                            time: "9h00 - 12h00",
                            title: "Pratique terrain intensive",
                            details: [
                                "Check DVA : routine de vérification systématique",
                                "Recherche DVA mono-victime : protocole complet",
                                "Recherche multi-victimes : gestion fonction marquage",
                                "Sondage systématique",
                                "Pelletage : méthode stratégique en V",
                                "Passer une alerte efficace",
                                "Mise en situation réaliste chronométrée"
                            ]
                        }
                    ],
                    formules: [
                        { nom: "Groupe 1-3 personnes", tarif: "80€/personne", description: "Formation ultra-personnalisée" },
                        { nom: "Groupe 4-6 personnes", tarif: "70€/personne", description: "Formation collective avec dynamique de groupe" }
                    ],
                    publicCible: [
                        { categorie: "Participants au week-end chalet", description: "Option du week-end premium chalet (7-8 février)" },
                        { categorie: "Niveau requis", description: "Aucun prérequis technique. Formation accessible à tous." }
                    ],
                    inclus: [
                        "Document de préparation théorique envoyé en amont",
                        "Formation pratique terrain (3h)",
                        "Prêt du matériel de sécurité si besoin",
                        "Attestation de suivi de formation",
                        "Document de synthèse PDF avec protocoles"
                    ],
                    nonInclus: [
                        "Skis de randonnée ou raquettes",
                        "Repas du samedi midi",
                        "Assurance personnelle"
                    ],
                    infos: {
                        date: "Samedi 7 février 2026, 9h00-12h00",
                        lieu: "Terrain proche du Chalet JUM (Chablais)",
                        reservation: "Option à ajouter via MP Instagram @avalanche_decision_lab",
                        important: "Cette formation n'est PAS diplômante."
                    }
                }
            }
        };

        function App() {
            const [activeTab, setActiveTab] = useState('keynote');
            const formation = formations[activeTab];

            return (
                <div className="min-h-screen p-6">
                    <div className="max-w-6xl mx-auto">
                        <div className="text-center mb-8">
                            <h1 className="text-4xl font-bold text-gray-800 mb-2">
                                Formations - Décision en Montagne
                            </h1>
                            <p className="text-gray-600">Janvier-Février 2026 - Vallée de Chamonix et Chablais</p>
                        </div>

                        {/* Profil */}
                        <div className="bg-gradient-to-br from-slate-800 to-slate-900 rounded-xl p-8 text-white mb-8">
                            <div className="flex items-start gap-6">
                                <div className="w-24 h-24 bg-blue-500 rounded-full flex items-center justify-center flex-shrink-0 text-4xl font-bold">
                                    GP
                                </div>
                                <div>
                                    <h2 className="text-2xl font-bold mb-4">Guillaume PELLET-BOURGEOIS</h2>
                                    <p className="text-slate-300 mb-4">
                                        Chercheur en prise de décision sous risque et psychophysiologie des émotions. 
                                        20 ans d'expérience dans l'accompagnement mental de haut niveau.
                                    </p>
                                    <div className="grid md:grid-cols-2 gap-4 text-sm text-gray-700">
                                    {Object.entries(formation.content.infos).map(([key, value]) => (
                                        <div key={key}>
                                            <span className="font-semibold capitalize">{key}: </span>
                                            <span>{value}</span>
                                        </div>
                                    ))}
                                </div>
                            </div>

                            {activeTab !== 'keynote' && (
                                <div className="bg-gray-50 rounded-xl p-6 text-sm text-gray-600">
                                    <p>
                                        <strong>Note sur les tarifs :</strong> Les tarifs incluent l'encadrement ski professionnel 
                                        (aligné sur les{' '}
                                        <a 
                                            href="https://www.esf-chamonix.com/tarifs-cours" 
                                            target="_blank" 
                                            rel="noopener noreferrer"
                                            className="text-blue-600 underline hover:text-blue-800"
                                        >
                                            tarifs ESF Chamonix
                                        </a>
                                        ) ainsi que l'expertise scientifique spécialisée en prise de décision.
                                    </p>
                                </div>
                            )}
                        </div>

                        {/* Footer */}
                        <div className="mt-12 bg-gradient-to-r from-blue-600 to-blue-800 rounded-xl p-8 text-white text-center">
                            <h3 className="text-2xl font-bold mb-4">Comprendre vos émotions. Maîtriser vos décisions.</h3>
                            <p className="mb-6 opacity-90">Réservation par message Instagram</p>
                            <div className="flex flex-col sm:flex-row gap-4 justify-center items-center mb-6">
                                <a 
                                    href="https://www.instagram.com/avalanche_decision_lab" 
                                    target="_blank"
                                    rel="noopener noreferrer"
                                    className="bg-white text-blue-600 px-8 py-3 rounded-lg font-semibold hover:bg-blue-50 transition-colors"
                                >
                                    Contacter sur Instagram
                                </a>
                            </div>
                            <div className="text-sm opacity-75 border-t border-white/20 pt-4 mt-4">
                                <p className="mb-2">Pour plus d'informations sur l'offre corporate :</p>
                                <div className="flex flex-col sm:flex-row gap-4 justify-center items-center">
                                    <a href="mailto:guillaume@brainyouup.com" className="hover:underline">
                                        guillaume@brainyouup.com
                                    </a>
                                    <span className="hidden sm:inline">|</span>
                                    <a href="tel:+33618415645" className="hover:underline">
                                        +33 6 18 41 56 45
                                    </a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            );
        }

        ReactDOM.render(<App />, document.getElementById('app'));
    </script>
</body>
</html> gap-4 mt-6">
                                        <div>
                                            <h3 className="font-semibold text-blue-300 mb-2">Expertise montagne</h3>
                                            <ul className="text-sm text-slate-300 space-y-1">
                                                <li>• Moniteur de ski diplômé d'État</li>
                                                <li>• Formateur Lycée de Chamonix</li>
                                                <li>• 400+ professionnels formés</li>
                                            </ul>
                                        </div>
                                        <div>
                                            <h3 className="font-semibold text-blue-300 mb-2">Expertise scientifique</h3>
                                            <ul className="text-sm text-slate-300 space-y-1">
                                                <li>• Master 2 Neuropsychologie</li>
                                                <li>• Publication Psychology of Sport and Exercise 2025</li>
                                                <li>• Chroniqueur Harvard Business Review</li>
                                            </ul>
                                        </div>
                                    </div>
                                    <div className="mt-6 p-4 bg-slate-700/50 rounded-lg">
                                        <p className="text-sm italic text-slate-300">
                                            "En 2010, après avoir perdu mon collègue et mentor dans une avalanche, une question m'obsède : 
                                            pourquoi les pros se font piéger sans s'en rendre compte ? Cette quête m'a mené de la montagne 
                                            au laboratoire pour comprendre le piège invisible des émotions dans nos décisions."
                                        </p>
                                    </div>
                                    <div className="mt-4 flex gap-4 text-sm flex-wrap">
                                        <span className="text-blue-300">+33 6 18 41 56 45</span>
                                        <span className="text-blue-300">guillaume@brainyouup.com</span>
                                    </div>
                                </div>
                            </div>
                        </div>

                        {/* Navigation */}
                        <div className="bg-white rounded-xl shadow-sm p-2 mb-8">
                            <div className="grid grid-cols-2 md:grid-cols-4 gap-2">
                                {Object.keys(formations).map(key => (
                                    <button
                                        key={key}
                                        onClick={() => setActiveTab(key)}
                                        className={`p-4 rounded-lg transition-all ${
                                            activeTab === key
                                                ? 'bg-blue-600 text-white shadow-lg'
                                                : 'bg-gray-50 text-gray-700 hover:bg-gray-100'
                                        }`}
                                    >
                                        <span className="text-sm font-medium">
                                            {key === 'keynote' ? 'Keynote' :
                                             key === 'rando' ? 'Ski de Rando' :
                                             key === 'horspiste' ? 'Hors-Piste' :
                                             'Sécurité Avalanche'}
                                        </span>
                                    </button>
                                ))}
                            </div>
                        </div>

                        {/* Contenu formation */}
                        <div className="space-y-8">
                            <div className={`${formation.color} rounded-xl p-8 text-white`}>
                                <h2 className="text-3xl font-bold mb-2">{formation.title}</h2>
                                <p className="text-lg opacity-90 mb-4">{formation.subtitle}</p>
                                <div className="flex gap-6 text-lg">
                                    <span className="font-semibold">{formation.price}</span>
                                    <span>{formation.duration}</span>
                                </div>
                            </div>

                            <div className="bg-white rounded-xl p-6 shadow-sm">
                                <p className="text-gray-700">{formation.content.description}</p>
                            </div>

                            <div className="bg-white rounded-xl p-6 shadow-sm">
                                <h3 className="text-xl font-bold text-gray-800 mb-4">Objectifs pédagogiques</h3>
                                <ul className="space-y-2">
                                    {formation.content.objectifs.map((obj, i) => (
                                        <li key={i} className="flex gap-3 text-gray-700">
                                            <span className="text-green-600 font-bold">✓</span>
                                            <span>{obj}</span>
                                        </li>
                                    ))}
                                </ul>
                            </div>

                            <div className="bg-white rounded-xl p-6 shadow-sm">
                                <h3 className="text-xl font-bold text-gray-800 mb-4">Programme détaillé</h3>
                                <div className="space-y-4">
                                    {formation.content.programme.map((section, i) => (
                                        <div key={i} className="border-l-4 border-blue-500 pl-4 py-2">
                                            <div className="flex items-center gap-3 mb-2">
                                                <span className="font-semibold text-blue-600">{section.time}</span>
                                                <span className="font-bold text-gray-800">{section.title}</span>
                                            </div>
                                            <ul className="space-y-1 ml-4">
                                                {section.details.map((detail, j) => (
                                                    <li key={j} className="text-sm text-gray-600">• {detail}</li>
                                                ))}
                                            </ul>
                                        </div>
                                    ))}
                                </div>
                            </div>

                            {formation.content.formules && (
                                <div className="bg-white rounded-xl p-6 shadow-sm">
                                    <h3 className="text-xl font-bold text-gray-800 mb-4">Formules</h3>
                                    <div className="grid md:grid-cols-2 gap-4">
                                        {formation.content.formules.map((formule, i) => (
                                            <div key={i} className="border-2 border-gray-200 rounded-lg p-4">
                                                <h4 className="font-bold text-lg mb-2">{formule.nom}</h4>
                                                <p className="text-2xl font-bold text-blue-600 mb-3">{formule.tarif}</p>
                                                <p className="text-gray-600 text-sm mb-3">{formule.description}</p>
                                                {formule.avantages && (
                                                    <ul className="text-xs text-gray-500">
                                                        {formule.avantages.map((av, j) => (
                                                            <li key={j}>✓ {av}</li>
                                                        ))}
                                                    </ul>
                                                )}
                                            </div>
                                        ))}
                                    </div>
                                </div>
                            )}

                            <div className="bg-white rounded-xl p-6 shadow-sm">
                                <h3 className="text-xl font-bold text-gray-800 mb-4">Public concerné</h3>
                                <div className="space-y-4">
                                    {formation.content.publicCible.map((pub, i) => (
                                        <div key={i}>
                                            <h4 className="font-semibold text-gray-800 mb-1">{pub.categorie}</h4>
                                            <p className="text-gray-600 text-sm">{pub.description}</p>
                                        </div>
                                    ))}
                                </div>
                            </div>

                            {formation.content.inclus && (
                                <div className="grid md:grid-cols-2 gap-6">
                                    <div className="bg-green-50 rounded-xl p-6">
                                        <h3 className="text-lg font-bold text-green-800 mb-4">Inclus</h3>
                                        <ul className="space-y-2 text-sm text-gray-700">
                                            {formation.content.inclus.map((item, i) => (
                                                <li key={i}>• {item}</li>
                                            ))}
                                        </ul>
                                    </div>
                                    <div className="bg-red-50 rounded-xl p-6">
                                        <h3 className="text-lg font-bold text-red-800 mb-4">Non inclus</h3>
                                        <ul className="space-y-2 text-sm text-gray-700">
                                            {formation.content.nonInclus.map((item, i) => (
                                                <li key={i}>• {item}</li>
                                            ))}
                                        </ul>
                                    </div>
                                </div>
                            )}

                            {formation.content.takeway && (
                                <div className="bg-white rounded-xl p-6 shadow-sm">
                                    <h3 className="text-xl font-bold text-gray-800 mb-4">Vous repartez avec</h3>
                                    <ul className="space-y-2">
                                        {formation.content.takeway.map((item, i) => (
                                            <li key={i} className="flex gap-3 text-gray-700">
                                                <span className="text-blue-600">•</span>
                                                <span>{item}</span>
                                            </li>
                                        ))}
                                    </ul>
                                </div>
                            )}

                            <div className="bg-blue-50 rounded-xl p-6">
                                <h3 className="text-xl font-bold text-blue-900 mb-4">Informations pratiques</h3>
                                <div className="grid md:grid-cols-2
