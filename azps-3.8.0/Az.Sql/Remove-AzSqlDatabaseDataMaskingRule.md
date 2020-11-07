---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 02a6090a98a80300f886e8bbbd8e2622aa7981d4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937621"
---
# <span data-ttu-id="921c2-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="921c2-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="921c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="921c2-102">SYNOPSIS</span></span>
<span data-ttu-id="921c2-103">Veritabanından veri maskeleme kuralı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="921c2-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="921c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="921c2-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="921c2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="921c2-105">DESCRIPTION</span></span>
<span data-ttu-id="921c2-106">**Remove-AzSqlDatabaseDataMaskingRule** cmdlet 'ı, Azure SQL veritabanından belirli bir veri maskeleme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="921c2-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="921c2-107">Bu cmdlet 'in kaldırıldığı kuralı belirlemek için *Resourcegroupname* , *ServerName* , *DatabaseName* ve *RuleId* parametrelerini kullanarak veri maskeleme kuralını kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="921c2-107">You can remove a data masking rule by using the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="921c2-108">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="921c2-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="921c2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="921c2-109">EXAMPLES</span></span>

### <span data-ttu-id="921c2-110">Örnek 1: veritabanı veri maskeleme kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="921c2-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="921c2-111">Bu komut Rule01 Database01 veritabanı için tanımlanan kural adını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="921c2-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="921c2-112">Veritabanı Server01 üzerinde yer alır ve kaynak grubuna ResourceGroup01 atanır.</span><span class="sxs-lookup"><span data-stu-id="921c2-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="921c2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="921c2-113">PARAMETERS</span></span>

### <span data-ttu-id="921c2-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="921c2-114">-ColumnName</span></span>
<span data-ttu-id="921c2-115">Maskeleme kuralı tarafından hedeflenen sütunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="921c2-115">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="921c2-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="921c2-116">-DatabaseName</span></span>
<span data-ttu-id="921c2-117">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="921c2-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="921c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="921c2-118">-DefaultProfile</span></span>
<span data-ttu-id="921c2-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="921c2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="921c2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="921c2-120">-Force</span></span>
<span data-ttu-id="921c2-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="921c2-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="921c2-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="921c2-122">-PassThru</span></span>
<span data-ttu-id="921c2-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="921c2-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="921c2-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="921c2-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="921c2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="921c2-125">-ResourceGroupName</span></span>
<span data-ttu-id="921c2-126">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="921c2-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="921c2-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="921c2-127">-SchemaName</span></span>
<span data-ttu-id="921c2-128">Şemanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="921c2-128">Specifies the name of a schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="921c2-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="921c2-129">-ServerName</span></span>
<span data-ttu-id="921c2-130">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="921c2-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="921c2-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="921c2-131">-TableName</span></span>
<span data-ttu-id="921c2-132">Azure SQL tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="921c2-132">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="921c2-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="921c2-133">-Confirm</span></span>
<span data-ttu-id="921c2-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="921c2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="921c2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="921c2-135">-WhatIf</span></span>
<span data-ttu-id="921c2-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="921c2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="921c2-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="921c2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="921c2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="921c2-138">CommonParameters</span></span>
<span data-ttu-id="921c2-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="921c2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="921c2-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="921c2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="921c2-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="921c2-141">INPUTS</span></span>

### <span data-ttu-id="921c2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="921c2-142">System.String</span></span>

## <span data-ttu-id="921c2-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="921c2-143">OUTPUTS</span></span>

### <span data-ttu-id="921c2-144">Microsoft. Azure. Commands. Sql. Datamaskeleme. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="921c2-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="921c2-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="921c2-145">NOTES</span></span>

## <span data-ttu-id="921c2-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="921c2-146">RELATED LINKS</span></span>

[<span data-ttu-id="921c2-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="921c2-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="921c2-148">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="921c2-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="921c2-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="921c2-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="921c2-150">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="921c2-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


