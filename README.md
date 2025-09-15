# ansible-cyberlab


# Automatisation des Équipements Réseau avec Ansible, Jinja2 et Python

## Table des Matières
- [Présentation](#présentation)
- [Objectifs du Projet](#objectifs-du-projet)
- [Technologies Utilisées](#technologies-utilisées)
- [Architecture du Projet](#architecture-du-projet)
- [Prérequis](#prérequis)
- [Installation et Configuration](#installation-et-configuration)

---

## Présentation
Ce projet a pour but d’automatiser la gestion et la configuration des équipements réseau (switches, routeurs, firewalls) à l’aide d’**Ansible**, en combinant la puissance des **templates Jinja2** et des scripts **Python** pour des tâches plus complexes.  
Le projet suit les bonnes pratiques de gestion de version via **Git** pour assurer la traçabilité et la collaboration.

---

## Objectifs du Projet
- Automatiser la configuration initiale et continue des équipements réseau.  
- Réduire les erreurs humaines lors de la configuration manuelle.  
- Générer des configurations dynamiques avec **Jinja2** selon le type d’équipement ou le rôle réseau.  
- Intégrer des scripts Python pour validations ou transformations avancées.  
- Assurer un workflow reproductible grâce à **Git**.

---

## Technologies Utilisées
- **Ansible** : Automatisation de la configuration réseau.  
- **Jinja2** : Templates pour générer dynamiquement les fichiers de configuration.  
- **Python** : Scripts pour manipulations spécifiques et validations.  
- **Git** : Gestion de version et collaboration.  
- **YAML** : Format pour les inventaires et les variables Ansible.

---

## Architecture du Projet

ansible-scripts/
│
├── ansible/
│ ├── inventory/
│ │ └── production.yml
│ ├── playbooks/
│ │ ├── deploy_config.yml
│ │ └── backup_config.yml
│ ├── roles/
│ │ ├── base_config/
│ │ │ ├── tasks/main.yml
│ │ │ └── templates/base_config.j2
│ │ └── vlan_config/
│ │ ├── tasks/main.yml
│ │ └── templates/vlan_config.j2
│ └── group_vars/
│ └── all.yml
│
├── scripts/
│ └── validate_config.py
│
├── docs/
│ └── architecture.png
│
├── README.md
└── requirements.txt


---

## Prérequis
Avant de commencer, assurez-vous d’avoir installé :
- **Python 3.9+**
- **Ansible 2.16+**
- **Git**
- Accès SSH aux équipements réseau
- Bibliothèques Python nécessaires (installables via `pip install -r requirements.txt`)

---

## Installation et Configuration

1. **Cloner le projet :**
```bash
git clone https://github.com/hilaire-projet/ansible-scripts.git
cd ansible-scripts




