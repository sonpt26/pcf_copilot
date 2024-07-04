## <a name="_toc28013430"></a><a name="_toc34222343"></a><a name="_toc36040526"></a><a name="_toc39134455"></a><a name="_toc43283402"></a><a name="_toc45134442"></a><a name="_toc49930042"></a><a name="_toc50024162"></a><a name="_toc51763650"></a><a name="_toc56594514"></a><a name="_toc67493856"></a><a name="_toc68169760"></a><a name="_toc73459370"></a><a name="_toc73459493"></a><a name="_toc74743030"></a><a name="_toc112918315"></a><a name="_toc120652816"></a><a name="_toc129205603"></a><a name="_toc129244422"></a><a name="_toc136530196"></a><a name="_toc136614793"></a><a name="_toc148460920"></a><a name="_toc151914917"></a><a name="_toc170121085"></a>5.6	Data Model
### <a name="_toc28013431"></a><a name="_toc34222344"></a><a name="_toc36040527"></a><a name="_toc39134456"></a><a name="_toc43283403"></a><a name="_toc45134443"></a><a name="_toc49930043"></a><a name="_toc50024163"></a><a name="_toc51763651"></a><a name="_toc56594515"></a><a name="_toc67493857"></a><a name="_toc68169761"></a><a name="_toc73459371"></a><a name="_toc73459494"></a><a name="_toc74743031"></a><a name="_toc112918316"></a><a name="_toc120652817"></a><a name="_toc129205604"></a><a name="_toc129244423"></a><a name="_toc136530197"></a><a name="_toc136614794"></a><a name="_toc148460921"></a><a name="_toc151914918"></a><a name="_toc170121086"></a>5.6.1	General
This clause specifies the application data model supported by the API.

Table 5.6.1-1 specifies the data types defined for the Npcf\_UEPolicyControl service based interface protocol.

**Table 5.6.1-1: Npcf\_UEPolicyControl specific Data Types**

|**Data type**|**Section defined**|**Description**|**Applicability**||||||
| :-: | :-: | :-: | :-: | :- | :- | :- | :- | :- |
|A2xCapability|5\.6.3.12|Indicates the A2X capabilities|A2X||||||
|LboRoamingInformation|5\.6.2.10|LBO roaming information for a DNN and S-NSSAI|VPLMNSpecificURSP||||||
|N1N2MessTransferErrorReply|5\.6.3.8|Error the V-PCF may send to the H-PCF when the V-PCF receives from the AMF an error to the N1N2MessageTransfer request.|EnErrorHandling||||||
|Non3gppAccess|5\.6.3.7|Represents a Non-3gpp access node.|SliceAwareANDSP||||||
|Pc5Capability|5\.6.3.5|Indicates the specific PC5 RAT(s) which the UE supports for V2X communications and/or A2X communications over PC5 reference point.|V2X||||||
|ProSeCapability|5\.6.3.6|Indicates the 5G ProSe capabilities.|ProSe||||||
|PolicyAssociation|5\.6.2.2|Description of a policy association that is returned by the PCF when a policy Association is created, updated, or read.|||||||
|PolicyAssociationReleaseCause|5\.6.3.4|The cause why the PCF requests the termination of the policy association.|||||||
|PolicyAssociationRequest|5\.6.2.3|Information that NF service consumer provides when requesting the creation of a policy association.|||||||
|PolicyAssociationUpdateRequest|5\.6.2.4|Information that NF service consumer provides when requesting the update of a policy association.|||||||
|PolicyStatus|5\.6.3.10|Represents the configuration status of a UE Policy in the UE.|SliceAwareANDSP||||||
|PolicyUpdate|5\.6.2.5|Updated policies that the PCF provides in a notification or in the reply to an Update Request.|||||||
|RangSLCapability|5\.6.3.10|Represents the Ranging/SL capabilities.|Ranging\_SL||||||
|RequestTrigger|5\.6.3.3|Enumeration of possible Request Triggers.|||||||
|TerminationNotification|5\.6.2.6|Request to terminate a policy Association that the PCF provides in a notification.|||||||
|UeRequestedValueRep|5\.6.2.8|Contains the current applicable values corresponding to the policy control request triggers.|ImmediateReport||||||
|UePolicy|5\.6.3.2|UE Policies|||||||
|UePolicyDeliveryResult|5\.6.3.2|UE Policy delivery Result|||||||
|UePolicyNotification|<p>5\.6.2.12</p><p></p>|Contains the delivery outcome of VPLMN-Specific URSP rules|VPLMNSpecificURSP||||||
|UePolicyParameters|5\.6.2.9|Contains the service parameters used to guide the VPLMN-specific URSP rule determination.|VPLMNSpecificURSP||||||
|UePolicyRequest|5\.6.3.2|Request for UE Policies|||||||
|UePolicyTransferFailureCause|5\.6.4.1|UE Policy Transfer Failure Cause|EnErrorHandling||||||
|UePolicyTransferFailureNotification|5\.6.2.7|Information that the UE policy is failure to be transferred to the UE.|||||||
|UrspEnforcementPduSession|5\.6.2.11|Represents URSP rule enforcement information for a PDU session.|URSPEnforcement||||||

Table 5.6.1-2 specifies data types re-used by the Npcf\_UEPolicyControl service based interface protocol from other specifications, including a reference to their respective specifications and when needed, a short description of their use within the Npcf\_UEPolicyControl service based interface. 

**Table 5.6.1-2: Npcf\_UEPolicyControl re-used Data Types**

|**Data type**|**Reference**|**Comments**|**Applicability**|
| :-: | :-: | :-: | :-: |
|AccessType|3GPP TS 29.571 [11]|Represents an Access Type.||
|Bytes|3GPP TS 29.571 [11]|String with format "byte".||
|ChargingInformation|3GPP TS 29.512 [31]|Contains the addresses, and if available, the instance ID and set ID, of the charging functions.|SLAMUP|
|ConfiguredSnssai|3GPP TS 29.531 [34]|Contains the configured S-NSSAI and optionally mapped home S-NSSA.|<p>SliceAwareANDSP,</p><p>NssaiChange</p>|
|CmState|3GPP TS 29.518 [14]|Connectivity state of UE|ConnectivityStateChange|
|Dnn|3GPP TS 29.571 [11]|Represents a DNN.|<p>VPLMNSpecificURSP</p><p>URSPEnforcement</p>|
|Event|3GPP TS 29.522 [41]|Subscription to notification about delivery of VPLMN specific URSP rule.|<p>VPLMNSpecificURSP</p><p></p>|
|Fqdn|3GPP TS 29.571 [11]|FQDN||
|Gpsi|3GPP TS 29.571 [11]|Generic Public Subscription Identifier||
|GroupId|3GPP TS 29.571 [11]|Represents a UE Group Identifier||
|Guami|3GPP TS 29.571 [11]|Globally Unique AMF Identifier||
|Ipv4Addr|3GPP TS 29.571 [11]|Represents an Ipv4 address.||
|Ipv6Addr|3GPP TS 29.571 [11]|Represents an Ipv6 address.||
|N1N2MessageTransferCause|3GPP TS 29.518 [14]|Contains an error cause for an N1 or N2 message transfer.||
|N2InfoContent|3GPP TS 29.518 [14]|Represents a transparent N2 information content to be relayed by AMF.|V2X, A2X, ProSe, Ranging\_SL|
|NfInstanceId|3GPP TS 29.571 [11]|Represents an NF instance identifier||
|PcEventNotification|3GPP TS 29.523 [30]|Represents notification about UE Policy Delivery outcome|VPLMNSpecificURSP|
|PcfUeCallbackInfo|3GPP TS 29.571 [11]|Contains the PCF for the UE callback information necessary for the PCF for the PDU session to send Establishment and Termination event.|URSPEnforcement|
|PduSessionInfo|3GPP TS 29.571 [11]|Contains a DNN and SNSSAI combination|<p>VPLMNSpecificURSP</p><p>URSPEnforcement</p>|
|PduSessionType|3GPP TS 29.571 [13]|Contains the PDU Session Type|URSPEnforcement|
|Pei|3GPP TS 29.571 [11]|Permanent Equipment Identifier||
|PlmnId|3GPP TS 29.571 [11]|Represents a PLMN identifier.||
|PlmnIdNid|3GPP TS 29.571 [11]|Identifies the network: PLMN Identifier or the SNPN Identifier (the PLMN Identifier and the NID).||
|PresenceInfo|3GPP TS 29.571 [11]|Presence reporting area information||
|ProblemDetails|3GPP TS 29.571 [11]|Contains detailed information about an error response.||
|RatType|3GPP TS 29.571 [11]|Represents a RAT type.||
|RedirectResponse|3GPP TS 29.571 [11]|Contains redirection related information.|ES3XX|
|ServiceName|3GPP TS 29.510 [13]|Name of the service instance.||
|SatelliteBackhaulCategory|3GPP TS 29.571 [11]|Indicates the satellite backhaul category or non-satellite backhaul.|EnSatBackhaulCategoryChg|
|Snssai|3GPP TS 29.571 [11]|Represents an S-NSSAI|SliceAwareANDSP|
|SscMode|3GPP TS 29.571 [11]|Service and session continuity mode.|URSPEnforcement|
|Supi|3GPP TS 29.571 [11]|Subscription Permanent Identifier||
|SupportedFeatures|3GPP TS 29.571 [11]|Used to negotiate the applicability of the optional features defined in table 5.8-1.||
|TimeZone|3GPP TS 29.571 [11]|Represents a time zone.||
|Uinteger|3GPP TS 29.571 [11]|Unsigned integer.||
|Uri|3GPP TS 29.571 [11]|Represents a URI.||
|UrspEnforcementInfo|3GPP TS 29.512 [31]|URSP rule enforcement information as received from the UE.|URSPEnforcement|
|UrspRuleRequest|3GPP TS 29.522 [41]|URSP rule guidance information|VPLMNSpecificURSP|
|UserLocation|3GPP TS 29.571 [11]|Contains User Location information.||

