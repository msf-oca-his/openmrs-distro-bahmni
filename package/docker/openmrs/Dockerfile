FROM bahmni/openmrs:1.0.0

# Remove omods
RUN rm -f ${OPENMRS_APPLICATION_DATA_DIRECTORY}/modules/patientidentifiergenerator-*.omod

# Copy omods
COPY target/patientidentifiergenerator-*.omod ${OPENMRS_APPLICATION_DATA_DIRECTORY}/modules
