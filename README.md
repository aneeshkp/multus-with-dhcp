
First run this to extecute dhcp daemon (Assuming multus is already installed)

kubectl create -f https://raw.githubusercontent.com/aneeshkp/reference-deployment/dhcp-daemon/multus-dhcp/dhcp-daemonset.yml

#building dhcp server (if required to make any changes to dnsmasq)
cd dhcp

podman build -t repo/imagename:latest .

podman push repo/imagename:latest



