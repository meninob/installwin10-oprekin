# installwin10-oprekin
Installing minikube &amp; K8s in windows 10, with a Oprekin win light distro

So, after researching on the Laptop I have, I bought this M.2 2242 SSD drive for 3 quid at CEX in Stratford UK, and then installed it, and it works quite fast, but what could I do with just 16gb ssd drive?
Initially I thought of installing a linux distro on it, but I already have linux mint on it, so whats the point in having 2 linux distro's on one laptop.
So thought of windows, but windows needs more than 16gn ram, and after reasearching, found superlite windows 10, and Oprekin Windows 10. tried superlite, but had issues on space.
Tried Oprekin, and works quite fast, wthout all the features, but required features are there - powershell, windows, and the basics. + is superfast.



---- to update above with more info

----- to get minikube to install on another drive, add a variable in systerm
start-> run-> sysdm.cpl -? Advanced tab -> [Environment Variables] -> {User Variables for <user> -> [New]
  variable name: MINIKUBE_HOME
  Variable value: e:\minikube
  
  make sure to create a .minikube folder in the e:\minikube directory.
  
  -----------------------------------------
  PS E:\minikube> .\minikube.exe start
* minikube v1.29.0 on Microsoft Windows 10 Pro 10.0.18363.753 Build 18363.753
  - MINIKUBE_HOME=e:\minikube\
* Automatically selected the virtualbox driver
* Downloading VM boot image ...
    > minikube-v1.29.0-amd64.iso....:  65 B / 65 B [---------] 100.00% ? p/s 0s
    > minikube-v1.29.0-amd64.iso:  276.35 MiB / 276.35 MiB  100.00% 1.62 MiB p/
* Starting control plane node minikube in cluster minikube
* Downloading Kubernetes v1.26.1 preload ...
    > preloaded-images-k8s-v18-v1...:  397.05 MiB / 397.05 MiB  100.00% 1.40 Mi
* Creating virtualbox VM (CPUs=2, Memory=2200MB, Disk=20000MB) ...
! This VM is having trouble accessing https://registry.k8s.io
* To pull new external images, you may need to configure a proxy: https://minikube.sigs.k8s.io/docs/reference/networking/proxy/
* Preparing Kubernetes v1.26.1 on Docker 20.10.23 ...
  - Generating certificates and keys ...
  - Booting up control plane ...
  - Configuring RBAC rules ...
* Configuring bridge CNI (Container Networking Interface) ...
  - Using image gcr.io/k8s-minikube/storage-provisioner:v5
* Enabled addons: default-storageclass
* Verifying Kubernetes components...
* kubectl not found. If you need it, try: 'minikube kubectl -- get pods -A'
* Done! kubectl is now configured to use "minikube" cluster and "default" namespace by default
  ---------------------------------------------------------------------------
  
