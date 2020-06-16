
First run this to extecute dhcp daemon (Assuming multus is already installed)

kubectl -f https://github.com/aneeshkp/reference-deployment/blob/dhcp-daemon/multus-dhcp/dhcp-daemonset.yml

#building dhcp server (if required to make any changes to dnsmasq)
cd dhcp

podman build -t repo/imagename:latest .

podman push repo/imagename:latest



