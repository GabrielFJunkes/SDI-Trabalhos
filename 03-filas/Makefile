# GNU Makefile
JAR=/usr/local/jdk1.8.0_131/bin/jar
JAVA=/usr/local/jdk1.8.0_131/bin/java
JAVAC=/usr/local/jdk1.8.0_131/bin/javac
CP=.:/usr/local/rabbitmq-jar/amqp-client-4.0.2.jar:/usr/local/rabbitmq-jar/slf4j-api-1.7.21.jar:/usr/local/rabbitmq-jar/slf4j-simple-1.7.22.jar

JFLAGS = -g -cp $(CP)
.SUFFIXES: .java .class
.java.class:
	$(JAVAC) $(JFLAGS) $*.java

CLASSES = \
	client/Client.java\
	server/Server.java\
	server/RunServer.java\
	utils/Logger.java\

default: classes
	@echo "############### #################### ###############"
	@echo "############### #################### ###############"
	@echo "Para executar, copie no terminal: "
	@echo "java -cp $(CP) client/Client"
	@echo " "
	@echo "java -cp $(CP) server/RunServer"
	@echo "############### #################### ###############"

classes: $(CLASSES:.java=.class)

clean:
	rm -f *.class 
