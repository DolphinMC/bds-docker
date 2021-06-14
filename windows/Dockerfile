FROM 

WORKDIR /tmp

# Dowload Bedrock dedicated server
ARG version = 1.17.0.03
ADD https://minecraft.azureedge.net/bin-win/bedrock-server-${version}.zip bds.zip

ENTRYPOINT [ "../entrypoint.sh" ]