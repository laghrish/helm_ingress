## Contenu
Ce projet contient les fichiers Helm pour déployer un Ingress afin d'exposer les APIs Clients, Produits et Commandes.

## Déploiement

1. Activer l'addon Ingress sur Minikube :
   ```bash
   minikube addons enable ingress
   ```

2. Installer l'Ingress avec Helm :
   ```bash
   helm install mspr-ingress .
   ```

3. Tester l'accès aux APIs :

   - Se connecter à Minikube en SSH :
     ```bash
     minikube ssh
     ```

   - Utiliser curl pour tester l'accès :
     ```bash
     curl http://192.168.49.2/clients/docs
     curl http://192.168.49.2/products/docs
     curl http://192.168.49.2/orders/docs
     ```

## Informations complémentaires
- L'Ingress utilise l'adresse IP de Minikube (`192.168.49.2`).
- Il n'est pas nécessaire de modifier le fichier hosts.
- Les chemins sont configurés pour accéder directement aux différentes APIs.
```
