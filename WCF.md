# WCF #
-----------------------------------------------------------

## Sessions and Instancing ##

*PerCall* - instance per call (default value). Allways for *basicHttpBinding*

*PerSession* - instance на каждого клиента, живет в памяти некоторое время (10 минут по дефолту)
	Завершается по команде от клиента или по timeout. Если по timeout, при следующем обращении
	клиенту отдаст *CommunicationObjectFaultedException*
