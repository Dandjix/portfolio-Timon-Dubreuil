<template>
    <main class="p-8 max-w-4xl mx-auto text-gray-800 text-[15px]">
        <h1 class="text-center">Stage de S6 - H2SYS</h1>
        <h4 class="text-center q-pa-none q-ma-none text-secondary"> Janvier à mai 2025</h4>

        <SectionCard>
            <h2 id="heading_1">Présentation de l'entreprise</h2>



            <div class="row">
                <div class="mb-4 col-12 col-md-6">
                    <p>
                        J'ai effectué mon stage de 15 semaines dans l'entreprise <strong>H2SYS</strong>, une
                        entreprise
                        spécialisée dans
                        le développement de solutions à hydrogène (groupes électrogènes notamment). Située à
                        <strong>Belfort</strong>,
                        H2SYS propose différents groupes électrogènes à hydrogène ainsi que des bancs didactiques et
                        des
                        piles à combustible.
                    </p>
                    <p>
                        L'entreprise a été fondée en 2017 et comptait 9 employés. Les effectifs ont augmentés
                        jusqu'à
                        atteindre 30 collaborateurs en 2021, puis l'effectif a baissé pour atteindre 12
                        collaborateurs
                        en 2025.
                    </p>
                    <p>
                        Ce stage était particulièrement adapté pour les raisons suivantes :
                    </p>
                    <ul>
                        <li>
                            L'ancienne IHM a été développée en React Js par un collaborateur ayant quitté
                            l'entreprise,
                            cette personne étant la seule personne dans l'entreprise familière avec React Js.
                        </li>
                        <li>
                            Yoann Powolny, mon maître de stage est occupé sur d'autres projets et n'est pas en
                            disposition de se dédier entièrement au développement d'une nouvelle IHM.
                        </li>
                        <li>
                            Il n'y a pas assez de tâches pour justifier l'emploi d'un nouveau collaborateur en CDI
                            pour
                            la mission du développement de l'IHM en Python NiceGUI, justifiant plutôt un stagiaire.
                        </li>
                    </ul>
                    <p>
                        La décision de l'entreprise a été faite de ne pas former les employés à une technologie web
                        telle que React Js, optant plutôt pour NiceGUI, framework connu par certains collaborateurs
                        de l'entreprise, que j'étais prêt à apprendre.
                    </p>
                </div>



                <img src="/images/stageS6/produitsEntreprise.png" alt="Produits de l'entreprise"
                    class="col-12 col-md-6 bigImg" style="height: 100%;" />
            </div>
        </SectionCard>

        <SectionCard>
            <h2 id="heading_2">Sujet du stage</h2>
            <div class="row">
                <img src="/images/stageS6/systèmeMothysSchema.png" alt="Schéma des composants du système Mothys"
                    class="col-12 col-md-6 bigImg" style="height: 100%;" />

                <div class="col-12 col-md-6">
                    <p class="mb-4">
                        Le but du stage était de concevoir une nouvelle Interface Homme-Machine (IHM) Web pour
                        remplacer
                        une
                        version obsolète pour le système Mothys. Le Mothys est un banc didactique composé d'une pile
                        à
                        combustible, d'une batterie et de ports permettant de brancher une source externe de
                        puissance
                        et une charge.
                        Le Raspberry Pi héberge l'IHM, qui est accessible via wifi depuis n'importe quel appareil.
                        Le Raspberry communique en Controller Area Network (CAN) avec les différents composants du
                        système Mothys.
                        Cette interface permet la visualisation et la gestion de données issues d’un <strong>bus
                            CAN</strong>,
                        avec des fonctionnalités comme :

                    </p>
                    <ul class="list-disc pl-6 mb-4">
                        <li>Visualisation en temps réel des données CAN</li>
                        <li>Graphiques dynamiques</li>
                        <li>Mode démo</li>
                        <li>Système de licences et gestion des utilisateurs</li>
                        <li>Traduction multi-langue et thème sombre</li>
                    </ul>
                </div>
            </div>
        </SectionCard>

        <SectionCard>
            <h2 id="heading_3">Technologies utilisées</h2>
            <ul class="list-none pl-0 mb-4 space-y-2 text-sm">
                <li class="flex items-center gap-2">
                    <img src="images/stageS6/tech/nicegui_dark.png" alt="NiceGUI" width="64px" class="q-mr-md"
                        v-if="isDark" />
                    <img src="images/stageS6/tech/nicegui_light.png" alt="NiceGUI" width="64px" class="q-mr-md"
                        v-else />
                    <strong>NiceGUI</strong>&nbsp; — pour le développement de l'IHM en Python
                </li>
                <li class="flex items-center gap-2">
                    <img src="images/stageS6/tech/konva.png" alt="Konva" width="64px" class="q-mr-md" />
                    <strong>Konva </strong>&nbsp; — pour le schéma électrique interactif
                </li>
                <li class="flex items-center gap-2">
                    <img src="images/stageS6/tech/echarts.png" alt="Apache Echarts" width="64px" class="q-mr-md" />
                    <strong>Apache ECharts</strong>&nbsp; — pour les graphiques en temps réel
                </li>
                <li class="flex items-center gap-2">
                    <img src="images/stageS6/tech/CAN_Logo.svg" alt="Controller Area Network (CAN)" width="64px"
                        class="q-mr-md" />
                    <strong>Controller Area Network </strong>&nbsp; (CAN) — pour la communication avec les
                    composants du
                    système Mothys

                </li>
                <li class="flex items-center gap-2">
                    <img src="images/stageS6/tech/raspberry-pi.png" alt="NiceGUI" width="64px" imgClass="q-mr-md" />
                    <strong>Raspberry Pi 5</strong>&nbsp; — comme plateforme embarquée
                </li>
            </ul>
        </SectionCard>


        <SectionCard>
            <h2 id="heading_4">Rôle et fonctionnalités de l'IHM</h2>
            <div class="row">
                <div class="col-12 col-md-6">
                    <p class="mb-4">
                        L’IHM développée en <strong>Python avec NiceGUI</strong> remplace une ancienne application
                        React
                        obsolète pour le banc didactique <strong>Mothys</strong> d’H2SYS. Cette IHM responsive
                        permet de
                        piloter
                        et superviser en temps réel un système d’hybridation énergétique à base de pile à
                        combustible
                        hydrogène,
                        batterie, panneau solaire ou autre source externe.
                    </p>
                </div>
            </div>


            <p class="font-semibold mb-2">Fonctionnalités principales :</p>
            <ul class="list-disc pl-6 mb-4 text-sm">
                <li>
                    Schéma interactif du système (contrôle et surveillance de chaque composant)
                    <BeforeAfter before="/images/stageS6/pageSchemaAvant.jpg"
                        after="/images/stageS6/pageSchemaAprès.png" />
                </li>
                <li>Tableau filtré de trames CAN reçues en direct
                    <BeforeAfter before="/images/stageS6/busViewerAvant.jpg"
                        after="/images/stageS6/busViewerAprès.png" />
                </li>
                <li>Lecture des variables système triées par sous-systèmes</li>
                <li>Visualisation et gestion des fichiers de logs CAN</li>
                <li>Graphiques en temps réel avec export CSV/image
                    <BeforeAfter before="/images/stageS6/pageGraphiquesAvant.jpg"
                        after="/images/stageS6/pageGraphiquesAprès.png" />

                </li>
                <li>Système de licences verrouillant certaines fonctionnalités</li>
                <li>Page d’alertes et notifications
                    <BeforeAfter before="/images/stageS6/alertesAvant.jpg" after="/images/stageS6/alertesAprès.png" />
                </li>
                <li>Dialogue manuel intégré (nouveau)</li>
                <li>Authentification multi-rôle avec permissions différenciées</li>
                <li>Paramètres configurables : gestion utilisateurs, langues (français, anglais, allemand,
                    espagnol),
                    wifi, logs, date</li>
                <li>Mise à jour logicielle cryptée via fichier ou clé USB</li>
                <li>Mode démo activable via mot de passe (rôle commercial)</li>
            </ul>

            <p class="mb-4">
                Deux rôles administrateur cachés permettent à H2SYS et aux commerciaux d’avoir un accès privilégié
                pour
                les démonstrations ou la maintenance. Ces rôles ne sont pas visibles par les utilisateurs standards.
            </p>

        </SectionCard>
        <SectionCard>
            <h2 id="heading_5">Réalisation</h2>

            <h3>Structure de l'application</h3>

            <p class="mb-4">
                Afin de structurer proprement le code de l’IHM et de garantir la clarté et la maintenabilité du
                projet,
                j’ai fait le choix d’une <strong>approche orientée objet</strong> pour organiser les données et les
                fonctionnalités métier.
            </p>

            <p class="mb-4">
                Les différentes parties de l’application, comme la gestion du <strong>bus CAN</strong>, des
                <strong>logs</strong>, des <strong>utilisateurs</strong> ou encore des <strong>licences</strong>,
                sont
                chacune encapsulées dans des <strong>services Python</strong> dédiés.
                Ces services contiennent la logique métier, les données observables, ainsi que les fonctions de
                traitement.
            </p>

            <p class="mb-4">
                Pour éviter d’avoir à <strong>passer explicitement les instances de services</strong> à chaque
                constructeur de page ou de composant dans NiceGUI, j’ai utilisé un <strong>pattern
                    Singleton</strong>
                sur la plupart des services.
                Cela m’a permis d’avoir un accès global contrôlé à chaque service, tout en assurant une instance
                unique
                et partagée dans l’application.
            </p>

            <ul class="list-disc pl-6 mb-4 text-sm">
                <li>Les vues (pages) peuvent accéder directement aux services sans injection complexe</li>
                <li>Les données sont centralisées et mises à jour automatiquement sur tous les composants qui y sont
                    liés</li>
                <li>Le code est plus lisible et les responsabilités de chaque classe sont clairement définies</li>
                <li>La logique métier reste découplée de l’affichage NiceGUI</li>
            </ul>

            <p>
                Cette organisation m’a permis d’appliquer de bonnes pratiques de développement logiciel en Python,
                tout
                en m’adaptant aux contraintes spécifiques de NiceGUI, qui ne propose pas de système d’injection de
                dépendances comme dans certains frameworks.
            </p>

            <q-separator></q-separator>
            <h3>Schéma interactif</h3>

            <div class="col">
                <div class="row" style="align-items: end; justify-content: center;">

                    <div class="col-12 col-md-6">
                        <p class="mb-4 smoltext">
                            Le schéma électrique interactif est un élément central de l'IHM du Mothys, permettant de
                            visualiser en
                            temps réel l'état du système
                            et d’interagir avec les composants. Ce module a été conçu à partir d’une base existante
                            initialement développée avec <strong>React Konva</strong>.
                        </p>

                        <p class="mb-4 smoltext">
                            Dans un premier temps, j’ai converti le code en <strong>Vue Konva</strong> pour
                            l'intégrer
                            plus
                            facilement dans une structure Vue.js.
                            Toutefois, cette version s’est révélée incompatible avec <strong>NiceGUI</strong>,
                            notamment
                            à
                            cause de
                            limitations dans l’intégration du canvas avec les composants NiceGUI.
                        </p>

                        <p class="mb-4 smoltext">
                            Finalement, j’ai choisi d’intégrer <strong>Konva JavaScript directement</strong>, chargé
                            depuis
                            le
                            dossier statique de l’application.
                            Cette solution, bien que plus manuelle, m’a permis un contrôle total sur le comportement
                            du
                            schéma et
                            une compatibilité complète avec NiceGUI.
                        </p>

                        <p class="mb-4 smoltext">
                            Chaque composant du schéma (source, charge, batterie, pile à combustible, etc.) a été
                            <strong>modularisé
                                en sous-éléments</strong> pour faciliter l’évolution du schéma et sa maintenabilité.
                            J’ai également revu entièrement le design pour le rendre plus intuitif : les
                            <strong>sources
                                sont
                                positionnées à gauche</strong>, et la <strong>charge à droite</strong>, conformément
                            au
                            layout réel
                            du PCB.
                        </p>

                        <p class="mb-4 smoltext">
                            J’ai aussi ajouté un nouveau composant graphique : le <strong>convertisseur
                                DC/DC</strong>,
                            qui joue un
                            rôle
                            clé dans
                            la gestion de la demande de puissance vers la pile à combustible.
                            Il permet de refléter dynamiquement le comportement de régulation énergétique du système
                            dans
                            l’IHM.
                        </p>

                        <p class="smoltext">
                            Ce travail m’a permis de mieux comprendre l’architecture Konva (scènes, calques,
                            événements), de
                            manipuler des éléments graphiques de façon dynamique en JavaScript,
                            et d’intégrer proprement une visualisation complexe dans un framework Python web.
                        </p>
                    </div>
                    <LegendedImg src="images/stageS6/mlg/shemaorig2.jpg" alt="Ancien Schéma" imgClass="col-12 col-md-6"
                        style="width: 50%; height: 100%;" />
                </div>
                <div class="row" style="align-items: start; justify-content: center;">

                    <LegendedImg src="images/stageS6/mlg/schema2.png" alt="Nouveau Schéma" imgClass="col-12 col-md-6"
                        style="width: 50%;" />
                    <LegendedImg src="images/stageS6/mlg/PCB.png" alt="Printed Circuit Board (PCB) du Mothys"
                        imgClass="col-12 col-md-6" style="width: 50%;" />

                </div>
            </div>






            <q-separator></q-separator>

            <h3>Graphiques en temps réel</h3>
            <div class="row">

                <div class="col-12 col-md-6">
                    <p class="mb-4">
                        L’ancienne IHM ne permettait d’afficher qu’un seul graphique à la fois, basé sur un fichier
                        journal. Les
                        interactions étaient limitées, et aucun affichage en direct n’était possible.
                        Pour répondre au besoin du client, j’ai conçu un système de <strong>graphique en temps
                            réel</strong>
                        intégré à l’IHM, en utilisant la bibliothèque <strong>Apache ECharts</strong>.
                    </p>

                    <p class="mb-4">
                        Les données du système Mothys sont reçues en direct via le <strong>bus CAN</strong>, puis
                        traitées dans
                        le backend pour être diffusées en temps réel au frontend via des WebSockets.
                        Les graphiques se mettent à jour dynamiquement avec une fréquence configurable.
                    </p>

                    <p class="mb-4">
                        Les utilisateurs peuvent visualiser simultanément jusqu’à <strong>quatre fenêtres de
                            graphiques</strong>, chacune pouvant contenir plusieurs courbes superposées.
                        Les graphiques sont interactifs : zoom, survol, légende dynamique, affichage de valeurs.
                    </p>

                    <ul class="list-disc pl-6 mb-4 text-sm">
                        <li>Les courbes sont sélectionnables par composant (batterie, pile, DCDC, etc.)</li>
                        <li>Les données affichées peuvent être <strong>exportées</strong> en image ou en <strong>CSV
                                interprété</strong></li>
                        <li>Certains affichages avancés sont <strong>verrouillés via le système de licence</strong></li>
                        <li>Les performances ont été optimisées pour que les graphes restent fluides même sur
                            <strong>Raspberry
                                Pi 5</strong>
                        </li>
                    </ul>


                </div>
                <img src="images/stageS6/pageGraphiquesAprès.png" alt="Page des graphiques finale"
                    class="col-12 col-md-6" style="height: 100%;">
            </div>
            <p>
                Cette partie m’a permis de manipuler des flux de données en temps réel, d’optimiser le rendu
                graphique
                dans un contexte contraint, et de construire une interface utilisateur claire et réactive
                adaptée à un
                usage pédagogique.
            </p>
            <q-separator></q-separator>

            <h3>Traduction multilingue</h3>
            <p class="mb-4">
                L’IHM devait être utilisable dans différents contextes pédagogiques à l’international. Une
                fonctionnalité de <strong>traduction multilingue</strong> a donc été implémentée afin de rendre
                l’application accessible à un plus large public.
            </p>

            <p class="mb-4">
                Quatre langues sont actuellement prises en charge : <strong>français</strong>,
                <strong>anglais</strong>,
                <strong>allemand</strong> et <strong>espagnol</strong>. L’utilisateur peut changer la langue
                directement
                depuis l’onglet <em>paramètres</em> de l’IHM.
            </p>

            <ul class="list-disc pl-6 mb-4 text-sm">
                <li>Structure centralisée des chaînes de caractères dans des fichiers de traduction</li>
                <li>Utilisation d’un système de clés pour rendre l’application facilement extensible</li>
                <li>Création de programmes de vérification et modification des fichiers de traduction pour
                    assurer
                    l'intégrité des différents dictionnaires de traduction</li>
            </ul>

            <p>
                Cette mise en place m’a amené à structurer proprement les composants et à anticiper les
                évolutions
                futures, notamment l’ajout potentiel d’autres langues ou de nouveaux contenus à traduire. La
                traduction
                est conçue pour être facile à maintenir par l’équipe H2SYS.
            </p>

            <q-separator></q-separator>
            <h3>Tests</h3>
            <div class="row">
                <div class="col-12 col-md-6">
                    <p class="mb-4">
                        L'application n'a pas été testée via des outils automatisés (tests unitaires ou
                        d'intégration).
                        À la
                        place, nous avons réalisé des <strong>tests manuels complets</strong> sur le banc
                        Mothys, en
                        environnement réel, afin de valider l'ensemble des fonctionnalités de l'IHM.
                    </p>


                    <p class="mb-4">
                        L’un des moments les plus critiques du stage a été la <strong>phase de test en
                            atmosphère
                            explosive</strong>, réalisée avec une pile à combustible alimentée en
                        <strong>hydrogène</strong>.
                        Dans ce contexte, l’application devait garantir la fiabilité de l’affichage, l’absence
                        de bugs
                        bloquants, le mécanisme de demande de puissance à la pile.
                    </p>



                    <p class="mb-4">
                        Chaque fonction de l’IHM a été testée à la main :
                    </p>

                    <ul class="list-disc pl-6 mb-4 text-sm">
                        <li>Activation et supervision du schéma interactif</li>
                        <li>Visualisation en direct des trames CAN</li>
                        <li>Affichage et rafraîchissement des graphiques en temps réel</li>
                        <li>Tests de changement de langue, de mode sombre, et de permissions utilisateur</li>
                        <li>Tests de la mise à jour logicielle et de la persistance des données après
                            redémarrage</li>
                        <li>Vérification du comportement des pages restreintes par la licence</li>
                    </ul>
                </div>
                <img src="/images/stageS6/testsATEX.png" alt="Tests en atmosphère explosive"
                    class="col-12 col-md-6 bigImg" style="height: 100%;" />
            </div>
            <p>
                Ces tests ont été réalisés en collaboration avec mon maître de stage et les techniciens,
                directement sur
                le matériel final. Ce processus m’a permis d’aborder les enjeux de sûreté, de précision et de
                robustesse
                dans un contexte industriel réel.
            </p>
        </SectionCard>



        <SectionCard>
            <h2 id="heading_6">Compétences mobilisées</h2>
            <h3>Réaliser un développement d’application</h3>
            <p class="mb-4">
                Durant mon stage chez <strong>H2SYS</strong>, j’ai développé une nouvelle Interface Homme-Machine
                (IHM)
                Web destinée à remplacer une version obsolète.
                Ce travail m’a permis de mettre en œuvre toutes les étapes de conception et de réalisation d’une
                application.
            </p>
            <ul class="list-disc pl-6 mb-4">
                <li>Conception et développement d’une IHM complète avec <strong>NiceGUI</strong></li>
                <li>Connexion au <strong>bus CAN</strong> pour interagir avec les composants du système Mothys</li>
                <li>Ajout de fonctionnalités : <em>mode démo, gestion des utilisateurs, schéma interactif, traduction,
                        etc.</em></li>
                <li>Déploiement sur <strong>Raspberry Pi 5</strong> dans un environnement embarqué</li>
            </ul>
            <p>
                Ce projet a couvert l’ensemble du cycle de développement logiciel, de la définition du besoin
                jusqu’au
                déploiement.
            </p>
            <q-separator></q-separator>
            <h3>Optimiser des applications</h3>
            <p class="mb-4">
                Au fil du développement, j’ai dû optimiser l’application pour répondre à des contraintes de
                performance
                et d’ergonomie, en particulier sur
                une plateforme embarquée (Raspberry Pi 5).
            </p>
            <ul class="list-disc pl-6 mb-4">
                <li>Optimisation du <strong>rendement graphique</strong> pour les schémas interactifs (Konva)</li>
                <li>Réduction du <strong>temps de chargement</strong> de l’IHM grâce à un <strong>routing
                        SPA</strong>
                </li>
                <li>Utilisation efficace des <strong>threads</strong> pour éviter le blocage de l’interface pendant
                    la
                    communication CAN</li>
                <li>Mise en cache partielle de certaines données pour éviter des rechargements inutiles</li>
                <li>Test et validation de l’IHM en conditions réelles sur le matériel cible pour ajuster les
                    performances</li>
            </ul>
            <p>
                Ces actions ont permis de garantir une application fluide, rapide et adaptée à un environnement
                matériel
                contraint.
            </p>
            <q-separator></q-separator>
            <h3>Collaborer au sein d’une équipe informatique</h3>
            <p class="mb-4">
                Bien que l'équipe de développement de l'IHM soit restreinte — composée uniquement de mon maître de
                stage
                <strong>Yoann Powolny</strong> et moi-même —
                nous avons mis en place des outils et des méthodes efficaces pour collaborer dans de bonnes
                conditions :
            </p>
            <ul class="list-disc pl-6 mb-4">
                <li><strong>Git</strong> a été utilisé pour la gestion de version : travail sur des branches,
                    commits
                    fréquents, revue de code et fusion structurée.</li>
                <li>Un <strong>backlog</strong> clair permettait de suivre les tâches, les priorités et l’évolution
                    du
                    projet.</li>
            </ul>
            <p>
                Cette organisation m’a permis d’acquérir des compétences concrètes en gestion collaborative de code,
                planification agile
                et communication technique au sein d'une équipe, même réduite.
            </p>
        </SectionCard>

        <SectionCard max-width="750px">
            <h2 id="heading_7">Bilan</h2>
            <p>
                Ce stage m’a permis de renforcer mes compétences en développement web, en systèmes embarqués
                et en gestion de projet logiciel. Il m’a également donné l’opportunité de travailler sur un produit
                utilisé en conditions réelles.
            </p>
            <p>J'ai réalisé un site web dans un framework que je ne connaissais pas, avec comme fonctionnalités
                intéressantes un schéma interractif et une page de graphiques en temps réel; tout en évoluant dans une
                PME et en me faisant une bonne idée du travail en entreprise. </p>
        </SectionCard>
    </main>
</template>

<script>
import { Dark } from 'quasar'
import BeforeAfter from 'src/components/elements/BeforeAfter.vue'
import SectionCard from 'src/components/elements/SectionCard.vue'
import LegendedImg from 'src/components/elements/LegendedImg.vue';

export default {
    data() {
        return {
            isDark: Dark.isActive
        }
    },
    mounted() {
        // Listen to system theme changes and update isDark accordingly
        window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', e => {
            this.isDark = e.matches
            Dark.set(e.matches)
        })
    },
    components: {
        BeforeAfter,
        SectionCard,
        LegendedImg
    }
}
</script>

<style lang="sass">
strong
  color: $secondary
</style>

<style>
img {
    padding: 10px;
    border-radius: 20px;
}



.bigImg {
    padding: 20px;
    border-radius: 40px;
}
</style>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500&family=Lora:wght@600&display=swap');

main {
    font-family: 'Inter', sans-serif;
    line-height: 1.6;
}


h1,
h2,
h3 {
    font-family: 'Roboto Condensed', serif;
    margin-top: 0.75rem;
    margin-bottom: 0.5rem;
}

p {
    text-align: justify;
}

.smoltext {
    font-size: max(0.75vw, 9px);
}
</style>
