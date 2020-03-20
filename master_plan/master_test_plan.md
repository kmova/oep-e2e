## Test Plan Template:

Director OnPrem

## TABLE OF CONTENTS

### 1.0 INTRODUCTION

### 2.0	OBJECTIVES AND TASKS 

#### 2.1	Objectives 
#### 2.2	Tasks 

### 3.0 SCOPE

### 4.0	Testing Strategy 

#### 4.1	Sanity Testing  
#### 4.2	Performance and Stress Testing 
#### 4.3	Compatibilty Testing
#### 4.4	Regression Testing 
#### 4.5	API integration Testing

### 5.0 Test Schedule

### 6.0 Features to Be Tested

### 7.0 Features Not to Be Tested
 
### 9.0 Resources/Roles & Responsibilities

### 10.0 Schedules

### 11.0 Significantly Impacted Departments (SIDs)

### 12.0 Dependencies

### 13.0 Risks/Assumptions

### 14.0 Tools

### 15.0	Approvals 


### 1.0 Introduction:
DirectorOnline, as well as Director OnPrem, helps us quickly view multi-cloud Kubernetes resources from a single console, helps in troubleshooting, monitoring stateful applications, access logs of applications at a central location, take a backup of applications, etc.
So, the features are the same for both Online as well as On-Premise version the only difference lies in the administration.

### 2.0 Objectives and tasks

#### 2.1 Objectives:
The objective should be to cover all the areas of DOP testing such as Authentication, Installation, cluster connect etc. 

#### 2.2 Tasks:
a. Test the DOP product(features and functionality) on every release.              
b. DOP testing should be done using E2E automation.                    
c. Manual testing will be require if E2E is not covered for any specfic feature or functionality.           
d. Once testing is done file issues for the bug.                                        
e. Set priority level for bug fixes for next release.    

### 3.0 Scope:

#### General:
There are different features and functionality of DOP that needed to be tested. Listing them below.
a. Authentication.                        
b. Browser                          
c. Profile                                         
d. connect cluster                                                                      
e. Dashboard                                                                                 
f. Scope                                         
e. Metrics                                                          
f. Alerts                                                  
g. Dmaas                                                    
h. Teaming                                                       
i. upgrade                                                                          
j. OpenEBS installation                                             
k. DOP upgrade
etc

#### List of items that will not be tested.                                          
a. The IOPS,thorughput,latency etc values that are shown in graphs are not tested means the values shown in graph is right or wrong.    
b. Exact error in the logs are not tested. We are not veryfing that whether we are getting exact logs with correct timestamp.
c. Cross-cloud-monitoring graphs values are not verified.

#### Tactics:
a.To get the build from Director team.                                                    
b. Install DOP on any cluster.                                                                     
c. Verify the installation part automated/manually.                                       
d. Verify the different features and functionality manually for the onces which had not been automated.             
e. End Goal is to have to e2e pipeline running for the new features and later on cover the existing features in E2E pipeline.

### 4.0 Testing statergy:
a. To verify the DOP installation should be smooth across different OnPrem clusters such as Kubeadm,konvoy, Rancher, Openshift etc.   
b. For installation of DOP cstor storage class should be used for the pvc(mysql,cassandra,elasticsearch,grafana and mayastore)        
c. After installation of DOP UI should be accessible.                              
d. Verify the authentication functionality of DOP. The Main focus area should be Local authentication.                             
e. Verify that UI should be accessible in chrome,firefox and safari.                                           
f. Verify that self connected cluster are shown in Administrator account.                                                   
g. Verify the cluster connect and disconnect functionality.                                                          
h. Verify all the dashboards are showing the graphs or data.                                        
i. Metrics are shown for volumes and pools.                                                        
j. Alerts are getting generated at cluster level.                                                          
k. Verify the teaming functionality.                                                                                             
l. Verify the dmaas functionality. Cover all the 3 providers (GCP,AWS and Minio)                                   
m. verify the OpenEBS installation functionality.                                                               
n. Verify the OpenEBS upgrade functionality.          

#### 4.1 Sanity Testing
a. DOP installation should be smooth. All the required images should be present in mayadata.
b. Signup and signin should happen for local Auth.
c. Cluster connect/disconnect check.
d. All the links should be working fine.
e. All the dashboards should show respectives info.


#### 4.2 Performance and stress testing:
a. Login to DOP from 500 browsers sessions.                                     
b. Connect clusters having 200 nodes.             
c. Connected cluster should have more than 50 Applications.                  

#### 4.3 Compatibilty testing:                 
a. Browsers(Chrome,firefox,safari).                                   
b. Platforms(Rancher,Kubeadm,kubespray,Konvoy,Openshit, etc).                               
c. Operating system(ubuntu 16.04 and other versions, Centos7.x,RancherOS, MicroOS, etc).
d. Different platform and operating system versions should also be considered.

#### 4.4	Regression Testing:

To make sure all the features which was working in previous release should not break with the intorduction of new features in new release.

#### 4.5 API Intergration testing.
TO DO

### 5.0 Test schedule.
OpenEBS control plane upgrade- 1.9                       
cstor pool provisioning - 1.9                                                                
Extend E2E to konvoy - 1.9                                                              
Extend E2E to Rancher - 1.9                                                          
Selinium based automation(for couple of TCs) - 1.9

### 6.0 Features to be tested:
a. OpenEBS installation basic and Advance.                
b. Teaming.                                                  
c. Dmaas.                                                           
d. OpenEBS upgrade.                                                                       
f. Control Plane upgrade.                                                           

### 7.0 Features not to be tested:
a. AD authentication.                                                                          
   Reason: We don't have configure AD server in cloud.                 
   
   
































 




























