---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 3a5da7972e70e3ebf9c86df62b2bbc79651e72a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098641"
---
# <span data-ttu-id="ba97a-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ba97a-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="ba97a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba97a-102">SYNOPSIS</span></span>
<span data-ttu-id="ba97a-103">Azure SQL veritabanı eşitleme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ba97a-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="ba97a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba97a-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba97a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba97a-105">DESCRIPTION</span></span>
<span data-ttu-id="ba97a-106">**Remove-AzSqlSyncGroup** cmdlet 'ı BIR Azure SQL veritabanı eşitleme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ba97a-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="ba97a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba97a-107">EXAMPLES</span></span>

### <span data-ttu-id="ba97a-108">Örnek 1: eşitleme grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="ba97a-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="ba97a-109">Bu komut, syncGroup01 adlı Azure SQL veritabanı eşitleme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ba97a-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="ba97a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba97a-110">PARAMETERS</span></span>

### <span data-ttu-id="ba97a-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ba97a-111">-DatabaseName</span></span>
<span data-ttu-id="ba97a-112">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="ba97a-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ba97a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba97a-113">-DefaultProfile</span></span>
<span data-ttu-id="ba97a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ba97a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba97a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ba97a-115">-Force</span></span>
<span data-ttu-id="ba97a-116">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="ba97a-116">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba97a-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="ba97a-117">-Name</span></span>
<span data-ttu-id="ba97a-118">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ba97a-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba97a-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ba97a-119">-PassThru</span></span>
<span data-ttu-id="ba97a-120">Kaldırılan eşitleme grubunu iade edilip edilmeyeceğini tanımlar</span><span class="sxs-lookup"><span data-stu-id="ba97a-120">Defines Whether return the removed sync group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba97a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba97a-121">-ResourceGroupName</span></span>
<span data-ttu-id="ba97a-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ba97a-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="ba97a-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ba97a-123">-ServerName</span></span>
<span data-ttu-id="ba97a-124">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="ba97a-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="ba97a-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="ba97a-125">-Confirm</span></span>
<span data-ttu-id="ba97a-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ba97a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba97a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba97a-127">-WhatIf</span></span>
<span data-ttu-id="ba97a-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba97a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba97a-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ba97a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba97a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba97a-130">CommonParameters</span></span>
<span data-ttu-id="ba97a-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba97a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba97a-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ba97a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba97a-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba97a-133">INPUTS</span></span>

### <span data-ttu-id="ba97a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ba97a-134">System.String</span></span>

## <span data-ttu-id="ba97a-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba97a-135">OUTPUTS</span></span>

### <span data-ttu-id="ba97a-136">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncgroupmodel</span><span class="sxs-lookup"><span data-stu-id="ba97a-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="ba97a-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba97a-137">NOTES</span></span>

## <span data-ttu-id="ba97a-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba97a-138">RELATED LINKS</span></span>

[<span data-ttu-id="ba97a-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ba97a-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="ba97a-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ba97a-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="ba97a-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ba97a-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)
