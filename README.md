# COMPOSANT_JWT

```
// ====================
// Génération d'un JWT
// 
// jeton (chaine) = COL_JWT.EncodeJWT( payload (json), durée validité (durée), secret (chaine) )
// SI durée validité = -1, le jeton n'expire pas
// ====================

gJsonPayload est un JSON
gJsonPayload["sub"] = 123

gsMonNouveauJeton est une chaîne
gsMonNouveauJeton = COL_JWT.EncodeJWT(gJsonPayload, 7j, "secret")

// ====================
// Vérification d'un JWT
// 
// payload (json) = COL_JWT.VérifieJWT( jeton (chaine), secret (chaine) )
// ====================

gsJetonAVérifier est une chaîne
gsJetonAVérifier = gsMonNouveauJeton

gJsonPayloadToken est un JSON
gJsonPayloadToken = COL_JWT.VérifieJWT(gsJetonAVérifier, "secret")

SI gJsonPayloadToken = -1 ALORS
	// Jeton invalide
SINON
	// Jeton valide
FIN
```
