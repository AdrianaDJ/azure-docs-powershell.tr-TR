---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 35f2bc63366a86501650af1808274a3a0403e77f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278473"
---
# <span data-ttu-id="994ab-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="994ab-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="994ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="994ab-102">SYNOPSIS</span></span>
<span data-ttu-id="994ab-103">Veritabanında veri maskeleme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="994ab-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="994ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="994ab-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="994ab-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="994ab-105">DESCRIPTION</span></span>
<span data-ttu-id="994ab-106">**New-AzSqlDatabaseDataMaskingRule** cmdlet 'ı BIR Azure SQL veritabanı için veri maskeleme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="994ab-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="994ab-107">Cmdlet 'i kullanmak için, kuralı belirlemek üzere *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="994ab-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the rule.</span></span>
<span data-ttu-id="994ab-108">Verilerin maskelenme biçimini tanımlamak için kuralın hedefini ve *Maskingişlevi* parametresini belirtmek üzere *TableName* ve *ColumnName* sağlayın.</span><span class="sxs-lookup"><span data-stu-id="994ab-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="994ab-109">*Maskingişlevinin* bir numarası veya metin değeri varsa, sayı *maskeleme veya metin* maskeleme için *NumberFrom* *PrefixSize* , *replacementstring* ve *soneboyutu* değerlerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="994ab-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="994ab-110">Komut başarılı ve *geçiş parametresi kullanılırsa* cmdlet, kural tanımlayıcılarının yanı sıra veri maskeleme kuralı özelliklerini açıklayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="994ab-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="994ab-111">Kural tanımlayıcıları, *Resourcegroupname* , *ServerName* , *DatabaseName* ve *RuleId* ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="994ab-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>
<span data-ttu-id="994ab-112">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="994ab-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="994ab-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="994ab-113">EXAMPLES</span></span>

### <span data-ttu-id="994ab-114">Örnek 1: veritabanındaki sayı sütunu için veri maskeleme kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="994ab-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"  -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="994ab-115">Bu komut Schema01 adlı şemada Table01 adındaki tabloda Column01 adlı sütunda bir veri maskeleme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="994ab-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="994ab-116">Database01 adlı veritabanı tüm bu öğeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="994ab-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="994ab-117">Kural, maske değeri olarak 5 ile 14 arasında rastgele bir sayı kullanan bir sayı maskeleme kuralıdır.</span><span class="sxs-lookup"><span data-stu-id="994ab-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>

## <span data-ttu-id="994ab-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="994ab-118">PARAMETERS</span></span>

