# ABIT Admin

Interface d’administration d’**AL Baraka International Trading**.

Gère :
- Demandes d’échange
- Commandes & tracking
- Produits de la boutique
- Taux de change & paramètres commerciaux
- Clients

**Même projet Firebase** que l’application client : `abit-d927a`

---

## Repos liés

| Repo | Rôle |
|------|------|
| [al-baraka-international-trading](https://github.com/ahmedaidara/al-baraka-international-trading) | Application **client** (mobile-first) |
| **abit-admin** (ce dépôt) | Application **administrateur** |

Les deux applications partagent Auth, Firestore et Storage.

---

## Accès administrateur

1. Crée un compte via l’app client (ou dans Firebase Authentication).
2. Dans Firestore → collection `users` → document de ton UID → change `role` en `"admin"`.
3. Connecte-toi ici avec le même email / mot de passe.

Un utilisateur avec le rôle `client` ne peut **jamais** accéder à cet admin (vérification côté code + règles Firestore).

---

## Structure

```
abit-admin/
├── index.html          # Tableau de bord
├── exchanges.html      # (à venir)
├── orders.html         # (à venir)
├── products.html       # (à venir)
├── tracking.html       # (à venir)
├── customers.html      # (à venir)
├── settings.html       # (à venir)
├── css/design-system.css
└── js/
    ├── firebase-config.js
    └── firebase-init.js
```

---

## État actuel

- Tableau de bord avec authentification admin
- Protection par rôle
- Design system partagé avec le client
- Prêt pour les pages de gestion (échanges, produits, commandes…)

---

**Projet Firebase :** abit-d927a  
**Repo client :** https://github.com/ahmedaidara/al-baraka-international-trading
