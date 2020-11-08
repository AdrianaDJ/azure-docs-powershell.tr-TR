---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: d7508f50b39f04894e365ff19b7018ecd4baf445
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096225"
---
# <span data-ttu-id="5782e-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5782e-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="5782e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5782e-102">SYNOPSIS</span></span>
<span data-ttu-id="5782e-103">Veritabanında veri maskeleme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5782e-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="5782e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5782e-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5782e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5782e-105">DESCRIPTION</span></span>
<span data-ttu-id="5782e-106">**New-AzSqlDatabaseDataMaskingRule** cmdlet 'ı BIR Azure SQL veritabanı için veri maskeleme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5782e-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="5782e-107">Cmdlet 'i kullanmak için, kuralı belirlemek üzere *Resourcegroupname* , *ServerName* , *DatabaseName* ve *RuleId* parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5782e-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="5782e-108">Verilerin maskelenme biçimini tanımlamak için kuralın hedefini ve *Maskingişlevi* parametresini belirtmek üzere *TableName* ve *ColumnName* sağlayın.</span><span class="sxs-lookup"><span data-stu-id="5782e-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="5782e-109">*Maskingişlevinin* bir numarası veya metin değeri varsa, sayı *maskeleme veya metin* maskeleme için *NumberFrom* *PrefixSize* , *replacementstring* ve *soneboyutu* değerlerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5782e-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="5782e-110">Komut başarılı ve *geçiş parametresi kullanılırsa* cmdlet, kural tanımlayıcılarının yanı sıra veri maskeleme kuralı özelliklerini açıklayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="5782e-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="5782e-111">Kural tanımlayıcıları, *Resourcegroupname* , *ServerName* , *DatabaseName* ve *RuleId* ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="5782e-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>
<span data-ttu-id="5782e-112">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="5782e-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5782e-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5782e-113">EXAMPLES</span></span>

### <span data-ttu-id="5782e-114">Örnek 1: veritabanındaki sayı sütunu için veri maskeleme kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="5782e-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="5782e-115">Bu komut Schema01 adlı şemada Table01 adındaki tabloda Column01 adlı sütunda bir veri maskeleme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5782e-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="5782e-116">Database01 adlı veritabanı tüm bu öğeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="5782e-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="5782e-117">Kural, maske değeri olarak 5 ile 14 arasında rastgele bir sayı kullanan bir sayı maskeleme kuralıdır.</span><span class="sxs-lookup"><span data-stu-id="5782e-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="5782e-118">Kural Rule01 olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="5782e-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="5782e-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5782e-119">PARAMETERS</span></span>

### <span data-ttu-id="5782e-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="5782e-120">-ColumnName</span></span>
<span data-ttu-id="5782e-121">Maskeleme kuralı tarafından hedeflenen sütunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5782e-121">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="5782e-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5782e-122">-DatabaseName</span></span>
<span data-ttu-id="5782e-123">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5782e-123">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="5782e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5782e-124">-DefaultProfile</span></span>
<span data-ttu-id="5782e-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5782e-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5782e-126">-Maskingişlevi</span><span class="sxs-lookup"><span data-stu-id="5782e-126">-MaskingFunction</span></span>
<span data-ttu-id="5782e-127">Kuralın kullandığı maskeleme işlevini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5782e-127">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="5782e-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5782e-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5782e-129">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="5782e-129">Default</span></span>
- <span data-ttu-id="5782e-130">Not</span><span class="sxs-lookup"><span data-stu-id="5782e-130">NoMasking</span></span>
- <span data-ttu-id="5782e-131">Metinleri</span><span class="sxs-lookup"><span data-stu-id="5782e-131">Text</span></span>
- <span data-ttu-id="5782e-132">Numarasıyla</span><span class="sxs-lookup"><span data-stu-id="5782e-132">Number</span></span>
- <span data-ttu-id="5782e-133">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="5782e-133">SocialSecurityNumber</span></span>
- <span data-ttu-id="5782e-134">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="5782e-134">CreditCardNumber</span></span>
- <span data-ttu-id="5782e-135">E-posta varsayılan değer varsayılandır.</span><span class="sxs-lookup"><span data-stu-id="5782e-135">Email The default value is Default.</span></span>

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

