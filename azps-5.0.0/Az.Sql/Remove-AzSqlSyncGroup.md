---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 3a5da7972e70e3ebf9c86df62b2bbc79651e72a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276977"
---
# <span data-ttu-id="d5c41-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d5c41-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="d5c41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5c41-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c41-103">Azure SQL veritabanı eşitleme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d5c41-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="d5c41-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5c41-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5c41-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5c41-105">DESCRIPTION</span></span>
<span data-ttu-id="d5c41-106">**Remove-AzSqlSyncGroup** cmdlet 'ı BIR Azure SQL veritabanı eşitleme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d5c41-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="d5c41-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5c41-107">EXAMPLES</span></span>

### <span data-ttu-id="d5c41-108">Örnek 1: eşitleme grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="d5c41-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="d5c41-109">Bu komut, syncGroup01 adlı Azure SQL veritabanı eşitleme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d5c41-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="d5c41-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5c41-110">PARAMETERS</span></span>

### <span data-ttu-id="d5c41-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d5c41-111">-DatabaseName</span></span>
<span data-ttu-id="d5c41-112">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="d5c41-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d5c41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5c41-113">-DefaultProfile</span></span>
<span data-ttu-id="d5c41-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d5c41-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5c41-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d5c41-115">-Force</span></span>
<span data-ttu-id="d5c41-116">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="d5c41-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d5c41-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="d5c41-117">-Name</span></span>
<span data-ttu-id="d5c41-118">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d5c41-118">The sync group name.</span></span>

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

### <span data-ttu-id="d5c41-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d5c41-119">-PassThru</span></span>
<span data-ttu-id="d5c41-120">Kaldırılan eşitleme grubunu iade edilip edilmeyeceğini tanımlar</span><span class="sxs-lookup"><span data-stu-id="d5c41-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="d5c41-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5c41-121">-ResourceGroupName</span></span>
<span data-ttu-id="d5c41-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d5c41-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="d5c41-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d5c41-123">-ServerName</span></span>
<span data-ttu-id="d5c41-124">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="d5c41-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d5c41-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="d5c41-125">-Confirm</span></span>
<span data-ttu-id="d5c41-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d5c41-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5c41-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5c41-127">-WhatIf</span></span>
<span data-ttu-id="d5c41-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d5c41-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5c41-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d5c41-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5c41-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c41-130">CommonParameters</span></span>
<span data-ttu-id="d5c41-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5c41-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c41-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d5c41-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c41-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5c41-133">INPUTS</span></span>

### <span data-ttu-id="d5c41-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d5c41-134">System.String</span></span>

## <span data-ttu-id="d5c41-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5c41-135">OUTPUTS</span></span>

### <span data-ttu-id="d5c41-136">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncgroupmodel</span><span class="sxs-lookup"><span data-stu-id="d5c41-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="d5c41-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5c41-137">NOTES</span></span>

## <span data-ttu-id="d5c41-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5c41-138">RELATED LINKS</span></span>

[<span data-ttu-id="d5c41-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d5c41-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="d5c41-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d5c41-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="d5c41-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d5c41-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

