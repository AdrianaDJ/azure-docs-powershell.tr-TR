---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: f74a031079ab35e1584d8c7e5536e2605ea665ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758920"
---
# <span data-ttu-id="99e7e-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="99e7e-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="99e7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99e7e-102">SYNOPSIS</span></span>
<span data-ttu-id="99e7e-103">Azure SQL eşitleme aracıları hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="99e7e-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="99e7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99e7e-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99e7e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="99e7e-105">DESCRIPTION</span></span>
<span data-ttu-id="99e7e-106">**Get-AzSqlSyncAgent** cmdlet 'i bir veya birden çok Azure SQL eşitleme Aracısı hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="99e7e-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="99e7e-107">Yalnızca bu eşitleme aracısının bilgilerini görmek için eşitleme aracısının adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="99e7e-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="99e7e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99e7e-108">EXAMPLES</span></span>

### <span data-ttu-id="99e7e-109">Örnek 1: Azure SQL Server 'a atanan tüm Azure SQL eşitleme Aracısı örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="99e7e-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="99e7e-110">Bu komut, Azure SQL Server 'a atanan tüm Azure SQL eşitleme aracıları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="99e7e-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="99e7e-111">Örnek 2: Azure SQL eşitleme Aracısı hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="99e7e-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="99e7e-112">Bu komut, "SyncAgent01" adıyla Azure SQL veritabanı eşitleme Aracısı hakkında bilgi alıyor</span><span class="sxs-lookup"><span data-stu-id="99e7e-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="99e7e-113">Örnek 3: filtreleme kullanarak Azure SQL Server 'a atanan Azure SQL eşitleme aracısının tüm örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="99e7e-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name SyncAgent* | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="99e7e-114">Bu komut, "SyncAgent" ile başlayan bir Azure SQL Server 'a atanan tüm Azure SQL eşitleme aracıları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="99e7e-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="99e7e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99e7e-115">PARAMETERS</span></span>

### <span data-ttu-id="99e7e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e7e-116">-DefaultProfile</span></span>
<span data-ttu-id="99e7e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="99e7e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99e7e-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="99e7e-118">-Name</span></span>
<span data-ttu-id="99e7e-119">Eşitleme aracısının adı.</span><span class="sxs-lookup"><span data-stu-id="99e7e-119">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="99e7e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99e7e-120">-ResourceGroupName</span></span>
<span data-ttu-id="99e7e-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="99e7e-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99e7e-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="99e7e-122">-ServerName</span></span>
<span data-ttu-id="99e7e-123">Eşitleme aracısının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="99e7e-123">The name of the Azure SQL Server the sync agent is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99e7e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e7e-124">CommonParameters</span></span>
<span data-ttu-id="99e7e-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99e7e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e7e-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="99e7e-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e7e-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99e7e-127">INPUTS</span></span>

### <span data-ttu-id="99e7e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="99e7e-128">System.String</span></span>

## <span data-ttu-id="99e7e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99e7e-129">OUTPUTS</span></span>

### <span data-ttu-id="99e7e-130">Microsoft. Azure. Commands. Sql. DataSync. model. azureskalite syncagentı</span><span class="sxs-lookup"><span data-stu-id="99e7e-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="99e7e-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99e7e-131">NOTES</span></span>

## <span data-ttu-id="99e7e-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99e7e-132">RELATED LINKS</span></span>

[<span data-ttu-id="99e7e-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="99e7e-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="99e7e-134">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="99e7e-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

