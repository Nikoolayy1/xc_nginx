
![image](https://github.com/Nikoolayy1/xc_nginx/assets/23706402/eb65fa64-a4ae-45d0-b6e6-18bc67d50bb0)


This is an nginx open-source deployment in the XC virtual kubernetes environment (vk8s) for advanced rewriting of the URL request paths or rewriting of the response body.

The nginx unprivileged image from https://github.com/nginxinc/docker-nginx-unprivileged is used because of the XC RE vk8s limitations on XC POPs/Regional Edges(RE) as mentioned in https://docs.cloud.f5.com/docs/how-to/app-management/create-vk8s-obj

The the open source nginx can replace some irule functionality in BIG-IP for advanced URL rewrite and response rewrite based on irule with a steam option or Load Balancer with rewrite profile.

For more about the XC Workload Object, see:

https://docs.cloud.f5.com/docs/how-to/app-management/vk8s-workload

For more advanced deployments of nginx for OAUTH or SAML authentication based on Nginx Plus see:

https://github.com/nginxinc/nginx-saml

https://github.com/f5devcentral/terraform-nginx-auth




You will need to modify the default.conf file to lead to your origin server IP address or domain! I have not added a resolver directive in the server object (example 'resolver 100.127.192.10;') as I saw that nginx is using the XC RE kubernetes resolver without an issue :)


![image](https://github.com/Nikoolayy1/xc_nginx/assets/23706402/b28ad50c-2ee8-4f2a-8393-e7d4e378525a)




F5 Devcentral article showing how to install the Nginx container/pod in XC :


https://community.f5.com/kb/communityarticles/f5-xc-vk8s-workload-with-open-source-nginx/328573


