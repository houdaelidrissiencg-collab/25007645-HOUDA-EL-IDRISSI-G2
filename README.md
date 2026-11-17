# F22 : Anticipations d'inflation (T10YIE)

Projet de régression sur série mensuelle : le niveau du T10YIE du mois t et son historique récent permettent-ils de mieux prévoir le T10YIE du mois t+1 qu'une simple persistance ?

**Auteure :** Houda El Idrissi, ENCG Settat (Gestion et Finance)

## Contenu
- `HOUDA_EL_IDRISI_CC_PARTIE_2.ipynb` : notebook (à placer à la racine)
- `docs/fiche_F22.md` : fiche attribuée, sources et références
- `data/raw/` : données brutes (voir `data/raw/README.md`)
- `requirements.txt` : environnement Python
- `DECLARATION_IA.md` : déclaration d'usage des outils d'IA

## Exécution
1. Installer l'environnement : `pip install -r requirements.txt`
2. Placer `T10YIE.csv` dans `data/raw/` (procédure dans `data/raw/README.md`).
3. Dans le notebook, régler le chemin : `URL = "data/raw/T10YIE.csv"` (sous Colab, chemin Drive d'origine).
4. Exécuter toutes les cellules dans l'ordre.

## Méthode
- Agrégation quotidienne vers mensuelle (moyenne, jours fériés ignorés).
- Variables construites uniquement avec le passé : niveau t, t−1, t−2, variation 1 mois, moyenne mobile 3 mois, volatilité intra-mensuelle.
- Découpage chronologique 70 % / 15 % / 15 %.
- Référence naïve : persistance. Métriques : RMSE (principale) et MAE sur le test.