### <a name="_toc28013432"></a><a name="_toc34222345"></a><a name="_toc36040528"></a><a name="_toc39134457"></a><a name="_toc43283404"></a><a name="_toc45134444"></a><a name="_toc49930044"></a><a name="_toc50024164"></a><a name="_toc51763652"></a><a name="_toc56594516"></a><a name="_toc67493858"></a><a name="_toc68169762"></a><a name="_toc73459372"></a><a name="_toc73459495"></a><a name="_toc74743032"></a><a name="_toc112918317"></a><a name="_toc120652818"></a><a name="_toc129205605"></a><a name="_toc129244424"></a><a name="_toc136530198"></a><a name="_toc136614795"></a><a name="_toc148460922"></a><a name="_toc151914919"></a><a name="_toc170121087"></a>5.6.2	Structured data types
#### <a name="_toc28013433"></a><a name="_toc34222346"></a><a name="_toc36040529"></a><a name="_toc39134458"></a><a name="_toc43283405"></a><a name="_toc45134445"></a><a name="_toc49930045"></a><a name="_toc50024165"></a><a name="_toc51763653"></a><a name="_toc56594517"></a><a name="_toc67493859"></a><a name="_toc68169763"></a><a name="_toc73459373"></a><a name="_toc73459496"></a><a name="_toc74743033"></a><a name="_toc112918318"></a><a name="_toc120652819"></a><a name="_toc129205606"></a><a name="_toc129244425"></a><a name="_toc136530199"></a><a name="_toc136614796"></a><a name="_toc148460923"></a><a name="_toc151914920"></a><a name="_toc170121088"></a>5.6.2.1	Introduction
This clause defines the structures to be used in resource representations. 
#### <a name="_toc28013434"></a><a name="_toc34222347"></a><a name="_toc36040530"></a><a name="_toc39134459"></a><a name="_toc43283406"></a><a name="_toc45134446"></a><a name="_toc49930046"></a><a name="_toc50024166"></a><a name="_toc51763654"></a><a name="_toc56594518"></a><a name="_toc67493860"></a><a name="_toc68169764"></a><a name="_toc73459374"></a><a name="_toc73459497"></a><a name="_toc74743034"></a><a name="_hlk526271999"></a><a name="_toc112918319"></a><a name="_toc120652820"></a><a name="_toc129205607"></a><a name="_toc129244426"></a><a name="_toc136530200"></a><a name="_toc136614797"></a><a name="_toc148460924"></a><a name="_toc151914921"></a><a name="_toc170121089"></a>5.6.2.2	Type PolicyAssociation
**Table 5.6.2.2-1: Definition of type PolicyAssociation**

|**Attribute name**|**Data type**|**P**|**Cardinality**|**Description**|**Applicability**|
| :-: | :-: | :-: | :-: | :-: | :-: |
|request|PolicyAssociationRequest|O|0\..1|The information provided by the NF service consumer when requesting the creation of a policy association||
|uePolicy|UePolicy|O|0\..1|The UE policy as determined by the H-PCF (for the H-PCF as NF service producer).||
|n2Pc5Pol|N2InfoContent|O|0\..1|The N2 PC5 policy for V2X communications as determined by the H-PCF.|V2X|
|n2Pc5PolA2x|N2InfoContent|O|0\..1|The N2 PC5 policy for A2X communications as determined by the H-PCF.|A2X|
|n2Pc5ProSePol|N2InfoContent|O|0\..1|The N2 PC5 policy for 5G ProSe as determined by the PCF.|ProSe|
|triggers|array(RequestTrigger)|O|1\..N|<p>Request Triggers to which the PCF subscribes.</p><p></p><p>(NOTE 1)</p>||
|pras|map(PresenceInfo)|C|1\..N|If the Request Trigger "PRA\_CH" is provided, the presence reporting area(s) for which reporting is requested shall be provided. The "praId" attribute within the PresenceInfo data type shall also be the key of the map. The "presenceState" and the "additionalPraId" attributes within the PresenceInfo data type shall not be supplied. The "praId" attribute within the PresenceInfo data type shall include the identifier of either a presence reporting area or a presence reporting area set.||
|andspDelInd|PolicyStatus|O|0\..1|Information about whether the updated ANDSP/WLANSP has been successfully delivered to the UE.|SliceAwareANDSP|
|andspInd|boolean|O|0\..1|<p>Indication of UE support of ANDSP.</p><p>True: The UE supports ANDSP; </p><p>False: The UE does not support ANDSP.</p>|UECapabilityIndication|
|pduSessions|array(PduSessionInfo)|O|1\..N|Contains the DNNs and S-NSSAIs for which LBO information is being requested. It may be provided when the "LBO\_INFO\_CH" request trigger is provided.|VPLMNSpecificURSP|
|suppFeat|SupportedFeatures|M|1|Indicates the negotiated supported features.||
|n2Pc5RsppPol|N2InfoContent|O|0\..1|The N2 PC5 policy for Ranging/SL as determined by the H-PCF.|Ranging\_SL|
|pcfUeInfo|PcfUeCallbackInfo|O|0\..1|Contains the PCF for the UE information necessary for the PCF for the PDU session to send established/terminated events notifications to the PCF for the UE.|URSPEnforcement|
|matchPdus|array(PduSessionInfo)|C|1\..N|<p>Indicates the matched PDU session(s) for which the AMF shall forward the PCF for the UE callback information in the "pcfUeInfo" attribute to the SMF. It shall be present when the "pcfUeInfo" attribute is present.</p><p>(NOTE 2)</p>|URSPEnforcement|
|<p>NOTE 1:	The "triggers" attribute shall only contain the RequestTrigger values that require explicit subscription as described in clause 5.6.3.3.</p><p>NOTE 2:	The DNN encoded within the PduSessionInfo element(s) of the "matchPdus" array may contain a full DNN or only the DNN Network Identifier. When the DNN contains the Network Identifier only, the AMF shall match a PDU session for the received Network Identifier and for any value of the Operator Identifier.</p>||||||

#### <a name="_toc28013437"></a><a name="_toc34222350"></a><a name="_toc36040533"></a><a name="_toc39134462"></a><a name="_toc43283409"></a><a name="_toc45134449"></a><a name="_toc49930049"></a><a name="_toc50024169"></a><a name="_toc51763657"></a><a name="_toc56594521"></a><a name="_toc67493863"></a><a name="_toc68169767"></a><a name="_toc73459377"></a><a name="_toc73459500"></a><a name="_toc74743037"></a><a name="_toc112918322"></a><a name="_toc120652822"></a><a name="_toc129205609"></a><a name="_toc129244428"></a><a name="_toc136530202"></a><a name="_toc136614799"></a><a name="_toc148460926"></a><a name="_toc151914923"></a><a name="_toc112918320"></a><a name="_toc120652821"></a><a name="_toc129205608"></a><a name="_toc129244427"></a><a name="_toc136530201"></a><a name="_toc136614798"></a><a name="_toc148460925"></a><a name="_toc151914922"></a><a name="_toc28013436"></a><a name="_toc34222349"></a><a name="_toc36040532"></a><a name="_toc39134461"></a><a name="_toc43283408"></a><a name="_toc45134448"></a><a name="_toc49930048"></a><a name="_toc50024168"></a><a name="_toc51763656"></a><a name="_toc56594520"></a><a name="_toc67493862"></a><a name="_toc68169766"></a><a name="_toc73459376"></a><a name="_toc73459499"></a><a name="_toc74743036"></a><a name="_toc112918321"></a><a name="_toc28013435"></a><a name="_toc34222348"></a><a name="_toc36040531"></a><a name="_toc39134460"></a><a name="_toc43283407"></a><a name="_toc45134447"></a><a name="_toc49930047"></a><a name="_toc50024167"></a><a name="_toc51763655"></a><a name="_toc56594519"></a><a name="_toc67493861"></a><a name="_toc68169765"></a><a name="_toc73459375"></a><a name="_toc73459498"></a><a name="_toc74743035"></a><a name="_toc105574946"></a><a name="_toc170121090"></a>5.6.2.3	Type PolicyAssociationRequest
**Table 5.6.2.3-1: Definition of type PolicyAssociationRequest**

