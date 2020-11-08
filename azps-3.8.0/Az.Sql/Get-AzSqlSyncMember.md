---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: e5bb853d9dd818801298254eac1f120efcc829a4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096243"
---
# <span data-ttu-id="18bf3-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="18bf3-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="18bf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="18bf3-103">Azure SQL veritabanı eşitleme üyeleriyle ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="18bf3-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="18bf3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18bf3-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18bf3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="18bf3-105">DESCRIPTION</span></span>
<span data-ttu-id="18bf3-106">**Get-AzSqlSyncMember** cmdlet 'i, bir veya daha fazla Azure SQL veritabanı eşitleme üyesiyle ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="18bf3-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="18bf3-107">Yalnızca bu eşitleme üyesiyle ilgili bilgileri görmek için eşitleme üyesinin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="18bf3-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="18bf3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18bf3-108">EXAMPLES</span></span>

### <span data-ttu-id="18bf3-109">Örnek 1: eşitleme grubuna atanan tüm Azure SQL eşitleme üyesi örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="18bf3-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="18bf3-110">Bu komut, eşitleme grubu SyncGroup01 atanan tüm Azure SQL veritabanı eşitleme üyesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="18bf3-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="18bf3-111">Örnek 2: Azure SQL veritabanı eşitleme üyesi hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="18bf3-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="18bf3-112">Bu komut, "SyncMember01" adlı Azure SQL veritabanı eşitleme üyesiyle ilgili bilgileri alıyor</span><span class="sxs-lookup"><span data-stu-id="18bf3-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="18bf3-113">Örnek 3: filtreleme kullanarak tüm Azure SQL eşitleme üyesinin eşitleme grubuna atanan örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="18bf3-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember*" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="18bf3-114">Bu komut, "SyncMember" ile başlayan eşitleme grubuna atanan tüm Azure SQL veritabanı eşitleme üyesiyle ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="18bf3-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="18bf3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18bf3-115">PARAMETERS</span></span>

### <span data-ttu-id="18bf3-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="18bf3-116">-DatabaseName</span></span>
<span data-ttu-id="18bf3-117">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="18bf3-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="18bf3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18bf3-118">-DefaultProfile</span></span>
<span data-ttu-id="18bf3-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="18bf3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18bf3-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="18bf3-120">-Name</span></span>
<span data-ttu-id="18bf3-121">Eşitleme üye adı.</span><span class="sxs-lookup"><span data-stu-id="18bf3-121">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bf3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18bf3-122">-ResourceGroupName</span></span>
<span data-ttu-id="18bf3-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="18bf3-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="18bf3-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="18bf3-124">-ServerName</span></span>
<span data-ttu-id="18bf3-125">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="18bf3-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="18bf3-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="18bf3-126">-SyncGroupName</span></span>
<span data-ttu-id="18bf3-127">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="18bf3-127">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bf3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18bf3-128">CommonParameters</span></span>
<span data-ttu-id="18bf3-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18bf3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18bf3-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="18bf3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18bf3-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18bf3-131">INPUTS</span></span>

### <span data-ttu-id="18bf3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="18bf3-132">System.String</span></span>

## <span data-ttu-id="18bf3-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18bf3-133">OUTPUTS</span></span>

### <span data-ttu-id="18bf3-134">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncmembermodel</span><span class="sxs-lookup"><span data-stu-id="18bf3-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="18bf3-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18bf3-135">NOTES</span></span>

## <span data-ttu-id="18bf3-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18bf3-136">RELATED LINKS</span></span>

[<span data-ttu-id="18bf3-137">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="18bf3-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="18bf3-138">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="18bf3-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="18bf3-139">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="18bf3-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)
