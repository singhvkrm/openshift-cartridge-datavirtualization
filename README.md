## DataVirtualizaton Cartridge for OpenShift

## Summary
This cartridge provides the RedHat JBoss **_DataVirtualization Platform_** for easy deployment to OpenShift. 

The [DataVirtualization Cartridge](https://github.com/mdrillin/openshift-cartridge-datavirtualization) provides the RedHat JBoss **DataVirtualization** components:

  - [Teiid](http://www.jboss.org/teiid/) - Data Virtualization system
  - [Modeshape](http://www.jboss.org/modeshape/) - Content Repository
  - [Dashboard Builder](https://access.redhat.com/site/documentation/en-US/Red_Hat_JBoss_Data_Virtualization/6/html/Administration_and_Configuration_Guide/chap-Dashboard_Builder_Technology_Preview.html) - interactive dashboard and report creation 

## Cartridge Installation
Create your free OpenShift user account - [instructions here](https://openshift.redhat.com/app/getting_started)

Deploy the cartridge via the [OpenShift Web Console](https://openshift.redhat.com/app/console/applications) :

At the bottom of the Applications page (Code Anything section), enter this for 'URL to cartridge definition':

```
https://raw.github.com/mdrillin/openshift-cartridge-datavirtualization/master/metadata/manifest.yml
```
 
Alternately, you can deploy the DataVirtualization cartridge via command line using this command:

```
rhc create-app [MYAPP] https://raw.github.com/mdrillin/openshift-cartridge-datavirtualization/master/metadata/manifest.yml
```

## Getting started with Data Virtualization
After the cartridge finishes deployment, enter this address to verify success

* http://[MYAPP]-[MYDOMAIN].rhcloud.com

### Teiid Data Virtualization
A series of quick starts using JBoss Developer Studio will be published soon to help you get started.

### Modeshape Content Repository
You can access Modeshape at

* http://[MYAPP]-[MYDOMAIN].rhcloud.com/modeshape-webdav

* http://[MYAPP]-[MYDOMAIN].rhcloud.com/modeshape-rest

Two users are provided with the installation for testing

* admin/admin - admin user
* guest/guest - guest user

Consult the [Modeshape Documentation](http://www.jboss.org/modeshape/) for more information.

### Dashboard Builder
Access the dashboard builder at the following address

* http://[MYAPP]-[MYDOMAIN].rhcloud.com/dashboard

Two users are provided with the installation for testing

* dbadmin/dbadmin - dashboard admin user with edit capability
* dbuser/dbuser - dashboard user with readonly capability

More information regarding Dashboard Builder will be coming soon.