|**Attribute name**|**Data type**|**P**|**Cardinality**|**Description**|**Applicability**|
| :-: | :-: | :-: | :-: | :-: | :-: |
|notificationUri|Uri|M|1|Identifies the recipient of Notifications sent by the PCF.||
|altNotifIpv4Addrs|array(Ipv4Addr)|O|1\..N|Alternate or backup IPv4 Addess(es) where to send Notifications.||
|altNotifIpv6Addrs|array(Ipv6Addr)|O|1\..N|Alternate or backup IPv6 Addess(es) where to send Notifications.||
|altNotifFqdns|array(Fqdn)|O|1\..N|Alternate or backup FQDN(s) where to send Notifications.||
|supi|Supi|M|1|Subscription Permanent Identifier. ||
|gpsi|Gpsi|C|0\..1|Generic Public Subscription Identifier. Shall be provided when available.||
|accessType|AccessType|C|0\..1|The Access Type where the served UE is camping. Shall be provided when available.||
|accessTypes|array(AccessType)|C|1\..N|The Access Type(s) where the served UE is camping. Shall be provided when available.|AccessChange|
|pei|Pei|C|0\..1|The Permanent Equipment Identifier of the served UE. Shall be provided when available.||
|userLoc|UserLocation|C|0\..1|The location of the served UE. Shall be provided when available.||
|timeZone|TimeZone|C|0\..1|The time zone of the network where the served UE is camping. Shall be provided when available.||
|servingPlmn|PlmnIdNid|C|0\..1|The serving network (a PLMN or an SNPN) where the served UE is camping. For the SNPN the NID together with the PLMN ID identifies the SNPN. Shall be provided when available.||
|ratType|RatType|C|0\..1|The RAT Type where the served UE is camping. Shall be provided when available.||
|ratTypes|array(RatType)|C|1\..N|The RAT Type(s) where the served UE is camping. Shall be provided when available.|AccessChange|
|groupIds|array(GroupId)|C|1\..N|Internal Group Identifier(s) of the served UE. Shall be provided when available.||
|hPcfId|NfInstanceId|C|0\..1|H-PCF Identifier. Shall be provided when available.||
|uePolReq|UePolicyRequest |C|0\..1|A request for UE Policies. Shall be provided when the AMF receives an "UE STATE INDICATION" message, as defined in Annex D.5.4 of 3GPP TS 24.501 [15].||
|guami|Guami|C|0\..1|The Globally Unique AMF Identifier (GUAMI) shall be provided by an AMF as NF service consumer.||
|serviceName|ServiceName|O|0\..1|If the NF service consumer is an AMF, it should provide the name of a service produced by the AMF that makes use of information received within the Npcf\_UEPolicyControl\_UpdateNotify service operation.||
|servingNfId|NfInstanceId|C|0\..1|If the NF service consumer is an AMF, it shall contain the identifier of the serving AMF.||
|pc5Capab|Pc5Capability|C|0\..1|Indicates the PC5 Capability for V2X communications supported by the UE. It shall be provided when available at the NF service consumer.|V2X|
|a2xCapab|array(A2xCapability)|C|1\..N|Indicates the A2X Capabilities for A2X communications supported by the UE. It shall be provided when available at the NF service consumer.|A2X|
|proSeCapab|array(ProSeCapability)|C|1\..N|<p>Indicates whether the UE is capable of one or more of the the following 5G ProSe Capabilities: 5G ProSe Direct Discovery, 5G ProSe Direct Communication, Layer-2 and/or Layer 3 5G ProSe UE-to-Network Relay and Layer-2 and/or Layer 3 5G ProSe Remote UE, and when the "ProSe\_Ph2" feature is supported, Layer-2 and/or Layer-3 5G ProSe UE-to-UE Relay and Layer-2 and/or Layer-3 5G ProSe End UE.</p><p>It shall be provided when available at the NF service consumer.</p>|ProSe|
|confSnssais|array(ConfiguredSnssai)|C|1\..N|<p>The Configured NSSAI for the serving PLMN, and optionally the mapped S-NSSAI value of home network corresponding to the configured S-NSSAI in the serving PLMN. </p><p>When the feature SliceAwareANDSP is supported, it shall be provided in the roaming case when available at the NF service consumer and the "n3gNodeReSel" attribute is present.</p><p>If the feature NssaiChange is supported, it shall be provided in the roaming case. (NOTE 1)</p>|SliceAwareANDSP, NssaiChange|
|n3gNodeReSel|Non3gppAccess|O|0\..1|A wrongly selected non-3gpp access node. It shall be provided when the UE has selected a non-3gpp access node that is not compatible with the Allowed NSSAI.|SliceAwareANDSP|
|satBackhaulCategory|SatelliteBackhaulCategory|C|0\..1|<p>Indicates types of the satellite backhaul based on satellite types (when satellite backhaul is used) or non-satellite backhaul (when satellite backhaul is not used).</p><p>The default value "NON\_SATELLITE" shall apply if the attribute is not present.</p><p></p>|EnSatBackhaulCategoryChg|
|vpsUePolGuidance|map(UePolicyParameters)|O|1\..N|<p>Contains the service parameter used to guide the VPLMN-specific URSP and may contain the subscription to VPLMN-specific URSP delivery outcome. The key of the map represents the AF request to guide the VPLMN-specific URSP rules.</p><p>This attribute only applies in roaming and when the V-PCF is the NF service consumer.</p>|VPLMNSpecificURSP|
|lboRoamInfo|array(LboRoamingInformation)|O|1\..N|<p>Contains LBO roaming information for DNN and S-NSSAI combination(s).</p><p>This attribute only applies in roaming and when the AMF is the NF service consumer.</p>|VPLMNSpecificURSP|
|5gsToEpsMob|boolean|O|0\..1|<p>When it is set to true, it indicates the UE Policy Association creation is triggered by a 5GS to EPS mobility scenario.</p><p>Default value is false.</p>|EpsUrsp|
|chfInfo|ChargingInformation|O|0\..1|Contains the CHF address(es), and if available, the associated CHF instance ID(s) and CHF set ID(s). (NOTE 2)|SLAMUP|
|suppFeat|SupportedFeatures|M|1|Indicates the features supported by the service consumer.||
|rangSlCapab|array(RangSLCapability)|C|1\..N|<p>Contains the Ranging/SL related UE capabilities.</p><p></p><p>It shall be provided when available at the NF service consumer.</p>|Ranging\_SL|
|<p>NOTE 1:	The "mappedHomeSnssai" attribute within the ConfiguredSnssai data type may only be provided if the "NssaiChange" feature is supported.</p><p>NOTE 2:	This attribute may only be supplied by the PCF in the response to the initial POST request that requested the creation of an individual UE policy resource.</p>||||||

#### <a name="_toc170121091"></a>5.6.2.4	Type PolicyAssociationUpdateRequest
**Table 5.6.2.4-1: Definition of type PolicyAssociationUpdateRequest**

