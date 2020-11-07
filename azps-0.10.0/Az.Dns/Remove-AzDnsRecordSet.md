---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: 10cd4936ad406be85f840b25c175d7900d66d679
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936725"
---
# <span data-ttu-id="18818-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="18818-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="18818-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18818-102">SYNOPSIS</span></span>
<span data-ttu-id="18818-103">Kayıt kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="18818-103">Deletes a record set.</span></span>

## <span data-ttu-id="18818-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18818-104">SYNTAX</span></span>

### <span data-ttu-id="18818-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="18818-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18818-106">Karıştır</span><span class="sxs-lookup"><span data-stu-id="18818-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-Force] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18818-107">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="18818-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18818-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="18818-108">DESCRIPTION</span></span>
<span data-ttu-id="18818-109">**Remove-AzDnsRecordSet** cmdlet 'i belirtilen bölgeden belirtilen kayıt kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="18818-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="18818-110">Bölge Apex otomatik olarak oluşturulan SOA veya ad sunucusu (NS) kayıtlarını silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="18818-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>

<span data-ttu-id="18818-111">Bir **Recordset** nesnesini, ardışık düzen işlecini veya parametre olarak bu cmdlet 'e geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18818-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="18818-112">Ad ve kayıt **kümesi** **nesnesi kullanmadan** bir kayıt kümesi tanımlamak için, bu cmdlet 'e, ardışık düzen işlecini veya parametre olarak kullanarak bölgeyi Bu cmdlet 'e geçirmelisiniz ya da *BölgeAdı* ve *resourcegroupname* parametrelerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18818-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="18818-113">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için Confirm parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18818-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="18818-114">Kayıt **kümesini kayıt kümesi nesnesi kullanarak** belirtirken, yerel **kayıt** kümesi NESNESI alındıktan sonra Azure DNS 'de değiştirilmişse kayıt kümesi silinmez.</span><span class="sxs-lookup"><span data-stu-id="18818-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="18818-115">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="18818-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="18818-116">Bunu, yinelenen değişikliklerden bağımsız olarak kayıt kümesini silen *overwrite* parametresini kullanarak kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18818-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="18818-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18818-117">EXAMPLES</span></span>

### <span data-ttu-id="18818-118">Örnek 1: kayıt kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="18818-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="18818-119">İlk komut belirtilen kayıt kümesini alır ve $RecordSet değişkeninde depolar. İkinci komut $RecordSet 'da kayıt kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="18818-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="18818-120">Örnek 2: kayıt kümesini kaldırma ve tüm onayı gösterme</span><span class="sxs-lookup"><span data-stu-id="18818-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="18818-121">İlk komut belirtilen kayıt kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="18818-121">The first command gets the specified record set.</span></span>

<span data-ttu-id="18818-122">İkinci komut, bu arada değişmiş olsa bile kayıt kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="18818-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="18818-123">Onay istemlerinin bastırılması</span><span class="sxs-lookup"><span data-stu-id="18818-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="18818-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18818-124">PARAMETERS</span></span>

### <span data-ttu-id="18818-125">-Force</span><span class="sxs-lookup"><span data-stu-id="18818-125">-Force</span></span>
<span data-ttu-id="18818-126">Bu parametre bu cmdlet için onaylanmaz.</span><span class="sxs-lookup"><span data-stu-id="18818-126">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="18818-127">Gelecek sürümde kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="18818-127">It will be removed in a future release.</span></span>

<span data-ttu-id="18818-128">Bu cmdlet 'in onaylamanız gerekip gerekmediğini denetlemek için, *Confirm* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="18818-128">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="18818-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="18818-129">-Name</span></span>
<span data-ttu-id="18818-130">Kaldırılacak **kayıt kümesinin** adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18818-130">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="18818-131">Ada göre kayıt kümesi belirtildiğinde, DNS bölgesi, *bölge* parametresi veya *BölgeAdı* ve *resourcegroupname* parametreleri kullanılarak belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="18818-131">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="18818-132">Alternatif olarak, kayıt kümesi, *Recordset* parametresi kullanılarak geçirilen bir **Recordset** nesnesi kullanılarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="18818-132">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields, Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18818-133">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="18818-133">-Overwrite</span></span>
<span data-ttu-id="18818-134">Kayıt **kümesini kayıt kümesi nesnesi kullanarak** belirtirken, yerel **kayıt** kümesi NESNESI alındıktan sonra Azure DNS 'de değiştirilmişse kayıt kümesi silinmez.</span><span class="sxs-lookup"><span data-stu-id="18818-134">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="18818-135">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="18818-135">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="18818-136">Bu, yinelenen değişikliklerden bağımsız olarak kayıt kümesini silen, *overwrite* parametresi kullanılarak bastırılabilir.</span><span class="sxs-lookup"><span data-stu-id="18818-136">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18818-137">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="18818-137">-PassThru</span></span>
<span data-ttu-id="18818-138">geçiş</span><span class="sxs-lookup"><span data-stu-id="18818-138">passthru</span></span>

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

### <span data-ttu-id="18818-139">-Kayıt kümesi</span><span class="sxs-lookup"><span data-stu-id="18818-139">-RecordSet</span></span>
<span data-ttu-id="18818-140">Kaldırılacak **kayıt kümesi** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18818-140">Specifies the **RecordSet** object to remove.</span></span>

