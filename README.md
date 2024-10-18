# FCSC 2022 Secure Green Server

La société MegaSecure met à disposition un serveur sécurisé permettant de lancer des opérations tout en maîtrisant la consommation énergétique de ce dernier.

Le serveur permet d’exécuter des commandes de manière sécurisée. En effet, il repose sur un composant sécurisé afin de vérifier la signature de toute commande reçue avant de l’exécuter.

Le code Python équivalent à la signature est le suivant :

```python
def sign(self, m):
    return pow(int(sha256(m), 16), self.d, self.N)
```
et la vérification est faite de la manière suivante :
```python
def verif(self, m, s):
    return int(sha256(m), 16) == pow(int(s), self.e, self.N)
```
Néanmoins, étant en phase de test seules deux commandes (```ls -la flag.txt``` et ```cat flag.txt```) sont disponibles. Par ailleurs, il a été remarqué que le serveur présente des comportements étranges dans certaines configurations.


Auteur : Ker

Origine : [Secure Green Server](https://hackropole.fr/fr/challenges/hardware/fcsc2022-hardware-secure-green-server/)


-----------

## Connectez vous en WEBSSH
> http://localhost

#### tentez 
> nc secure-green-server.cyrhades.fr:4000

-----------

## Ou directement avec netcat
> nc localhost:4000


-----------

## Installation manuel
Vous n'utilisez pas l'application **les CTFs de Cyrhades** ? C'est dommage !
Mais voici comment installer ce CTF manuellement :

> git clone https://github.com/Hack-Oeil/fcsc2022-hardware-secure-green-server.git

> cd fcsc2022-hardware-secure-green-server


-----------

## Sur le site officiel hackropole.fr
> https://hackropole.fr/fr/challenges/hardware/fcsc2022-hardware-secure-green-server/