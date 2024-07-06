**Issue**
Newly created .NET Core API returns empty response with 200 status code
**Reason**
The class or model thats being returned should have properties all as public in order for the JSONSerialiser to see and serialise the properties

