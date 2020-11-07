---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: dd29dd7e58a233d62e3af5260971d56300a43230
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762339"
---
# <span data-ttu-id="7771e-101">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="7771e-101">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="7771e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7771e-102">SYNOPSIS</span></span>
<span data-ttu-id="7771e-103">Veritabanı için veri maskeleme kuralı özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7771e-103">Sets the properties of a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7771e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7771e-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7771e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7771e-105">DESCRIPTION</span></span>
<span data-ttu-id="7771e-106">**Set-AzureRmSqlDatabaseDataMaskingRule** cmdlet 'i, BIR Azure SQL veritabanı için veri maskeleme kuralı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7771e-106">The **Set-AzureRmSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="7771e-107">Cmdlet 'i kullanmak için, kuralı belirlemek üzere *Resourcegroupname* , *ServerName* , *DatabaseName* ve *RuleId* parametrelerini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="7771e-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="7771e-108">Kuralı yeniden uygulamak için *SchemaName* , *TableName* ve *ColumnName* parametrelerinden herhangi birini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7771e-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="7771e-109">Verilerin maskelenme biçimini değiştirmek için *Maskingişlevi* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="7771e-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>

<span data-ttu-id="7771e-110">*Maskingişlevi* Için bir sayı veya metin değeri belirtirseniz, sayı maskeleme için sayı veya sayı veya *NumberFrom* metin maskeleme için *PrefixSize* , *replacementstring* ve *soneboyutu* *parametrelerini belirtebilirsiniz* .</span><span class="sxs-lookup"><span data-stu-id="7771e-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="7771e-111">Komut başarılı olur ve *geçiş parametresini belirtirseniz* cmdlet, veri maskeleme kuralı özelliklerini ve kural tanımlayıcılarını tanımlayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="7771e-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="7771e-112">Kural tanımlayıcıları, **Resourcegroupname** , **ServerName** , **DatabaseName** ve **RuleId** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="7771e-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>

<span data-ttu-id="7771e-113">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="7771e-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7771e-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7771e-114">EXAMPLES</span></span>

### <span data-ttu-id="7771e-115">Örnek 1: veritabanında veri maskeleme kuralı aralığını değiştirme</span><span class="sxs-lookup"><span data-stu-id="7771e-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="7771e-116">Bu komut, Rule17 KIMLIĞINE sahip bir veri maskeleme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7771e-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="7771e-117">Bu kural, Database01 adındaki veritabanında server01.</span><span class="sxs-lookup"><span data-stu-id="7771e-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="7771e-118">Bu komut, maskelenmiş değer olarak rastgele bir sayının üretildiği aralığın sınırlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7771e-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="7771e-119">Yeni Aralık 23 ile 42 arasındadır.</span><span class="sxs-lookup"><span data-stu-id="7771e-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="7771e-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7771e-120">PARAMETERS</span></span>

### <span data-ttu-id="7771e-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="7771e-121">-ColumnName</span></span>
<span data-ttu-id="7771e-122">Maskeleme kuralı tarafından hedeflenen sütunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7771e-122">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="7771e-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7771e-123">-DatabaseName</span></span>
<span data-ttu-id="7771e-124">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7771e-124">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="7771e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7771e-125">-DefaultProfile</span></span>
<span data-ttu-id="7771e-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7771e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7771e-127">-Maskingişlevi</span><span class="sxs-lookup"><span data-stu-id="7771e-127">-MaskingFunction</span></span>
<span data-ttu-id="7771e-128">Kuralın kullandığı maskeleme işlevini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7771e-128">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="7771e-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7771e-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7771e-130">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="7771e-130">Default</span></span>
- <span data-ttu-id="7771e-131">Not</span><span class="sxs-lookup"><span data-stu-id="7771e-131">NoMasking</span></span>
- <span data-ttu-id="7771e-132">Metinleri</span><span class="sxs-lookup"><span data-stu-id="7771e-132">Text</span></span>
- <span data-ttu-id="7771e-133">Numarasıyla</span><span class="sxs-lookup"><span data-stu-id="7771e-133">Number</span></span>
- <span data-ttu-id="7771e-134">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="7771e-134">SocialSecurityNumber</span></span>
- <span data-ttu-id="7771e-135">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="7771e-135">CreditCardNumber</span></span>
- <span data-ttu-id="7771e-136">E-posta</span><span class="sxs-lookup"><span data-stu-id="7771e-136">Email</span></span>

