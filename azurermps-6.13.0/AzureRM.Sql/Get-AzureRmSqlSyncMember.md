---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
ms.openlocfilehash: 30a73047282508adc0c2aa0d0d64a61f9f70e71a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593636"
---
# <span data-ttu-id="68832-101">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="68832-101">Get-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="68832-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68832-102">SYNOPSIS</span></span>
<span data-ttu-id="68832-103">Azure SQL veritabanı eşitleme üyeleriyle ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="68832-103">Returns information about Azure SQL Database Sync Members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68832-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68832-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68832-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="68832-105">DESCRIPTION</span></span>
<span data-ttu-id="68832-106">**Get-AzureRmSqlSyncMember** cmdlet 'i, bir veya daha fazla Azure SQL veritabanı eşitleme üyesiyle ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="68832-106">The **Get-AzureRmSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="68832-107">Yalnızca bu eşitleme üyesiyle ilgili bilgileri görmek için eşitleme üyesinin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="68832-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="68832-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68832-108">EXAMPLES</span></span>

### <span data-ttu-id="68832-109">Örnek 1: eşitleme grubuna atanan tüm Azure SQL eşitleme üyesi örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="68832-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
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

<span data-ttu-id="68832-110">Bu komut, eşitleme grubu SyncGroup01 atanan tüm Azure SQL veritabanı eşitleme üyesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="68832-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="68832-111">Örnek 2: Azure SQL veritabanı eşitleme üyesi hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="68832-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
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

<span data-ttu-id="68832-112">Bu komut, "SyncMember01" adlı Azure SQL veritabanı eşitleme üyesiyle ilgili bilgileri alıyor</span><span class="sxs-lookup"><span data-stu-id="68832-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

## <span data-ttu-id="68832-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68832-113">PARAMETERS</span></span>

### <span data-ttu-id="68832-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="68832-114">-DatabaseName</span></span>
<span data-ttu-id="68832-115">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="68832-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="68832-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68832-116">-DefaultProfile</span></span>
<span data-ttu-id="68832-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="68832-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68832-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="68832-118">-Name</span></span>
<span data-ttu-id="68832-119">Eşitleme üye adı.</span><span class="sxs-lookup"><span data-stu-id="68832-119">The sync member name.</span></span>

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

### <span data-ttu-id="68832-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68832-120">-ResourceGroupName</span></span>
<span data-ttu-id="68832-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="68832-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="68832-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="68832-122">-ServerName</span></span>
<span data-ttu-id="68832-123">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="68832-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="68832-124">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="68832-124">-SyncGroupName</span></span>
<span data-ttu-id="68832-125">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="68832-125">The sync group name.</span></span>

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

### <span data-ttu-id="68832-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68832-126">CommonParameters</span></span>
<span data-ttu-id="68832-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68832-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68832-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68832-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68832-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68832-129">INPUTS</span></span>

### <span data-ttu-id="68832-130">System. String</span><span class="sxs-lookup"><span data-stu-id="68832-130">System.String</span></span>

## <span data-ttu-id="68832-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68832-131">OUTPUTS</span></span>

### <span data-ttu-id="68832-132">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncmembermodel</span><span class="sxs-lookup"><span data-stu-id="68832-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="68832-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68832-133">NOTES</span></span>

## <span data-ttu-id="68832-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68832-134">RELATED LINKS</span></span>

[<span data-ttu-id="68832-135">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="68832-135">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="68832-136">Güncelleştirme-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="68832-136">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="68832-137">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="68832-137">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

