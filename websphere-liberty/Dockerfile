FROM websphere-liberty:webProfile8
RUN chgrp -R 0 /opt/ibm/wlp/usr/servers/defaultServer/dropins && chmod -R g=u /opt/ibm/wlp/usr/servers/defaultServer/dropins
RUN chgrp -R 0 /opt/ibm/wlp/output/defaultServer/workarea && chmod -R g=u /opt/ibm/wlp/output/defaultServer/workarea
# Add binary deployment artifact to 'dropins' folder
#RUN wget --directory-prefix=/opt/ibm/wlp/usr/servers/defaultServer/dropins/ $BINARY_DEPLOYMENT_ARTIFACT_URL
COPY app/* /config/dropins/

##RUN chmod a+rwx /opt/ibm/wlp/output/defaultServer

# IBM WebSphere Liberty license must be accepted
ENV LICENSE $LICENSE