<span data-ttu-id="7771e-137">Varsayılan değer varsayılandır.</span><span class="sxs-lookup"><span data-stu-id="7771e-137">The default value is Default.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7771e-138">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="7771e-138">-NumberFrom</span></span>
<span data-ttu-id="7771e-139">Rastgele bir değer seçilen aralığın alt sınır numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7771e-139">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="7771e-140">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir sayı değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="7771e-140">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="7771e-141">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="7771e-141">The default value is 0.</span></span>

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

### <span data-ttu-id="7771e-142">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="7771e-142">-NumberTo</span></span>
<span data-ttu-id="7771e-143">Rastgele bir değer seçilen aralığın üst sınır numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7771e-143">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="7771e-144">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir sayı değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="7771e-144">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="7771e-145">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="7771e-145">The default value is 0.</span></span>

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

### <span data-ttu-id="7771e-146">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7771e-146">-PassThru</span></span>
<span data-ttu-id="7771e-147">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="7771e-147">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7771e-148">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="7771e-148">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7771e-149">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="7771e-149">-PrefixSize</span></span>
<span data-ttu-id="7771e-150">Metnin başındaki metnin başındaki karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7771e-150">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="7771e-151">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="7771e-151">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="7771e-152">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="7771e-152">The default value is 0.</span></span>

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

### <span data-ttu-id="7771e-153">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="7771e-153">-ReplacementString</span></span>
<span data-ttu-id="7771e-154">Metin düzeyinde, maskelenmeyen karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7771e-154">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="7771e-155">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="7771e-155">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="7771e-156">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="7771e-156">The default value is 0.</span></span>

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

### <span data-ttu-id="7771e-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7771e-157">-ResourceGroupName</span></span>
<span data-ttu-id="7771e-158">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7771e-158">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="7771e-159">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="7771e-159">-SchemaName</span></span>
<span data-ttu-id="7771e-160">Şemanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7771e-160">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="7771e-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7771e-161">-ServerName</span></span>
<span data-ttu-id="7771e-162">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7771e-162">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="7771e-163">-Soneboyut</span><span class="sxs-lookup"><span data-stu-id="7771e-163">-SuffixSize</span></span>
<span data-ttu-id="7771e-164">Metin düzeyinde, maskelenmeyen karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7771e-164">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="7771e-165">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="7771e-165">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="7771e-166">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="7771e-166">The default value is 0.</span></span>

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

### <span data-ttu-id="7771e-167">-TableName</span><span class="sxs-lookup"><span data-stu-id="7771e-167">-TableName</span></span>
<span data-ttu-id="7771e-168">Maskelenmiş sütununu içeren veritabanı tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7771e-168">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="7771e-169">-Onay</span><span class="sxs-lookup"><span data-stu-id="7771e-169">-Confirm</span></span>
<span data-ttu-id="7771e-170">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7771e-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7771e-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7771e-171">-WhatIf</span></span>
<span data-ttu-id="7771e-172">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7771e-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7771e-173">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7771e-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7771e-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7771e-174">CommonParameters</span></span>
<span data-ttu-id="7771e-175">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7771e-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7771e-176">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7771e-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7771e-177">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7771e-177">INPUTS</span></span>

###  
<span data-ttu-id="7771e-178">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7771e-178">None</span></span>

## <span data-ttu-id="7771e-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7771e-179">OUTPUTS</span></span>

### <span data-ttu-id="7771e-180">Microsoft. Azure. Commands. Sql. Security. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="7771e-180">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="7771e-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7771e-181">NOTES</span></span>

## <span data-ttu-id="7771e-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7771e-182">RELATED LINKS</span></span>

[<span data-ttu-id="7771e-183">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="7771e-183">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="7771e-184">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="7771e-184">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="7771e-185">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="7771e-185">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="7771e-186">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="7771e-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


