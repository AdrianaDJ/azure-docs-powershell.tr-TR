---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 4e5f2578d0e9dbb2139b330ec0a7c2fe81b3124e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588029"
---
# <span data-ttu-id="92283-101">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="92283-101">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="92283-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92283-102">SYNOPSIS</span></span>
<span data-ttu-id="92283-103">Veritabanı için veri maskeleme kuralı özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="92283-103">Sets the properties of a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92283-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92283-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92283-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="92283-105">DESCRIPTION</span></span>
<span data-ttu-id="92283-106">**Set-AzureRmSqlDatabaseDataMaskingRule** cmdlet 'i, BIR Azure SQL veritabanı için veri maskeleme kuralı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="92283-106">The **Set-AzureRmSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="92283-107">Cmdlet 'i kullanmak için, kuralı belirlemek üzere *Resourcegroupname* , *ServerName* , *DatabaseName* ve *RuleId* parametrelerini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="92283-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="92283-108">Kuralı yeniden uygulamak için *SchemaName* , *TableName* ve *ColumnName* parametrelerinden herhangi birini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="92283-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="92283-109">Verilerin maskelenme biçimini değiştirmek için *Maskingişlevi* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="92283-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="92283-110">*Maskingişlevi* Için bir sayı veya metin değeri belirtirseniz, sayı maskeleme için sayı veya sayı veya *NumberFrom* metin maskeleme için *PrefixSize* , *replacementstring* ve *soneboyutu* *parametrelerini belirtebilirsiniz* .</span><span class="sxs-lookup"><span data-stu-id="92283-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="92283-111">Komut başarılı olur ve *geçiş parametresini belirtirseniz* cmdlet, veri maskeleme kuralı özelliklerini ve kural tanımlayıcılarını tanımlayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="92283-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="92283-112">Kural tanımlayıcıları, **Resourcegroupname** , **ServerName** , **DatabaseName** ve **RuleId** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="92283-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>
<span data-ttu-id="92283-113">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="92283-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="92283-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92283-114">EXAMPLES</span></span>

### <span data-ttu-id="92283-115">Örnek 1: veritabanında veri maskeleme kuralı aralığını değiştirme</span><span class="sxs-lookup"><span data-stu-id="92283-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="92283-116">Bu komut, Rule17 KIMLIĞINE sahip bir veri maskeleme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="92283-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="92283-117">Bu kural, Database01 adındaki veritabanında server01.</span><span class="sxs-lookup"><span data-stu-id="92283-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="92283-118">Bu komut, maskelenmiş değer olarak rastgele bir sayının üretildiği aralığın sınırlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="92283-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="92283-119">Yeni Aralık 23 ile 42 arasındadır.</span><span class="sxs-lookup"><span data-stu-id="92283-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="92283-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92283-120">PARAMETERS</span></span>

### <span data-ttu-id="92283-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="92283-121">-ColumnName</span></span>
<span data-ttu-id="92283-122">Maskeleme kuralı tarafından hedeflenen sütunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92283-122">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="92283-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="92283-123">-DatabaseName</span></span>
<span data-ttu-id="92283-124">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92283-124">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="92283-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92283-125">-DefaultProfile</span></span>
<span data-ttu-id="92283-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="92283-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92283-127">-Maskingişlevi</span><span class="sxs-lookup"><span data-stu-id="92283-127">-MaskingFunction</span></span>
<span data-ttu-id="92283-128">Kuralın kullandığı maskeleme işlevini belirtir.</span><span class="sxs-lookup"><span data-stu-id="92283-128">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="92283-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="92283-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="92283-130">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="92283-130">Default</span></span>
- <span data-ttu-id="92283-131">Not</span><span class="sxs-lookup"><span data-stu-id="92283-131">NoMasking</span></span>
- <span data-ttu-id="92283-132">Metinleri</span><span class="sxs-lookup"><span data-stu-id="92283-132">Text</span></span>
- <span data-ttu-id="92283-133">Numarasıyla</span><span class="sxs-lookup"><span data-stu-id="92283-133">Number</span></span>
- <span data-ttu-id="92283-134">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="92283-134">SocialSecurityNumber</span></span>
- <span data-ttu-id="92283-135">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="92283-135">CreditCardNumber</span></span>
- <span data-ttu-id="92283-136">E-posta varsayılan değer varsayılandır.</span><span class="sxs-lookup"><span data-stu-id="92283-136">Email The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92283-137">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="92283-137">-NumberFrom</span></span>
<span data-ttu-id="92283-138">Rastgele bir değer seçilen aralığın alt sınır numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92283-138">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="92283-139">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir sayı değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="92283-139">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="92283-140">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="92283-140">The default value is 0.</span></span>

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

