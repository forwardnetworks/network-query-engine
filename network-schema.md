# Schema Types

<details>
  <summary><strong>Table of Contents</strong></summary>

  * [Query](#query)
  * [Objects](#objects)
    * [AfiSafi](#afisafi)
    * [AfiSafiNeighbor](#afisafineighbor)
    * [AfiSafiNeighborAdjRib](#afisafineighboradjrib)
    * [Afts](#afts)
    * [Aggregation](#aggregation)
    * [AsPath](#aspath)
    * [AttrSet](#attrset)
    * [BgpRib](#bgprib)
    * [Bridge](#bridge)
    * [Device](#device)
    * [Ethernet](#ethernet)
    * [Iface](#iface)
    * [IfaceSubIface](#ifacesubiface)
    * [IpEntry](#ipentry)
    * [IpEntryConnection](#ipentryconnection)
    * [IpUnicast](#ipunicast)
    * [Ipv4Address](#ipv4address)
    * [Ipv4Addresses](#ipv4addresses)
    * [Ipv6Address](#ipv6address)
    * [Ipv6Addresses](#ipv6addresses)
    * [NetworkInstance](#networkinstance)
    * [NextHop](#nexthop)
    * [PageInfo](#pageinfo)
    * [PhysicalLink](#physicallink)
    * [Platform](#platform)
    * [Route](#route)
    * [RouteConnection](#routeconnection)
    * [RoutedVlan](#routedvlan)
    * [SubInterface](#subinterface)
    * [SubInterfaceVlanQINQ_ID](#subinterfacevlanqinq_id)
    * [SubInterfaceVlanVLAN_ID](#subinterfacevlanvlan_id)
    * [SwitchedSubInterfaceVlans](#switchedsubinterfacevlans)
    * [SwitchedVlan](#switchedvlan)
    * [TeTunnel](#tetunnel)
    * [TeTunnelNextHop](#tetunnelnexthop)
    * [Tunnel](#tunnel)
    * [Vlan](#vlan)
    * [VlanIdOrRangeID](#vlanidorrangeid)
    * [VlanIdOrRangeRANGE](#vlanidorrangerange)
    * [VlanIdSet](#vlanidset)
    * [VlanIdSetOrAllALL](#vlanidsetorallall)
    * [VlanIdSetOrAllIDS](#vlanidsetorallids)
    * [VlanPair](#vlanpair)
  * [Enums](#enums)
    * [AdminStatus](#adminstatus)
    * [AfiSafiNeighborState](#afisafineighborstate)
    * [AfiSafiType](#afisafitype)
    * [AsType](#astype)
    * [DuplexMode](#duplexmode)
    * [EncapsulationHeaderType](#encapsulationheadertype)
    * [IfaceType](#ifacetype)
    * [NetworkInstanceType](#networkinstancetype)
    * [NextHopType](#nexthoptype)
    * [OS](#os)
    * [OperStatus](#operstatus)
    * [Origin](#origin)
    * [OriginProtocol](#originprotocol)
    * [PortSpeed](#portspeed)
    * [SubInterfaceVlanType](#subinterfacevlantype)
    * [Vendor](#vendor)
    * [VlanIdOrRangeType](#vlanidorrangetype)
    * [VlanIdSetOrAllType](#vlanidsetoralltype)
    * [VlanModeType](#vlanmodetype)
  * [Scalars](#scalars)
    * [Boolean](#boolean)
    * [Int](#int)
    * [IpAddress](#ipaddress)
    * [IpSubnet](#ipsubnet)
    * [Long](#long)
    * [MacAddress](#macaddress)
    * [MplsLabel](#mplslabel)
    * [String](#string)
    * [VlanId](#vlanid)
  * [Interfaces](#interfaces)
    * [SubInterfaceVlan](#subinterfacevlan)
    * [VlanIdOrRange](#vlanidorrange)
    * [VlanIdSetOrAll](#vlanidsetorall)

</details>

## Query
<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>devices</strong></td>
<td valign="top">[<a href="#device">Device</a>]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">name</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

## Objects

### AfiSafi

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>afiSafiName</strong></td>
<td valign="top"><a href="#afisafitype">AfiSafiType</a>!</td>
<td>

 The afi-safi type.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>neighbors</strong></td>
<td valign="top">[<a href="#afisafineighbor">AfiSafiNeighbor</a>]!</td>
<td>

 List of neighbors (peers) of the local BGP speaker.

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">neighborAddress</td>
<td valign="top"><a href="#ipaddress">IpAddress</a></td>
<td></td>
</tr>
</tbody>
</table>

### AfiSafiNeighbor

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>neighborAddress</strong></td>
<td valign="top"><a href="#ipaddress">IpAddress</a>!</td>
<td>

 The address of the neighbor (peer).

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>adjRibInPost</strong></td>
<td valign="top"><a href="#afisafineighboradjrib">AfiSafiNeighborAdjRib</a></td>
<td>

 This is a per-neighbor table containing the routes received from the neighbor that are eligible for best-path selection after local input policy rules have been applied. Note that on some platforms, these routes may not show import policy modifications.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>adjRibOutPost</strong></td>
<td valign="top"><a href="#afisafineighboradjrib">AfiSafiNeighborAdjRib</a></td>
<td>

 Per-neighbor table containing paths eligble for sending (advertising) to the neighbor after output policy rules have been applied.

</td>
</tr>
</tbody>
</table>

### AfiSafiNeighborAdjRib

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>state</strong></td>
<td valign="top"><a href="#afisafineighborstate">AfiSafiNeighborState</a>!</td>
<td>

 Operational state of neighbor (peer).

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>routesPage</strong></td>
<td valign="top"><a href="#routeconnection">RouteConnection</a>!</td>
<td>

 List of routes in the table, keyed by the route prefix.

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">prefix</td>
<td valign="top"><a href="#ipsubnet">IpSubnet</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### Afts

 The abstract forwarding tables (AFTs) that are associated with the network instance. An AFT is instantiated per-protocol running within the network-instance - such that one exists for IPv4 Unicast, IPv6 Unicast, MPLS, L2 forwarding entries, etc. A forwarding entry within the FIB has a set of next-hops, which may be a reference to an entry within another table - e.g., where a Layer 3 next-hop has an associated Layer 2 forwarding entry.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>ipv4Unicast</strong></td>
<td valign="top"><a href="#ipunicast">IpUnicast</a></td>
<td>

 The abstract forwarding table for IPv4 unicast. Entries within this table are uniquely keyed on the IPv4 unicast destination prefix which is matched by ingress packets. The data set represented by the IPv4 Unicast AFT is the set of entries from the IPv4 unicast RIB that have been selected for installation into the FIB of the device.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ipv6Unicast</strong></td>
<td valign="top"><a href="#ipunicast">IpUnicast</a></td>
<td>

 The abstract forwarding table for IPv6 unicast. Entries within this table are uniquely keyed on the IPv6 unicast destination prefix which is matched by ingress packets. The data set represented by the IPv6 Unicast AFT is the set of entries from the IPv6 unicast RIB that have been selected for installation into the FIB of the device.

</td>
</tr>
</tbody>
</table>

### Aggregation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>memberNames</strong></td>
<td valign="top">[<a href="#string">String</a>]!</td>
<td>

 List of actual, current member interfaces for the aggregate, expressed as references to existing interfaces.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>configuredMemberNames</strong></td>
<td valign="top">[<a href="#string">String</a>]!</td>
<td>

 List of configured member interfaces for the aggregate.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>switchedVlan</strong></td>
<td valign="top"><a href="#switchedvlan">SwitchedVlan</a></td>
<td></td>
</tr>
</tbody>
</table>

### AsPath

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>asType</strong></td>
<td valign="top"><a href="#astype">AsType</a>!</td>
<td>

 The type of AS-PATH.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>members</strong></td>
<td valign="top">[<a href="#long">Long</a>]!</td>
<td>

 List of the AS numbers in the AS-PATH.

</td>
</tr>
</tbody>
</table>

### AttrSet

 Path attributes that may be in use by multiple routes in the table.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>origin</strong></td>
<td valign="top"><a href="#origin">Origin</a>!</td>
<td>

 BGP attribute defining the origin of the path information.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nextHop</strong></td>
<td valign="top"><a href="#ipaddress">IpAddress</a>!</td>
<td>

 The IP address of the router that should be used as the next hop to the destination.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>med</strong></td>
<td valign="top"><a href="#long">Long</a></td>
<td>

 The multi-exit discriminator attribute used in BGP route selection process.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>localPref</strong></td>
<td valign="top"><a href="#long">Long</a></td>
<td>

 Local preference attribute sent to internal peers to indicate the degree of preference for externally learned routes. The route with the highest local preference value is preferred.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>originatorId</strong></td>
<td valign="top"><a href="#ipaddress">IpAddress</a></td>
<td>

 BGP attribute that provides the id as an IPv4 address of the originator of the announcement.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>asPath</strong></td>
<td valign="top"><a href="#aspath">AsPath</a>!</td>
<td>

 BGP AS-PATH attribute.

</td>
</tr>
</tbody>
</table>

### BgpRib

 Defines a data model for representing BGP routing table contents.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>afiSafis</strong></td>
<td valign="top">[<a href="#afisafi">AfiSafi</a>]!</td>
<td>

 Address families.

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">afiSafiName</td>
<td valign="top"><a href="#afisafitype">AfiSafiType</a></td>
<td></td>
</tr>
</tbody>
</table>

### Bridge

 Bridge domain related data for a bridge interface.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>memberNames</strong></td>
<td valign="top">[<a href="#string">String</a>]!</td>
<td>

 The members of the bridge interface.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ipv4</strong></td>
<td valign="top"><a href="#ipv4addresses">Ipv4Addresses</a>!</td>
<td>

 The IPv4 addresses configured on the bridge interface.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ipv6</strong></td>
<td valign="top"><a href="#ipv6addresses">Ipv6Addresses</a>!</td>
<td>

 The IPv6 addresses configured on the bridge interface.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>vlan</strong></td>
<td valign="top"><a href="#vlanid">VlanId</a></td>
<td>

 The VLAN of the bridge interface. This VLAN will be pushed on packets while sending them out of this bridge interface as part of L3 forwarding.

</td>
</tr>
</tbody>
</table>

### Device

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>platform</strong></td>
<td valign="top"><a href="#platform">Platform</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>interfaces</strong></td>
<td valign="top">[<a href="#iface">Iface</a>]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">name</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>networkInstances</strong></td>
<td valign="top">[<a href="#networkinstance">NetworkInstance</a>]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">name</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>bgpRib</strong></td>
<td valign="top"><a href="#bgprib">BgpRib</a></td>
<td></td>
</tr>
</tbody>
</table>

### Ethernet

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>macAddress</strong></td>
<td valign="top"><a href="#macaddress">MacAddress</a></td>
<td>

 MAC address of the Ethernet interface.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>negotiatedDuplexMode</strong></td>
<td valign="top"><a href="#duplexmode">DuplexMode</a>!</td>
<td>

 This value shows the duplex mode that has been negotiated.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>negotiatedPortSpeed</strong></td>
<td valign="top"><a href="#portspeed">PortSpeed</a>!</td>
<td>

 This value shows the interface speed that has been negotiated.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>aggregateId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

 Specifies the logical aggregate interface to which this interface belongs.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>switchedVlan</strong></td>
<td valign="top"><a href="#switchedvlan">SwitchedVlan</a></td>
<td></td>
</tr>
</tbody>
</table>

### Iface

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

 The name of the interface.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>interfaceType</strong></td>
<td valign="top"><a href="#ifacetype">IfaceType</a>!</td>
<td>

 The type of the interface.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>mtu</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

 Set the max transmission unit size in octets for the physical interface.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>loopbackMode</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td>

 When set to true, the interface is logically looped back, such that packets that are forwarded via the interface are received on the same interface.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

 A textual description of the interface.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>adminStatus</strong></td>
<td valign="top"><a href="#adminstatus">AdminStatus</a>!</td>
<td>

 The desired state of the interface. Here, it reflects the administrative state as set by enabling or disabling the interface.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>operStatus</strong></td>
<td valign="top"><a href="#operstatus">OperStatus</a>!</td>
<td>

 The current operational state of the interface.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subinterfaces</strong></td>
<td valign="top">[<a href="#subinterface">SubInterface</a>]!</td>
<td>

 The list of subinterfaces (logical interfaces) associated with a physical interface.

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">name</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ethernet</strong></td>
<td valign="top"><a href="#ethernet">Ethernet</a>!</td>
<td>

 Ethernet-specific configuration and state of the interface.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>routedVlan</strong></td>
<td valign="top"><a href="#routedvlan">RoutedVlan</a></td>
<td>

 Non-null when the interface is a logical interface providing L3 routing for VLANs.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>bridge</strong></td>
<td valign="top"><a href="#bridge">Bridge</a></td>
<td>

 Non-null when the interface is a bridge (BVI, BDI, etc.)

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>aggregation</strong></td>
<td valign="top"><a href="#aggregation">Aggregation</a></td>
<td>

 Non-null when the interface is set to type IF_AGGREGATE.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tunnel</strong></td>
<td valign="top"><a href="#tunnel">Tunnel</a></td>
<td>

 In the case that the interface is logical tunnel interface, the parameters for the tunnel are specified within this subtree.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>teTunnel</strong></td>
<td valign="top"><a href="#tetunnel">TeTunnel</a></td>
<td>

 In the case that the interface is a logical Traffic Engineering (TE) tunnel interface, the parameters for the TE tunnel are specified within this subtree.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>links</strong></td>
<td valign="top">[<a href="#physicallink">PhysicalLink</a>]!</td>
<td>

 The other interfaces that this interface connects to.

</td>
</tr>
</tbody>
</table>

### IfaceSubIface

 The names of the interface and subinterface that are associated with the network instance.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>interfaceName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subInterfaceName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### IpEntry

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>prefix</strong></td>
<td valign="top"><a href="#ipsubnet">IpSubnet</a>!</td>
<td>

 Reference to the IP destination prefix which must be matched to utilise the AFT entry.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nextHops</strong></td>
<td valign="top">[<a href="#nexthop">NextHop</a>]!</td>
<td>

 The list of next-hops that are to be used for entry within the AFT table. The structure of each next-hop is address family independent, such that it is possible to resolve fully how the next-hop is treated. For example: - Where ingress IPv4 unicast packets are to be forwarded via an MPLS LSP, the next-hop list should indicate the MPLS label stack that is used to the next-hop. - Where ingress MPLS labeled packets are to be forwarded to an IPv6 nexthop (for example, a CE within a VPN, then the popped label stack, and IPv6 next-hop address should be indicated).

</td>
</tr>
</tbody>
</table>

### IpEntryConnection

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>items</strong></td>
<td valign="top">[<a href="#ipentry">IpEntry</a>]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pageInfo</strong></td>
<td valign="top"><a href="#pageinfo">PageInfo</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### IpUnicast

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>ipEntriesPage</strong></td>
<td valign="top"><a href="#ipentryconnection">IpEntryConnection</a>!</td>
<td>

 List of the IP unicast entries within the abstract forwarding table. This list is keyed by the destination IPv4/IPv6 prefix.

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">prefix</td>
<td valign="top"><a href="#ipsubnet">IpSubnet</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">first</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### Ipv4Address

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>ip</strong></td>
<td valign="top"><a href="#ipaddress">IpAddress</a>!</td>
<td>

 The IPv4 address on an interface.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>prefixLength</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>

 The length of the subnet prefix.

</td>
</tr>
</tbody>
</table>

### Ipv4Addresses

 The IPv4 addresses configured on an interface.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>addresses</strong></td>
<td valign="top">[<a href="#ipv4address">Ipv4Address</a>]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fhrpAddresses</strong></td>
<td valign="top">[<a href="#ipv4address">Ipv4Address</a>]!</td>
<td></td>
</tr>
</tbody>
</table>

### Ipv6Address

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>ip</strong></td>
<td valign="top"><a href="#ipaddress">IpAddress</a>!</td>
<td>

 The IPv6 address on an interface.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>prefixLength</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>

 The length of the subnet prefix.

</td>
</tr>
</tbody>
</table>

### Ipv6Addresses

 The IPv6 addresses configured on an interface.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>addresses</strong></td>
<td valign="top">[<a href="#ipv6address">Ipv6Address</a>]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fhrpAddresses</strong></td>
<td valign="top">[<a href="#ipv6address">Ipv6Address</a>]!</td>
<td></td>
</tr>
</tbody>
</table>

### NetworkInstance

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

 A unique name identifying the network instance. The value is either "default" or a unique VRF name.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>instanceType</strong></td>
<td valign="top"><a href="#networkinstancetype">NetworkInstanceType</a>!</td>
<td>

 Type of network instance.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>afts</strong></td>
<td valign="top"><a href="#afts">Afts</a>!</td>
<td>

 The abstract forwarding tables (AFTs) that are associated with the network instance.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>interfaces</strong></td>
<td valign="top">[<a href="#ifacesubiface">IfaceSubIface</a>]!</td>
<td>

 The interfaces that are associated with this network instance.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>vlans</strong></td>
<td valign="top">[<a href="#vlan">Vlan</a>]!</td>
<td>

 Vlans that are associated with this network instance.

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">vlanId</td>
<td valign="top"><a href="#vlanid">VlanId</a></td>
<td></td>
</tr>
</tbody>
</table>

### NextHop

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>weight</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>

 The weight of the next-hop. Traffic is balanced according to the ratio described by the relative weights of the next hops that exist for the AFT entry. Note that all next-hops that are specified are assumed to be active next-hops and therefore eligible (and selected) to be installed in the FIB, and hence used for packet forwarding.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ipAddress</strong></td>
<td valign="top"><a href="#ipaddress">IpAddress</a>!</td>
<td>

 The IP address of the next-hop system.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>macAddress</strong></td>
<td valign="top"><a href="#macaddress">MacAddress</a></td>
<td>

 The MAC address of the next-hop if resolved by the local network instance.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>vrf</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

 The next VRF to process the packet.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>poppedMplsLabels</strong></td>
<td valign="top">[<a href="#mplslabel">MplsLabel</a>]!</td>
<td>

 The MPLS labels to be popped from the packet when switched by the system. A swap operation is reflected by entries in the popped-mpls-label-stack and pushed-mpls-label-stack nodes.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pushedMplsLabels</strong></td>
<td valign="top">[<a href="#mplslabel">MplsLabel</a>]!</td>
<td>

 The MPLS labels to be pushed from the packet when switched by the system. A swap operation is reflected by entries in the popped-mpls-label-stack and pushed-mpls-label-stack nodes.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>interfaceName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

 The interface on this system to get to the next-hop.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subInterfaceName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

 The sub-interface on this system to get to the next-hop.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nextHopType</strong></td>
<td valign="top"><a href="#nexthoptype">NextHopType</a>!</td>
<td>

 Type of next-hop.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>encapsulateHeader</strong></td>
<td valign="top"><a href="#encapsulationheadertype">EncapsulationHeaderType</a></td>
<td>

 When forwarding a packet to the specified next-hop the local system performs an encapsulation of the packet - adding the specified header-type.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>originProtocol</strong></td>
<td valign="top"><a href="#originprotocol">OriginProtocol</a>!</td>
<td>

 The protocol from which the AFT entry was learned.

</td>
</tr>
</tbody>
</table>

### PageInfo

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>hasNextPage</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>endCursor</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### PhysicalLink

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>deviceName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>interfaceName</strong> ⚠️</td>
<td valign="top"><a href="#string">String</a>!</td>
<td>
<p>⚠️ <strong>DEPRECATED</strong></p>
<blockquote>

Use name in iface link. May be removed after 2019-06-01

</blockquote>
</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>iface</strong></td>
<td valign="top"><a href="#iface">Iface</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Platform

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>vendor</strong></td>
<td valign="top"><a href="#vendor">Vendor</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>model</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>os</strong></td>
<td valign="top"><a href="#os">OS</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>osVersion</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### Route

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>prefix</strong></td>
<td valign="top"><a href="#ipsubnet">IpSubnet</a>!</td>
<td>

 Prefix for the route.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>activeRoute</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td>

 Whether route is active.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>attributes</strong></td>
<td valign="top"><a href="#attrset">AttrSet</a>!</td>
<td>

 Attributes for the route.

</td>
</tr>
</tbody>
</table>

### RouteConnection

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>items</strong></td>
<td valign="top">[<a href="#route">Route</a>]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pageInfo</strong></td>
<td valign="top"><a href="#pageinfo">PageInfo</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### RoutedVlan

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>vlan</strong></td>
<td valign="top"><a href="#vlanid">VlanId</a>!</td>
<td>

 References the VLAN for which this IP interface provides routing services -- similar to a switch virtual interface (SVI), or integrated routing and bridging interface (IRB) in some implementations.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ipv4</strong></td>
<td valign="top"><a href="#ipv4addresses">Ipv4Addresses</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ipv6</strong></td>
<td valign="top"><a href="#ipv6addresses">Ipv6Addresses</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### SubInterface

 Subinterface data for logical interfaces associated with a given interface.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

 The system-assigned name for the sub-interface.  This MAY be a combination of the base interface name and the subinterface index, or some other convention used by the system.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

 A textual description of the interface.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>adminStatus</strong></td>
<td valign="top"><a href="#adminstatus">AdminStatus</a>!</td>
<td>

 The desired state of the interface. Here, it reflects the administrative state as set by enabling or disabling the interface.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>operStatus</strong></td>
<td valign="top"><a href="#operstatus">OperStatus</a>!</td>
<td>

 The current operational state of the interface.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>vlan</strong></td>
<td valign="top"><a href="#subinterfacevlan">SubInterfaceVlan</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ipv4</strong></td>
<td valign="top"><a href="#ipv4addresses">Ipv4Addresses</a>!</td>
<td>

 Configuration and state for IPv4 interfaces.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ipv6</strong></td>
<td valign="top"><a href="#ipv6addresses">Ipv6Addresses</a>!</td>
<td>

 Configuration and state for IPv6 interfaces.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>switchedVlans</strong></td>
<td valign="top"><a href="#switchedsubinterfacevlans">SwitchedSubInterfaceVlans</a></td>
<td>

 Switched VLAN configuration of the subinterface. Non-null if this interface is a switch-subinterface.

</td>
</tr>
</tbody>
</table>

### SubInterfaceVlanQINQ_ID

 Type definition representing a single double-tagged/QinQ VLAN identifier. The format of a QinQ VLAN-ID is x.y where X is the 'outer' VLAN identifier, and y is the 'inner' VLAN identifier. Both x and y must be valid VLAN IDs (1 <= vlan-id <= 4094) with the exception that y may be equal to a wildcard (*). In cases where y is set to the wildcard, this represents all inner VLAN identifiers where the outer VLAN identifier is equal to x.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>tag</strong></td>
<td valign="top"><a href="#subinterfacevlantype">SubInterfaceVlanType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>QINQ_ID</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### SubInterfaceVlanVLAN_ID

 A single VLAN ID configured for the subinterface.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>tag</strong></td>
<td valign="top"><a href="#subinterfacevlantype">SubInterfaceVlanType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>VLAN_ID</strong></td>
<td valign="top"><a href="#vlanid">VlanId</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### SwitchedSubInterfaceVlans

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>outerVlans</strong></td>
<td valign="top"><a href="#vlanidsetorall">VlanIdSetOrAll</a>!</td>
<td>

 The outer VLANs configured on a switch-subinterface.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>innerVlans</strong></td>
<td valign="top"><a href="#vlanidsetorall">VlanIdSetOrAll</a>!</td>
<td>

 The inner VLANs configured on a switch-subinterface.

</td>
</tr>
</tbody>
</table>

### SwitchedVlan

 Type for VLAN interface-specific data on Ethernet interfaces. These are for standard L2, switched-style VLANs.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>interfaceMode</strong></td>
<td valign="top"><a href="#vlanmodetype">VlanModeType</a>!</td>
<td>

 Access or trunk mode for VLANs.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nativeVlan</strong></td>
<td valign="top"><a href="#vlanid">VlanId</a></td>
<td>

 Native VLAN is valid for trunk mode interfaces.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accessVlan</strong></td>
<td valign="top"><a href="#vlanid">VlanId</a></td>
<td>

 Access VLAN assigned to the interfaces.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>trunkVlans</strong></td>
<td valign="top">[<a href="#vlanidorrange">VlanIdOrRange</a>]!</td>
<td>

 Specifies VLANs, or ranges thereof, that the interface may carry when in trunk mode. If not specified, all VLANs are allowed on the interface. Ranges are specified in the form x..y, where x<y - ranges are assumed to be inclusive (such that the VLAN range is x <= range <= y).

</td>
</tr>
</tbody>
</table>

### TeTunnel

 Configuraton parameters relating to a TE-tunnel interface.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>nextHops</strong></td>
<td valign="top">[<a href="#tetunnelnexthop">TeTunnelNextHop</a>]!</td>
<td>

 Next hops for the tunnel.

</td>
</tr>
</tbody>
</table>

### TeTunnelNextHop

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>interfaceName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

 Output interface for the packet.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ipAddress</strong></td>
<td valign="top"><a href="#ipaddress">IpAddress</a>!</td>
<td>

 Next hop IP address for the outgoing packet.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>mplsLabels</strong></td>
<td valign="top">[<a href="#mplslabel">MplsLabel</a>]!</td>
<td>

 MPLS labels to push on the outgoing patcket.

</td>
</tr>
</tbody>
</table>

### Tunnel

 Configuraton parameters relating to a tunnel interface.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>src</strong></td>
<td valign="top"><a href="#ipaddress">IpAddress</a>!</td>
<td>

 The source address for the tunnel.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dst</strong></td>
<td valign="top"><a href="#ipaddress">IpAddress</a>!</td>
<td>

 The destination address for the tunnel.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ipv4</strong></td>
<td valign="top"><a href="#ipv4addresses">Ipv4Addresses</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ipv6</strong></td>
<td valign="top"><a href="#ipv6addresses">Ipv6Addresses</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Vlan

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>vlanId</strong></td>
<td valign="top"><a href="#vlanid">VlanId</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

 Name for this vlan.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>memberNames</strong></td>
<td valign="top">[<a href="#string">String</a>]!</td>
<td>

 Interfaces carrying this vlan.

</td>
</tr>
</tbody>
</table>

### VlanIdOrRangeID

 Type definition representing a single-tagged VLAN.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>tag</strong></td>
<td valign="top"><a href="#vlanidorrangetype">VlanIdOrRangeType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ID</strong></td>
<td valign="top"><a href="#vlanid">VlanId</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### VlanIdOrRangeRANGE

 Type definition representing a range of single-tagged VLANs. A range is specified as x..y where x and y are valid VLAN IDs (1 <= vlan-id <= 4094). The range is assumed to be inclusive, such that any VLAN-ID matching x <= VLAN-ID <= y falls within the range.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>tag</strong></td>
<td valign="top"><a href="#vlanidorrangetype">VlanIdOrRangeType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>RANGE</strong></td>
<td valign="top"><a href="#vlanpair">VlanPair</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### VlanIdSet

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>vlans</strong></td>
<td valign="top">[<a href="#vlanid">VlanId</a>]!</td>
<td></td>
</tr>
</tbody>
</table>

### VlanIdSetOrAllALL

 All VLAN IDs.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>tag</strong></td>
<td valign="top"><a href="#vlanidsetoralltype">VlanIdSetOrAllType</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### VlanIdSetOrAllIDS

 Individual VLAN IDs.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>tag</strong></td>
<td valign="top"><a href="#vlanidsetoralltype">VlanIdSetOrAllType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>IDS</strong></td>
<td valign="top"><a href="#vlanidset">VlanIdSet</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### VlanPair

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>from</strong></td>
<td valign="top"><a href="#vlanid">VlanId</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>to</strong></td>
<td valign="top"><a href="#vlanid">VlanId</a>!</td>
<td></td>
</tr>
</tbody>
</table>

## Enums

### AdminStatus

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>DOWN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>UP</strong></td>
<td></td>
</tr>
</tbody>
</table>

### AfiSafiNeighborState

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>ACTIVE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CONNECT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ESTABLISHED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IDLE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OPEN_CONFIRM</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OPEN_SENT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SHUTDOWN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>UNKNOWN</strong></td>
<td></td>
</tr>
</tbody>
</table>

### AfiSafiType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>IPV4_UNICAST</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IPV6_UNICAST</strong></td>
<td></td>
</tr>
</tbody>
</table>

### AsType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>AS_SEQ</strong></td>
<td></td>
</tr>
</tbody>
</table>

### DuplexMode

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>FULL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>HALF</strong></td>
<td></td>
</tr>
</tbody>
</table>

### EncapsulationHeaderType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>GRE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IPV4</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IPV6</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>MPLS</strong></td>
<td></td>
</tr>
</tbody>
</table>

### IfaceType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>IF_AGGREGATE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IF_ETHERNET</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IF_LOOPBACK</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IF_ROUTED_VLAN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IF_SONET</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IF_TE_TUNNEL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IF_TUNNEL_GRE4</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IF_TUNNEL_GRE6</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IF_TUNNEL_IPSEC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IF_TUNNEL_IP_IN_IP</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IF_TUNNEL_L2_VPN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IF_TUNNEL_UNKNOWN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IF_TUNNEL_VXLAN</strong></td>
<td></td>
</tr>
</tbody>
</table>

### NetworkInstanceType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>DEFAULT_INSTANCE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>L3VRF</strong></td>
<td></td>
</tr>
</tbody>
</table>

### NextHopType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>ATTACHED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>BROADCAST</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DROP</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RECEIVE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RECURSIVE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>REDIRECT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>REMOTE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>UNDEFINED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>VRF_FORWARDED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### OS

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>ACOS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ARISTA_EOS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ASA</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>AVI_VANTAGE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>BLUECOAT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CHECKPOINT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CUMULUS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ESXI</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>F5</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FORTINET</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>HP_COMWARE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>HP_PROVISION</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IOS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IOS_XE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IOS_XR</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>JUNOS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LINUX</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LINUX_OVS_OFCTL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>MPLS_VPN_SERVICE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NETRONOME_OVS_OFCTL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NETSCALER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NETSCREEN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NXOS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OTHER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PAN_OS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PICA8_OVS_OFCTL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SRX</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>UNKNOWN</strong></td>
<td></td>
</tr>
</tbody>
</table>

### OperStatus

 The current operational state of the interface.

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>DORMANT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DOWN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LOWER_LAYER_DOWN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NOT_PRESENT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TESTING</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>UNKNOWN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>UP</strong></td>
<td></td>
</tr>
</tbody>
</table>

### Origin

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>EGP</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IGP</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>INCOMPLETE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### OriginProtocol

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>BGP</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DIRECT_CONNECTED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>EIGRP</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FRR</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IGMP</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ISIS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LDP</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LOCAL_AGGREGATE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ODR</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OSPF</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PIM</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RIP</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RSVP</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>STATIC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>UNKNOWN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>VPLS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>VPN</strong></td>
<td></td>
</tr>
</tbody>
</table>

### PortSpeed

 Type to specify available Ethernet link speeds.

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>SPEED_100GB</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SPEED_100MB</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SPEED_10GB</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SPEED_10MB</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SPEED_1GB</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SPEED_2500MB</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SPEED_25GB</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SPEED_40GB</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SPEED_50GB</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SPEED_5GB</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SPEED_UNKNOWN</strong></td>
<td></td>
</tr>
</tbody>
</table>

### SubInterfaceVlanType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>QINQ_ID</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>VLAN_ID</strong></td>
<td></td>
</tr>
</tbody>
</table>

### Vendor

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>A10</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>AMAZON</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ARISTA</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>AVI_NETWORKS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CHECKPOINT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CISCO</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CITRIX</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CUMULUS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>F5</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FORTINET</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FORWARD_CUSTOM</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>HP</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>JUNIPER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LINUX_GENERIC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NETRONOME</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OPENFLOW_GENERIC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PALO_ALTO_NETWORKS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PICA8</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SYMANTEC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>UNKNOWN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>VMWARE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### VlanIdOrRangeType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>ID</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RANGE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### VlanIdSetOrAllType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>ALL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IDS</strong></td>
<td></td>
</tr>
</tbody>
</table>

### VlanModeType

 VLAN interface mode (trunk or access).

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>ACCESS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TRUNK</strong></td>
<td></td>
</tr>
</tbody>
</table>

## Scalars

### Boolean

Built-in Boolean

### Int

Built-in Int

### IpAddress

An IPv4 or IPv6 IP address

### IpSubnet

An IPv4 or IPv6 IP subnet

### Long

Long type

### MacAddress

A MAC address

### MplsLabel

An MPLS Label (1-1048575)

### String

Built-in String

### VlanId

VLAN ID (1-4094)


## Interfaces


### SubInterfaceVlan

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>tag</strong></td>
<td valign="top"><a href="#subinterfacevlantype">SubInterfaceVlanType</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### VlanIdOrRange

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>tag</strong></td>
<td valign="top"><a href="#vlanidorrangetype">VlanIdOrRangeType</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### VlanIdSetOrAll

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>tag</strong></td>
<td valign="top"><a href="#vlanidsetoralltype">VlanIdSetOrAllType</a>!</td>
<td></td>
</tr>
</tbody>
</table>