|**Attribute name**|**Data type**|**P**|**Cardinality**|**Description**|**Applicability**||||||||
| :-: | :-: | :-: | :-: | :-: | :-: | :- | :- | :- | :- | :- | :- | :- |
|notificationUri|Uri|O|0\..1|Identifies the recipient of Notifications sent by the PCF.|||||||||
|altNotifIpv4Addrs|array(Ipv4Addr)|O|1\..N|Alternate or backup IPv4 Address(es) where to send Notifications.|||||||||
|altNotifIpv6Addrs|array(Ipv6Addr)|O|1\..N|Alternate or backup IPv6 Address(es) where to send Notifications.|||||||||
|altNotifFqdns|array(Fqdn)|O|1\..N|Alternate or backup FQDN(s) where to send Notifications.|||||||||
|triggers|array(RequestTrigger)|C|1\..N|Request Triggers that the NF service consumer observes.|||||||||
|praStatuses|map(PresenceInfo)|C|1\..N|If the Trigger "PRA\_CH" is reported, the UE presence status for tracking area for which changes of the UE presence occurred shall be provided. The "praId" attribute within the PresenceInfo data type shall also be the key of the map. The "presenceState" attribute within the PresenceInfo data type shall be supplied. The "additionalPraId" attribute within the PresenceInfo data type shall not be supplied. The "praId" attribute within the PresenceInfo data type shall include the identifier of an individual presence reporting area.|||||||||
|userLoc|UserLocation|C|0\..1|The location of the served UE shall be provided for trigger "LOC\_CH".|||||||||
|uePolDelResult|UePolicyDeliveryResult|C|0\..1|UE Policy Delivery Result. Shall be provided together with trigger "UE\_POLICY" when a "MANAGE UE POLICY COMPLETE" message or a "MANAGE UE POLICY COMMAND REJECT" message, as defined in Annex D.5 of 3GPP TS 24.501 [15], has been received by the V-PCF and is being forwarded to the H-PCF.|||||||||
|uePolTransFailNotif|UePolicyTransferFailureNotification|C|0\..1|The UE policy transfer failure notification. Shall be the provided together with trigger "UE\_POLICY" when a response with HTTP status code 4xx or 5xx as defined in clause 5.2.2.3.1.2 of 3GPP TS 29.518 [14] or a N1N2 Transfer Failure Notification as defined in clause 5.2.2.3.2 of 3GPP TS 29.518 [14] is received after the V-PCF provisioned the UE policy by invoking the Namf\_Communication\_N1N2MessageTransfer service operation to the AMF and is notifying the H-PCF.|||||||||
|uePolReq|UePolicyRequest |C|0\..1|A request for UE Policies. Shall be provided together with trigger "UE\_POLICY" when the V-PCF receives an "UE POLICY PROVISIONING REQUEST" message, as defined in clause 7.2.1.1 of 3GPP TS 24.587 [24], if the "V2X" feature is supported, and/or when the V-PCF receives an "UE POLICY PROVISIONING REQUEST" message for 5G ProSe, as defined in clause 10.4.1 of 3GPP TS 24.554 [28], if the "ProSe" feature is supported and/or when the V-PCF receives an "UE POLICY PROVISIONING REQUEST" message for A2X, as defined 3GPP TS 24.577 [32], if the "A2X" feature is supported and/or when the V-PCF receives an "UE POLICY PROVISIONING REQUEST" message for Ranging/SL, as defined 3GPP TS 24.514 [42], if the "Ranging\_SL" feature is supported..|V2X, A2X, ProSe, Ranging\_SL||||||||
|guami|Guami|C|0\..1|The Globally Unique AMF Identifier (GUAMI) shall be provided by an AMF as NF service consumer during the AMF relocation.|||||||||
|servingNfId|NfInstanceId|C|0\..1|It shall contain the identifier of the new AMF during the AMF relocation.|||||||||
|plmnId|PlmnIdNid|C|0\..1|The serving network identity (a PLMN or an SNPN) of the served UE shall be provided for trigger "PLMN\_CH".|PlmnChange||||||||
|connectState|CmState|C|0\..1|The connectivity state of the served UE shall be provided for trigger "CON\_STATE\_CH".|ConnectivityStateChange||||||||
|groupIds|array(GroupId)|C|1\..N|Internal Group Identifier(s) of the served UE. Shall be provided for trigger "GROUP\_ID\_LIST\_CHG".|GroupIdListChange||||||||
|pc5Capab|Pc5Capability|C|0\..1|<p>Indicates the PC5 Capability for V2X communications supported by the UE. It shall be provided when available at the NF service consumer.</p><p>It shall be included by the target AMF only in inter-AMF mobility scenarios and for trigger "FEAT\_RENEG". It requires that the "V2X" feature is supported.</p>|FeatureRenegotiation||||||||
|a2xCapab|array(A2xCapability)|C|1\..N|<p>Indicates the A2X capabilities supported by the UE. It shall be provided when available at the NF service consumer.</p><p>It shall be included by the target AMF only in inter-AMF mobility scenarios and for trigger "FEAT\_RENEG". It requires that the "A2X" feature is supported.</p>|FeatureRenegotiation||||||||
|proSeCapab|array(ProSeCapability)|O|1\..N|Indicates whether the UE is capable of one or more of the the following 5G ProSe Capabilities: 5G ProSe Direct Discovery, 5G ProSe Direct Communication, Layer-2 and/or Layer 3 5G ProSe UE-to-Network Relay and Layer-2 and/or Layer 3 5G ProSe Remote UE, and when the "ProSe\_Ph2" feature is supported, Layer-2 and/or Layer-3 5G ProSe UE-to-UE Relay and Layer-2 and/or Layer-3 5G ProSe End UE.|ProSe||||||||
|confSnssais|array(ConfiguredSnssai)|C|1\..N|The Configured NSSAI for the serving PLMN, and optionally the mapped S-NSSAI value of home network corresponding to the configured S-NSSAI in the serving PLMN. It shall be provided in case of roaming for trigger "CONF\_NSSAI\_CH" or for trigger "NON\_3GPP\_NODE\_RESELECTION". (NOTE)|SliceAwareANDSP, NssaiChange||||||||
|n3gNodeReSel|Non3gppAccess|O|0\..1|A wrongly selected non-3gpp access node. It shall be provided when available at the NF service consumer and the "NON\_3GPP\_NODE\_RESELECTION" trigger is reported within the "triggers" attribute. |SliceAwareANDSP||||||||
|satBackhaulCategory|SatelliteBackhaulCategory|C|0\..1|<p>Indicates types of the satellite backhaul based on satellite types (when satellite backhaul is used) or non-satellite backhaul (when satellite backhaul is not used).</p><p>It shall be provided for trigger "SAT\_CATEGORY\_CHG".</p>|EnSatBackhaulCategoryChg||||||||
|urspEnfReport|map(UrspEnforcementPduSession)|O|1\..N|<p>Represents information about the enforced URSP rule(s) in one or more PDU sessions for the affected UE. </p><p>The key of the map is a character string that represents an integer value (it may correspond with a PDU session identifier).</p><p></p><p>It shall be present when the notified policy control request trigger is "URSP\_ENF\_INFO".</p>|URSPEnforcement||||||||
|vpsUePolGuidance|map(UePolicyParameters)|O|1\..N|<p>Contains the service parameter used to guide the VPLMN-specific URSP rule determination and may contain the subscription to VPLMN-specific URSP delivery outcome. The key of the map represents the AF request to guide VPLMN-specific URSP rules.</p><p>This attribute only applies in roaming and when the V-PCF is the NF service consumer.</p>|VPLMNSpecificURSP||||||||
|lboRoamInfo|array(LboRoamingInformation)|O|1\..N|<p>Contains LBO roaming information for a DNN and S-NSSAI combination(s).</p><p>This attribute only applies in roaming and when the AMF is the NF service consumer.</p>|VPLMNSpecificURSP||||||||
|accessTypes|array(AccessType)|C|1\..N|The Access Type(s) where the served UE is camping. It shall be provided for trigger "ACCESS\_TYPE\_CH" when the access type(s) changes or when the access type(s) is initially reported as consequence of the provisioning of the trigger.|AccessChange||||||||
|ratTypes|array(RatType)|C|1\..N|The RAT Type(s), if available, for the reported "accessTypes" where the served UE is camping. It shall be provided, if available, for trigger "ACCESS\_TYPE\_CH" when the access type(s) changes or when the access type(s) is initially reported as consequence of the provisioning of the trigger.|AccessChange||||||||
|suppFeat|SupportedFeatures|C|0\..1|Indicates the features supported by the NF service consumer.<br>It shall be included by the target AMF in inter-AMF mobility scenarios for trigger "FEAT\_RENEG".|FeatureRenegotiation||||||||
|rangSlCapab|array(RangSLCapability)|O|1\..N|Contains the Ranging/SL related UE capabilities.|Ranging\_SL||||||||
|NOTE:	The "mappedHomeSnssai" attribute within the ConfiguredSnssai data type may only be provided if the "NssaiChange" feature is supported.|||||||||||||

