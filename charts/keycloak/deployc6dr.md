When logged into the DR cluster, run these.


```
helm upgrade --install "sso-keycloak" ./sso-keycloak-1.14.4.tgz \
-n c6af30-dev --version 1.14.4 -f "./values.yaml" \
-f "./values-golddr-c6af30-dev-active.yaml"
```

```
helm upgrade --install "sso-keycloak" ./sso-keycloak-1.14.4.tgz \
-n c6af30-test --version 1.14.4 -f "./values.yaml" \
-f "./values-golddr-c6af30-test-active.yaml"
```

```
helm upgrade --install "sso-keycloak" ./sso-keycloak-1.14.4.tgz \
-n c6af30-prod --version 1.14.4 -f "./values.yaml" \
-f "./values-golddr-c6af30-prod-active.yaml"
```

Postgres 15 needs the extra command
```
psql
\c ssokeycloak
GRANT ALL ON SCHEMA public TO ssokeycloak;
```

To navigate to the page, take the generated route and and `\auth` to it.
