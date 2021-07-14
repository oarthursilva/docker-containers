FROM afuscella/opensuse:jre8u181

# scc Version
ENV SCC_VERSION_MAJOR 2
ENV SCC_VERSION_MINOR 13
ENV SCC_VERSION_BUILD 1

# create folder for scc
RUN mkdir -p /tmp/scc

# download and unarchive the SAP Cloud Connector
RUN wget --no-check-certificate \
	--header "Cookie: eula_3_1_agreed=tools.hana.ondemand.com/developer-license-3_1.txt" \
	"https://tools.hana.ondemand.com/additional/sapcc-${SCC_VERSION_MAJOR}.${SCC_VERSION_MINOR}.${SCC_VERSION_BUILD}-linux-x64.zip" \
	-O /tmp/scc/sapscc.zip &&\
	unzip /tmp/scc/sapscc.zip -d /tmp/scc &&\
	rm /tmp/scc/*.zip

# delete unused files
RUN rpm -ivf /tmp/scc/*.rpm
RUN rm /tmp/scc/*.rpm

USER sccadmin

WORKDIR /opt/sap/scc

# expose ports
EXPOSE 3000 8000 443 8443

ENTRYPOINT ["/opt/sap/scc/go.sh"]