#### <a name="_toc28013438"></a><a name="_toc34222351"></a><a name="_toc36040534"></a><a name="_toc39134463"></a><a name="_toc43283410"></a><a name="_toc45134450"></a><a name="_toc49930050"></a><a name="_toc50024170"></a><a name="_toc51763658"></a><a name="_toc56594522"></a><a name="_toc67493864"></a><a name="_toc68169768"></a><a name="_toc73459378"></a><a name="_toc73459501"></a><a name="_toc74743038"></a><a name="_toc112918323"></a><a name="_toc120652824"></a><a name="_toc114078875"></a><a name="_toc129205610"></a><a name="_toc129244429"></a><a name="_toc136530203"></a><a name="_toc136614800"></a><a name="_toc148460927"></a><a name="_toc151914924"></a><a name="_toc170121092"></a>5.6.2.5	Type PolicyUpdate
**Table 5.6.2.5-1: Definition of type PolicyUpdate**

|**Attribute name**|**Data type**|**P**|**Cardinality**|**Description**|**Applicability**||||||||
| :-: | :-: | :-: | :-: | :-: | :-: | :- | :- | :- | :- | :- | :- | :- |
|resourceUri|Uri|M|1|<p>The resource URI of the individual UE policy association related to the notification.</p><p>(NOTE 2)</p>|||||||||
|uePolicy|UePolicy|O|0\..1|The UE policy as determined by the H-PCF.|||||||||
|n2Pc5Pol|N2InfoContent|O|0\..1|The N2 PC5 policy for V2X communications as determined by the H-PCF.|V2X||||||||
|n2Pc5PolA2x|N2InfoContent|O|0\..1|The N2 PC5 policy for A2X communications as determined by the H-PCF.|A2X||||||||
|n2Pc5ProSePol|N2InfoContent|O|0\..1|The N2 PC5 policy for 5G ProSe as determined by the PCF.|ProSe||||||||
|triggers|array(RequestTrigger)|O|1\..N|<p>Request Triggers that the PCF subscribes.</p><p></p><p>(NOTE 1)</p>|||||||||
|pras|map(PresenceInfoRm)|C|1\..N|If the Trigger "PRA\_CH" is provided or if that trigger was already set but the requested presence reporting areas need to be changed, the presence reporting area(s) for which reporting is requested shall be provided. The "praId" attribute within the PresenceInfoRm data type shall also be the key of the map. The "presenceState" attribute within the PresenceInfo data type shall not be supplied. The "praId" attribute within the PresenceInfo data type shall include the identifier of either a presence reporting area or a presence reporting area set.|PresenceInfo||||||||
|andspDelInd|PolicyStatus|O|0\..1|Information about whether the updated ANDSP/WLANSP has been successfully delivered to the UE.|SliceAwareANDSP||||||||
|delivReport|map(UePolicyNotification)|O|1\..N|<p>Contains the delivery outcome of VPLMN-Specific URSP rules. It may be included if the V-PCF indicated the subscription to delivery outcome events as described in clause 4.2.2.2.3.2.</p><p>The key of the map represents the AF request of the corresponding subscription, i.e. its value shall match the key that was previously provided by the V-PCF in the “vpsUePolGuidance“ attribute.</p>|VPLMNSpecificURSP||||||||
|pduSessions|array(PduSessionInfo)|O|1\..N|Contains the list of the DNN and SNSSAI pairs for which LBO information is being requested. It may be provided when the "LBO\_INFO\_CH" request trigger is provided.|VPLMNSpecificURSP||||||||
|pcfUeInfo|PcfUeCallbackInfo|O|0\..1|Contains the PCF for the UE callback information necessary for the PCF for the PDU session to send established/terminated events notifications to the PCF for the UE.|URSPEnforcement||||||||
|matchPdus|array(PduSessionInfo)|O|1\..N|<p>Indicates the matched PDU session(s) for which the AMF shall forward the PCF for the UE information in the "pcfUeInfo" attribute to the SMF. It shall be present when the "pcfUeInfo" attribute is present.</p><p>(NOTE 3)</p>|URSPEnforcement||||||||
|suppFeat|SupportedFeatures|C|0\..1|Indicates the negotiated supported features.<br>It shall be included in the HTTP POST response when the NF service consumer provided the supported features in the HTTP POST request.|FeatureRenegotiation||||||||
|n2Pc5RsppPol|N2InfoContent|O|0\..1|The N2 PC5 policy for Ranging/SL as determined by the H-PCF.|Ranging\_SL||||||||
|<p>NOTE 1:	The "triggers" attribute shall only contain the RequestTrigger values that require explicit subscription as described in clause 5.6.3.3.</p><p>NOTE 2:	When the PolicyUpdate data type is used in a policy update notify service operation, either the complete resource URI included in the "resourceUri" attribute or the "apiSpecificResourceUriPart" component (see clause 5.1) of the resource URI included in the "resourceUri" attribute may be used by the NF service consumer (e.g. AMF) for the identification of the Individual UE Policy Association resource related to the notification.</p><p>NOTE 3:	The DNN encoded within the PduSessionInfo element(s) of the "matchPdus" array may contain a full DNN or only the DNN Network Identifier. When the DNN contains the Network Identifier only, the AMF shall match a PDU session for the received Network Identifier and for any value of the Operator Identifier.</p>|||||||||||||

#### <a name="_toc129205611"></a><a name="_toc129244430"></a><a name="_toc136530204"></a><a name="_toc136614801"></a><a name="_toc148460928"></a><a name="_toc151914925"></a><a name="_toc170121093"></a>5.6.2.6	Type TerminationNotification
**Table 5.6.2.6-1: Definition of type TerminationNotification**

|**Attribute name**|**Data type**|**P**|**Cardinality**|**Description**|**Applicability**|
| :-: | :-: | :-: | :-: | :-: | :-: |
|resourceUri|Uri|M|1|<p>The resource URI of the individual UE policy association related to the notification.</p><p>(NOTE)</p>||
|cause|PolicyAssociationReleaseCause|M|1|The cause why the PCF requests the termination of the policy association.||
|NOTE:	Either the complete resource URI included in the "resourceUri" attribute or the "apiSpecificResourceUriPart" component (see clause 5.1) of the resource URI included in the "resourceUri" attribute may be used by the NF service consumer (e.g. AMF) for the identification of the Individual UE Policy Association resource related to the termination notification.||||||

#### <a name="_toc28013439"></a><a name="_toc34222352"></a><a name="_toc36040535"></a><a name="_toc39134464"></a><a name="_toc43283411"></a><a name="_toc45134451"></a><a name="_toc49930051"></a><a name="_toc50024171"></a><a name="_toc51763659"></a><a name="_toc56594523"></a><a name="_toc67493865"></a><a name="_toc68169769"></a><a name="_toc73459379"></a><a name="_toc73459502"></a><a name="_toc74743039"></a><a name="_toc112918324"></a><a name="_toc120652825"></a><a name="_toc129205612"></a><a name="_toc129244431"></a><a name="_toc136530205"></a><a name="_toc136614802"></a><a name="_toc148460929"></a><a name="_toc151914926"></a><a name="_toc170121094"></a>5.6.2.7	Type UePolicyTransferFailureNotification
**Table 5.6.2.7-1: UEPolicyTransferFailureNotification**

|**Attribute name**|**Data type**|**P**|**Cardinality**|**Description**|**Applicability**|
| :-: | :-: | :-: | :-: | :-: | :-: |
|cause|UePolicyTransferFailureCause|M|1|<p>Indicates the reason why the UE policy could not be transferred by the AMF.</p><p>When the feature "EnErrorHandling" is supported, the "cause" attribute may include the enumeration values defined in the "N1N2MessTransferErrorReply" data type.</p>||
|retryAfter|Uinteger|O|0\..1|The V-PCF may include this IE if the AMF requests to stop sending the N1N2MessageTransfer before timeout of the indicated time period.|EnErrorHandling|
|ptis|array(Uinteger)|M|1\..N|Contains a list of PTI assigned by the H-PCF corresponding to the UE policy(s) which could not be transferred by the AMF.||

#### <a name="_toc28013440"></a><a name="_toc34222353"></a><a name="_toc36040536"></a><a name="_toc39134465"></a><a name="_toc43283412"></a><a name="_toc45134452"></a><a name="_toc49930052"></a><a name="_toc50024172"></a><a name="_toc51763660"></a><a name="_toc56594525"></a><a name="_toc67493867"></a><a name="_toc68169771"></a><a name="_toc73459381"></a><a name="_toc73459504"></a><a name="_toc74743041"></a><a name="_toc112918326"></a><a name="_toc28012237"></a><a name="_toc34123090"></a><a name="_toc36038040"></a><a name="_toc38875422"></a><a name="_toc43191903"></a><a name="_toc45133298"></a><a name="_toc51316802"></a><a name="_toc51761982"></a><a name="_toc56594524"></a><a name="_toc67493866"></a><a name="_toc68169770"></a><a name="_toc73459380"></a><a name="_toc73459503"></a><a name="_toc74743040"></a><a name="_toc112918325"></a><a name="_toc120652826"></a><a name="_toc129205613"></a><a name="_toc129244432"></a><a name="_toc136530206"></a><a name="_toc136614803"></a><a name="_toc148460930"></a><a name="_toc151914927"></a><a name="_toc170121095"></a>5.6.2.8	Type UeRequestedValueRep
**Table 5.6.2.8-1: Definition of type UeRequestedValueRep**

