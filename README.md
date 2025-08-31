the right code is in main ;the wrong one is in dev ;and when the dev is correct pull in the main directly before another file add pushed
#################################################################################################################
-git init
-git add guess_number.py
-git commit -m "Guesse the right number"        
-git status
-git push origin dev  
__________________________________________________________________________________
definition of branch:
__________________________________________________________________________________
main (ou master)
👉 c’est la branche principale, souvent considérée comme stable.
Le code qui s’y trouve doit normalement être prêt à être livré, testé, ou utilisé en production.
dev
👉 c’est une branche de développement.
Tu y ajoutes tes nouvelles fonctionnalités, tes correctifs, tu testes des choses… bref, c’est la zone de travail.
Quand tout est validé, on fusionne (merge ou pull request) vers main.
__________________________________________________________________________________
2️⃣ Méthode en local (merge direct)
Tu peux fusionner en local, puis pousser sur GitHub :
git checkout main        # aller sur main
git merge dev            # fusionner dev dans main
git push origin main     # envoyer sur GitHub
👉 Avec ça, tout ce qui est dans dev se retrouve aussi dans main.
_________________________________________________________________________________
3️⃣ (Option avancée) Copier un seul commit de dev vers main
Si tu ne veux pas tout merge, mais juste un commit précis de dev :
git checkout main
git cherry-pick <id_du_commit>
git push origin main
____________________________________________________________________________________