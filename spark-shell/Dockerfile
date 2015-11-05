FROM ubuntu:14.04.1

RUN apt-get -y update && apt-get install -y wget

RUN wget http://www.apache.org/dyn/closer.lua/spark/spark-1.5.1/spark-1.5.1-bin-hadoop2.6.tgz /var/tmp/spark.tgz

RUN apt-get -y remove wget

RUN mkdir -p /usr/local/spark

RUN tar -xfz /var/tmp/spark.tgz /usr/local/spark

CMD /usr/local/spark/bin/spark-shell