|**Attribute name**|**Data type**|**P**|**Cardinality**|**Description**|**Applicability**||||||||
| :-: | :-: | :-: | :-: | :-: | :-: | :- | :- | :- | :- | :- | :- | :- |
|userLoc|UserLocation|C|0\..1|The location of the served UE is camping shall be provided for trigger "LOC\_CH".|||||||||
|praStatuses|map(PresenceInfo)|C|1\..N|<p>The UE presence statuses for tracking areas shall be provided for trigger "PRA\_CH". </p><p>The "praId" attribute within the PresenceInfo data type shall also be the key of the map.</p>|||||||||
|plmnId|PlmnIdNid|C|0\..1|The serving network identity (a PLMN or an SNPN) of the served UE shall be provided for trigger "PLMN\_CH".|PlmnChange||||||||
|connectState|CmState|C|0\..1|The connectivity state of the served UE. It shall be provided for trigger "CON\_STATE\_CH".|ConnectivityStateChange||||||||
|satBackhaulCategory|SatelliteBackhaulCategory|C|0\..1|Indicates types of the satellite backhaul based on satellite types (when satellite backhaul is used) or non-satellite backhaul (when satellite backhaul is not used). It shall be provided for trigger "SAT\_CATEGORY\_CHG".|EnSatBackhaulCategoryChg||||||||
|urspEnfReport|map(UrspEnforcementPduSession)|C|1\..N|<p>Represents information about the enforced URSP rule(s) in one or more PDU sessions for the affected UE. </p><p></p><p>The key of the map is a character string that represents an integer value (it may correspond with a PDU session identifier).</p><p></p><p>It shall be present when the notified policy control request trigger is "URSP\_ENF\_INFO".</p>|URSPEnforcement||||||||
|lboRoamInfo|array(LboRoamingInformation)|C|1\..N|Contains a list of LBO roaming information for a DNN and S-NSSAI combination. It shall be provided for trigger "LBO\_INFO\_CH".|VPLMNSpecificURSP||||||||
|confSnssais|array(ConfiguredSnssai)|C|1\..N|<p><a name="_hlk143553937"></a>The Configured NSSAI for the serving PLMN, and the mapped S-NSSAI value of home network corresponding to the configured S-NSSAI in the serving PLMN. </p><p>It shall be provided for trigger "CONF\_NSSAI\_CH".</p>|NssaiChange||||||||
|accessTypes|array(AccessType)|C|1\..N|The Access Type(s) where the served UE is camping. Shall be provided for trigger "ACCESS\_TYPE\_CH".|AccessChange||||||||
|ratTypes|array(RatType)|C|1\..N|The RAT Type(s), if available, for the reported "accessTypes" where the served UE is camping. It shall be provided, if available, for trigger "ACCESS\_TYPE\_CH.|AccessChange||||||||

#### <a name="_toc120652827"></a><a name="_toc129205614"></a><a name="_toc129244433"></a><a name="_toc136530207"></a><a name="_toc136614804"></a><a name="_hlk140686510"></a><a name="_toc148460931"></a><a name="_toc151914928"></a><a name="_toc170121096"></a>5.6.2.9	Type UePolicyParameters
**Table 5.6.2.9-1: Definition of type UePolicyParameters**

|**Attribute name**|**Data type**|**P**|**Cardinality**|**Description**|**Applicability**|
| :-: | :-: | :-: | :-: | :-: | :-: |
|urspGuidance|array(UrspRuleRequest)|O|1\..N|Contains the service parameter used to guide the VPLMN-specific URSP.||
|deliveryEvents|array(Event)|O|1\..N|<p>Identifies the AF subscribed event(s) related to AF provisioned guidance for VPLMN-specific URSP rules.</p><p>(NOTE)</p>||
|NOTE: 	In this release of the specification, only the "SUCCESS\_UE\_POL\_DEL\_SP" and "UNSUCCESS\_UE\_POL\_DEL\_SP" events apply.||||||

#### <a name="_toc148460932"></a><a name="_toc151914929"></a><a name="_toc170121097"></a>5.6.2.10	Type LboRoamingInformation
**Table 5.6.2.10-1: Definition of type LboRoamingInformation**

|**Attribute name**|**Data type**|**P**|**Cardinality**|**Description**|**Applicability**|
| :-: | :-: | :-: | :-: | :-: | :-: |
|lboRoamAllowed|boolean|O|0\..1|<p>Indicates whether local breakout for the DNN and S-NSSAI is allowed when roaming.</p><p>true: allowed</p><p>false: not allowed.</p><p>If the attribute is absent it means not allowed.</p>||
|dnn|Dnn|M|1|Data Network Name with Network Identifier only.||
|snssai|Snssai|M|1|S-NSSAI.||

#### <a name="_toc148460933"></a><a name="_toc151914930"></a><a name="_toc170121098"></a>5.6.2.11	Type UrspEnforcementPduSession
**Table 5.6.2.11-1: Definition of type UrspEnforcementPduSession**

|**Attribute name**|**Data type**|**P**|**Cardinality**|**Description**|**Applicability**|
| :-: | :-: | :-: | :-: | :-: | :-: |
|urspEnfInfo|UrspEnforcementInfo|M|1|<p>Represents UE provided information about the enforced URSP rule(s) in one PDU session. </p><p></p><p></p>||
|sscMode|SscMode|C|0\..1|<p>SSC Mode of the PDU session.</p><p></p><p>It shall be provided when URSP rule enforcement information is provided for the first time. </p><p></p>||
|ueReqDnn|Dnn|C|0\..1|<p>UE requested DNN.</p><p></p><p>It shall be provided when URSP rule enforcement information is provided for the first time, if available and different from the selected DNN.</p><p></p>||
|ueReqPduSessionType|PduSessionType|O|0\..1|<p>UE requested PDU session Type.</p><p></p><p>It shall be provided when URSP rule enforcement information is provided for the first time.</p>||
|dnn|Dnn|C|0\..1|<p>Selected DNN.</p><p></p><p>It shall be provided when URSP rule enforcement information is provided for the first time.</p><p></p>||
|snssai|Snssai|C|0\..1|<p>S-NSSAI of the HPLMN.</p><p></p><p>It shall be provided when URSP rule enforcement information is provided for the first time.</p><p></p>||

#### <a name="_toc148460934"></a><a name="_toc151914931"></a><a name="_toc170121099"></a>5.6.2.12	Type UePolicyNotification
**Table 5.6.2.12-1: Definition of type UePolicyNotification**

|**Attribute name**|**Data type**|**P**|**Cardinality**|**Description**|**Applicability**|
| :-: | :-: | :-: | :-: | :-: | :-: |
|eventNotifs|array(PcEventNotification)|M|1\..N|<p>Represents the events to be reported according to the subscription to delivery outcome events as described in clause 4.2.2.2.3.2.</p><p>(NOTE)</p>||
|NOTE: 	In this release of the specification, only the "SUCCESS\_UE\_POL\_DEL\_SP" and "UNSUCCESS\_UE\_POL\_DEL\_SP" events apply for the "events" attribute within the PcEventNotification data type.||||||

