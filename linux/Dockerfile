FROM buildpack-deps:curl

# Create variables
ARG VERSION = 1.17.0.03
ENV VERSION = ${VERSION}

# Install unzip
RUN apt-get update && apt-get install -y --no-install-recommends \unzip \&& apt-get clean

# Create server folder
RUN mkdir server

# Move workspace into server folder
WORKDIR /server

# Dowload Bedrock dedicated server
RUN curl --fail https://minecraft.azureedge.net/bin-linux/bedrock-server-${VERSION}.zip --output bedrock-server.zip

# Unzip the folder
RUN unzip bedrock-server.zip

# Remove the zip folder
RUN rm --force bedrock-server.zip

# Move workspace into bedrock-server
WORKDIR /bedrock-server

CMD [ "bedrock_server" ]