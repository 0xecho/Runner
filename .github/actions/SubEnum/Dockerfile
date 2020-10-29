FROM golang:latest

# Install python-pip
RUN apt-get update && apt-get install -y python3 python-pip

RUN go get github.com/Emoe/kxss
RUN go get -u github.com/hahwul/dalfox
RUN go get -u github.com/tomnomnom/qsreplace
RUN go get github.com/tomnomnom/waybackurls
RUN mkdir /all
RUN git clone https://github.com/0xecho/photon /all/photon

COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
ENTRYPOINT ["bash","/entrypoint.sh"]
