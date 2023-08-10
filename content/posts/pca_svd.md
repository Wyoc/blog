---
title: "L'Analyse en composantes principales est une SVD, avec un twist"
date: 2023-08-09T11:02:40+02:00
draft: true
---

Au cours de mes études j'ai eu tout le loisir d'aller à la rencontre de plein d'outils mathématiques, mais toujours de façon très compartimentée[^1]. Ainsi se sont faite parallèlement les découvertes de l'Analyse en Composantes Principales et la Décomposition en Valeurs Singulières (respectivement PCA et SVD par la suite), en cours de stats et d’algèbre. J'ai fini par comprendre que les deux étaient liés sur le tard, pendant la thèse, et parce que mon camarade Nathanaël était intéressé par la question, je vais la raconter ici.

# La SVD, c'est quoi ?
La décomposition en valeurs singulières (ou _singular value decomposition_ dans la langue de Cher) est ce qu'on appelle est une méthode de factorisation de matrice, c'est à dire un moyen de transformer une matrice en le produit de plusieurs autres.

Plus formellement, nous allons considérer une matrice \\( M \in \mathbb{R}^{m\times n}\\) [^2]. Il existe alors une factorisation de \\(M\\) tel quel
\\[M = U \Sigma V^\ast\\],
avec:

- \\(V\in\mathbb{R}^{n\times n}\\) 
- \\(U\in\mathbb{R}^{m\times m}\\) 
- \\(\Sigma\in\mathbb{R}^{m\times n}\\) 

[^1]:Les disciplines communiquaient peu, probablement parce que j'étais dans des cursus de physique et d'ingénierie.

[^2]:Autrement dit, une matrice de \\(m\\) lignes et \\(n\\) colonnes, dont tous les coefficients sont réels. Et nous allons nous arrêter au cas réel, mais ça fonctionne tout aussi bien avec le corps des nombres complexes.