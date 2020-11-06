---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 62f3c74f94ac0e775adc70f4eef9c4250e041145
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594334"
---
# <span data-ttu-id="e9aed-101">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e9aed-101">Remove-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="e9aed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9aed-102">SYNOPSIS</span></span>
<span data-ttu-id="e9aed-103">Azure SQL veritabanı eşitleme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e9aed-103">Removes an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9aed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9aed-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9aed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9aed-105">DESCRIPTION</span></span>
<span data-ttu-id="e9aed-106">**Remove-AzureRmSqlSyncGroup** cmdlet 'ı BIR Azure SQL veritabanı eşitleme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e9aed-106">The **Remove-AzureRmSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="e9aed-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9aed-107">EXAMPLES</span></span>

### <span data-ttu-id="e9aed-108">Örnek 1: eşitleme grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="e9aed-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="e9aed-109">Bu komut, syncGroup01 adlı Azure SQL veritabanı eşitleme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e9aed-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="e9aed-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9aed-110">PARAMETERS</span></span>

### <span data-ttu-id="e9aed-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e9aed-111">-DatabaseName</span></span>
<span data-ttu-id="e9aed-112">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="e9aed-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e9aed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9aed-113">-DefaultProfile</span></span>
<span data-ttu-id="e9aed-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e9aed-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9aed-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e9aed-115">-Force</span></span>
<span data-ttu-id="e9aed-116">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="e9aed-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="e9aed-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="e9aed-117">-Name</span></span>
<span data-ttu-id="e9aed-118">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e9aed-118">The sync group name.</span></span>

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

### <span data-ttu-id="e9aed-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e9aed-119">-PassThru</span></span>
<span data-ttu-id="e9aed-120">Kaldırılan eşitleme grubunu iade edilip edilmeyeceğini tanımlar</span><span class="sxs-lookup"><span data-stu-id="e9aed-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="e9aed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9aed-121">-ResourceGroupName</span></span>
<span data-ttu-id="e9aed-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e9aed-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="e9aed-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e9aed-123">-ServerName</span></span>
<span data-ttu-id="e9aed-124">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="e9aed-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e9aed-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="e9aed-125">-Confirm</span></span>
<span data-ttu-id="e9aed-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e9aed-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9aed-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9aed-127">-WhatIf</span></span>
<span data-ttu-id="e9aed-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9aed-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9aed-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e9aed-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9aed-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9aed-130">CommonParameters</span></span>
<span data-ttu-id="e9aed-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9aed-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9aed-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9aed-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9aed-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9aed-133">INPUTS</span></span>

### <span data-ttu-id="e9aed-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e9aed-134">System.String</span></span>

## <span data-ttu-id="e9aed-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9aed-135">OUTPUTS</span></span>

### <span data-ttu-id="e9aed-136">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncgroupmodel</span><span class="sxs-lookup"><span data-stu-id="e9aed-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="e9aed-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9aed-137">NOTES</span></span>

## <span data-ttu-id="e9aed-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9aed-138">RELATED LINKS</span></span>

[<span data-ttu-id="e9aed-139">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e9aed-139">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="e9aed-140">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e9aed-140">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="e9aed-141">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e9aed-141">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

