FROM node:8.11.3-alpine

ARG angularprojectname
RUN mkdir /mnt/$angularprojectname \
    && mkdir /mnt/$angularprojectname/node_modules \
    && chown -R node:node /mnt/$angularprojectname/node_modules
VOLUME ["/mnt", "/mnt/$angularprojectname/node_modules"]

USER node

RUN mkdir /home/node/.npm-global
ENV PATH=/home/node/.npm-global/bin:$PATH
ENV NPM_CONFIG_PREFIX=/home/node/.npm-global
ENV ANGULARPROJECTNAME=$angularprojectname

RUN npm install -g @angular/cli && npm cache clean --force

WORKDIR /mnt

ENTRYPOINT ["sh"]
