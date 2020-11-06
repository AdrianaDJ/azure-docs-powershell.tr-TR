---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
ms.openlocfilehash: 7737baa8459cc9acae86cbd3e632dd73f9433056
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593611"
---
# <span data-ttu-id="bac87-101">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="bac87-101">Update-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="bac87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bac87-102">SYNOPSIS</span></span>
<span data-ttu-id="bac87-103">Azure SQL veritabanı eşitleme üyesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="bac87-103">Updates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bac87-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bac87-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bac87-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bac87-105">DESCRIPTION</span></span>
<span data-ttu-id="bac87-106">**Update-AzureRmSqlSyncGroup** cmdlet 'ı, Azure SQL veritabanı eşitleme üyesinin özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bac87-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="bac87-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bac87-107">EXAMPLES</span></span>

### <span data-ttu-id="bac87-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bac87-108">Example 1</span></span>
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

<span data-ttu-id="bac87-109">Bu komut, üye veritabanının yönetici parolasını sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="bac87-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="bac87-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bac87-110">PARAMETERS</span></span>

### <span data-ttu-id="bac87-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bac87-111">-DatabaseName</span></span>
<span data-ttu-id="bac87-112">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="bac87-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="bac87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bac87-113">-DefaultProfile</span></span>
<span data-ttu-id="bac87-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bac87-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bac87-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="bac87-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="bac87-116">Azure SQL veritabanının kimlik bilgileri (Kullanıcı adı ve parola).</span><span class="sxs-lookup"><span data-stu-id="bac87-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="bac87-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="bac87-117">-Name</span></span>
<span data-ttu-id="bac87-118">Eşitleme üye adı.</span><span class="sxs-lookup"><span data-stu-id="bac87-118">The sync member name.</span></span>

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

### <span data-ttu-id="bac87-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bac87-119">-ResourceGroupName</span></span>
<span data-ttu-id="bac87-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bac87-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="bac87-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bac87-121">-ServerName</span></span>
<span data-ttu-id="bac87-122">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="bac87-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="bac87-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="bac87-123">-SyncGroupName</span></span>
<span data-ttu-id="bac87-124">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bac87-124">The sync group name.</span></span>

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

### <span data-ttu-id="bac87-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="bac87-125">-Confirm</span></span>
<span data-ttu-id="bac87-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bac87-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bac87-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bac87-127">-WhatIf</span></span>
<span data-ttu-id="bac87-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bac87-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bac87-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bac87-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bac87-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac87-130">CommonParameters</span></span>
<span data-ttu-id="bac87-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bac87-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac87-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bac87-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac87-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bac87-133">INPUTS</span></span>

### <span data-ttu-id="bac87-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bac87-134">System.String</span></span>

## <span data-ttu-id="bac87-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bac87-135">OUTPUTS</span></span>

### <span data-ttu-id="bac87-136">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncmembermodel</span><span class="sxs-lookup"><span data-stu-id="bac87-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="bac87-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bac87-137">NOTES</span></span>

## <span data-ttu-id="bac87-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bac87-138">RELATED LINKS</span></span>

[<span data-ttu-id="bac87-139">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="bac87-139">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="bac87-140">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="bac87-140">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="bac87-141">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="bac87-141">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

