---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 8b590e6ba8329ba6e0c45d30f7163c637d90f79e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589998"
---
# <span data-ttu-id="c99fe-101">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="c99fe-101">Get-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="c99fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c99fe-102">SYNOPSIS</span></span>
<span data-ttu-id="c99fe-103">Azure SQL eşitleme aracıları hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="c99fe-103">Returns information about Azure SQL Sync Agents.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c99fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c99fe-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c99fe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c99fe-105">DESCRIPTION</span></span>
<span data-ttu-id="c99fe-106">**Get-AzureRmSqlSyncAgent** cmdlet 'i, bir veya birden çok Azure SQL eşitleme Aracısı hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="c99fe-106">The **Get-AzureRmSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="c99fe-107">Yalnızca bu eşitleme aracısının bilgilerini görmek için eşitleme aracısının adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="c99fe-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="c99fe-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c99fe-108">EXAMPLES</span></span>

### <span data-ttu-id="c99fe-109">Örnek 1: Azure SQL Server 'a atanan tüm Azure SQL eşitleme Aracısı örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="c99fe-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
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

<span data-ttu-id="c99fe-110">Bu komut, Azure SQL Server 'a atanan tüm Azure SQL eşitleme aracıları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c99fe-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="c99fe-111">Örnek 2: Azure SQL eşitleme Aracısı hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="c99fe-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
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

<span data-ttu-id="c99fe-112">Bu komut, "SyncAgent01" adıyla Azure SQL veritabanı eşitleme Aracısı hakkında bilgi alıyor</span><span class="sxs-lookup"><span data-stu-id="c99fe-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

## <span data-ttu-id="c99fe-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c99fe-113">PARAMETERS</span></span>

### <span data-ttu-id="c99fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c99fe-114">-DefaultProfile</span></span>
<span data-ttu-id="c99fe-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c99fe-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99fe-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="c99fe-116">-Name</span></span>
<span data-ttu-id="c99fe-117">Eşitleme aracısının adı.</span><span class="sxs-lookup"><span data-stu-id="c99fe-117">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99fe-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c99fe-118">-ResourceGroupName</span></span>
<span data-ttu-id="c99fe-119">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c99fe-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="c99fe-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c99fe-120">-ServerName</span></span>
<span data-ttu-id="c99fe-121">Eşitleme aracısının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="c99fe-121">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="c99fe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c99fe-122">CommonParameters</span></span>
<span data-ttu-id="c99fe-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c99fe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c99fe-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c99fe-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c99fe-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c99fe-125">INPUTS</span></span>

### <span data-ttu-id="c99fe-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c99fe-126">System.String</span></span>

## <span data-ttu-id="c99fe-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c99fe-127">OUTPUTS</span></span>

### <span data-ttu-id="c99fe-128">Microsoft. Azure. Commands. Sql. DataSync. model. azureskalite syncagentı</span><span class="sxs-lookup"><span data-stu-id="c99fe-128">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="c99fe-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c99fe-129">NOTES</span></span>

## <span data-ttu-id="c99fe-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c99fe-130">RELATED LINKS</span></span>

[<span data-ttu-id="c99fe-131">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="c99fe-131">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="c99fe-132">Yeni-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="c99fe-132">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

