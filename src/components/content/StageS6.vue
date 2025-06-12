<template>
    <main class="p-8 max-w-4xl mx-auto text-gray-800 text-[15px]">
        <h1 class="text-3xl font-bold mb-6 text-center text-indigo-700 font-serif">Mon Stage de Fin d'Études</h1>

        <section class="mb-10">
            <h2 class="text-xl font-semibold mb-2 text-indigo-600">Présentation de l'entreprise</h2>
            <p class="mb-4">
                J'ai effectué mon stage de 15 semaines dans l'entreprise <strong>H2SYS</strong>, une entreprise
                spécialisée dans
                <em>le développement de solutions à hydrogène (groupes électrogènes notamment)</em>. Située à
                <strong>Belfort</strong>,
                elle développe des outils de supervision via des interfaces web modernes.
            </p>
            <img src="/images/entreprise.jpg" alt="Photo de l'entreprise" class="rounded-xl shadow-md w-full mb-6" />
        </section>

        <section class="mb-10">
            <h2 class="text-xl font-semibold mb-2 text-indigo-600">Sujet du stage</h2>
            <p class="mb-4">
                Le but du stage était de concevoir une nouvelle Interface Homme-Machine (IHM) Web pour remplacer une
                version obsolète.
                Cette interface permet la visualisation et la gestion de données issues d’un <strong>bus CAN</strong>,
                avec des fonctionnalités comme :
            </p>
            <ul class="list-disc pl-6 mb-4">
                <li>Visualisation en temps réel des données CAN</li>
                <li>Graphiques dynamiques</li>
                <li>Mode démo</li>
                <li>Système de licences et gestion des utilisateurs</li>
                <li>Traduction multi-langue et thème sombre</li>
            </ul>
            <img src="/images/ihm_ancienne.png" alt="Ancienne IHM" class="rounded-xl shadow mb-4" />
            <img src="/images/ihm_nouvelle.png" alt="Nouvelle IHM" class="rounded-xl shadow" />
        </section>

        <section class="mb-10">
            <h2 class="text-xl font-semibold mb-2 text-indigo-600">Technologies utilisées</h2>
            <ul class="list-disc pl-6 mb-4">
                <li><strong>NiceGUI</strong> pour le développement de l'IHM</li>
                <li><strong>Konva</strong> pour le schéma électrique interactif</li>
                <li><strong>Apache Echarts</strong> pour les graphiques en temps réel</li>
                <li><strong>CAN</strong> (Controller Area Network) pour communiquer avec les différents composants</li>
                <li><strong>Raspberry Pi 5</strong> comme plateforme cible</li>
            </ul>
        </section>

        <section class="mb-10">
            <h2 class="text-xl font-semibold mb-2 text-indigo-600">Rôle et fonctionnalités de l'IHM</h2>
            <p class="mb-4">
                L’IHM développée en <strong>Python avec NiceGUI</strong> remplace une ancienne application React
                obsolète pour le banc didactique <strong>Mothys</strong> d’H2SYS. Cette IHM responsive permet de piloter
                et superviser en temps réel un système d’hybridation énergétique à base de pile à combustible hydrogène,
                batterie, panneau solaire ou autre source externe.
            </p>

            <p class="mb-4">
                Accessible via un hotspot Wi-Fi intégré au Mothys, l’IHM est disponible sur tablette, PC ou mobile. Elle
                centralise la surveillance et le contrôle du système tout en ajoutant des fonctions avancées de
                sécurité, de gestion utilisateur, et de maintenance.
            </p>

            <p class="font-semibold mb-2">Fonctionnalités principales :</p>
            <ul class="list-disc pl-6 mb-4 text-sm">
                <li>Schéma interactif du système (contrôle et surveillance de chaque composant)</li>
                <li>Tableau filtré de trames CAN reçues en direct</li>
                <li>Lecture des variables système triées par sous-systèmes</li>
                <li>Visualisation et gestion des fichiers de logs CAN</li>
                <li>Graphiques en temps réel avec export CSV/image</li>
                <li>Système de licences verrouillant certaines fonctionnalités</li>
                <li>Page d’alertes et notifications</li>
                <li>Dialogue manuel intégré (nouveau)</li>
                <li>Authentification multi-rôle avec permissions différenciées</li>
                <li>Paramètres configurables : gestion utilisateurs, langues (français, anglais, allemand, espagnol),
                    wifi, logs, date</li>
                <li>Mise à jour logicielle cryptée via fichier ou clé USB</li>
                <li>Mode démo activable via mot de passe (rôle commercial)</li>
            </ul>

            <p class="mb-4">
                Deux rôles administrateur cachés permettent à H2SYS et aux commerciaux d’avoir un accès privilégié pour
                les démonstrations ou la maintenance. Ces rôles ne sont pas visibles par les utilisateurs standards.
            </p>
        </section>


        <section class="mb-10">
            <h2 class="text-xl font-semibold mb-2 text-indigo-600">Réaliser un développement d’application</h2>
            <p class="mb-4">
                Durant mon stage chez <strong>H2SYS</strong>, j’ai développé une nouvelle Interface Homme-Machine (IHM)
                Web destinée à remplacer une version obsolète.
                Ce travail m’a permis de mettre en œuvre toutes les étapes de conception et de réalisation d’une
                application.
            </p>
            <ul class="list-disc pl-6 mb-4">
                <li>Conception et développement d’une IHM complète avec <strong>NiceGUI</strong></li>
                <li>Développement <strong>frontend</strong> (affichage, interactions, graphismes dynamiques) et
                    <strong>backend</strong> (serveur FastAPI)
                </li>
                <li>Connexion au <strong>bus CAN</strong> pour afficher des données en temps réel</li>
                <li>Ajout de fonctionnalités : <em>mode démo, gestion des utilisateurs, thème sombre, traduction,
                        etc.</em></li>
                <li>Déploiement sur <strong>Raspberry Pi 5</strong> dans un environnement embarqué</li>
            </ul>
            <p>
                Ce projet a couvert l’ensemble du cycle de développement logiciel, de la définition du besoin jusqu’au
                déploiement.
            </p>
        </section>

        <section class="mb-10">
            <h2 class="text-xl font-semibold mb-2 text-indigo-600">Optimiser des applications</h2>
            <p class="mb-4">
                Au fil du développement, j’ai dû optimiser l’application pour répondre à des contraintes de performance
                et d’ergonomie, en particulier sur
                une plateforme embarquée (Raspberry Pi 5).
            </p>
            <ul class="list-disc pl-6 mb-4">
                <li>Optimisation du <strong>rendement graphique</strong> pour les schémas interactifs (Konva)</li>
                <li>Réduction du <strong>temps de chargement</strong> de l’IHM grâce à un <strong>routing SPA</strong>
                </li>
                <li>Utilisation efficace des <strong>threads</strong> pour éviter le blocage de l’interface pendant la
                    communication CAN</li>
                <li>Mise en cache partielle de certaines données pour éviter des rechargements inutiles</li>
                <li>Test et validation de l’IHM en conditions réelles sur le matériel cible pour ajuster les
                    performances</li>
            </ul>
            <p>
                Ces actions ont permis de garantir une application fluide, rapide et adaptée à un environnement matériel
                contraint.
            </p>
        </section>



        <section class="mb-10">
            <h2 class="text-xl font-semibold mb-2 text-indigo-600">Collaborer au sein d’une équipe informatique</h2>
            <p class="mb-4">
                Bien que l'équipe de développement de l'IHM soit restreinte — composée uniquement de mon maître de stage
                <strong>Yoann Powolny</strong> et moi-même —
                nous avons mis en place des outils et des méthodes efficaces pour collaborer dans de bonnes conditions :
            </p>
            <ul class="list-disc pl-6 mb-4">
                <li><strong>Git</strong> a été utilisé pour la gestion de version : travail sur des branches, commits
                    fréquents, revue de code et fusion structurée.</li>
                <li>Un <strong>backlog</strong> clair permettait de suivre les tâches, les priorités et l’évolution du
                    projet.</li>
            </ul>
            <p>
                Cette organisation m’a permis d’acquérir des compétences concrètes en gestion collaborative de code,
                planification agile
                et communication technique au sein d'une équipe, même réduite.
            </p>
        </section>

        <section class="mb-10">
            <h2 class="text-xl font-semibold mb-2 text-indigo-600">Bilan</h2>
            <p>
                Ce stage m’a permis de renforcer mes compétences en développement web, en systèmes embarqués
                et en gestion de projet logiciel. Il m’a également donné l’opportunité de travailler sur un produit
                utilisé en conditions réelles.
            </p>
        </section>
    </main>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500&family=Lora:wght@600&display=swap');

main {
    font-family: 'Inter', sans-serif;
    line-height: 1.6;
}

h1,
h2 {
    font-family: 'Lora', serif;
}
</style>
