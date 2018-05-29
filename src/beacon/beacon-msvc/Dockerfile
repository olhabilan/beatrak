FROM beatrak/node-base

ENV PS1="[beatrak/beacon]# "

RUN mkdir -p /root/app
RUN mkdir -p /root/common
RUN mkdir -p /root/keys
RUN mkdir -p /root/protos

ADD ./app /root/app
ADD ./common /root/common
ADD ./keys /root/keys
ADD ./protos /root/protos

WORKDIR /root/common
RUN npm install

WORKDIR /root/app
RUN npm install

EXPOSE 8080

CMD ["npm", "start"]



