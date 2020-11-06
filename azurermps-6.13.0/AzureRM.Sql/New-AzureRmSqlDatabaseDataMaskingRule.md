---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 69e59580d5ada03400420788169bba18d2f30444
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593631"
---
# <span data-ttu-id="b1cf4-101">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b1cf4-101">New-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="b1cf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="b1cf4-103">Veritabanında veri maskeleme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-103">Creates a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1cf4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1cf4-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1cf4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1cf4-105">DESCRIPTION</span></span>
<span data-ttu-id="b1cf4-106">**New-AzureRmSqlDatabaseDataMaskingRule** cmdlet 'i, BIR Azure SQL veritabanı için veri maskeleme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-106">The **New-AzureRmSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="b1cf4-107">Cmdlet 'i kullanmak için, kuralı belirlemek üzere *Resourcegroupname* , *ServerName* , *DatabaseName* ve *RuleId* parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="b1cf4-108">Verilerin maskelenme biçimini tanımlamak için kuralın hedefini ve *Maskingişlevi* parametresini belirtmek üzere *TableName* ve *ColumnName* sağlayın.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="b1cf4-109">*Maskingişlevinin* bir numarası veya metin değeri varsa, sayı *maskeleme veya metin* maskeleme için *NumberFrom* *PrefixSize* , *replacementstring* ve *soneboyutu* değerlerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="b1cf4-110">Komut başarılı ve *geçiş parametresi kullanılırsa* cmdlet, kural tanımlayıcılarının yanı sıra veri maskeleme kuralı özelliklerini açıklayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="b1cf4-111">Kural tanımlayıcıları, *Resourcegroupname* , *ServerName* , *DatabaseName* ve *RuleId* ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>
<span data-ttu-id="b1cf4-112">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b1cf4-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1cf4-113">EXAMPLES</span></span>

### <span data-ttu-id="b1cf4-114">Örnek 1: veritabanındaki sayı sütunu için veri maskeleme kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b1cf4-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="b1cf4-115">Bu komut Schema01 adlı şemada Table01 adındaki tabloda Column01 adlı sütunda bir veri maskeleme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="b1cf4-116">Database01 adlı veritabanı tüm bu öğeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="b1cf4-117">Kural, maske değeri olarak 5 ile 14 arasında rastgele bir sayı kullanan bir sayı maskeleme kuralıdır.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="b1cf4-118">Kural Rule01 olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="b1cf4-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1cf4-119">PARAMETERS</span></span>

### <span data-ttu-id="b1cf4-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="b1cf4-120">-ColumnName</span></span>
<span data-ttu-id="b1cf4-121">Maskeleme kuralı tarafından hedeflenen sütunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-121">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="b1cf4-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b1cf4-122">-DatabaseName</span></span>
<span data-ttu-id="b1cf4-123">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-123">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="b1cf4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1cf4-124">-DefaultProfile</span></span>
<span data-ttu-id="b1cf4-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b1cf4-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1cf4-126">-Maskingişlevi</span><span class="sxs-lookup"><span data-stu-id="b1cf4-126">-MaskingFunction</span></span>
<span data-ttu-id="b1cf4-127">Kuralın kullandığı maskeleme işlevini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-127">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="b1cf4-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b1cf4-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b1cf4-129">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="b1cf4-129">Default</span></span>
- <span data-ttu-id="b1cf4-130">Not</span><span class="sxs-lookup"><span data-stu-id="b1cf4-130">NoMasking</span></span>
- <span data-ttu-id="b1cf4-131">Metinleri</span><span class="sxs-lookup"><span data-stu-id="b1cf4-131">Text</span></span>
- <span data-ttu-id="b1cf4-132">Numarasıyla</span><span class="sxs-lookup"><span data-stu-id="b1cf4-132">Number</span></span>
- <span data-ttu-id="b1cf4-133">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="b1cf4-133">SocialSecurityNumber</span></span>
- <span data-ttu-id="b1cf4-134">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="b1cf4-134">CreditCardNumber</span></span>
- <span data-ttu-id="b1cf4-135">E-posta varsayılan değer varsayılandır.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-135">Email The default value is Default.</span></span>

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

