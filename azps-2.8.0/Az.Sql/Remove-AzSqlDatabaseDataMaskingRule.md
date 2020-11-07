---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 016b77c7e58a3c95405d6364118a9d0ec7815660
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933552"
---
# <span data-ttu-id="eb0a4-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="eb0a4-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="eb0a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb0a4-102">SYNOPSIS</span></span>
<span data-ttu-id="eb0a4-103">Veritabanından veri maskeleme kuralı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="eb0a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb0a4-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb0a4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb0a4-105">DESCRIPTION</span></span>
<span data-ttu-id="eb0a4-106">**Remove-AzSqlDatabaseDataMaskingRule** cmdlet 'ı, Azure SQL veritabanından belirli bir veri maskeleme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="eb0a4-107">Bu cmdlet 'in kaldırıldığı kuralı belirlemek için *Resourcegroupname* , *ServerName* , *DatabaseName* ve *RuleId* parametrelerini kullanarak veri maskeleme kuralını kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-107">You can remove a data masking rule by using the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="eb0a4-108">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="eb0a4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb0a4-109">EXAMPLES</span></span>

### <span data-ttu-id="eb0a4-110">Örnek 1: veritabanı veri maskeleme kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="eb0a4-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="eb0a4-111">Bu komut Rule01 Database01 veritabanı için tanımlanan kural adını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="eb0a4-112">Veritabanı Server01 üzerinde yer alır ve kaynak grubuna ResourceGroup01 atanır.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="eb0a4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb0a4-113">PARAMETERS</span></span>

### <span data-ttu-id="eb0a4-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="eb0a4-114">-ColumnName</span></span>
<span data-ttu-id="eb0a4-115">Maskeleme kuralı tarafından hedeflenen sütunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="eb0a4-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eb0a4-116">-DatabaseName</span></span>
<span data-ttu-id="eb0a4-117">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="eb0a4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb0a4-118">-DefaultProfile</span></span>
<span data-ttu-id="eb0a4-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="eb0a4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb0a4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="eb0a4-120">-Force</span></span>
<span data-ttu-id="eb0a4-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eb0a4-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="eb0a4-122">-PassThru</span></span>
<span data-ttu-id="eb0a4-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="eb0a4-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eb0a4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb0a4-125">-ResourceGroupName</span></span>
<span data-ttu-id="eb0a4-126">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="eb0a4-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="eb0a4-127">-SchemaName</span></span>
<span data-ttu-id="eb0a4-128">Şemanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-128">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="eb0a4-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eb0a4-129">-ServerName</span></span>
<span data-ttu-id="eb0a4-130">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="eb0a4-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="eb0a4-131">-TableName</span></span>
<span data-ttu-id="eb0a4-132">Azure SQL tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-132">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="eb0a4-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="eb0a4-133">-Confirm</span></span>
<span data-ttu-id="eb0a4-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb0a4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb0a4-135">-WhatIf</span></span>
<span data-ttu-id="eb0a4-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb0a4-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb0a4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb0a4-138">CommonParameters</span></span>
<span data-ttu-id="eb0a4-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb0a4-140">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="eb0a4-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb0a4-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb0a4-141">INPUTS</span></span>

### <span data-ttu-id="eb0a4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="eb0a4-142">System.String</span></span>

## <span data-ttu-id="eb0a4-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb0a4-143">OUTPUTS</span></span>

### <span data-ttu-id="eb0a4-144">Microsoft. Azure. Commands. Sql. Datamaskeleme. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="eb0a4-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="eb0a4-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb0a4-145">NOTES</span></span>

## <span data-ttu-id="eb0a4-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb0a4-146">RELATED LINKS</span></span>

[<span data-ttu-id="eb0a4-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="eb0a4-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="eb0a4-148">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="eb0a4-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="eb0a4-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="eb0a4-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="eb0a4-150">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="eb0a4-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