### <a name="_toc151914932"></a><a name="_toc170121100"></a>5.6.3	Simple data types and enumerations
#### <a name="_toc28013441"></a><a name="_toc34222354"></a><a name="_toc36040537"></a><a name="_toc39134466"></a><a name="_toc43283413"></a><a name="_toc45134453"></a><a name="_toc49930053"></a><a name="_toc50024173"></a><a name="_toc51763661"></a><a name="_toc56594526"></a><a name="_toc67493868"></a><a name="_toc68169772"></a><a name="_toc73459382"></a><a name="_toc73459505"></a><a name="_toc74743042"></a><a name="_toc112918327"></a><a name="_toc120652828"></a><a name="_toc129205615"></a><a name="_toc129244434"></a><a name="_toc136530208"></a><a name="_toc136614805"></a><a name="_toc148460935"></a><a name="_toc151914933"></a><a name="_toc170121101"></a>5.6.3.1	Introduction
This clause defines simple data types and enumerations that can be referenced from data structures defined in the previous clauses.
#### <a name="_toc28013442"></a><a name="_toc34222355"></a><a name="_toc36040538"></a><a name="_toc39134467"></a><a name="_toc43283414"></a><a name="_toc45134454"></a><a name="_toc49930054"></a><a name="_toc50024174"></a><a name="_toc51763662"></a><a name="_toc56594527"></a><a name="_toc67493869"></a><a name="_toc68169773"></a><a name="_toc73459383"></a><a name="_toc73459506"></a><a name="_toc74743043"></a><a name="_toc112918328"></a><a name="_toc120652829"></a><a name="_toc129205616"></a><a name="_toc129244435"></a><a name="_toc136530209"></a><a name="_toc136614806"></a><a name="_toc148460936"></a><a name="_toc151914934"></a><a name="_toc170121102"></a>5.6.3.2	Simple data types
The simple data types defined in table 5.6.3.2-1 shall be supported.

**Table 5.6.3.2-1: Simple data types**

|**Type Name**|**Type Definition**|**Description**|**Applicability**|
| :-: | :-: | :-: | :-: |
|UePolicy|Bytes|"MANAGE UE POLICY COMMAND" message content, as defined in Table D.5.1.1.1 of 3GPP TS 24.501 [15]||
|UePolicyDeliveryResult|Bytes|"MANAGE UE POLICY COMPLETE" message content, as defined in Table D.5.2.1.1 of 3GPP TS 24.501 [15], or "MANAGE UE POLICY COMMAND REJECT" message content, as defined in Table D.5.3.1.1 of 3GPP TS 24.501 [15]||
|UePolicyRequest|Bytes|"UE STATE INDICATION" message content, as defined in Table D.5.4.1.1 of 3GPP TS 24.501 [15] or "UE POLICY PROVISIONING REQUEST" message content, as defined in clause 7.2.1.1 of 3GPP TS 24.587 [24].||

#### <a name="_toc28013443"></a><a name="_toc34222356"></a><a name="_toc36040539"></a><a name="_toc39134468"></a><a name="_toc43283415"></a><a name="_toc45134455"></a><a name="_toc49930055"></a><a name="_toc50024175"></a><a name="_toc51763663"></a><a name="_toc56594528"></a><a name="_toc67493870"></a><a name="_toc68169774"></a><a name="_toc73459384"></a><a name="_toc73459507"></a><a name="_toc74743044"></a><a name="_toc112918329"></a><a name="_toc120652830"></a><a name="_toc129205617"></a><a name="_toc129244436"></a><a name="_toc136530210"></a><a name="_toc136614807"></a><a name="_toc148460937"></a><a name="_toc151914935"></a><a name="_toc170121103"></a>5.6.3.3	Enumeration: <a name="_hlk511068497"></a>RequestTrigger
The enumeration RequestTrigger represents the possible Policy Control Request Triggers. It shall comply with the provisions defined in table 5.6.3.3-1.

**Table 5.6.3.3-1: Enumeration RequestTrigger**

|**Enumeration value**|**Description**|**Applicability**|||||||||
| :-: | :-: | :-: | :- | :- | :- | :- | :- | :- | :- | :- |
|LOC\_CH|Location change (tracking area): the tracking area of the UE has changed. (NOTE)||||||||||
|PRA\_CH|Change of UE presence in PRA: the AMF reports the current presence status of the UE in a Presence Reporting Area, and notifies that the UE enters/leaves the Presence Reporting Area. (NOTE)||||||||||
|UE\_POLICY|<p>A "MANAGE UE POLICY COMPLETE" message, a "MANAGE UE POLICY COMMAND REJECT" message, as defined in Annex D.5 of 3GPP TS 24.501 [15] has been received by the V-PCF and is being forwarded to the H-PCF, or has been received by a PCF for a PDU session and is being forwarded to the (V-)PCF (and then from the V-PCF to the H-PCF) when the "EpsUrsp" feature is supported. A Namf\_Communication\_N1N2MessageTransfer failure response as defined in clause 5.2.2.3.1.2 of 3GPP TS 29.518 [14], an N1N2 Transfer Failure Notification as defined in clause 5.2.2.3.2 of 3GPP TS 29.518 [14], a UE Policy transfer failure is notifying to the H-PCF, or a UE Policy transfer failure is notifying to the (V-)PCF when the "EpsUrsp" feature is supported. </p><p>When the "ProSe" feature is supported it indicates that a "UE POLICY PROVISIONING REQUEST" message, as defined in clause 10.4 of 3GPP TS 24.554 [28] has been received by the V-PCF and is being forwarded to the H-PCF.</p><p>When the "V2X" feature is supported it indicates that a "UE POLICY PROVISIONING REQUEST" message, as defined in clause 7.2 of 3GPP TS 24.587 [24] has been received by the V-PCF and is being forwarded to the H-PCF.</p><p>When the "A2X" feature is supported it indicates that a "UE POLICY PROVISIONING REQUEST" message, as defined in 3GPP TS 24.577 [32] has been received by the V-PCF and is being forwarded to the H-PCF.</p><p>When the "Ranging\_SL" feature is supported it indicates that a "UE POLICY PROVISIONING REQUEST" message, as defined in 3GPP TS 24.514 [42] has been received by the V-PCF and is being forwarded to the H-PCF.</p><p>This event does not require a subscription and is only applicable for the VPCF as NF service consumer and the HPCF as NF service producer or a PCF for a PDU session as NF service consumer and the (V-)PCF as NF service producer when the “EpsUrsp” feature is supported.</p>||||||||||
|PLMN\_CH|PLMN change: the serving network (a PLMN or an SNPN) of UE has changed. (NOTE)|PlmnChange|||||||||
|CON\_STATE\_CH|Connectivity state change: the connectivity state of UE has changed. (NOTE)|ConnectivityStateChange|||||||||
|GROUP\_ID\_LIST\_CHG|UE Internal Group Identifier(s) has changed: the AMF reports that UDM provided list of group Ids has changed. This policy control request trigger does not require a subscription.|GroupIdListChange|||||||||
|UE\_CAP\_CH|UE Capabilities change: the UE provided 5G ProSe capabilities have changed. This policy control request trigger does not require subscription.|ProSe|||||||||
|SAT\_CATEGORY\_CHG|<a name="_hlk69488065"></a>Satellite Backhaul Category change: the AMF has detected a change between different satellite backhaul category, or a change between satellite and non-satellite backhaul. (NOTE)|EnSatBackhaulCategoryChg|||||||||
|CONF\_NSSAI\_CH|<p>Configured NSSAI change: the configured NSSAI has changed. This policy control request trigger only applies in roaming scenarios when the NF service consumer is the AMF.</p><p>(NOTE)</p>|NssaiChange|||||||||
|NON\_3GPP\_NODE\_RESELECTION|Wrong TNGF or N3IWF: the UE has connected to a wrong non-3GPP access node that does not match its subscribed S-NSSAI(s). This policy control request trigger does not require a subscription.|SliceAwareANDSP|||||||||
|FEAT\_RENEG|The target AMF determines feature re-negotiation is required. This policy control request trigger does not require subscription.|FeatureRenegotiation|||||||||
|URSP\_ENF\_INFO|<p><a name="_hlk142241358"></a>The V-PCF has received URSP rule enforcement information about the enforced URSP rule(s) in one or more PDU sessions. This trigger only applies in roaming scenarios and to the V-PCF.</p><p>(NOTE)</p>|<p>URSPEnforcement</p><p></p>|||||||||
|LBO\_INFO\_CH|<p><a name="_hlk142311541"></a>LBO information change: The AMF reports LBO roaming allowed or not allowed for the requested DNN(s) and S-NSSAI(s). This policy control request trigger only applies in roaming scenarios when the NF service consumer is the AMF.</p><p>(NOTE)</p>|VPLMNSpecificURSP|||||||||
|ACCESS\_TYPE\_CH|<p>Access Type change: The registered access type and RAT type has changed, an access type and RAT type is added or removed.</p><p>(NOTE)</p>|AccessChange|||||||||
|NOTE:	The report of this trigger includes reporting the current value at the time the trigger is provisioned during the update or update notification of the policy association.|||||||||||

