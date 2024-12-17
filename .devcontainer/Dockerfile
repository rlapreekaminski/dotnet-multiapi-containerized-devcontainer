# Utilise l'image officielle .NET 9 SDK
FROM mcr.microsoft.com/devcontainers/dotnet:dev-9.0   

# Configure le répertoire de travail
WORKDIR /workspace

# Installe le client Docker pour utiliser Docker depuis le conteneur
RUN apt-get update && apt-get install -y docker.io

# Installe le client Docker Compose pour utiliser Docker Compose depuis le conteneur
RUN apt-get update && apt-get install -y curl jq \
  && curl -L "https://github.com/docker/compose/releases/download/$(curl -s https://api.github.com/repos/docker/compose/releases/latest | jq -r .tag_name)/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose \
  && chmod +x /usr/local/bin/docker-compose

# Ajoutez cet utilisateur au groupe 'docker'
RUN usermod -aG docker vscode

# Installe le débogueur .NET (vsdbg)
RUN curl -sSL https://aka.ms/getvsdbgsh | bash /dev/stdin -v latest -l /vsdbg

# Nettoyage
RUN apt-get clean && rm -rf /var/lib/apt/lists/*

# Expose les ports pour les .NET Minimal API (HTTP)
EXPOSE 5136 5137

# Définit le point d'entrée par défaut
CMD ["sleep", "infinity"]
