# WCF #
-----------------------------------------------------------

## Sessions and Instancing ##

* **PerCall**. Instance per call (default value). Allways for *basicHttpBinding*

* **PerSession**. Instance per client, lives in memory some time (10 mins by default). Closed by client termination call or timeout. If there is a timeout, next client call will receive *CommunicationObjectFaultedException*. Caller or server can change timeout value. If the times are different, the shortest configured timeout prevails. Can't be used for *basicHttpBinding*

* **Singleton mode**. Only one instance of the service’s implementation class is created. The instance lives forever (or
close to forever) and is disposed of only when the host process shuts down. Some kind of mess with sessions if they are required.