### <span data-ttu-id="92283-141">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="92283-141">-NumberTo</span></span>
<span data-ttu-id="92283-142">Rastgele bir değer seçilen aralığın üst sınır numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92283-142">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="92283-143">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir sayı değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="92283-143">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="92283-144">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="92283-144">The default value is 0.</span></span>

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

### <span data-ttu-id="92283-145">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="92283-145">-PassThru</span></span>
<span data-ttu-id="92283-146">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="92283-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="92283-147">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="92283-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="92283-148">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="92283-148">-PrefixSize</span></span>
<span data-ttu-id="92283-149">Metnin başındaki metnin başındaki karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92283-149">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="92283-150">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="92283-150">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="92283-151">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="92283-151">The default value is 0.</span></span>

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

### <span data-ttu-id="92283-152">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="92283-152">-ReplacementString</span></span>
<span data-ttu-id="92283-153">Metin düzeyinde, maskelenmeyen karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92283-153">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="92283-154">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="92283-154">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="92283-155">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="92283-155">The default value is 0.</span></span>

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

### <span data-ttu-id="92283-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92283-156">-ResourceGroupName</span></span>
<span data-ttu-id="92283-157">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92283-157">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="92283-158">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="92283-158">-SchemaName</span></span>
<span data-ttu-id="92283-159">Şemanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92283-159">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="92283-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="92283-160">-ServerName</span></span>
<span data-ttu-id="92283-161">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92283-161">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="92283-162">-Soneboyut</span><span class="sxs-lookup"><span data-stu-id="92283-162">-SuffixSize</span></span>
<span data-ttu-id="92283-163">Metin düzeyinde, maskelenmeyen karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92283-163">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="92283-164">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="92283-164">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="92283-165">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="92283-165">The default value is 0.</span></span>

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

### <span data-ttu-id="92283-166">-TableName</span><span class="sxs-lookup"><span data-stu-id="92283-166">-TableName</span></span>
<span data-ttu-id="92283-167">Maskelenmiş sütununu içeren veritabanı tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92283-167">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="92283-168">-Onay</span><span class="sxs-lookup"><span data-stu-id="92283-168">-Confirm</span></span>
<span data-ttu-id="92283-169">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="92283-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92283-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92283-170">-WhatIf</span></span>
<span data-ttu-id="92283-171">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="92283-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92283-172">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="92283-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92283-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92283-173">CommonParameters</span></span>
<span data-ttu-id="92283-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92283-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92283-175">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92283-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92283-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92283-176">INPUTS</span></span>

### <span data-ttu-id="92283-177">System. String</span><span class="sxs-lookup"><span data-stu-id="92283-177">System.String</span></span>

### <span data-ttu-id="92283-178">System. Nullable ' 1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="92283-178">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="92283-179">System. Nullable ' 1 [[System. Double, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="92283-179">System.Nullable\`1[[System.Double, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="92283-180">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92283-180">OUTPUTS</span></span>

### <span data-ttu-id="92283-181">Microsoft. Azure. Commands. Sql. Datamaskeleme. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="92283-181">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="92283-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92283-182">NOTES</span></span>

## <span data-ttu-id="92283-183">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92283-183">RELATED LINKS</span></span>

[<span data-ttu-id="92283-184">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="92283-184">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="92283-185">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="92283-185">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="92283-186">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="92283-186">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="92283-187">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="92283-187">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


