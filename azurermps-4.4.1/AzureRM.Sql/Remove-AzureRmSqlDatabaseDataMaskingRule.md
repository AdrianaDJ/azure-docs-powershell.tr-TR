---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 7f5f72652a0b3c8e1944b6091b43f1458fd17839
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765051"
---
# <span data-ttu-id="fbd66-101">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fbd66-101">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="fbd66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbd66-102">SYNOPSIS</span></span>
<span data-ttu-id="fbd66-103">Veritabanından veri maskeleme kuralı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fbd66-103">Removes a data masking rule from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbd66-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fbd66-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbd66-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fbd66-105">DESCRIPTION</span></span>
<span data-ttu-id="fbd66-106">**Remove-AzureRmSqlDatabaseDataMaskingRule** cmdlet 'ı, Azure SQL veritabanından belirli bir veri maskeleme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fbd66-106">The **Remove-AzureRmSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="fbd66-107">Bu cmdlet 'in kaldırıldığı kuralı belirlemek için *Resourcegroupname* , *ServerName* , *DatabaseName* ve *RuleId* parametrelerini kullanarak veri maskeleme kuralını kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbd66-107">You can remove a data masking rule by using the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>

<span data-ttu-id="fbd66-108">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="fbd66-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="fbd66-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fbd66-109">EXAMPLES</span></span>

### <span data-ttu-id="fbd66-110">Örnek 1: veritabanı veri maskeleme kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="fbd66-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="fbd66-111">Bu komut Rule01 Database01 veritabanı için tanımlanan kural adını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fbd66-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="fbd66-112">Veritabanı Server01 üzerinde yer alır ve kaynak grubuna ResourceGroup01 atanır.</span><span class="sxs-lookup"><span data-stu-id="fbd66-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="fbd66-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fbd66-113">PARAMETERS</span></span>

### <span data-ttu-id="fbd66-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="fbd66-114">-ColumnName</span></span>
<span data-ttu-id="fbd66-115">Maskeleme kuralı tarafından hedeflenen sütunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbd66-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="fbd66-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fbd66-116">-DatabaseName</span></span>
<span data-ttu-id="fbd66-117">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbd66-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="fbd66-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fbd66-118">-Force</span></span>
<span data-ttu-id="fbd66-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="fbd66-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fbd66-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fbd66-120">-PassThru</span></span>
<span data-ttu-id="fbd66-121">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="fbd66-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fbd66-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="fbd66-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fbd66-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbd66-123">-ResourceGroupName</span></span>
<span data-ttu-id="fbd66-124">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbd66-124">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="fbd66-125">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="fbd66-125">-SchemaName</span></span>
<span data-ttu-id="fbd66-126">Şemanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbd66-126">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="fbd66-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fbd66-127">-ServerName</span></span>
<span data-ttu-id="fbd66-128">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbd66-128">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="fbd66-129">-TableName</span><span class="sxs-lookup"><span data-stu-id="fbd66-129">-TableName</span></span>
<span data-ttu-id="fbd66-130">Azure SQL tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbd66-130">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="fbd66-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="fbd66-131">-Confirm</span></span>
<span data-ttu-id="fbd66-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fbd66-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbd66-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbd66-133">-WhatIf</span></span>
<span data-ttu-id="fbd66-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fbd66-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbd66-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fbd66-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbd66-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbd66-136">-DefaultProfile</span></span>
<span data-ttu-id="fbd66-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fbd66-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbd66-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbd66-138">CommonParameters</span></span>
<span data-ttu-id="fbd66-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fbd66-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbd66-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbd66-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbd66-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fbd66-141">INPUTS</span></span>

### <span data-ttu-id="fbd66-142">Microsoft. Azure. Commands. Sql. Security. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="fbd66-142">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="fbd66-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fbd66-143">OUTPUTS</span></span>

### <span data-ttu-id="fbd66-144">Microsoft. Azure. Commands. Sql. Security. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="fbd66-144">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="fbd66-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fbd66-145">NOTES</span></span>

## <span data-ttu-id="fbd66-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fbd66-146">RELATED LINKS</span></span>

[<span data-ttu-id="fbd66-147">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fbd66-147">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="fbd66-148">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fbd66-148">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="fbd66-149">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fbd66-149">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="fbd66-150">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="fbd66-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


