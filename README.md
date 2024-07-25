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

JSON Content to implement block 
{
    "metadata": {
      "name": "test-waf",
      "namespace": "k-baum"
    },
  "spec": {
    "allow_all_response_codes": null,
    "blocking": {},
    "bot_protection_setting": {
        "good_bot_action": "REPORT",
        "malicious_bot_action": "BLOCK",
        "suspicious_bot_action": "BLOCK"
    },
    "default_attack_type_settings": {
        "only_high_accuracy_signatures": {}
      },
      "stage_new_and_updated_signatures": {
        "staging_period": 0
      },
      "stage_new_signatures": {
        "staging_period": 0
      },
      "violation_settings": {
        "disabled_violation_types": [
          "VIOL_NONE"
        ]
      },
    "disable_anonymization": {},
    "use_default_blocking_page": {}
  }
}