### <span data-ttu-id="5782e-136">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="5782e-136">-NumberFrom</span></span>
<span data-ttu-id="5782e-137">Rastgele bir değer seçilen aralığın alt sınır numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5782e-137">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="5782e-138">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir sayı değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="5782e-138">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="5782e-139">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="5782e-139">The default value is 0.</span></span>

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

### <span data-ttu-id="5782e-140">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="5782e-140">-NumberTo</span></span>
<span data-ttu-id="5782e-141">Rastgele bir değer seçilen aralığın üst sınır numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5782e-141">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="5782e-142">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir sayı değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="5782e-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="5782e-143">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="5782e-143">The default value is 0.</span></span>

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

### <span data-ttu-id="5782e-144">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5782e-144">-PassThru</span></span>
<span data-ttu-id="5782e-145">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="5782e-145">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5782e-146">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="5782e-146">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5782e-147">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="5782e-147">-PrefixSize</span></span>
<span data-ttu-id="5782e-148">Metnin başındaki metnin başındaki karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5782e-148">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="5782e-149">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="5782e-149">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="5782e-150">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="5782e-150">The default value is 0.</span></span>

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

### <span data-ttu-id="5782e-151">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="5782e-151">-ReplacementString</span></span>
<span data-ttu-id="5782e-152">Metin kutusunun sonundaki karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5782e-152">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="5782e-153">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="5782e-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="5782e-154">Varsayılan değer boş bir dizedir.</span><span class="sxs-lookup"><span data-stu-id="5782e-154">The default value is an empty string.</span></span>

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

### <span data-ttu-id="5782e-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5782e-155">-ResourceGroupName</span></span>
<span data-ttu-id="5782e-156">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5782e-156">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="5782e-157">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="5782e-157">-SchemaName</span></span>
<span data-ttu-id="5782e-158">Şemanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5782e-158">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="5782e-159">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5782e-159">-ServerName</span></span>
<span data-ttu-id="5782e-160">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5782e-160">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="5782e-161">-Soneboyut</span><span class="sxs-lookup"><span data-stu-id="5782e-161">-SuffixSize</span></span>
<span data-ttu-id="5782e-162">Metin düzeyinde, maskelenmeyen karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5782e-162">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="5782e-163">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="5782e-163">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="5782e-164">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="5782e-164">The default value is 0.</span></span>

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

### <span data-ttu-id="5782e-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="5782e-165">-TableName</span></span>
<span data-ttu-id="5782e-166">Maskelenmiş sütununu içeren veritabanı tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5782e-166">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="5782e-167">-Onay</span><span class="sxs-lookup"><span data-stu-id="5782e-167">-Confirm</span></span>
<span data-ttu-id="5782e-168">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5782e-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5782e-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5782e-169">-WhatIf</span></span>
<span data-ttu-id="5782e-170">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5782e-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5782e-171">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5782e-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5782e-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5782e-172">CommonParameters</span></span>
<span data-ttu-id="5782e-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5782e-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5782e-174">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5782e-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5782e-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5782e-175">INPUTS</span></span>

### <span data-ttu-id="5782e-176">System. String</span><span class="sxs-lookup"><span data-stu-id="5782e-176">System.String</span></span>

### <span data-ttu-id="5782e-177">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="5782e-177">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5782e-178">System. Nullable ' 1 [[System. Double, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="5782e-178">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5782e-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5782e-179">OUTPUTS</span></span>

### <span data-ttu-id="5782e-180">Microsoft. Azure. Commands. Sql. Datamaskeleme. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="5782e-180">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="5782e-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5782e-181">NOTES</span></span>

## <span data-ttu-id="5782e-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5782e-182">RELATED LINKS</span></span>

[<span data-ttu-id="5782e-183">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5782e-183">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="5782e-184">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5782e-184">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="5782e-185">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5782e-185">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="5782e-186">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="5782e-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

