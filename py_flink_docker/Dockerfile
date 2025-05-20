FROM flink:2.0.0


# install python3 and pip3
RUN apt-get update -y && \
apt-get install -y python3 python3-pip python3-dev && rm -rf /var/lib/apt/lists/*
RUN ln -s /usr/bin/python3 /usr/bin/python

RUN apt-get update
RUN apt install software-properties-common -y
RUN add-apt-repository ppa:openjdk-r/ppa
RUN apt install openjdk-17-jdk -y
RUN ls /usr/lib/jvm/
ENV JAVA_HOME=/usr/lib/jvm/java-17-openjdk-arm64

# install PyFlink
RUN pip3 install apache-flink==2.0.0