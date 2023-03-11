FROM azul/zulu-openjdk:17

RUN apt update && apt install -y screen
RUN useradd -s /bin/bash -m  minecraft
RUN mkdir -p /opt/minecraft 

COPY spigot-1.19.3.jar /home/minecraft/
COPY startup.sh /home/minecraft/

RUN chown -R minecraft:minecraft /home/minecraft /opt/minecraft

USER minecraft

WORKDIR /home/minecraft

EXPOSE 25565

ENTRYPOINT [ "/home/minecraft/startup.sh" ]