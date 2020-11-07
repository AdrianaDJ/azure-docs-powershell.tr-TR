---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
ms.openlocfilehash: f72091d142b57cc7ef3897eceda2219634376daf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763093"
---
# <span data-ttu-id="375e9-101">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="375e9-101">Update-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="375e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="375e9-102">SYNOPSIS</span></span>
<span data-ttu-id="375e9-103">Azure SQL veritabanı eşitleme üyesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="375e9-103">Updates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="375e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="375e9-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="375e9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="375e9-105">DESCRIPTION</span></span>
<span data-ttu-id="375e9-106">**Update-AzureRmSqlSyncGroup** cmdlet 'ı, Azure SQL veritabanı eşitleme üyesinin özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="375e9-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="375e9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="375e9-107">EXAMPLES</span></span>

### <span data-ttu-id="375e9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="375e9-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
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

<span data-ttu-id="375e9-109">Bu komut, üye veritabanının yönetici parolasını sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="375e9-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="375e9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="375e9-110">PARAMETERS</span></span>

### <span data-ttu-id="375e9-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="375e9-111">-Confirm</span></span>
<span data-ttu-id="375e9-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="375e9-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="375e9-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="375e9-113">-DatabaseName</span></span>
<span data-ttu-id="375e9-114">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="375e9-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="375e9-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="375e9-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="375e9-116">Azure SQL veritabanının kimlik bilgileri (Kullanıcı adı ve parola).</span><span class="sxs-lookup"><span data-stu-id="375e9-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="375e9-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="375e9-117">-Name</span></span>
<span data-ttu-id="375e9-118">Eşitleme üye adı.</span><span class="sxs-lookup"><span data-stu-id="375e9-118">The sync member name.</span></span>

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

### <span data-ttu-id="375e9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="375e9-119">-ResourceGroupName</span></span>
<span data-ttu-id="375e9-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="375e9-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="375e9-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="375e9-121">-ServerName</span></span>
<span data-ttu-id="375e9-122">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="375e9-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="375e9-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="375e9-123">-SyncGroupName</span></span>
<span data-ttu-id="375e9-124">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="375e9-124">The sync group name.</span></span>

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

### <span data-ttu-id="375e9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="375e9-125">-WhatIf</span></span>
<span data-ttu-id="375e9-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="375e9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="375e9-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="375e9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="375e9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="375e9-128">-DefaultProfile</span></span>
<span data-ttu-id="375e9-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="375e9-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="375e9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="375e9-130">CommonParameters</span></span>
<span data-ttu-id="375e9-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="375e9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="375e9-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="375e9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="375e9-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="375e9-133">INPUTS</span></span>

## <span data-ttu-id="375e9-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="375e9-134">OUTPUTS</span></span>

### <span data-ttu-id="375e9-135">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncmembermodel</span><span class="sxs-lookup"><span data-stu-id="375e9-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="375e9-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="375e9-136">NOTES</span></span>

## <span data-ttu-id="375e9-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="375e9-137">RELATED LINKS</span></span>

[<span data-ttu-id="375e9-138">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="375e9-138">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="375e9-139">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="375e9-139">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="375e9-140">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="375e9-140">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

