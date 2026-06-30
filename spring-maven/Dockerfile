FROM eclipse-temurin:17-jre

# Création d'un utilisateur non privilégié
RUN addgroup --system spring && adduser --system --ingroup spring spring

WORKDIR /app
COPY target/*.jar app.jar

# Bascule vers l'utilisateur non-root
USER spring

EXPOSE 8080
ENTRYPOINT ["java","-jar","app.jar"]