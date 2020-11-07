---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: 8b0f67aa8e85ce9123b515f12c2e3a7da84f860d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933586"
---
# <span data-ttu-id="f4596-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f4596-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="f4596-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4596-102">SYNOPSIS</span></span>
<span data-ttu-id="f4596-103">Azure SQL veritabanı eşitleme üyeleriyle ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="f4596-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="f4596-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4596-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4596-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4596-105">DESCRIPTION</span></span>
<span data-ttu-id="f4596-106">**Get-AzSqlSyncMember** cmdlet 'i, bir veya daha fazla Azure SQL veritabanı eşitleme üyesiyle ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="f4596-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="f4596-107">Yalnızca bu eşitleme üyesiyle ilgili bilgileri görmek için eşitleme üyesinin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="f4596-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="f4596-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4596-108">EXAMPLES</span></span>

### <span data-ttu-id="f4596-109">Örnek 1: eşitleme grubuna atanan tüm Azure SQL eşitleme üyesi örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="f4596-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
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

<span data-ttu-id="f4596-110">Bu komut, eşitleme grubu SyncGroup01 atanan tüm Azure SQL veritabanı eşitleme üyesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="f4596-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="f4596-111">Örnek 2: Azure SQL veritabanı eşitleme üyesi hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="f4596-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
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

<span data-ttu-id="f4596-112">Bu komut, "SyncMember01" adlı Azure SQL veritabanı eşitleme üyesiyle ilgili bilgileri alıyor</span><span class="sxs-lookup"><span data-stu-id="f4596-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="f4596-113">Örnek 3: filtreleme kullanarak tüm Azure SQL eşitleme üyesinin eşitleme grubuna atanan örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="f4596-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
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

<span data-ttu-id="f4596-114">Bu komut, "SyncMember" ile başlayan eşitleme grubuna atanan tüm Azure SQL veritabanı eşitleme üyesiyle ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="f4596-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="f4596-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4596-115">PARAMETERS</span></span>

### <span data-ttu-id="f4596-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f4596-116">-DatabaseName</span></span>
<span data-ttu-id="f4596-117">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="f4596-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f4596-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4596-118">-DefaultProfile</span></span>
<span data-ttu-id="f4596-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f4596-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4596-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="f4596-120">-Name</span></span>
<span data-ttu-id="f4596-121">Eşitleme üye adı.</span><span class="sxs-lookup"><span data-stu-id="f4596-121">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f4596-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4596-122">-ResourceGroupName</span></span>
<span data-ttu-id="f4596-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f4596-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="f4596-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f4596-124">-ServerName</span></span>
<span data-ttu-id="f4596-125">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="f4596-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="f4596-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f4596-126">-SyncGroupName</span></span>
<span data-ttu-id="f4596-127">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f4596-127">The sync group name.</span></span>

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

### <span data-ttu-id="f4596-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4596-128">CommonParameters</span></span>
<span data-ttu-id="f4596-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4596-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4596-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f4596-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4596-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4596-131">INPUTS</span></span>

### <span data-ttu-id="f4596-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f4596-132">System.String</span></span>

## <span data-ttu-id="f4596-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4596-133">OUTPUTS</span></span>

### <span data-ttu-id="f4596-134">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncmembermodel</span><span class="sxs-lookup"><span data-stu-id="f4596-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="f4596-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4596-135">NOTES</span></span>

## <span data-ttu-id="f4596-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4596-136">RELATED LINKS</span></span>

[<span data-ttu-id="f4596-137">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f4596-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="f4596-138">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f4596-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="f4596-139">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f4596-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