#### <a name="_toc28013444"></a><a name="_toc34222357"></a><a name="_toc36040540"></a><a name="_toc39134469"></a><a name="_toc43283416"></a><a name="_toc45134456"></a><a name="_toc49930056"></a><a name="_toc50024176"></a><a name="_toc51763664"></a><a name="_toc56594529"></a><a name="_toc67493871"></a><a name="_toc68169775"></a><a name="_toc73459385"></a><a name="_toc73459508"></a><a name="_toc74743045"></a><a name="_toc112918330"></a><a name="_toc120652831"></a><a name="_toc129205618"></a><a name="_toc129244437"></a><a name="_toc136530211"></a><a name="_toc136614808"></a><a name="_toc148460938"></a><a name="_toc151914936"></a><a name="_toc170121104"></a>5.6.3.4	Enumeration: PolicyAssociationReleaseCause
The enumeration PolicyAssociationReleaseCause represents the cause why the PCF requests the termination of the policy association. It shall comply with the provisions defined in table 5.6.3.4-1.

**Table 5.6.3.4-1: Enumeration PolicyAssociationReleaseCause**

|**Enumeration value**|**Description**|**Applicability**|
| :-: | :-: | :-: |
|UNSPECIFIED|This value is used for unspecified reasons.||
|UE\_SUBSCRIPTION|This value is used to indicate that the policy association needs to be terminated because the subscription of UE has changed (e.g. was removed).||
|INSUFFICIENT\_RES|This value is used to indicate that the server is overloaded and needs to abort the policy association.||

#### <a name="_toc34222358"></a><a name="_toc36040541"></a><a name="_toc39134470"></a><a name="_toc43283417"></a><a name="_toc45134457"></a><a name="_toc49930057"></a><a name="_toc50024177"></a><a name="_toc51763665"></a><a name="_toc56594530"></a><a name="_toc67493872"></a><a name="_toc68169776"></a><a name="_toc73459386"></a><a name="_toc73459509"></a><a name="_toc74743046"></a><a name="_toc112918331"></a><a name="_toc120652832"></a><a name="_toc129205619"></a><a name="_toc129244438"></a><a name="_toc136530212"></a><a name="_toc136614809"></a><a name="_toc148460939"></a><a name="_toc151914937"></a><a name="_toc170121105"></a>5.6.3.5	Enumeration: Pc5Capability
The enumeration Pc5Capability indicates the specific PC5 RAT(s) which the UE supports for V2X communication over PC5 reference point. It shall comply with the provisions defined in table 5.6.3.5-1.

**Table 5.6.3.5-1: Enumeration Pc5Capability**

|**Enumeration value**|**Description**|**Applicability**|
| :-: | :-: | :-: |
|LTE\_PC5|This value is used to indicate that the UE supports PC5 LTE RAT for V2X communication over PC5 reference point.||
|NR\_PC5|This value is used to indicate that the UE supports PC5 LTE RAT for V2X communication over PC5 reference point.||
|LTE\_NR\_PC5|This value is used to indicate that the UE supports both PC5 LTE and NR RAT for V2X communication over PC5 reference point.||

#### <a name="_toc73459510"></a><a name="_toc74743047"></a><a name="_toc112918332"></a><a name="_toc120652833"></a><a name="_toc129205620"></a><a name="_toc129244439"></a><a name="_toc136530213"></a><a name="_toc136614810"></a><a name="_toc148460940"></a><a name="_toc151914938"></a><a name="_toc170121106"></a>5.6.3.6	Enumeration: ProSeCapability
This enumeration indicates the 5G ProSe capabilities. It shall comply with the provisions defined in table 5.6.3.6-1.

**Table 5.6.3.6-1: Enumeration ProSeCapability**

|**Enumeration value**|**Description**|**Applicability**|
| :-: | :-: | :-: |
|PROSE\_DD|This value is used to indicate that 5G ProSe Direct Discovery is supported by the UE.||
|PROSE\_DC|This value is used to indicate that 5G ProSe Direct Communication is supported by the UE.||
|PROSE\_L2\_U2N\_RELAY|This value is used to indicate that Layer-2 5G ProSe UE-to-Network Relay is supported by the UE.||
|PROSE\_L3\_U2N\_RELAY|This value is used to indicate that Layer-3 5G ProSe UE-to-Network Relay is supported by the UE.||
|PROSE\_L2\_REMOTE\_UE|This value is used to indicate that Layer-2 5G ProSe Remote UE is supported by the UE.||
|PROSE\_L3\_REMOTE\_UE|This value is used to indicate that Layer-3 5G ProSe Remote UE is supported by the UE.||
|PROSE\_L2\_U2U\_RELAY|This value is used to indicate that Layer-2 5G ProSe UE-to-UE Relay is supported by the UE.|ProSe\_Ph2|
|PROSE\_L3\_U2U\_RELAY|This value is used to indicate that Layer-3 5G ProSe UE-to-UE Relay is supported by the UE.|ProSe\_Ph2|
|PROSE\_L2\_END\_UE|This value is used to indicate that Layer-2 5G ProSe End UE is supported by the UE.|ProSe\_Ph2|
|PROSE\_L3\_END\_UE|This value is used to indicate that Layer-3 5G ProSe End UE is supported by the UE.|ProSe\_Ph2|

5\.6.3.7	Enumeration: Non3gppAccess

The enumeration Non3gppAccess represents the possible Non-3gpp access nodes. It shall comply with the provisions defined in table 5.6.3.7-1.

**Table 5.6.3.7-1: Non3gppAccess**

|**Enumeration value**|**Description**|**Applicability**|
| :-: | :-: | :-: |
|N3IWF|Non-3gpp Interworking Function||
|TNGF|Trusted Non-3GPP Gateway Function||

#### <a name="_toc170121107"></a>5.6.3.8	Void
#### <a name="_toc170121108"></a>5.6.3.9	Enumeration: N1N2MessTransferErrorReply
The enumeration N1N2MessTransferErrorReply represents the possible errors the V-PCF may send to the H-PCF when the V-PCF receives from the AMF an error reply to the N1N2MessageTransfer request. It shall comply with the provisions defined table 5.6.3.9-1.

**Table 5.6.3.9-1: N1N2MessTransferErrorReply**

|**Enumeration value**|**Description**|**Applicability**|
| :-: | :-: | :-: |
|UE\_NOT\_REACHABLE|The UE is not reachable for paging.||
|UNSPECIFIED|Unspecified error.||

#### <a name="_toc151914939"></a><a name="_toc170121109"></a>5.6.3.10	Enumeration: RangSLCapability
The enumeration RangSLCapability represents the Ranging and Sidelink Capability. It shall comply with the provisions defined in table 5.6.3.10-1.

**Table 5.6.3.10-1: Enumeration RangSLCapability**

|**Enumeration value**|**Description**|**Applicability**|
| :-: | :-: | :-: |
|PC5\_RANGING\_SL|Indicates that the PC5 Capability for Ranging and Sidelink is supported by the UE.||

#### <a name="_toc170121110"></a>5.6.3.11	Enumeration: PolicyStatus
The enumeration PolicyStatus represents the configuration status of a UE Policy in the UE. It shall comply with the provisions defined in table 5.6.3.11-1.

**Table 5.6.3.11-1: PolicyStatus**

|**Enumeration value**|**Description**|**Applicability**|
| :-: | :-: | :-: |
|CONFIGURED|The UE Policy is configured in the UE.||
|NOT\_CONFIGURED|The UE Policy is not configured in the UE.||

### <a name="_toc170121111"></a>5.6.4	Data types describing alternative data types or combinations of data types
#### <a name="_toc145707591"></a><a name="_toc151914940"></a><a name="_toc170121112"></a>5.6.4.1	Type: UePolicyTransferFailureCause
**Table 5.6.4.1-1: Definition of type UePolicyTransferFailureCause as a list of non-exclusive alternatives**

|**Data type**|**Cardinality**|**Description**|**Applicability**|
| :-: | :-: | :-: | :-: |
|N1N2MessageTransferCause|0\..1|The failure causes notified by the AMF within the N1 Message Transfer Failure notification.||
|N1N2MessTransferErrorReply|0\..1|Error reply the AMF may indicate within the response to N1N2MessageTransfer request.||

#### <a name="_toc170121113"></a>5.6.3.12	Enumeration: A2xCapability
The enumeration A2xCapability indicates the A2X capabilities the UE supports for A2X communication. It shall comply with the provisions defined in table 5.6.3.12-1.

**Table 5.6.3.12-1: Enumeration A2xCapability**

|**Enumeration value**|**Description**|**Applicability**|
| :-: | :-: | :-: |
|EUTRA\_PC5|This value is used to indicate that the UE supports PC5 E-UTRA RAT for A2X communication over PC5 reference point.||
|NR\_PC5|This value is used to indicate that the UE supports PC5 NR RAT for A2X communication over PC5 reference point.||
|UU|This value is used to indicate that the UE supports A2X communication over Uu reference point.||


