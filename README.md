# mesosphere_openstack_heat
Heat templates to deploy mesosphere cluster (3masters,3slaves) to openstack

## Requirements
Openstack with heat support
Openstack commandline client http://docs.openstack.org/user-guide/common/cli-install-openstack-command-line-clients.html
Openstack ubuntu trysty image

## Usage
Copy repository to your local drive and cd to copied repository
Mesos cluster can be launched via :
`$openstack stack create -t mesos.yaml -f yaml --parameter "__parameter1__=__your_parameter__;__parameter3_=__your_parameter2__" mesos_masters`

### Parameters 
Template requires several parameters - defaults probably wont match your openstack settings
* image - ubunty 14.04 trusty image is required (http://cloud-images.ubuntu.com/trusty/)
* flavor - default m1.small should be enough for small tests
* key_name - your ssh keyname registered in openstack
* private_network - predefined private network with assignable ip addresses
* public_network - floating ip network

