---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 02a6090a98a80300f886e8bbbd8e2622aa7981d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276640"
---
# <span data-ttu-id="3c231-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3c231-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="3c231-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c231-102">SYNOPSIS</span></span>
<span data-ttu-id="3c231-103">Veritabanından veri maskeleme kuralı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3c231-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="3c231-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c231-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c231-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c231-105">DESCRIPTION</span></span>
<span data-ttu-id="3c231-106">**Remove-AzSqlDatabaseDataMaskingRule** cmdlet 'ı, Azure SQL veritabanından belirli bir veri maskeleme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3c231-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="3c231-107">Bu cmdlet 'in kaldırıldığı kuralı belirlemek için *Resourcegroupname* , *ServerName* , *DatabaseName* ve *RuleId* parametrelerini kullanarak veri maskeleme kuralını kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3c231-107">You can remove a data masking rule by using the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="3c231-108">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="3c231-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3c231-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c231-109">EXAMPLES</span></span>

### <span data-ttu-id="3c231-110">Örnek 1: veritabanı veri maskeleme kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="3c231-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="3c231-111">Bu komut Rule01 Database01 veritabanı için tanımlanan kural adını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3c231-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="3c231-112">Veritabanı Server01 üzerinde yer alır ve kaynak grubuna ResourceGroup01 atanır.</span><span class="sxs-lookup"><span data-stu-id="3c231-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="3c231-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c231-113">PARAMETERS</span></span>

### <span data-ttu-id="3c231-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="3c231-114">-ColumnName</span></span>
<span data-ttu-id="3c231-115">Maskeleme kuralı tarafından hedeflenen sütunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c231-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="3c231-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3c231-116">-DatabaseName</span></span>
<span data-ttu-id="3c231-117">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c231-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="3c231-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c231-118">-DefaultProfile</span></span>
<span data-ttu-id="3c231-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3c231-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c231-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3c231-120">-Force</span></span>
<span data-ttu-id="3c231-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3c231-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3c231-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3c231-122">-PassThru</span></span>
<span data-ttu-id="3c231-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="3c231-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3c231-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="3c231-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3c231-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c231-125">-ResourceGroupName</span></span>
<span data-ttu-id="3c231-126">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c231-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="3c231-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="3c231-127">-SchemaName</span></span>
<span data-ttu-id="3c231-128">Şemanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c231-128">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="3c231-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3c231-129">-ServerName</span></span>
<span data-ttu-id="3c231-130">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c231-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="3c231-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="3c231-131">-TableName</span></span>
<span data-ttu-id="3c231-132">Azure SQL tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c231-132">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="3c231-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="3c231-133">-Confirm</span></span>
<span data-ttu-id="3c231-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3c231-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c231-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c231-135">-WhatIf</span></span>
<span data-ttu-id="3c231-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c231-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c231-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3c231-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c231-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c231-138">CommonParameters</span></span>
<span data-ttu-id="3c231-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c231-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c231-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3c231-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c231-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c231-141">INPUTS</span></span>

### <span data-ttu-id="3c231-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3c231-142">System.String</span></span>

## <span data-ttu-id="3c231-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c231-143">OUTPUTS</span></span>

### <span data-ttu-id="3c231-144">Microsoft. Azure. Commands. Sql. Datamaskeleme. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="3c231-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="3c231-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c231-145">NOTES</span></span>

## <span data-ttu-id="3c231-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c231-146">RELATED LINKS</span></span>

[<span data-ttu-id="3c231-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3c231-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="3c231-148">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3c231-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="3c231-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3c231-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="3c231-150">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="3c231-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


