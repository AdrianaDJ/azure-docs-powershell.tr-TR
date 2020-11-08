---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 544db2f0e23cb510c81fb64898b6bcf856e760e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279787"
---
# <span data-ttu-id="908cf-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="908cf-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="908cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="908cf-102">SYNOPSIS</span></span>
<span data-ttu-id="908cf-103">Veritabanı için veri maskeleme kuralı özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="908cf-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="908cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="908cf-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="908cf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="908cf-105">DESCRIPTION</span></span>
<span data-ttu-id="908cf-106">**Set-AzSqlDatabaseDataMaskingRule** cmdlet 'i, BIR Azure SQL veritabanı için veri maskeleme kuralı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="908cf-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="908cf-107">Cmdlet 'i kullanmak için, kuralı belirlemek üzere *Resourcegroupname* , *ServerName* , *DatabaseName* ve *RuleId* parametrelerini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="908cf-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="908cf-108">Kuralı yeniden uygulamak için *SchemaName* , *TableName* ve *ColumnName* parametrelerinden herhangi birini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="908cf-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="908cf-109">Verilerin maskelenme biçimini değiştirmek için *Maskingişlevi* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="908cf-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="908cf-110">*Maskingişlevi* Için bir sayı veya metin değeri belirtirseniz, sayı maskeleme için sayı veya sayı veya *NumberFrom* metin maskeleme için *PrefixSize* , *replacementstring* ve *soneboyutu* *parametrelerini belirtebilirsiniz* .</span><span class="sxs-lookup"><span data-stu-id="908cf-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="908cf-111">Komut başarılı olur ve *geçiş parametresini belirtirseniz* cmdlet, veri maskeleme kuralı özelliklerini ve kural tanımlayıcılarını tanımlayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="908cf-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="908cf-112">Kural tanımlayıcıları, **Resourcegroupname** , **ServerName** , **DatabaseName** ve **RuleId** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="908cf-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>
<span data-ttu-id="908cf-113">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="908cf-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="908cf-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="908cf-114">EXAMPLES</span></span>

### <span data-ttu-id="908cf-115">Örnek 1: veritabanında veri maskeleme kuralı aralığını değiştirme</span><span class="sxs-lookup"><span data-stu-id="908cf-115">Example 1: Change the range of a data masking rule in a database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="908cf-116">Bu komut, Rule17 KIMLIĞINE sahip bir veri maskeleme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="908cf-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="908cf-117">Bu kural, Database01 adındaki veritabanında server01.</span><span class="sxs-lookup"><span data-stu-id="908cf-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="908cf-118">Bu komut, maskelenmiş değer olarak rastgele bir sayının üretildiği aralığın sınırlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="908cf-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="908cf-119">Yeni Aralık 23 ile 42 arasındadır.</span><span class="sxs-lookup"><span data-stu-id="908cf-119">The new range is between 23 and 42.</span></span>

### <span data-ttu-id="908cf-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="908cf-120">Example 2</span></span>

<span data-ttu-id="908cf-121">Veritabanı için veri maskeleme kuralı özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="908cf-121">Sets the properties of a data masking rule for a database.</span></span> <span data-ttu-id="908cf-122">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="908cf-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## <span data-ttu-id="908cf-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="908cf-123">PARAMETERS</span></span>

### <span data-ttu-id="908cf-124">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="908cf-124">-ColumnName</span></span>
<span data-ttu-id="908cf-125">Maskeleme kuralı tarafından hedeflenen sütunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="908cf-125">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="908cf-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="908cf-126">-DatabaseName</span></span>
<span data-ttu-id="908cf-127">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="908cf-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="908cf-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="908cf-128">-DefaultProfile</span></span>
<span data-ttu-id="908cf-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="908cf-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="908cf-130">-Maskingişlevi</span><span class="sxs-lookup"><span data-stu-id="908cf-130">-MaskingFunction</span></span>
<span data-ttu-id="908cf-131">Kuralın kullandığı maskeleme işlevini belirtir.</span><span class="sxs-lookup"><span data-stu-id="908cf-131">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="908cf-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="908cf-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="908cf-133">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="908cf-133">Default</span></span>
- <span data-ttu-id="908cf-134">Not</span><span class="sxs-lookup"><span data-stu-id="908cf-134">NoMasking</span></span>
- <span data-ttu-id="908cf-135">Metinleri</span><span class="sxs-lookup"><span data-stu-id="908cf-135">Text</span></span>
- <span data-ttu-id="908cf-136">Numarasıyla</span><span class="sxs-lookup"><span data-stu-id="908cf-136">Number</span></span>
- <span data-ttu-id="908cf-137">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="908cf-137">SocialSecurityNumber</span></span>
- <span data-ttu-id="908cf-138">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="908cf-138">CreditCardNumber</span></span>
- <span data-ttu-id="908cf-139">E-posta varsayılan değer varsayılandır.</span><span class="sxs-lookup"><span data-stu-id="908cf-139">Email The default value is Default.</span></span>

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

