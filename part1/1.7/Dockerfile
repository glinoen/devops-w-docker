FROM ubuntu:16.04

WORKDIR /mydockdir
RUN apt-get update && apt-get install -y curl

COPY scriptfile.sh .
CMD ["bash", "./scriptfile.sh"]

