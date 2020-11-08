---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: d751954a5c66d9220513017aa62b6797f8f1ea6f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279795"
---
# <span data-ttu-id="0978a-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0978a-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="0978a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0978a-102">SYNOPSIS</span></span>
<span data-ttu-id="0978a-103">Elastik bir veritabanı havuzunu siler.</span><span class="sxs-lookup"><span data-stu-id="0978a-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="0978a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0978a-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0978a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0978a-105">DESCRIPTION</span></span>
<span data-ttu-id="0978a-106">**Remove-Azsqlelaunpool** cmdlet 'ı BIR Azure SQL veritabanı esnek havuzunu siler.</span><span class="sxs-lookup"><span data-stu-id="0978a-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="0978a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0978a-107">EXAMPLES</span></span>

### <span data-ttu-id="0978a-108">Örnek 1: esnek havuz silme</span><span class="sxs-lookup"><span data-stu-id="0978a-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="0978a-109">Bu komut, ElasticPool01 adlı bir esnek havuzu siler.</span><span class="sxs-lookup"><span data-stu-id="0978a-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="0978a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0978a-110">PARAMETERS</span></span>

### <span data-ttu-id="0978a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0978a-111">-DefaultProfile</span></span>
<span data-ttu-id="0978a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0978a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0978a-113">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="0978a-113">-ElasticPoolName</span></span>
<span data-ttu-id="0978a-114">Bu cmdlet 'in sildiği esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0978a-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0978a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0978a-115">-Force</span></span>
<span data-ttu-id="0978a-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="0978a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0978a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0978a-117">-ResourceGroupName</span></span>
<span data-ttu-id="0978a-118">Esnek havuzun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0978a-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="0978a-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0978a-119">-ServerName</span></span>
<span data-ttu-id="0978a-120">Esnek havuzu barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0978a-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="0978a-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="0978a-121">-Confirm</span></span>
<span data-ttu-id="0978a-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0978a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0978a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0978a-123">-WhatIf</span></span>
<span data-ttu-id="0978a-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0978a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0978a-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0978a-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0978a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0978a-126">CommonParameters</span></span>
<span data-ttu-id="0978a-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0978a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0978a-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0978a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0978a-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0978a-129">INPUTS</span></span>

### <span data-ttu-id="0978a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0978a-130">System.String</span></span>

## <span data-ttu-id="0978a-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0978a-131">OUTPUTS</span></span>

### <span data-ttu-id="0978a-132">Microsoft. Azure. Commands. Sql. Elaunpool. model. Azuresqlelakpoolmodel</span><span class="sxs-lookup"><span data-stu-id="0978a-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="0978a-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0978a-133">NOTES</span></span>

## <span data-ttu-id="0978a-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0978a-134">RELATED LINKS</span></span>

[<span data-ttu-id="0978a-135">Get-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="0978a-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="0978a-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="0978a-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="0978a-137">Get-Azsqlelaunpooldatabase</span><span class="sxs-lookup"><span data-stu-id="0978a-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="0978a-138">New-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="0978a-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="0978a-139">Set-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="0978a-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="0978a-140">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="0978a-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