### <span data-ttu-id="908cf-140">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="908cf-140">-NumberFrom</span></span>
<span data-ttu-id="908cf-141">Rastgele bir değer seçilen aralığın alt sınır numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="908cf-141">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="908cf-142">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir sayı değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="908cf-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="908cf-143">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="908cf-143">The default value is 0.</span></span>

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

### <span data-ttu-id="908cf-144">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="908cf-144">-NumberTo</span></span>
<span data-ttu-id="908cf-145">Rastgele bir değer seçilen aralığın üst sınır numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="908cf-145">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="908cf-146">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir sayı değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="908cf-146">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="908cf-147">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="908cf-147">The default value is 0.</span></span>

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

### <span data-ttu-id="908cf-148">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="908cf-148">-PassThru</span></span>
<span data-ttu-id="908cf-149">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="908cf-149">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="908cf-150">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="908cf-150">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="908cf-151">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="908cf-151">-PrefixSize</span></span>
<span data-ttu-id="908cf-152">Metnin başındaki metnin başındaki karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="908cf-152">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="908cf-153">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="908cf-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="908cf-154">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="908cf-154">The default value is 0.</span></span>

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

### <span data-ttu-id="908cf-155">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="908cf-155">-ReplacementString</span></span>
<span data-ttu-id="908cf-156">Metin düzeyinde, maskelenmeyen karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="908cf-156">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="908cf-157">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="908cf-157">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="908cf-158">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="908cf-158">The default value is 0.</span></span>

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

### <span data-ttu-id="908cf-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="908cf-159">-ResourceGroupName</span></span>
<span data-ttu-id="908cf-160">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="908cf-160">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="908cf-161">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="908cf-161">-SchemaName</span></span>
<span data-ttu-id="908cf-162">Şemanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="908cf-162">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="908cf-163">-ServerName</span><span class="sxs-lookup"><span data-stu-id="908cf-163">-ServerName</span></span>
<span data-ttu-id="908cf-164">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="908cf-164">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="908cf-165">-Soneboyut</span><span class="sxs-lookup"><span data-stu-id="908cf-165">-SuffixSize</span></span>
<span data-ttu-id="908cf-166">Metin düzeyinde, maskelenmeyen karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="908cf-166">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="908cf-167">Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="908cf-167">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="908cf-168">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="908cf-168">The default value is 0.</span></span>

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

### <span data-ttu-id="908cf-169">-TableName</span><span class="sxs-lookup"><span data-stu-id="908cf-169">-TableName</span></span>
<span data-ttu-id="908cf-170">Maskelenmiş sütununu içeren veritabanı tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="908cf-170">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="908cf-171">-Onay</span><span class="sxs-lookup"><span data-stu-id="908cf-171">-Confirm</span></span>
<span data-ttu-id="908cf-172">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="908cf-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="908cf-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="908cf-173">-WhatIf</span></span>
<span data-ttu-id="908cf-174">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="908cf-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="908cf-175">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="908cf-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="908cf-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="908cf-176">CommonParameters</span></span>
<span data-ttu-id="908cf-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="908cf-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="908cf-178">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="908cf-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="908cf-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="908cf-179">INPUTS</span></span>

### <span data-ttu-id="908cf-180">System. String</span><span class="sxs-lookup"><span data-stu-id="908cf-180">System.String</span></span>

### <span data-ttu-id="908cf-181">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="908cf-181">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="908cf-182">System. Nullable ' 1 [[System. Double, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="908cf-182">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="908cf-183">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="908cf-183">OUTPUTS</span></span>

### <span data-ttu-id="908cf-184">Microsoft. Azure. Commands. Sql. Datamaskeleme. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="908cf-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="908cf-185">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="908cf-185">NOTES</span></span>

## <span data-ttu-id="908cf-186">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="908cf-186">RELATED LINKS</span></span>

[<span data-ttu-id="908cf-187">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="908cf-187">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="908cf-188">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="908cf-188">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="908cf-189">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="908cf-189">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="908cf-190">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="908cf-190">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


