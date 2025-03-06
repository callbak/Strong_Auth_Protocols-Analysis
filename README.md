# Strong Authentication Protocols Analysis - Analyse des Protocoles d'Authentification Forte 

# Table des matières

1. [Description](#description)
2. [🚀 Installation & Exécution](#-installation-exécution)
   1. [Méthode 1](#méthode-1)
   2. [Méthode 2](#méthode-2)
3. [🔍 Résultats](#-résultats)


## Description

Ce projet implémente trois protocoles d'authentification indépendants :
1. **Authentification asymétrique forte** (`.txt`, `.hlpsl`)
2. **Authentification symétrique forte** (`.txt`, `.hlpsl`)
3. **Authentification XOR forte** (`.txt`, `.hlpsl`)

Les protocoles ont été testés sous une machine virtuelle Ubuntu avec SPAN. Les deux premiers protocoles ont été jugés sûrs, mais une attaque a été détectée dans l'authentification XOR.

---

## 🚀 Installation & Exécution
### Méthode 1
#### Cloner le dépôt
```bash
git clone https://github.com/callbak/Strong_Auth_Protocols-Analysis.git
cd Strong_Auth_Protocols-Analysis
```

#### Installer SPAN (Si non installé)
```bash
sudo apt update && sudo apt install avispa-tools
```

#### Vérifier les protocoles avec AVISPA
Exécutez la commande suivante pour tester un fichier :
```bash
span strong_asymmetric_authentication.hlpsl
```

Remplacez `strong_asymmetric_authentication.hlpsl` par le fichier souhaité.

### Méthode 2
#### Installation et utilisation de SPAN

1. Installer **SPAN-Ubuntu10.10-light** dans une machine virtuelle.
2. Ouvrir SPAN et charger le fichier `.hlpsl` souhaité.
3. Sélectionner l'option `ofmc`.
4. Cliquer sur **Execute** pour visualiser les résultats.
5. Pour voir la simulation du protocole, utiliser l'option **Protocol Simulation** dans SPAN.

---

## 🔍 Résultats
- **Authentification asymétrique forte** ✅ (Système sûr)
  - ![sa_asymm](https://github.com/user-attachments/assets/f7a097e9-0d53-46f8-816a-1a27096b2f51)
- **Authentification symétrique forte** ✅ (Système sûr)
  -  ![sa_symm](https://github.com/user-attachments/assets/128af6c9-69fd-4023-851d-9cb3f929fd87)
- **Authentification XOR forte** ❌ (Attaque détectée)
  - ![sa_xor](https://github.com/user-attachments/assets/b58a8b59-1b51-4e7c-a117-870ae4ed7594)


