FROM golang:latest

# Install python-pip
# RUN find /github
RUN apt-get update && apt-get install -y python3 python3-pip
RUN git clone https://github.com/0xecho/photon /all/photon
RUN pip3 install -r /all/photon/requirements.txt
RUN git clone https://github.com/0xecho/Arjun /all/Arjun
RUN go get github.com/Emoe/kxss
RUN go get -u github.com/tomnomnom/qsreplace
RUN go get github.com/tomnomnom/waybackurls
RUN go get -u github.com/jaeles-project/gospider
RUN go get -u github.com/tomnomnom/httprobe
RUN git clone https://github.com/hahwul/dalfox
RUN cd dalfox && go install && go build

COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
ENTRYPOINT ["bash","/entrypoint.sh"]
