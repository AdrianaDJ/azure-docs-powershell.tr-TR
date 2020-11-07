---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: 634ce84e355dbd106865b0f1072b693bd03a623b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937939"
---
# <span data-ttu-id="8c7d0-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="8c7d0-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="8c7d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c7d0-102">SYNOPSIS</span></span>
<span data-ttu-id="8c7d0-103">Azure SQL veritabanı eşitleme üyesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8c7d0-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="8c7d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8c7d0-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c7d0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c7d0-105">DESCRIPTION</span></span>
<span data-ttu-id="8c7d0-106">**Update-AzSqlSyncGroup** cmdlet 'ı, Azure SQL veritabanı eşitleme üyesinin özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8c7d0-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="8c7d0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8c7d0-107">EXAMPLES</span></span>

### <span data-ttu-id="8c7d0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8c7d0-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
-MemberDatabaseCredential $credential | Format-List
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
MemberDatabaseUserName      : myAccount-new
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="8c7d0-109">Bu komut, üye veritabanının yönetici parolasını sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="8c7d0-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="8c7d0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8c7d0-110">PARAMETERS</span></span>

### <span data-ttu-id="8c7d0-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8c7d0-111">-DatabaseName</span></span>
<span data-ttu-id="8c7d0-112">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="8c7d0-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="8c7d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c7d0-113">-DefaultProfile</span></span>
<span data-ttu-id="8c7d0-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8c7d0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c7d0-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="8c7d0-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="8c7d0-116">Azure SQL veritabanının kimlik bilgileri (Kullanıcı adı ve parola).</span><span class="sxs-lookup"><span data-stu-id="8c7d0-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c7d0-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="8c7d0-117">-Name</span></span>
<span data-ttu-id="8c7d0-118">Eşitleme üye adı.</span><span class="sxs-lookup"><span data-stu-id="8c7d0-118">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7d0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c7d0-119">-ResourceGroupName</span></span>
<span data-ttu-id="8c7d0-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8c7d0-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="8c7d0-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8c7d0-121">-ServerName</span></span>
<span data-ttu-id="8c7d0-122">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="8c7d0-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="8c7d0-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="8c7d0-123">-SyncGroupName</span></span>
<span data-ttu-id="8c7d0-124">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8c7d0-124">The sync group name.</span></span>

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

### <span data-ttu-id="8c7d0-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="8c7d0-125">-Confirm</span></span>
<span data-ttu-id="8c7d0-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8c7d0-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c7d0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c7d0-127">-WhatIf</span></span>
<span data-ttu-id="8c7d0-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8c7d0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c7d0-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8c7d0-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c7d0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c7d0-130">CommonParameters</span></span>
<span data-ttu-id="8c7d0-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8c7d0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c7d0-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8c7d0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c7d0-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8c7d0-133">INPUTS</span></span>

### <span data-ttu-id="8c7d0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8c7d0-134">System.String</span></span>

## <span data-ttu-id="8c7d0-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8c7d0-135">OUTPUTS</span></span>

### <span data-ttu-id="8c7d0-136">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncmembermodel</span><span class="sxs-lookup"><span data-stu-id="8c7d0-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="8c7d0-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8c7d0-137">NOTES</span></span>

## <span data-ttu-id="8c7d0-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c7d0-138">RELATED LINKS</span></span>

[<span data-ttu-id="8c7d0-139">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="8c7d0-139">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="8c7d0-140">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="8c7d0-140">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="8c7d0-141">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="8c7d0-141">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

