## User Signup and Contact Management w/2FA for OpenStack Multi-Tenant Cloud

### What and why?

I am currently working on launching a 'lite' cloud services startup in Asia, leveraging components of OpenStack to provide compute, block and object storage, load balancing, image backups/restoration, firewall, DBaaS, one-click depoyable open source apps via ansible & airflow, and several other services. The service will soft launch in Jakarta and Singapore in May to closed customers. The user/contact management system currently does not exist and will need to be created.

### For whom?

The user management system will be used for customers of the cloud service. This will be an actual project that will be deployed into production.

### Collaboration

This is a very timely project and within reasonable scope to be completed by 1-2 students in 10 weeks. I would prefer to do this project on my own as it is within my ability to complete it and I have to do it anyways. If there would be another student assigned, the student will need to sign an NDA.

### How and Scope

The user management system must cover these minimum functionalities.

1.  Allow users to sign up and modify and update their password and billing and contact information (including email and phone numbers)

2.  2FA capability (acutally it will be mandatory) upon login, via either email or SMS

3.  Password/account reset functionality

Additional Functionalities if Time Permits:

4.  Capability for users with admin access (the first to sign up would be defaulted as admin) on their own company accounts to create and manage additional users and assign them roles (such as admin, or basic user) within the confines of their company account cloud resources assigned. I.e. an admin panel for customers to manage their own users.

5.  Backend admin panel for the customer service/the company to manage all users

### Additional information

- We will deploy OpenID Connect and Keycloak to provide core logic out of box for identity access/management and for interfacing with our core cloud public API services that will then interact with openstack system user to grant customer access to specific task/roles
  i.e. we will be creating all control panels, UI, and database (and the logic) that stores contact info, but the auth piece against cloud service will be proxied by Keycloak and our cloud's public API
- We will leverage either opensource or a commercial product to provide 2FA. Currently looking at Twilio's Authy
