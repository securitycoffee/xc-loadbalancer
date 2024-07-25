# xc-loadbalancer
Some basic API calls "API Cheatsheet" for F5 Distributed Cloud Services for basic functions

You can use Postman or VSCode Thunder client to call the API of XC

Call a load balancer on a namespace 
GET  https://f5-amer-ent.console.ves.volterra.io/api/config/namespaces/k-baum/http_loadbalancers/appsechero1-lb

List all HTTP Load balancers in namespace 
GET  https://f5-amer-ent.console.ves.volterra.io/api/config/namespaces/k-baum/http_loadbalancers

List Service Policies in a namespace 
GET  https://f5-amer-ent.console.ves.volterra.io/api/config/namespaces/k-baum/service_policys

Modify Service Policies
POST https://f5-amer-ent.console.ves.volterra.io/api/config/namespaces/k-baum/service_policys

List all WAFs in namespace 
GET  https://f5-amer-ent.console.ves.volterra.io/api/config/namespaces/k-baum/app_firewalls

Delete a WAF 
DELETE  https://f5-amer-ent.console.ves.volterra.io/api/config/namespaces/k-baum/app_firewalls/appsechero98-waf

Change settings in a WAF policy 
PUT  https://f5-amer-ent.console.ves.volterra.io/api/config/namespaces/k-baum/app_firewalls/appsechero96-blocking

Create a WAF policy 
POST  https://f5-amer-ent.console.ves.volterra.io/api/config/namespaces/k-baum/app_firewalls


List a single WAF policy 
GET  https://f5-amer-ent.console.ves.volterra.io/api/config/namespaces/k-baum/app_firewalls/test-waf

Modify WAF policy to blocking 
PUT  https://f5-amer-ent.console.ves.volterra.io/api/config/namespaces/k-baum/app_firewalls/test-waf










