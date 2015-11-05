FROM ubuntu:14.04.1

RUN apt-get -y update && apt-get install -y wget

RUN wget http://apache.mirror.gtcomm.net/spark/spark-1.5.1/spark-1.5.1-bin-hadoop2.6.tgz -O /var/tmp/spark.tgz

RUN apt-get -y remove wget

RUN mkdir -p /usr/local/spark

RUN tar -xzf /var/tmp/spark.tgz -C /usr/local/spark

RUN rm /var/tmp/spark.tgz

RUN apt-get install -y default-jre

CMD /usr/local/spark/spark-1.5.1-bin-hadoop2.6/bin/spark-shell
