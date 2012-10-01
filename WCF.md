# WCF #
-----------------------------------------------------------

## Sessions and Instancing ##

**PerCall** - instance per call (default value). Allways for *basicHttpBinding*

**PerSession** - instance per client, lives in memory some time (10 mins by default)
	Closed by client termination call or timeout. If there is a timeout, next client
	call will receive *CommunicationObjectFaultedException*

	You can change timeout value. Can't be used for *basicHttpBinding*