### <span data-ttu-id="994ab-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="994ab-119">-ColumnName</span></span>
<span data-ttu-id="994ab-120">Maskeleme kuralı tarafından hedeflenen sütunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="994ab-120">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="994ab-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="994ab-121">-DatabaseName</span></span>
<span data-ttu-id="994ab-122">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="994ab-122">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="994ab-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="994ab-123">-DefaultProfile</span></span>
<span data-ttu-id="994ab-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="994ab-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="994ab-125">-Maskingişlevi</span><span class="sxs-lookup"><span data-stu-id="994ab-125">-MaskingFunction</span></span>
<span data-ttu-id="994ab-126">Kuralın kullandığı maskeleme işlevini belirtir.</span><span class="sxs-lookup"><span data-stu-id="994ab-126">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="994ab-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="994ab-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="994ab-128">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="994ab-128">Default</span></span>
- <span data-ttu-id="994ab-129">Not</span><span class="sxs-lookup"><span data-stu-id="994ab-129">NoMasking</span></span>
- <span data-ttu-id="994ab-130">Metinleri</span><span class="sxs-lookup"><span data-stu-id="994ab-130">Text</span></span>
- <span data-ttu-id="994ab-131">Numarasıyla</span><span class="sxs-lookup"><span data-stu-id="994ab-131">Number</span></span>
- <span data-ttu-id="994ab-132">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="994ab-132">SocialSecurityNumber</span></span>
- <span data-ttu-id="994ab-133">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="994ab-133">CreditCardNumber</span></span>
- <span data-ttu-id="994ab-134">E-posta varsayılan değer varsayılandır.</span><span class="sxs-lookup"><span data-stu-id="994ab-134">Email The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="994ab-135">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="994ab-135">-NumberFrom</span></span>
<span data-ttu-id="994ab-136">Rastgele bir değer seçilen aralığın alt sınır numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="994ab-136">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="994ab-137">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir sayı değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="994ab-137">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="994ab-138">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="994ab-138">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="994ab-139">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="994ab-139">-NumberTo</span></span>
<span data-ttu-id="994ab-140">Rastgele bir değer seçilen aralığın üst sınır numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="994ab-140">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="994ab-141">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir sayı değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="994ab-141">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="994ab-142">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="994ab-142">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="994ab-143">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="994ab-143">-PassThru</span></span>
<span data-ttu-id="994ab-144">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="994ab-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="994ab-145">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="994ab-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="994ab-146">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="994ab-146">-PrefixSize</span></span>
<span data-ttu-id="994ab-147">Metnin başındaki metnin başındaki karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="994ab-147">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="994ab-148">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="994ab-148">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="994ab-149">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="994ab-149">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="994ab-150">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="994ab-150">-ReplacementString</span></span>
<span data-ttu-id="994ab-151">Metin kutusunun sonundaki karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="994ab-151">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="994ab-152">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="994ab-152">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="994ab-153">Varsayılan değer boş bir dizedir.</span><span class="sxs-lookup"><span data-stu-id="994ab-153">The default value is an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="994ab-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="994ab-154">-ResourceGroupName</span></span>
<span data-ttu-id="994ab-155">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="994ab-155">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="994ab-156">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="994ab-156">-SchemaName</span></span>
<span data-ttu-id="994ab-157">Şemanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="994ab-157">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="994ab-158">-ServerName</span><span class="sxs-lookup"><span data-stu-id="994ab-158">-ServerName</span></span>
<span data-ttu-id="994ab-159">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="994ab-159">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="994ab-160">-Soneboyut</span><span class="sxs-lookup"><span data-stu-id="994ab-160">-SuffixSize</span></span>
<span data-ttu-id="994ab-161">Metin düzeyinde, maskelenmeyen karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="994ab-161">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="994ab-162">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="994ab-162">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="994ab-163">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="994ab-163">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="994ab-164">-TableName</span><span class="sxs-lookup"><span data-stu-id="994ab-164">-TableName</span></span>
<span data-ttu-id="994ab-165">Maskelenmiş sütununu içeren veritabanı tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="994ab-165">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="994ab-166">-Onay</span><span class="sxs-lookup"><span data-stu-id="994ab-166">-Confirm</span></span>
<span data-ttu-id="994ab-167">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="994ab-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="994ab-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="994ab-168">-WhatIf</span></span>
<span data-ttu-id="994ab-169">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="994ab-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="994ab-170">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="994ab-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="994ab-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="994ab-171">CommonParameters</span></span>
<span data-ttu-id="994ab-172">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="994ab-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="994ab-173">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="994ab-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="994ab-174">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="994ab-174">INPUTS</span></span>

### <span data-ttu-id="994ab-175">System. String</span><span class="sxs-lookup"><span data-stu-id="994ab-175">System.String</span></span>

### <span data-ttu-id="994ab-176">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="994ab-176">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="994ab-177">System. Nullable ' 1 [[System. Double, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="994ab-177">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="994ab-178">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="994ab-178">OUTPUTS</span></span>

### <span data-ttu-id="994ab-179">Microsoft. Azure. Commands. Sql. Datamaskeleme. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="994ab-179">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="994ab-180">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="994ab-180">NOTES</span></span>

## <span data-ttu-id="994ab-181">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="994ab-181">RELATED LINKS</span></span>

[<span data-ttu-id="994ab-182">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="994ab-182">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="994ab-183">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="994ab-183">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="994ab-184">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="994ab-184">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="994ab-185">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="994ab-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


