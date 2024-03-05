This is an nginx open-source deployment in the XC virtual kubernetes environment (vk8s) for advanced rewriting of the URL request paths or rewriting of the response body.

The nginx unprivileged image from https://github.com/nginxinc/docker-nginx-unprivileged is used because of the XC RE vk8s deployment limitations as mentioned in https://docs.cloud.f5.com/docs/how-to/app-management/create-vk8s-obj

The the open source nginx can replace some irule functionality in BIG-IP for advanced URL rewrite and response rewrite based on irule with a steam option or Load Balancer with rewrite profile.

For more advanced deployments of nginx for OAUTH or SAML authentication based on Nginx Plus see:

https://github.com/nginxinc/nginx-saml

https://github.com/f5devcentral/terraform-nginx-auth
