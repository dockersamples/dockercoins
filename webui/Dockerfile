FROM node:4-slim@sha256:b5ae41b735cad519ae32cd6eeafbc1191c2d8e9056baf421a17f1c666c2a3753
RUN npm install express && npm install redis
#AUNQUE SE PUSIERA JUNTO ESTARIAN EN DIFERENTES CAPAS (diferentes rutas no empeoran el rendimiento, la misma ya penaliza mas)
#si en la misma linea creas y borras archivos tambien es optimo (la capa se guarda al final) 
COPY files/ /files/
COPY webui.js /
ENTRYPOINT ["node"]
CMD ["webui.js"]
EXPOSE 8080
