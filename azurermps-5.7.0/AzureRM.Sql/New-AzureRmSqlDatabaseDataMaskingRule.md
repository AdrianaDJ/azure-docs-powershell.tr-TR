---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: b53b32b30e1b69da94ac8319ed3a5f4eee7ffc0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573169"
---
# <span data-ttu-id="acd4e-101">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="acd4e-101">New-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="acd4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acd4e-102">SYNOPSIS</span></span>
<span data-ttu-id="acd4e-103">Veritabanında veri maskeleme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="acd4e-103">Creates a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acd4e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="acd4e-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="acd4e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="acd4e-105">DESCRIPTION</span></span>
<span data-ttu-id="acd4e-106">**New-AzureRmSqlDatabaseDataMaskingRule** cmdlet 'i, BIR Azure SQL veritabanı için veri maskeleme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="acd4e-106">The **New-AzureRmSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="acd4e-107">Cmdlet 'i kullanmak için, kuralı belirlemek üzere *Resourcegroupname* , *ServerName* , *DatabaseName* ve *RuleId* parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="acd4e-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="acd4e-108">Verilerin maskelenme biçimini tanımlamak için kuralın hedefini ve *Maskingişlevi* parametresini belirtmek üzere *TableName* ve *ColumnName* sağlayın.</span><span class="sxs-lookup"><span data-stu-id="acd4e-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>

<span data-ttu-id="acd4e-109">*Maskingişlevinin* bir numarası veya metin değeri varsa, sayı *maskeleme veya metin* maskeleme için *NumberFrom* *PrefixSize* , *replacementstring* ve *soneboyutu* değerlerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="acd4e-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>

<span data-ttu-id="acd4e-110">Komut başarılı ve *geçiş parametresi kullanılırsa* cmdlet, kural tanımlayıcılarının yanı sıra veri maskeleme kuralı özelliklerini açıklayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="acd4e-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="acd4e-111">Kural tanımlayıcıları, *Resourcegroupname* , *ServerName* , *DatabaseName* ve *RuleId* ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="acd4e-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>

<span data-ttu-id="acd4e-112">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="acd4e-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="acd4e-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="acd4e-113">EXAMPLES</span></span>

### <span data-ttu-id="acd4e-114">Örnek 1: veritabanındaki sayı sütunu için veri maskeleme kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="acd4e-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="acd4e-115">Bu komut Schema01 adlı şemada Table01 adındaki tabloda Column01 adlı sütunda bir veri maskeleme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="acd4e-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="acd4e-116">Database01 adlı veritabanı tüm bu öğeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="acd4e-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="acd4e-117">Kural, maske değeri olarak 5 ile 14 arasında rastgele bir sayı kullanan bir sayı maskeleme kuralıdır.</span><span class="sxs-lookup"><span data-stu-id="acd4e-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="acd4e-118">Kural Rule01 olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="acd4e-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="acd4e-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="acd4e-119">PARAMETERS</span></span>

### <span data-ttu-id="acd4e-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="acd4e-120">-ColumnName</span></span>
<span data-ttu-id="acd4e-121">Maskeleme kuralı tarafından hedeflenen sütunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acd4e-121">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd4e-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="acd4e-122">-DatabaseName</span></span>
<span data-ttu-id="acd4e-123">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acd4e-123">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd4e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acd4e-124">-DefaultProfile</span></span>
<span data-ttu-id="acd4e-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="acd4e-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd4e-126">-Maskingişlevi</span><span class="sxs-lookup"><span data-stu-id="acd4e-126">-MaskingFunction</span></span>
<span data-ttu-id="acd4e-127">Kuralın kullandığı maskeleme işlevini belirtir.</span><span class="sxs-lookup"><span data-stu-id="acd4e-127">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="acd4e-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="acd4e-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="acd4e-129">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="acd4e-129">Default</span></span>
- <span data-ttu-id="acd4e-130">Not</span><span class="sxs-lookup"><span data-stu-id="acd4e-130">NoMasking</span></span>
- <span data-ttu-id="acd4e-131">Metinleri</span><span class="sxs-lookup"><span data-stu-id="acd4e-131">Text</span></span>
- <span data-ttu-id="acd4e-132">Numarasıyla</span><span class="sxs-lookup"><span data-stu-id="acd4e-132">Number</span></span>
- <span data-ttu-id="acd4e-133">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="acd4e-133">SocialSecurityNumber</span></span>
- <span data-ttu-id="acd4e-134">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="acd4e-134">CreditCardNumber</span></span>
- <span data-ttu-id="acd4e-135">E-posta</span><span class="sxs-lookup"><span data-stu-id="acd4e-135">Email</span></span>

