# Politique de confidentialité — TheRuler

*Dernière mise à jour : 4 octobre 2026* · [English version below](#privacy-policy--theruler)

TheRuler (« le bot ») est un bot Discord édité par **kibushiii** (« nous »).
Cette politique explique quelles données le bot traite, pourquoi, combien de temps et comment les faire supprimer.

## 1. Données collectées

Le bot ne collecte que ce qui est nécessaire à ses fonctionnalités. Il n'a pas accès à vos messages privés avec d'autres personnes, à votre adresse e-mail ni à votre mot de passe.

| Fonctionnalité | Données conservées |
| --- | --- |
| Niveaux & XP | identifiant Discord, identifiant du serveur, niveau, XP, date du dernier message ayant rapporté de l'XP |
| Réputation | identifiant Discord, score de réputation, date de votre dernier vote pour chaque membre (anti-abus) |
| Succès | identifiant Discord, succès débloqués et épinglés, dates |
| Profil | thème, mode d'affichage, choix de visibilité dans `/whoplays` |
| Langue | langue choisie (par utilisateur), langue du serveur (par serveur) |
| Jeux (Humans & Vampires, Eryndal) | identifiant Discord, progression de la partie en cours (inventaire, équipement…), statistiques de jeu |
| Loup-Garou | identifiants et pseudos des joueurs, rôles, votes et actions de la partie en cours ; journal technique de la partie ; **résultat de chaque joueur** à la fin (serveur, rôle, victoire ou défaite, Cristaux gagnés, date) pour `/loup-garou-stats` |
| Cristaux (monnaie virtuelle) | identifiant Discord, solde, total gagné et dépensé ; historique des transactions (montant, type, raison, serveur, date) |
| Boutique | articles configurés par les administrateurs du serveur ; pour un rôle personnalisé acheté : identifiant du membre et du rôle, nom choisi, dates de création et d'expiration |
| Compte Riot (`/lol`) | identifiant Discord, Riot ID (nom#tag), identifiant de compte Riot (PUUID), serveur League of Legends, date de liaison |
| Statistiques du serveur | nombre de messages, de mini-jeux et de parties de Loup-Garou **par serveur** (de simples compteurs : ni contenu, ni auteur) |
| Tickets | identifiant du serveur, du salon et de l'auteur du ticket, statut et dates |
| Configuration de serveur | salons et options choisis par les administrateurs (logs, bienvenue, autorôles, XP) |

**Données lues mais non conservées :**
- **Contenu des messages** : sa longueur sert à calculer l'XP ; chaque message est compté dans les statistiques du serveur sans être lu ni enregistré. Pendant une partie de Loup-Garou avec le rôle **Loup Bavard**, les messages de ce joueur dans le salon de la partie sont analysés pour y chercher son mot secret, puis oubliés. Si un administrateur a activé les logs, le contenu d'un message supprimé ou modifié est republié dans le salon de logs du serveur, sans être stocké par le bot.
- **Statut d'activité** (« joue à… ») : lu uniquement au moment d'une recherche `/whoplays`, si vous n'avez pas désactivé votre visibilité.
- **Textes à traduire** (`/translate`) : envoyés au service de traduction (voir section 3), jamais enregistrés par le bot.
- **Vocal (Loup-Garou)** : le bot parle dans le salon vocal de la partie (maître du jeu). Il n'écoute personne, **sauf** dans une partie personnalisée comprenant le rôle **Loup Bavard** : la voix de **ce seul joueur** est alors reçue, uniquement le jour et tant que son mot n'est pas trouvé, puis **transcrite localement**, sur le serveur du bot, par un modèle de reconnaissance vocale (Whisper). **L'audio n'est jamais enregistré** : il est traité en mémoire puis effacé. Seule la transcription peut figurer dans le journal technique de la partie (voir section 4). La voix des autres joueurs n'est jamais décodée.

## 2. Utilisation des données

Les données servent uniquement à fournir les fonctionnalités du bot : afficher votre profil, vos niveaux, vos succès et vos statistiques, faire fonctionner les jeux et la monnaie virtuelle, appliquer la configuration de votre serveur.
Elles ne sont **jamais vendues**, ni utilisées à des fins publicitaires, ni partagées avec des tiers, sauf pour les services nécessaires listés ci-dessous ou en cas d'obligation légale.

## 3. Sous-traitants et services tiers

- **Discord** : plateforme sur laquelle le bot fonctionne ([politique de Discord](https://discord.com/privacy)).
- **Hébergement de la base de données** : les données sont stockées dans une base MongoDB hébergée par l'éditeur.
- **Synthèse vocale Microsoft Edge** (narration du Loup-Garou) : seules les phrases fixes du maître de jeu (« La nuit tombe… ») sont envoyées. Aucune donnée personnelle n'est transmise.
- **API Riot Games** (`/lol`) : le Riot ID demandé est envoyé à Riot Games pour obtenir les statistiques publiques du compte ([politique de Riot](https://www.riotgames.com/en/privacy-notice)).
- **Traduction** (`/translate`) : le texte à traduire est envoyé à MyMemory (Translated srl) ou, si configuré, à DeepL.
- **Reconnaissance vocale** (Loup Bavard) : le modèle Whisper fonctionne **sur le serveur du bot** ; aucun audio n'est envoyé à un service extérieur (le modèle est seulement téléchargé une fois depuis Hugging Face).

## 4. Durée de conservation

- Partie de Loup-Garou : supprimée à la fin de la partie ; son journal technique (y compris d'éventuelles transcriptions du Loup Bavard) est effacé automatiquement après **30 jours**.
- Résultats de Loup-Garou, Cristaux et transactions : conservés tant que le bot les utilise, ou jusqu'à votre demande de suppression.
- Rôle personnalisé : supprimé automatiquement à son expiration, si vous quittez le serveur ou si le rôle est supprimé.
- Compte Riot lié : conservé jusqu'à ce que vous le déliiez (`/lol unlink`) ou demandiez sa suppression.
- Parties de jeux solo : supprimées à la fin ou à l'abandon de la partie.
- Autres données (XP, réputation, succès, préférences) : conservées tant que le bot les utilise, ou jusqu'à votre demande de suppression.
- Configuration et compteurs d'un serveur : conservés jusqu'à la demande d'un administrateur.

## 5. Vos droits

Vous pouvez demander l'accès à vos données, leur rectification ou leur **suppression** en nous contactant (voir ci-dessous) avec votre identifiant Discord. Nous traitons les demandes dans un délai de 30 jours. Vous pouvez aussi délier vous-même votre compte Riot avec `/lol unlink`.
Si vous résidez dans l'Union européenne, vous disposez des droits prévus par le RGPD, dont celui d'introduire une réclamation auprès de l'autorité de protection des données (en France, la CNIL).

## 6. Mineurs

Le bot est destiné aux utilisateurs respectant l'âge minimum requis par Discord dans leur pays.

## 7. Modifications

Cette politique peut évoluer. La date de mise à jour en haut de page indique la dernière version.

## 8. Contact

**theruler.support@gmail.com** — ou sur le serveur Discord de support : **(https://discord.gg/B5DAq2emHc)**

---

# Privacy Policy — TheRuler

*Last updated: October 4, 2026*

TheRuler ("the bot") is a Discord bot operated by **kibushiii** ("we").
This policy explains what data the bot processes, why, for how long, and how to have it deleted.

## 1. Data we collect

The bot only collects what its features need. It has no access to your private conversations with other people, your e-mail address or your password.

| Feature | Data stored |
| --- | --- |
| Levels & XP | Discord user ID, server ID, level, XP, time of the last message that earned XP |
| Reputation | Discord user ID, reputation score, time of your last vote for each member (anti-abuse) |
| Achievements | Discord user ID, unlocked and pinned achievements, dates |
| Profile | theme, display mode, visibility choice for `/whoplays` |
| Language | chosen language (per user), server language (per server) |
| Games (Humans & Vampires, Eryndal) | Discord user ID, progress of the current game (inventory, equipment…), game statistics |
| Werewolf | players' IDs and nicknames, roles, votes and actions of the current game; technical game log; **each player's result** at the end (server, role, win or loss, Crystals earned, date) for `/werewolf-stats` |
| Crystals (virtual currency) | Discord user ID, balance, total earned and spent; transaction history (amount, type, reason, server, date) |
| Shop | articles set up by the server's administrators; for a bought custom role: member and role IDs, chosen name, creation and expiry dates |
| Riot account (`/lol`) | Discord user ID, Riot ID (name#tag), Riot account ID (PUUID), League of Legends server, link date |
| Server statistics | number of messages, mini-games and Werewolf games **per server** (plain counters: no content, no author) |
| Tickets | server, channel and author IDs of the ticket, status and dates |
| Server configuration | channels and options chosen by administrators (logs, welcome, auto-roles, XP) |

**Data read but not stored:**
- **Message content**: its length is used to compute XP; every message is counted in the server statistics without being read or saved. During a Werewolf game with the **Chatty Wolf** role, that player's messages in the game channel are checked for their secret word, then forgotten. If an administrator enabled logs, the content of a deleted or edited message is reposted in that server's log channel, without being stored by the bot.
- **Activity status** ("playing…"): only read during a `/whoplays` search, unless you turned your visibility off.
- **Texts to translate** (`/translate`): sent to the translation service (see section 3), never saved by the bot.
- **Voice (Werewolf)**: the bot speaks in the game's voice channel (game master). It does not listen to anyone, **except** in a custom game that includes the **Chatty Wolf** role: the voice of **that player only** is then received, only during the day and until their word is found, and **transcribed locally**, on the bot's own server, by a speech-recognition model (Whisper). **Audio is never recorded**: it is processed in memory and then discarded. Only the transcription may appear in the game's technical log (see section 4). Other players' voices are never decoded.

## 2. How we use data

Data is only used to provide the bot's features: show your profile, levels, achievements and statistics, run the games and the virtual currency, apply your server's configuration.
It is **never sold**, never used for advertising and never shared with third parties, except with the necessary services listed below or where required by law.

## 3. Service providers and third-party services

- **Discord**: the platform the bot runs on ([Discord's policy](https://discord.com/privacy)).
- **Database hosting**: data is stored in a MongoDB database hosted by the operator.
- **Microsoft Edge text-to-speech** (Werewolf narration): only the game master's fixed sentences ("Night falls…") are sent. No personal data is transmitted.
- **Riot Games API** (`/lol`): the requested Riot ID is sent to Riot Games to get the account's public statistics ([Riot's policy](https://www.riotgames.com/en/privacy-notice)).
- **Translation** (`/translate`): the text to translate is sent to MyMemory (Translated srl) or, if configured, to DeepL.
- **Speech recognition** (Chatty Wolf): the Whisper model runs **on the bot's own server**; no audio is sent to any outside service (the model is only downloaded once from Hugging Face).

## 4. Retention

- Werewolf game: deleted when the game ends; its technical log (including any Chatty Wolf transcriptions) is erased automatically after **30 days**.
- Werewolf results, Crystals and transactions: kept while the bot uses them, or until you ask for deletion.
- Custom role: deleted automatically when it expires, if you leave the server, or if the role is deleted.
- Linked Riot account: kept until you unlink it (`/lol unlink`) or ask for deletion.
- Solo game sessions: deleted when the game ends or is abandoned.
- Other data (XP, reputation, achievements, preferences): kept while the bot uses it, or until you ask for deletion.
- Server configuration and counters: kept until an administrator asks for deletion.

## 5. Your rights

You can ask to access, correct or **delete** your data by contacting us (see below) with your Discord user ID. Requests are handled within 30 days. You can also unlink your Riot account yourself with `/lol unlink`.
If you live in the European Union, you have the rights granted by the GDPR, including the right to lodge a complaint with your data protection authority.

## 6. Minors

The bot is intended for users who meet Discord's minimum age in their country.

## 7. Changes

This policy may change. The date at the top shows the latest version.

## 8. Contact

**theruler.support@gmail.com** — or on the support Discord server: **(https://discord.gg/B5DAq2emHc)**
