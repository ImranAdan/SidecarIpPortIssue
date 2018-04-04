# SidecarIpPortIssue

Sidecar Issue - Prefer IP Address (true) is ignored in additon to non-secure-port (any int) is ignored. 

We have a sample Eureka server and two eureka clients. In one client we add the sidecar as an additional dependency. In both project we specify the following config:

prefer-ip-address = true 
non-secure-port = any_int 

When the instances are registered with Eureka, the non-sidecar instance registers using the IP address and the non-secure-port, this is the behaviour we expect and the behaviour we want. 

When the sidecar instance is registered it registers using the hostname and the server port. This is a default behaviour of a typical eureka client, we do not want this as we have specified the instance to prefer using IP address in addition the non-secure port. 

The question becomes, why is it when sidecar is added as a dependency the eureka client ignores the  prefer-ip-address and the non-secure-port configuration? 

