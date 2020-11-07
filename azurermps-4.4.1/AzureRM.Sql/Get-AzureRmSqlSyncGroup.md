---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
ms.openlocfilehash: e581f0bd94e58f725055c0dc1a4f1d704b891c86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762191"
---
# <span data-ttu-id="2de30-101">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2de30-101">Get-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="2de30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2de30-102">SYNOPSIS</span></span>
<span data-ttu-id="2de30-103">Azure SQL veritabanı eşitleme gruplarıyla ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="2de30-103">Returns information about Azure SQL Database Sync Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2de30-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2de30-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2de30-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2de30-105">DESCRIPTION</span></span>
<span data-ttu-id="2de30-106">**Get-AzureRmSqlSyncGroup** cmdlet 'i, bir veya daha fazla Azure SQL veritabanı eşitleme grubuyla ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="2de30-106">The **Get-AzureRmSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="2de30-107">Yalnızca bu eşitleme grubuyla ilgili bilgileri görmek için eşitleme grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="2de30-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="2de30-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2de30-108">EXAMPLES</span></span>

### <span data-ttu-id="2de30-109">Örnek 1: Azure SQL veritabanına atanan tüm Azure SQL eşitleme grubu örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="2de30-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="2de30-110">Bu komut, Azure SQL veritabanına atanmış tüm Azure SQL veritabanı eşitleme grupları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2de30-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="2de30-111">Örnek 2: Azure SQL veritabanı eşitleme grubu hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="2de30-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="2de30-112">Bu komut, "SyncGroup01" adlı Azure SQL veritabanı eşitleme grubu hakkında bilgi alıyor</span><span class="sxs-lookup"><span data-stu-id="2de30-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

## <span data-ttu-id="2de30-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2de30-113">PARAMETERS</span></span>

### <span data-ttu-id="2de30-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2de30-114">-DatabaseName</span></span>
<span data-ttu-id="2de30-115">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="2de30-115">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de30-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="2de30-116">-Name</span></span>
<span data-ttu-id="2de30-117">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2de30-117">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de30-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de30-118">-ResourceGroupName</span></span>
<span data-ttu-id="2de30-119">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2de30-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="2de30-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2de30-120">-ServerName</span></span>
<span data-ttu-id="2de30-121">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="2de30-121">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="2de30-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de30-122">-DefaultProfile</span></span>
<span data-ttu-id="2de30-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2de30-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2de30-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de30-124">CommonParameters</span></span>
<span data-ttu-id="2de30-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2de30-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de30-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2de30-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de30-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2de30-127">INPUTS</span></span>

## <span data-ttu-id="2de30-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2de30-128">OUTPUTS</span></span>

### <span data-ttu-id="2de30-129">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncgroupmodel</span><span class="sxs-lookup"><span data-stu-id="2de30-129">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="2de30-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2de30-130">NOTES</span></span>

## <span data-ttu-id="2de30-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2de30-131">RELATED LINKS</span></span>

[<span data-ttu-id="2de30-132">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2de30-132">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="2de30-133">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2de30-133">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="2de30-134">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2de30-134">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

