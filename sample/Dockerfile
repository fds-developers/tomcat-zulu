FROM fds/tomcat:9-zuluopenjdk11
WORKDIR $CATALINA_HOME

# Optimization - cleanup unrequired files
RUN rm -rf $CATALINA_HOME/webapps/docs $CATALINA_HOME/webapps/examples $CATALINA_HOME/webapps/host-manager $CATALINA_HOME/webapps/manager $CATALINA_HOME/webapps/ROOT

COPY ROOT/index.html $CATALINA_HOME/webapps/ROOT/

###
### SECURITY

RUN groupadd -g 1000 user \
   && useradd -u 1000 -g 1000 -m -s /bin/bash user \
   && chown -R 1000 /usr/local/tomcat
USER user

EXPOSE 8080
CMD ["catalina.sh", "run"]