<span data-ttu-id="acd4e-136">Varsayılan değer varsayılandır.</span><span class="sxs-lookup"><span data-stu-id="acd4e-136">The default value is Default.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd4e-137">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="acd4e-137">-NumberFrom</span></span>
<span data-ttu-id="acd4e-138">Rastgele bir değer seçilen aralığın alt sınır numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acd4e-138">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="acd4e-139">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir sayı değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="acd4e-139">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="acd4e-140">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="acd4e-140">The default value is 0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd4e-141">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="acd4e-141">-NumberTo</span></span>
<span data-ttu-id="acd4e-142">Rastgele bir değer seçilen aralığın üst sınır numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acd4e-142">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="acd4e-143">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir sayı değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="acd4e-143">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="acd4e-144">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="acd4e-144">The default value is 0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd4e-145">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="acd4e-145">-PassThru</span></span>
<span data-ttu-id="acd4e-146">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="acd4e-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="acd4e-147">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="acd4e-147">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd4e-148">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="acd4e-148">-PrefixSize</span></span>
<span data-ttu-id="acd4e-149">Metnin başındaki metnin başındaki karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acd4e-149">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="acd4e-150">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="acd4e-150">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="acd4e-151">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="acd4e-151">The default value is 0.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd4e-152">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="acd4e-152">-ReplacementString</span></span>
<span data-ttu-id="acd4e-153">Metin kutusunun sonundaki karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acd4e-153">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="acd4e-154">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="acd4e-154">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="acd4e-155">Varsayılan değer boş bir dizedir.</span><span class="sxs-lookup"><span data-stu-id="acd4e-155">The default value is an empty string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd4e-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acd4e-156">-ResourceGroupName</span></span>
<span data-ttu-id="acd4e-157">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acd4e-157">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd4e-158">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="acd4e-158">-SchemaName</span></span>
<span data-ttu-id="acd4e-159">Şemanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acd4e-159">Specifies the name of a schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd4e-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="acd4e-160">-ServerName</span></span>
<span data-ttu-id="acd4e-161">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acd4e-161">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd4e-162">-Soneboyut</span><span class="sxs-lookup"><span data-stu-id="acd4e-162">-SuffixSize</span></span>
<span data-ttu-id="acd4e-163">Metin düzeyinde, maskelenmeyen karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acd4e-163">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="acd4e-164">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="acd4e-164">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="acd4e-165">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="acd4e-165">The default value is 0.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd4e-166">-TableName</span><span class="sxs-lookup"><span data-stu-id="acd4e-166">-TableName</span></span>
<span data-ttu-id="acd4e-167">Maskelenmiş sütununu içeren veritabanı tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acd4e-167">Specifies the name of the database table that contains the masked column.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd4e-168">-Onay</span><span class="sxs-lookup"><span data-stu-id="acd4e-168">-Confirm</span></span>
<span data-ttu-id="acd4e-169">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="acd4e-169">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd4e-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acd4e-170">-WhatIf</span></span>
<span data-ttu-id="acd4e-171">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="acd4e-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acd4e-172">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="acd4e-172">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd4e-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd4e-173">CommonParameters</span></span>
<span data-ttu-id="acd4e-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="acd4e-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd4e-175">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acd4e-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd4e-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="acd4e-176">INPUTS</span></span>

###  
<span data-ttu-id="acd4e-177">Yabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="acd4e-177">None.</span></span>

## <span data-ttu-id="acd4e-178">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="acd4e-178">OUTPUTS</span></span>

### <span data-ttu-id="acd4e-179">Microsoft. Azure. Commands. Sql. Security. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="acd4e-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="acd4e-180">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="acd4e-180">NOTES</span></span>

## <span data-ttu-id="acd4e-181">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="acd4e-181">RELATED LINKS</span></span>

[<span data-ttu-id="acd4e-182">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="acd4e-182">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="acd4e-183">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="acd4e-183">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="acd4e-184">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="acd4e-184">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="acd4e-185">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="acd4e-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


