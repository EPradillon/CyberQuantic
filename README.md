# R&D Projet N2 - Photon-Scan: 

## <u>1. Les acteurs :</u>
**IMB** vs **GOOGLE** vs **CHINE**

Leader : IBM avec le nouveau **127-qubit Eagle**

## <u>2. "La suprémacie quantique"</u>
Nom donné au point à partir duquel les ordinateurs quantiques peuvent résoudre un problème qu'un ordinateur classique jugerait impossible.

## <u>3. Le Qubit</u>
Chaque Qubit suplémentaire represente un avancée significative en Puissance.

>Contrairement à l'augmentation linéraire des ordinateurs classiques chaque nouveau Qubit double la puissance effective d'un processeur quantique

En pratique : cela signifie qu'actuellement il est plus efficient d'augmenter la puissance d'un processeur que d'en créer un second et cela jusqu'au seuil d'expansion thérorique du millier de Qubit. A partir de ce point un reseau optique de processeurs sera le nouveau chemin pour continuer d'améliorer la puissance de calcul.

## 4 <u>Quantum-Enhanced Capture of Photons Using Optical Ratchet States</u>
*source : The Journal of Physical Chemistry*
___
### 4.1. Le Dispositif
Pour améliorer la consommation d'energie du matériel, les fabricants informatiques ont développés des outils modernes de monitoring. Cette capacité à mesurer les flux energétiques d'une machine introduit une nouvelle faille dans le domaine de la sécurité informatique nommée :"Covert Channels"

> https://en.wikipedia.org/wiki/Covert_channel

Notre attaque s'inspire de cette ouverture. L'objectif est de créer un canal de communication illicite et unidirectionnel entre un espion et une machine cible.

Notre espion est équipé d'un objectif de capture quantique renforcée de photons.
> Un Mecanisme opto-mécanique peut détécter de façon non destructive les signaux d'une large gamme de fréquences.
> 
Il est doté de la capacité de mesurer sans émettre.

Dans notre modèle l'espion peut lire des estimations de consommation d'énergie RAPL (Running Average Power Limit) sur les domaines PP0 (consomation des coeurs) PP1 (consomation des composants graphiques = GPU) et DRAM (Dynamic random-access memory). 
> Sous linux, l'éspion peut utiliser le module "powercap" pour lire la consommation d'énergie fournie par les registres RAPL. (NB: Ceci ne nécessite aucune permission privilégiée)

### 4.2. Fonctionnement
- Dans une première phase le dispositif effectue une de lecture de consommation matérielle de tous les composants.

- Dans la seconde phase de l'attaque la puissance du processeur quantique permet d'interpréter l'enregistrement pour le retransformer en données. 

> L'attaque est possiblement **multi-thread**, ne **communique jamais explicitement** son activité et n'a **jamais besoin d'acceder au réseau.**

<!-- ![Steady-state exciton population](https://pubs.acs.org/na101/home/literatum/publisher/achs/journals/content/jpccck/2017/jpccck.2017.121.issue-38/acs.jpcc.7b07138/20171002/images/medium/jp-2017-07138c_0003.gif) -->

<img src="https://pubs.acs.org/na101/home/literatum/publisher/achs/journals/content/jpccck/2017/jpccck.2017.121.issue-38/acs.jpcc.7b07138/20171002/images/medium/jp-2017-07138c_0003.gif" width="300">

| parameter                   | symbol | default value         |
|-----------------------------|--------|-----------------------|
| atomic transition frequency | ω      | 1.8 eV – 2S           |
| hopping strength            | S      | 0.02 eV               |
| spontaneous emission rate   | γo     | 1.52 × 109 Hz ≡ 1 μeV |
| phonon relaxation rate      | γp     | 103 γo                |
| extraction rate             | γx     | 10–1 γo               |
| photon bath temperature     | To     | 5800 K                |
| phonon bath temperature     | Tp     | 300 K                 |


<!-- ![Absolute power output](https://pubs.acs.org/na101/home/literatum/publisher/achs/journals/content/jpccck/2017/jpccck.2017.121.issue-38/acs.jpcc.7b07138/20171002/images/medium/jp-2017-07138c_0004.gif) -->
<img src="https://pubs.acs.org/na101/home/literatum/publisher/achs/journals/content/jpccck/2017/jpccck.2017.121.issue-38/acs.jpcc.7b07138/20171002/images/medium/jp-2017-07138c_0004.gif" width="300">

> Puissance de sortie absolue
