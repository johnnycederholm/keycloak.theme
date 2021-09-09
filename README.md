```powershell
docker run -d --name keycloak -p 10001:8080 `
--mount type=bind,source=$(PWD)/theme,target=/opt/jboss/keycloak/themes/customtheme `
--mount type=bind,source=$(PWD)/standalone-ha.xml,target=/opt/jboss/keycloak/standalone/configuration/standalone-ha.xml `
-e KEYCLOAK_USER=admin `
-e KEYCLOAK_PASSWORD=admin `
jboss/keycloak:15.0.0
```