---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
ms.openlocfilehash: d117ef9685a235528cb91c82a148ff0dddb2d96c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096244"
---
# <span data-ttu-id="3fcc2-101">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3fcc2-101">Get-AzSqlSyncGroup</span></span>

## <span data-ttu-id="3fcc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fcc2-102">SYNOPSIS</span></span>
<span data-ttu-id="3fcc2-103">Azure SQL veritabanı eşitleme gruplarıyla ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="3fcc2-103">Returns information about Azure SQL Database Sync Groups.</span></span>

## <span data-ttu-id="3fcc2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3fcc2-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fcc2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3fcc2-105">DESCRIPTION</span></span>
<span data-ttu-id="3fcc2-106">**Get-AzSqlSyncGroup** cmdlet 'i, bir veya daha fazla Azure SQL veritabanı eşitleme grubuyla ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="3fcc2-106">The **Get-AzSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="3fcc2-107">Yalnızca bu eşitleme grubuyla ilgili bilgileri görmek için eşitleme grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3fcc2-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="3fcc2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3fcc2-108">EXAMPLES</span></span>

### <span data-ttu-id="3fcc2-109">Örnek 1: Azure SQL veritabanına atanan tüm Azure SQL eşitleme grubu örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="3fcc2-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
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

<span data-ttu-id="3fcc2-110">Bu komut, Azure SQL veritabanına atanmış tüm Azure SQL veritabanı eşitleme grupları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="3fcc2-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="3fcc2-111">Örnek 2: Azure SQL veritabanı eşitleme grubu hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="3fcc2-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
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

<span data-ttu-id="3fcc2-112">Bu komut, "SyncGroup01" adlı Azure SQL veritabanı eşitleme grubu hakkında bilgi alıyor</span><span class="sxs-lookup"><span data-stu-id="3fcc2-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

### <span data-ttu-id="3fcc2-113">Örnek 3: filtreleme kullanarak Azure SQL veritabanına atanan tüm Azure SQL eşitleme grubu örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="3fcc2-113">Example 3: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database using filtering</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup*" | Format-List
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

<span data-ttu-id="3fcc2-114">Bu komut, "SyncGroup" ile başlayan bir Azure SQL veritabanına atanmış tüm Azure SQL veritabanı eşitleme grupları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="3fcc2-114">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database that start with "SyncGroup".</span></span>

## <span data-ttu-id="3fcc2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3fcc2-115">PARAMETERS</span></span>

### <span data-ttu-id="3fcc2-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3fcc2-116">-DatabaseName</span></span>
<span data-ttu-id="3fcc2-117">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="3fcc2-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="3fcc2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fcc2-118">-DefaultProfile</span></span>
<span data-ttu-id="3fcc2-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3fcc2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fcc2-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="3fcc2-120">-Name</span></span>
<span data-ttu-id="3fcc2-121">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3fcc2-121">The sync group name.</span></span>

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

### <span data-ttu-id="3fcc2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fcc2-122">-ResourceGroupName</span></span>
<span data-ttu-id="3fcc2-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3fcc2-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="3fcc2-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3fcc2-124">-ServerName</span></span>
<span data-ttu-id="3fcc2-125">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="3fcc2-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="3fcc2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fcc2-126">CommonParameters</span></span>
<span data-ttu-id="3fcc2-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3fcc2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fcc2-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3fcc2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fcc2-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3fcc2-129">INPUTS</span></span>

### <span data-ttu-id="3fcc2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3fcc2-130">System.String</span></span>

## <span data-ttu-id="3fcc2-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3fcc2-131">OUTPUTS</span></span>

### <span data-ttu-id="3fcc2-132">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncgroupmodel</span><span class="sxs-lookup"><span data-stu-id="3fcc2-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="3fcc2-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3fcc2-133">NOTES</span></span>

## <span data-ttu-id="3fcc2-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3fcc2-134">RELATED LINKS</span></span>

[<span data-ttu-id="3fcc2-135">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3fcc2-135">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="3fcc2-136">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3fcc2-136">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="3fcc2-137">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3fcc2-137">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