### <span data-ttu-id="b1cf4-136">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="b1cf4-136">-NumberFrom</span></span>
<span data-ttu-id="b1cf4-137">Rastgele bir değer seçilen aralığın alt sınır numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-137">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="b1cf4-138">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir sayı değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-138">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="b1cf4-139">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-139">The default value is 0.</span></span>

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

### <span data-ttu-id="b1cf4-140">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="b1cf4-140">-NumberTo</span></span>
<span data-ttu-id="b1cf4-141">Rastgele bir değer seçilen aralığın üst sınır numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-141">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="b1cf4-142">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir sayı değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="b1cf4-143">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-143">The default value is 0.</span></span>

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

### <span data-ttu-id="b1cf4-144">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b1cf4-144">-PassThru</span></span>
<span data-ttu-id="b1cf4-145">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-145">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b1cf4-146">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-146">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b1cf4-147">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="b1cf4-147">-PrefixSize</span></span>
<span data-ttu-id="b1cf4-148">Metnin başındaki metnin başındaki karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-148">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="b1cf4-149">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-149">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="b1cf4-150">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-150">The default value is 0.</span></span>

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

### <span data-ttu-id="b1cf4-151">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="b1cf4-151">-ReplacementString</span></span>
<span data-ttu-id="b1cf4-152">Metin kutusunun sonundaki karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-152">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="b1cf4-153">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="b1cf4-154">Varsayılan değer boş bir dizedir.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-154">The default value is an empty string.</span></span>

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

### <span data-ttu-id="b1cf4-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1cf4-155">-ResourceGroupName</span></span>
<span data-ttu-id="b1cf4-156">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-156">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="b1cf4-157">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="b1cf4-157">-SchemaName</span></span>
<span data-ttu-id="b1cf4-158">Şemanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-158">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="b1cf4-159">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b1cf4-159">-ServerName</span></span>
<span data-ttu-id="b1cf4-160">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-160">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="b1cf4-161">-Soneboyut</span><span class="sxs-lookup"><span data-stu-id="b1cf4-161">-SuffixSize</span></span>
<span data-ttu-id="b1cf4-162">Metin düzeyinde, maskelenmeyen karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-162">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="b1cf4-163">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-163">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="b1cf4-164">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-164">The default value is 0.</span></span>

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

### <span data-ttu-id="b1cf4-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="b1cf4-165">-TableName</span></span>
<span data-ttu-id="b1cf4-166">Maskelenmiş sütununu içeren veritabanı tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-166">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="b1cf4-167">-Onay</span><span class="sxs-lookup"><span data-stu-id="b1cf4-167">-Confirm</span></span>
<span data-ttu-id="b1cf4-168">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1cf4-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1cf4-169">-WhatIf</span></span>
<span data-ttu-id="b1cf4-170">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1cf4-171">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1cf4-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1cf4-172">CommonParameters</span></span>
<span data-ttu-id="b1cf4-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1cf4-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1cf4-174">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1cf4-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1cf4-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1cf4-175">INPUTS</span></span>

### <span data-ttu-id="b1cf4-176">System. String</span><span class="sxs-lookup"><span data-stu-id="b1cf4-176">System.String</span></span>

### <span data-ttu-id="b1cf4-177">System. Nullable ' 1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b1cf4-177">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b1cf4-178">System. Nullable ' 1 [[System. Double, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b1cf4-178">System.Nullable\`1[[System.Double, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b1cf4-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1cf4-179">OUTPUTS</span></span>

### <span data-ttu-id="b1cf4-180">Microsoft. Azure. Commands. Sql. Datamaskeleme. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="b1cf4-180">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="b1cf4-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1cf4-181">NOTES</span></span>

## <span data-ttu-id="b1cf4-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1cf4-182">RELATED LINKS</span></span>

[<span data-ttu-id="b1cf4-183">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b1cf4-183">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b1cf4-184">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b1cf4-184">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b1cf4-185">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b1cf4-185">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b1cf4-186">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="b1cf4-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


