FROM gameflow625/voip-server-def:def


WORKDIR /server-context


ENV DEBIAN_FRONTEND=noninteractive

ENV GODOT_VERSION "3.3.4"

RUN wget https://downloads.tuxfamily.org/godotengine/${GODOT_VERSION}/Godot_v${GODOT_VERSION}-stable_x11.64.zip \ 
    && unzip Godot_v${GODOT_VERSION}-stable_x11.64.zip \
    && mv Godot_v${GODOT_VERSION}-stable_x11.64 /usr/local/bin/godot-engine \
    && rm -f  Godot_v${GODOT_VERSION}-stable_x11.64.zip



ADD client.x86_64 .
ADD client.pck .


EXPOSE 4321



CMD [ "godot", "client", "--main-pack", "client.pck"]