<span data-ttu-id="18818-141">Alternatif olarak, kayıt kümesi *ad* ve *bölge* parametreleri kullanılarak veya *Name, BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak *ZoneName* belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="18818-141">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18818-142">-RecordType</span><span class="sxs-lookup"><span data-stu-id="18818-142">-RecordType</span></span>
<span data-ttu-id="18818-143">DNS kaydı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="18818-143">Specifies the type of DNS record.</span></span>

<span data-ttu-id="18818-144">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="18818-144">Valid values are:</span></span>

- <span data-ttu-id="18818-145">Bir</span><span class="sxs-lookup"><span data-stu-id="18818-145">A</span></span>
- <span data-ttu-id="18818-146">AAAA</span><span class="sxs-lookup"><span data-stu-id="18818-146">AAAA</span></span>
- <span data-ttu-id="18818-147">KAYDıNı</span><span class="sxs-lookup"><span data-stu-id="18818-147">CNAME</span></span>
- <span data-ttu-id="18818-148">DOSYASıNA</span><span class="sxs-lookup"><span data-stu-id="18818-148">MX</span></span>
- <span data-ttu-id="18818-149">Seç</span><span class="sxs-lookup"><span data-stu-id="18818-149">NS</span></span>
- <span data-ttu-id="18818-150">PTR</span><span class="sxs-lookup"><span data-stu-id="18818-150">PTR</span></span>
- <span data-ttu-id="18818-151">SRV</span><span class="sxs-lookup"><span data-stu-id="18818-151">SRV</span></span>
- <span data-ttu-id="18818-152">,</span><span class="sxs-lookup"><span data-stu-id="18818-152">TXT</span></span>

<span data-ttu-id="18818-153">SOA kayıtları bölge silindiğinde otomatik olarak silinir.</span><span class="sxs-lookup"><span data-stu-id="18818-153">SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="18818-154">SOA kayıtlarını el ile silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="18818-154">You cannot manually delete SOA records.</span></span>

```yaml
Type: RecordType
Parameter Sets: Fields, Mixed
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18818-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18818-155">-ResourceGroupName</span></span>
<span data-ttu-id="18818-156">Silinecek **kayıt kümesini** içeren DNS bölgesini içeren kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="18818-156">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="18818-157">Bu parametre yalnızca, kayıt kümesi ve DNS bölgesi ad ve *BölgeAdı* kullanılarak belirtildiğinde uygulanabilir *Name* .</span><span class="sxs-lookup"><span data-stu-id="18818-157">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>

<span data-ttu-id="18818-158">Alternatif olarak, kayıt *kümesini kayıt kümesi parametresini veya* *ad* ve *bölge* parametrelerini kullanarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18818-158">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18818-159">-Bölge</span><span class="sxs-lookup"><span data-stu-id="18818-159">-Zone</span></span>
<span data-ttu-id="18818-160">Silinecek **kayıt kümesini** içeren DNS bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18818-160">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="18818-161">Bu parametre yalnızca *Name* parametresi kullanılarak kayıt kümesi belirtildiğinde uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="18818-161">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>

<span data-ttu-id="18818-162">Alternatif olarak, kayıt *kümesini kayıt kümesi parametresini veya* *Name, BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak *ZoneName* belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18818-162">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18818-163">-BölgeAdı</span><span class="sxs-lookup"><span data-stu-id="18818-163">-ZoneName</span></span>
<span data-ttu-id="18818-164">Silinecek **kayıt kümesini** içeren bölgenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18818-164">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="18818-165">*Name* ve *resourcegroupname* parametrelerini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="18818-165">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="18818-166">Alternatif olarak, kayıt kümesi, kayıt *kümesi* parametresi veya *ad* ve *bölge* parametreleriyle belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="18818-166">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18818-167">-Onay</span><span class="sxs-lookup"><span data-stu-id="18818-167">-Confirm</span></span>
<span data-ttu-id="18818-168">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="18818-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18818-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18818-169">-WhatIf</span></span>
<span data-ttu-id="18818-170">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="18818-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18818-171">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="18818-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18818-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18818-172">CommonParameters</span></span>
<span data-ttu-id="18818-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18818-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18818-174">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18818-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18818-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18818-175">INPUTS</span></span>

### <span data-ttu-id="18818-176">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="18818-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="18818-177">Bir **Recordset** nesnesini bu cmdlet 'e boru yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18818-177">You can pipe a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="18818-178">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18818-178">OUTPUTS</span></span>

### <span data-ttu-id="18818-179">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="18818-179">None</span></span>
<span data-ttu-id="18818-180">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="18818-180">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="18818-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18818-181">NOTES</span></span>
<span data-ttu-id="18818-182">*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="18818-182">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="18818-183">Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.</span><span class="sxs-lookup"><span data-stu-id="18818-183">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="18818-184">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="18818-184">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="18818-185">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="18818-185">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="18818-186">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18818-186">RELATED LINKS</span></span>

[<span data-ttu-id="18818-187">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="18818-187">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="18818-188">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="18818-188">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="18818-189">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="18818-189">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
