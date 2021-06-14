FROM mcr.microsoft.com/powershell

# Create variables
ARG VERSION = 1.17.0.03
ENV VERSION = ${VERSION}

# Create server folder
RUN mkdir server

# Move workspace into server folder
WORKDIR /server

# Dowload Bedrock dedicated server
RUN Invoke-WebRequest -Uri https://minecraft.azureedge.net/bin-win/bedrock-server-${VERSION}.zip -OutFile bedrock-server.zip

# Unzip the folder
RUN Expand-Archive -LiteralPath bedrock-server.zip -DestinationPath bedrock-server

# Remove the zip folder
RUN del bedrock-server.zip

# Move workspace into bedrock-server
WORKDIR /bedrock-server

CMD [ "bedrock_server.exe" ]