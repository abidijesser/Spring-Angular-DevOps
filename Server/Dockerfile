# Étape 1 : Utiliser une image Java 17
FROM openjdk:17-jdk-slim

# Étape 2 : Définir le répertoire de travail dans le conteneur
WORKDIR /app

# Étape 3 : Créer le dossier de logs
RUN mkdir -p logs

# Étape 4 : Copier le fichier JAR généré dans le dossier target
COPY target/*.jar app.jar

# Étape 5 : Exposer le port 8089 (port défini dans application.properties)
EXPOSE 8089

# Étape 6 : Commande pour exécuter l'application Spring Boot
ENTRYPOINT ["java", "-Dspring.profiles.active=prod", "-jar", "app.jar"]
