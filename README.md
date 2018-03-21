# BackupRegistry
Backup the NiFi Registry

import nipyapi
nipyapi.config.nifi_config.host = 'http://server:9090/nifi-api' 
nipyapi.config.registry_config.host = 'http://server:61080/nifi-registry-api' 
identifier = 'nipyapi_console_process_group_0' 
process_group = nipyapi.canvas.get_process_group(identifier, identifier_type='name') 
print(nipyapi.canvas.get_variable_registry(process_group, ancestors=True))


https://community.hortonworks.com/articles/177301/big-data-devops-apache-nifi-flow-versioning-and-au.html


Export a Template As a String

t_id='21e95277-98ae-38ce-9235-bbf90772cef3' 
print(nipyapi.templates.export_template(t_id, output='string'))
