# jenkins-openshift-setup

## Requirements
1. Jenkins 2.x environment <br>
2. OpenShift Container Platform 3.3+  <br>
3. Web Port (8080 by default)

## Plugins
1. OpenShift Client <br>
2. OpenShift Sync <br>
3. OpenShift Login <br>

## Jenkins Global Tool Configuration
1. Manage Jenkins -> Global Tool Configuration <br>
2. Add OpenShift Client Tools <br>
3. Click on "Add OpenShift Client Tools"

<li>Name : oc </li>
<li>Install automatically : checked</li>
<li>Click on "Add OpenShift Client Tools</li>
<li>Choose "Extract *.zip/*.tar.gz"</li>
<li>Label : empty</li>
<li>Download URL for binary archive <br> https://mirror.openshift.com/pub/openshift-v4/clients/oc/latest/linux/oc.tar.gz </li>
<li>Subdirectory of extracted archive : Leave empty</li>
<li>Click Apply </li>
  
## JDK Installations
<li>Click on "Add JDK"</li>
<li>Name : jdk11</li>
<li>Install Automatically : uncheck</li>
<li>JAVA_HOME : /path/openjdk-11-rhel7</li>
<li>Click Apply</li>
  
## Maven Installations
<li>Click on "Add Maven" </li>
<li>Name : maven-3.8.5</li>
<li>Install automatically : checked </li>
<li>Install from Apache Version : 3.8.5</li>
<li>Click Apply & Save</li>

## Configure OpenShift Cluster Details
 <li> Manage Jenkins -> Configure System </li>
 <li> OpenShift Client Plugin </li>
 <li> Click on "Add OpenShift Cluster"</li>
 <li> Cluster Name : ocp4</li>
 <li> API URL : custer api details </li>
 <li> Disable TLS Verify : checked </li>
 <li> Credentials : Click on "Add" </li>
 <li> Kind : "OpenShift Token for OpenShift Client Plugin" </li>
 <li> ID : token-name
 <li> Click "Add" </li>
 <li> Credentials : token-name </li>
 <li> Click on Apply & Save </li>
