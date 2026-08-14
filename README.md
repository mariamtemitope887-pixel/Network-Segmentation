<h1>Network Segmentation Project</h1>
<h3>Mapping the ISO27001 Segregation of networks control to the Protect function of the NIST CSF</h3>
<p>This document presents the technical design and implementation of a departmental network segmentation project, simulated entirely within an Oracle VirtualBox lab environment. The project demonstrates the application of subnetting (CIDR/VLSM) principles to divide a single network block into four logically and technically isolated departmental subnets: </p>

<ol>
  <li>Finance,</li>
  <li>Audit</li>
  <li>IT, and </li>
  <li>Procurement.</li>
</ol>
<p>The base network 10.0.2.0/24 was subdivided into four equal-sized /26 subnets, each providing 62 usable host addresses — comfortably accommodating the lab's per-department device count while leaving headroom for future growth. Network isolation was implemented using VirtualBox's NATNetwork feature, creating four independent virtual networks, each acting as the equivalent of a separate VLAN or physical network segment in a production environment.</p>

<p>Sixteen virtual machines were deployed across the four subnets — three employee workstation VMs and one server VM per department — for a total of 12 workstations and 4 servers. Each VM's network adapter was explicitly attached to its corresponding departmental NATNetwork, ensuring that devices in one department cannot directly communicate with devices in another without passing through a controlled routing or firewall boundary. This project demonstrates core network security principles including the reduction of lateral movement risk, the containment of a potential breach to a single department, and the enforcement of the principle of least privilege at the network layer.</p>
