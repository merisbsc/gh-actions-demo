FROM openjdk:16

RUN mkdir /deployments
COPY ./demo.jar /deployments/
#COPY ./deployments/lib/* /deployments/lib/
COPY scripts/* /deployments/
RUN sed -e 's/\r$//' -i /deployments/.sh && chmod +x /deployments/.sh

EXPOSE 8080
WORKDIR /deployments
ENTRYPOINT ["./run.sh"]
