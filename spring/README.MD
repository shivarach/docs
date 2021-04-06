* How to add cutom(eg: enum type in postgres)in `MapSqlParameterSource`
```
var queryParameters = MapSqlParameterSource()
queryParameters.addValue("organization_id", organizationId) //normal value
queryParameters.addValue("role", Role.BRAND.name, java.sql.Types.OTHER) //cutom type
