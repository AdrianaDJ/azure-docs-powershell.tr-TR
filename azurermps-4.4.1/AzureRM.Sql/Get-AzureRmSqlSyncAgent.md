---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 5aeb6688f33f9a21cfe20ee91043a8db7bd0313c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587762"
---
# <span data-ttu-id="00d19-101">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="00d19-101">Get-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="00d19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00d19-102">SYNOPSIS</span></span>
<span data-ttu-id="00d19-103">Azure SQL eşitleme aracıları hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="00d19-103">Returns information about Azure SQL Sync Agents.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00d19-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00d19-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00d19-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00d19-105">DESCRIPTION</span></span>
<span data-ttu-id="00d19-106">**Get-AzureRmSqlSyncAgent** cmdlet 'i, bir veya birden çok Azure SQL eşitleme Aracısı hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="00d19-106">The **Get-AzureRmSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="00d19-107">Yalnızca bu eşitleme aracısının bilgilerini görmek için eşitleme aracısının adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="00d19-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="00d19-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00d19-108">EXAMPLES</span></span>

### <span data-ttu-id="00d19-109">Örnek 1: Azure SQL Server 'a atanan tüm Azure SQL eşitleme Aracısı örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="00d19-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
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

<span data-ttu-id="00d19-110">Bu komut, Azure SQL Server 'a atanan tüm Azure SQL eşitleme aracıları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="00d19-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="00d19-111">Örnek 2: Azure SQL eşitleme Aracısı hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="00d19-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
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

<span data-ttu-id="00d19-112">Bu komut, "SyncAgent01" adıyla Azure SQL veritabanı eşitleme Aracısı hakkında bilgi alıyor</span><span class="sxs-lookup"><span data-stu-id="00d19-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

## <span data-ttu-id="00d19-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00d19-113">PARAMETERS</span></span>

### <span data-ttu-id="00d19-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="00d19-114">-Name</span></span>
<span data-ttu-id="00d19-115">Eşitleme aracısının adı.</span><span class="sxs-lookup"><span data-stu-id="00d19-115">The sync agent name.</span></span>

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

### <span data-ttu-id="00d19-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00d19-116">-ResourceGroupName</span></span>
<span data-ttu-id="00d19-117">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="00d19-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="00d19-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="00d19-118">-ServerName</span></span>
<span data-ttu-id="00d19-119">Eşitleme aracısının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="00d19-119">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="00d19-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00d19-120">-DefaultProfile</span></span>
<span data-ttu-id="00d19-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00d19-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00d19-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00d19-122">CommonParameters</span></span>
<span data-ttu-id="00d19-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00d19-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00d19-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00d19-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00d19-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00d19-125">INPUTS</span></span>

## <span data-ttu-id="00d19-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00d19-126">OUTPUTS</span></span>

### <span data-ttu-id="00d19-127">Microsoft. Azure. Commands. Sql. DataSync. model. azureskalite syncagentı</span><span class="sxs-lookup"><span data-stu-id="00d19-127">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="00d19-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00d19-128">NOTES</span></span>

## <span data-ttu-id="00d19-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00d19-129">RELATED LINKS</span></span>

[<span data-ttu-id="00d19-130">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="00d19-130">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="00d19-131">Yeni-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="00d19-131">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

