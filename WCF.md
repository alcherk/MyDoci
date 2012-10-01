# WCF #
-----------------------------------------------------------

## Sessions and Instancing ##

*PerCall* - instance на каждый вызов (обычно по default). Всегда для *basicHttpBinding*

*PerSession* - instance на каждого клиента, живет в памяти некоторое время (10 минут по дефолту)
	Завершается по команде от клиента или по timeout. Если по timeout, при следующем обращении
	клиенту отдаст *CommunicationObjectFaultedException*
