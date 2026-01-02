<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formations Décision en Montagne - Guillaume Pellet-Bourgeois</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gradient-to-br from-slate-50 to-blue-50 p-6">
    <div class="max-w-6xl mx-auto">
        <!-- Header -->
        <div class="text-center mb-8">
            <h1 class="text-4xl font-bold text-gray-800 mb-2">Formations - Décision en Montagne</h1>
            <p class="text-gray-600">Janvier-Février 2026 - Vallée de Chamonix et Chablais</p>
        </div>

        <!-- Profil -->
        <div class="bg-gradient-to-br from-slate-800 to-slate-900 rounded-xl p-8 text-white mb-8">
            <div class="flex items-start gap-6">
                <div class="w-24 h-24 bg-blue-500 rounded-full flex items-center justify-center flex-shrink-0 text-4xl font-bold">GP</div>
                <div>
                    <h2 class="text-2xl font-bold mb-4">Guillaume PELLET-BOURGEOIS</h2>
                    <p class="text-slate-300 mb-4">Chercheur en prise de décision sous risque et psychophysiologie des émotions. 20 ans d'expérience dans l'accompagnement mental de haut niveau.</p>
                    <div class="grid md:grid-cols-2 gap-4 mt-6">
                        <div>
                            <h3 class="font-semibold text-blue-300 mb-2">Expertise montagne</h3>
                            <ul class="text-sm text-slate-300 space-y-1">
                                <li>• Moniteur de ski diplômé d'État</li>
                                <li>• Formateur Lycée de Chamonix</li>
                                <li>• 400+ professionnels formés</li>
                            </ul>
                        </div>
                        <div>
                            <h3 class="font-semibold text-blue-300 mb-2">Expertise scientifique</h3>
                            <ul class="text-sm text-slate-300 space-y-1">
                                <li>• Master 2 Neuropsychologie</li>
                                <li>• Publication Psychology of Sport and Exercise 2025</li>
                                <li>• Chroniqueur Harvard Business Review</li>
                            </ul>
                        </div>
                    </div>
                    <div class="mt-6 p-4 bg-slate-700/50 rounded-lg">
                        <p class="text-sm italic text-slate-300">"En 2010, après avoir perdu mon collègue et mentor dans une avalanche, une question m'obsède : pourquoi les pros se font piéger sans s'en rendre compte ? Cette quête m'a mené de la montagne au laboratoire pour comprendre le piège invisible des émotions dans nos décisions."</p>
                    </div>
                    <div class="mt-4 flex gap-4 text-sm flex-wrap">
                        <span class="text-blue-300">+33 6 18 41 56 45</span>
                        <span class="text-blue-300">guillaume@brainyouup.com</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Navigation -->
        <div class="bg-white rounded-xl shadow-sm p-2 mb-8">
            <div class="grid grid-cols-2 md:grid-cols-4 gap-2">
                <button onclick="showFormation('keynote')" id="btn-keynote" class="p-4 rounded-lg transition-all bg-blue-600 text-white shadow-lg text-sm font-medium">Keynote</button>
                <button onclick="showFormation('rando')" id="btn-rando" class="p-4 rounded-lg transition-all bg-gray-50 text-gray-700 hover:bg-gray-100 text-sm font-medium">Ski de Rando</button>
                <button onclick="showFormation('horspiste')" id="btn-horspiste" class="p-4 rounded-lg transition-all bg-gray-50 text-gray-700 hover:bg-gray-100 text-sm font-medium">Hors-Piste</button>
                <button onclick="showFormation('secu')" id="btn-secu" class="p-4 rounded-lg transition-all bg-gray-50 text-gray-700 hover:bg-gray-100 text-sm font-medium">Sécurité Avalanche</button>
            </div>
        </div>

        <!-- Contenu formations -->
        <div id="formation-content"></div>

        <!-- Footer -->
        <div class="mt-12 bg-gradient-to-r from-blue-600 to-blue-800 rounded-xl p-8 text-white text-center">
            <h3 class="text-2xl font-bold mb-4">Comprendre vos émotions. Maîtriser vos décisions.</h3>
            <p class="mb-6 opacity-90">Réservation par message Instagram</p>
            <div class="flex flex-col sm:flex-row gap-4 justify-center items-center mb-6">
                <a href="https://www.instagram.com/avalanche_decision_lab" target="_blank" class="bg-white text-blue-600 px-8 py-3 rounded-lg font-semibold hover:bg-blue-50 transition-colors">Contacter sur Instagram</a>
            </div>
            <div class="text-sm opacity-75 border-t border-white/20 pt-4 mt-4">
                <p class="mb-2">Pour plus d'informations sur l'offre corporate :</p>
                <div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
                    <a href="mailto:guillaume@brainyouup.com" class="hover:underline">guillaume@brainyouup.com</a>
                    <span class="hidden sm:inline">|</span>
                    <a href="tel:+33618415645" class="hover:underline">+33 6 18 41 56 45</a>
                </div>
            </div>
        </div>
    </div>

    <script>
        const formations = {
            keynote: {
                title: "KEYNOTE",
                subtitle: "Décider sous incertitude : leçons de la montagne",
                color: "bg-blue-600",
                price: "39€",
                duration: "1h30",
                description: "Une conférence qui révèle les mécanismes émotionnels de vos décisions face au risque. À travers le prisme de la montagne et les résultats d'une étude scientifique unique menée auprès de 70 guides de haute montagne, vous découvrirez comment vos émotions biaisent vos choix... sans que vous vous en rendiez compte.",
                objectifs: ["Identifier les 3 pièges émotionnels", "Comprendre pourquoi l'expertise peut devenir un piège (paradoxe compétence-vulnérabilité)", "Découvrir les parallèles concrets entre la gestion du risque en montagne et en entreprise", "Acquérir des outils pratiques pour améliorer votre prise de décision"],
                programme: [{time:"18h00-19h00",title:"Conférence",details:["Le jour blanc émotionnel","Les 3 pièges émotionnels","Étude scientifique Psychology of Sport and Exercise 2025","70 guides testés","Avalanche vs décision sous risque"]},{time:"19h00-19h30",title:"Questions/Réponses",details:["Échanges sur vos situations","Application concrète"]},{time:"19h30-20h00",title:"Networking",details:["Échanges avec participants","Discussions avec Guillaume"]}],
                publicCible: [{cat:"Pratiquants de montagne",desc:"Skieurs de randonnée, hors-piste, alpinistes"},{cat:"Professionnels de la montagne",desc:"Guides, moniteurs, pisteurs"},{cat:"Dirigeants et décideurs",desc:"Managers, entrepreneurs, chefs de projet"},{cat:"Curieux de neurosciences",desc:"Compréhension des mécanismes de décision"}],
                takeway: ["Document PDF de synthèse","Exercices pratiques","Bibliographie scientifique"],
                infos: {Date:"Vendredi 30 janvier 2026",Horaire:"18h00-20h00",Lieu:"Chamonix (lieu communiqué aux inscrits)",Places:"Nombre de places limité",Réservation:"Pré-réservation jusqu'au 15 janvier 2026 via MP Instagram @avalanche_decision_lab"}
            },
            rando: {
                title: "JOURNÉE SKI DE RANDONNÉE",
                subtitle: "Décider en conditions réelles",
                color: "bg-green-600",
                price: "125-700€",
                duration: "Journée complète",
                description: "Une journée d'immersion totale en ski de randonnée. Au-delà de la pratique technique, nous pourrons échanger ensemble sur des situations réelles de prise de décision et vous découvrirez les pièges émotionnels les plus fréquents lors du débriefing.",
                objectifs: ["Identifier les pièges émotionnels en situation réelle","Comprendre l'anatomie de vos décisions sous risque","Découvrir une méthode complète de gestion du risque qui intègre le facteur humain","Pratiquer le ski de randonnée dans un cadre sécurisé"],
                programme: [{time:"8h30-9h00",title:"Accueil & Briefing",details:["Rappel des objectifs","Présentation du terrain","Briefing sécurité et check matériel"]},{time:"9h00-12h30",title:"Terrain - Ski de randonnée",details:["Situations réelles : choix d'itinéraire, lecture du terrain, gestion du groupe"]},{time:"12h30-14h00",title:"Pause déjeuner",details:["Refuge/restaurant/pique-nique (à votre charge)","Échange informel"]},{time:"14h00-16h00",title:"Débriefing",details:["Retour sur les décisions clés","Identification des 3 pièges émotionnels","Liens avec l'étude neurosciences","Exercices pratiques"]}],
                formules: [{nom:"FORMULE PREMIUM",tarif:"700€ (1-3 pers)",desc:"Expérience ultra-personnalisée",av:["Débriefing approfondi","Flexibilité terrain"]},{nom:"FORMULE GROUPE",tarif:"125€/pers (4-6 pers)",desc:"Dynamique collective enrichissante",av:["Diversité des profils","Observation dynamiques de groupe","Excellent rapport qualité/prix"]}],
                publicCible: [{cat:"Niveau technique requis",desc:"Bonne maîtrise ski toutes neiges + expérience ski de randonnée souhaitée"},{cat:"Profil idéal",desc:"Pratiquants réguliers cherchant autonomie et lucidité"}],
                inclus: ["Encadrement journée complète (Guillaume, moniteur diplômé d'État)","Débriefing (2h)","Document de synthèse personnalisé","Plan d'action envoyé quelques jours après"],
                nonInclus: ["Matériel ski de randonnée","Matériel sécurité DVA/pelle/sonde","Repas","Assurance personnelle","Transport"],
                infos: {Dates:"Tous les jours du samedi 21 au samedi 28 février 2026",Lieu:"Vallée de Chamonix ou Chablais",Réservation:"MP Instagram @avalanche_decision_lab avec date+formule+nb personnes",Paiement:"50% à la réservation, solde 7 jours avant"},
                showTarif: true
            },
            horspiste: {
                title: "JOURNÉE HORS-PISTE",
                subtitle: "Décider en terrain non sécurisé",
                color: "bg-orange-600",
                price: "125-700€",
                duration: "Journée complète",
                description: "Une journée hors-piste qui va au-delà de la descente technique. Nous pourrons échanger ensemble sur des situations réelles de prise de décision et vous découvrirez les pièges émotionnels les plus fréquents lors du débriefing.",
                objectifs: ["Développer votre lecture du terrain hors-piste","Identifier les réactions émotionnelles face au risque avalanche","Comprendre vos biais décisionnels en contexte adrénaline","Découvrir une méthode complète de gestion du risque qui intègre le facteur humain","Progresser techniquement en ski toutes neiges"],
                programme: [{time:"8h30-9h00",title:"Accueil & Briefing",details:["Rappel des objectifs","Analyse BERA","Check matériel sécurité","Définition terrain selon niveau"]},{time:"9h00-12h30",title:"Session hors-piste",details:["Accès via remontées","3-4 descentes progressives","Briefing terrain + analyse collective","Travail technique ski"]},{time:"12h30-14h00",title:"Pause déjeuner",details:["Restaurant d'altitude ou pique-nique (à votre charge)","Échange informel"]},{time:"14h00-16h00",title:"Débriefing",details:["Retour sur les situations clés","Analyse : vu/ressenti/décidé","Identification des 3 pièges émotionnels","Lien avec l'étude guides","Outils pratiques"]}],
                formules: [{nom:"FORMULE PREMIUM",tarif:"700€ (1-3 pers)",desc:"Attention maximale sur progression technique ET décisionnelle",av:["Débriefing individuel approfondi","Choix domaine optimal"]},{nom:"FORMULE GROUPE",tarif:"125€/pers (4-6 pers)",desc:"Dynamique de groupe enrichissante",av:["Apprentissage par les pairs","Cohésion et sécurité collective","Rapport qualité/prix optimal"]}],
                publicCible: [{cat:"Niveau technique requis",desc:"Très bonne maîtrise ski piste (pistes noires). Capacité ski toutes neiges souhaitée mais pas obligatoire"},{cat:"Profil idéal",desc:"Skieurs confirmés cherchant à sortir du domaine sécurisé avec lucidité"}],
                inclus: ["Encadrement journée complète (Guillaume, moniteur diplômé d'État)","Débriefing (2h)","Document de synthèse personnalisé","Plan d'action envoyé quelques jours après","Conseils techniques ski personnalisés"],
                nonInclus: ["Forfait remontées mécaniques (Chamonix Le Pass minimum)","Matériel de ski","Matériel sécurité DVA/pelle/sonde","Repas","Assurance personnelle","Transport"],
                infos: {Dates:"Tous les jours du samedi 21 au samedi 28 février 2026",Lieu:"Domaine skiable Chamonix Mont-Blanc",Réservation:"MP Instagram @avalanche_decision_lab avec date+formule+nb personnes",Paiement:"50% à la réservation, solde 7 jours avant"},
                showTarif: true
            },
            secu: {
                title: "FORMATION SÉCURITÉ AVALANCHE",
                subtitle: "Option SECU+ Week-end Chalet",
                color: "bg-red-600",
                price: "70-80€",
                duration: "3h (9h-12h)",
                description: "Formation complémentaire au week-end chalet, axée sur les compétences techniques de sauvetage et la gestion pratique du risque avalanche.",
                objectifs: ["Maîtriser l'utilisation du DVA (recherche mono et multi-victimes)","Acquérir les techniques de sondage et pelletage efficaces","Savoir passer une alerte claire et complète","Intégrer une routine de sécurité pré-sortie"],
                programme: [{time:"Avant formation",title:"Préparation théorique",details:["Envoi document écrit","Lecture BERA","Base matériel sécurité","Protocoles de sauvetage"]},{time:"9h00-12h00",title:"Pratique terrain intensive",details:["Check DVA","Recherche DVA mono-victime","Recherche multi-victimes","Sondage systématique","Pelletage méthode V","Passer une alerte efficace","Mise en situation chronométrée"]}],
                formules: [{nom:"Groupe 1-3 personnes",tarif:"80€/pers",desc:"Formation ultra-personnalisée"},{nom:"Groupe 4-6 personnes",tarif:"70€/pers",desc:"Formation collective avec dynamique de groupe"}],
                publicCible: [{cat:"Participants au week-end chalet",desc:"Option du week-end premium chalet (7-8 février)"},{cat:"Niveau requis",desc:"Aucun prérequis. Formation accessible à tous"}],
                inclus: ["Document préparation théorique en amont","Formation pratique terrain (3h)","Prêt matériel sécurité si besoin","Attestation de suivi","Document synthèse PDF avec protocoles"],
                nonInclus: ["Skis de randonnée ou raquettes","Repas samedi midi","Assurance personnelle"],
                infos: {Date:"Samedi 7 février 2026, 9h00-12h00",Lieu:"Terrain proche Chalet JUM (Chablais)",Réservation:"Option à ajouter via MP Instagram @avalanche_decision_lab",Important:"Cette formation n'est PAS diplômante"},
                showTarif: true
            }
        };

        function showFormation(key) {
            const f = formations[key];
            const btns = ['keynote','rando','horspiste','secu'];
            btns.forEach(b => {
                const btn = document.getElementById('btn-'+b);
                if(b === key) {
                    btn.className = 'p-4 rounded-lg transition-all bg-blue-600 text-white shadow-lg text-sm font-medium';
                } else {
                    btn.className = 'p-4 rounded-lg transition-all bg-gray-50 text-gray-700 hover:bg-gray-100 text-sm font-medium';
                }
            });

            let html = `
                <div class="space-y-8">
                    <div class="${f.color} rounded-xl p-8 text-white">
                        <h2 class="text-3xl font-bold mb-2">${f.title}</h2>
                        <p class="text-lg opacity-90 mb-4">${f.subtitle}</p>
                        <div class="flex gap-6 text-lg">
                            <span class="font-semibold">${f.price}</span>
                            <span>${f.duration}</span>
                        </div>
                    </div>
                    <div class="bg-white rounded-xl p-6 shadow-sm">
                        <p class="text-gray-700">${f.description}</p>
                    </div>
                    <div class="bg-white rounded-xl p-6 shadow-sm">
                        <h3 class="text-xl font-bold text-gray-800 mb-4">Objectifs pédagogiques</h3>
                        <ul class="space-y-2">
                            ${f.objectifs.map(o => `<li class="flex gap-3 text-gray-700"><span class="text-green-600 font-bold">✓</span><span>${o}</span></li>`).join('')}
                        </ul>
                    </div>
                    <div class="bg-white rounded-xl p-6 shadow-sm">
                        <h3 class="text-xl font-bold text-gray-800 mb-4">Programme détaillé</h3>
                        <div class="space-y-4">
                            ${f.programme.map(p => `
                                <div class="border-l-4 border-blue-500 pl-4 py-2">
                                    <div class="flex items-center gap-3 mb-2">
                                        <span class="font-semibold text-blue-600">${p.time}</span>
                                        <span class="font-bold text-gray-800">${p.title}</span>
                                    </div>
                                    <ul class="space-y-1 ml-4">
                                        ${p.details.map(d => `<li class="text-sm text-gray-600">• ${d}</li>`).join('')}
                                    </ul>
                                </div>
                            `).join('')}
                        </div>
                    </div>`;

            if(f.formules) {
                html += `<div class="bg-white rounded-xl p-6 shadow-sm">
                    <h3 class="text-xl font-bold text-gray-800 mb-4">Formules</h3>
                    <div class="grid md:grid-cols-2 gap-4">
                        ${f.formules.map(fm => `
                            <div class="border-2 border-gray-200 rounded-lg p-4">
                                <h4 class="font-bold text-lg mb-2">${fm.nom}</h4>
                                <p class="text-2xl font-bold text-blue-600 mb-3">${fm.tarif}</p>
                                <p class="text-gray-600 text-sm mb-3">${fm.desc}</p>
                                ${fm.av ? `<ul class="text-xs text-gray-500">${fm.av.map(a => `<li>✓ ${a}</li>`).join('')}</ul>` : ''}
                            </div>
                        `).join('')}
                    </div>
                </div>`;
            }

            html += `<div class="bg-white rounded-xl p-6 shadow-sm">
                <h3 class="text-xl font-bold text-gray-800 mb-4">Public concerné</h3>
                <div class="space-y-4">
                    ${f.publicCible.map(p => `<div><h4 class="font-semibold text-gray-800 mb-1">${p.cat}</h4><p class="text-gray-600 text-sm">${p.desc}</p></div>`).join('')}
                </div>
            </div>`;

            if(f.inclus) {
                html += `<div class="grid md:grid-cols-2 gap-6">
                    <div class="bg-green-50 rounded-xl p-6">
                        <h3 class="text-lg font-bold text-green-800 mb-4">Inclus</h3>
                        <ul class="space-y-2 text-sm text-gray-700">
                            ${f.inclus.map(i => `<li>• ${i}</li>`).join('')}
                        </ul>
                    </div>
                    <div class="bg-red-50 rounded-xl p-6">
                        <h3 class="text-lg font-bold text-red-800 mb-4">Non inclus</h3>
                        <ul class="space-y-2 text-sm text-gray-700">
                            ${f.nonInclus.map(n => `<li>• ${n}</li>`).join('')}
                        </ul>
                    </div>
                </div>`;
            }

            if(f.takeway) {
                html += `<div class="bg-white rounded-xl p-6 shadow-sm">
                    <h3 class="text-xl font-bold text-gray-800 mb-4">Vous repartez avec</h3>
                    <ul class="space-y-2">
                        ${f.takeway.map(t => `<li class="flex gap-3 text-gray-700"><span class="text-blue-600">•</span><span>${t}</span></li>`).join('')}
                    </ul>
                </div>`;
            }

            html += `<div class="bg-blue-50 rounded-xl p-6">
                <h3 class="text-xl font-bold text-blue-900 mb-4">Informations pratiques</h3>
                <div class="grid md:grid-cols-2 gap-4 text-sm text-gray-700">
                    ${Object.entries(f.infos).map(([k,v]) => `<div><span class="font-semibold">${k}:</span> <span>${v}</span></div>`).join('')}
                </div>
            </div>`;

            if(f.showTarif) {
                html += `<div class="bg-gray-50 rounded-xl p-6 text-sm text-gray-600">
                    <p><strong>Note sur les tarifs :</strong> Les tarifs incluent l'encadrement ski professionnel (aligné sur les <a href="https://www.esf-chamonix.com/tarifs-cours" target="_blank" class="text-blue-600 underline hover:text-blue-800">tarifs ESF Chamonix</a>) ainsi que l'expertise scientifique spécialisée en prise de décision.</p>
                </div>`;
            }

            html += `</div>`;
            document.getElementById('formation-content').innerHTML = html;
        }

        showFormation('keynote');
    </script>
</body>
</html>
