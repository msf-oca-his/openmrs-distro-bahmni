FROM bahmni/openmrs:1.0.0

# Remove omods
RUN rm -f ${OPENMRS_APPLICATION_DATA_DIRECTORY}/modules/patientidentifiergenerator-*.omod

# Copy omods
COPY target/patientidentifiergenerator-*.omod ${OPENMRS_APPLICATION_DATA_DIRECTORY}/modules

#Create directories if not present
RUN mkdir -p /home/bahmni/document_images
RUN mkdir -p /home/bahmni/uploaded_results
RUN mkdir -p /home/bahmni/uploaded-files

#Copy our startup script
COPY package/docker/openmrs/bahmni_startup.sh /openmrs/
RUN chmod +x /openmrs/bahmni_startup.sh
