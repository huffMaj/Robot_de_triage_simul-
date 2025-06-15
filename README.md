📦 Color Sorting Robot Simulation
📖 Description

Ce projet implémente la simulation d’un robot mobile à roues équipé d’un bras articulé à 2 degrés de liberté, capable de trier des objets colorés (sphères) dans des boîtes de couleurs correspondantes.
La simulation est entièrement visualisée sous RViz 2 via des transformations TF et des markers.
🎯 Fonctionnalités

    Déplacement simulé de la base mobile dans l’environnement RViz.

    Animation d’un bras à 2 articulations simulées.

    Prise et dépose des objets via changements de frame TF.

    Simulation d’un scénario de tri préprogrammé :

        Le robot se positionne devant les objets.

        Prend une balle en fonction de sa couleur.

        Se dirige vers la boîte correspondante.

        Dépose la balle et recommence.

🛠️ Technologies et Outils

    ROS 2 Humble Hawksbill

    RViz 2 (visualisation 3D)

    TF2 (gestion des transformations spatiales)

    URDF (modélisation du robot)

    Python (rclpy) (programmation des nodes)

    Colcon (compilation des packages ROS 2)

📂 Structure du Package
simple_sorter_sim/
├── urdf/
│   └── simple_arm.urdf        # Description du robot
├── launch/
│   └── sorter_simulation.launch.py  # Script de lancement
├── scripts/
│   └── sorter_logic.py        # Node ROS 2 pour la logique de tri
├── rviz/
│   └── sorter_sim.rviz        # Configuration RViz
├── package.xml
└── setup.py
⚙️ Installation et Lancement

1.    Installer ROS 2 Humble et Colcon.

 2.   Cloner ce dépôt dans un workspace ROS 2 :

cd ~/ros2_ws/src
git clone <repository-url>

3.Compiler le package :

cd ~/ros2_ws
colcon build --packages-select simple_sorter_sim
source install/setup.bash

4.Lancer la simulation :

ros2 launch simple_sorter_sim sorter_simulation.launch.py
📌 Remarques

    La prise et dépose des balles est simulée par un changement de frame_id dans TF.

    Le robot effectue des séquences de déplacement et de tri prédéfinies.

    Pas d’environnement physique (pas de Gazebo).
