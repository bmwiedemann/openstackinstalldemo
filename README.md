This repo contains files and instructions needed to install your own demo cloud

##Prerequisites

- A Machine with
  - RAM (16GB)
  - HDD (100GB)
- Have repositories and other data synced via `syncdata` script

## Pointers

- https://github.com/bmwiedemann/openstackinstalldemo - this repo
- https://github.com/SUSE-Cloud/automation/blob/master/scripts/jenkins/qa_openstack.sh
- https://github.com/SUSE-Cloud/automation/blob/jenkins/scripts/jenkins/ci.opensuse.org/openstack-cleanvm.xml#L152
- https://build.opensuse.org/project/show/Cloud:OpenStack:Newton


## Finally
cd libvirt/ && setupVM
ssh cleanvm "
    export mirror=http://192.168.23.1/images
    export cloudsource=openstacknewton
    bash -x qa_openstack.sh
"
