---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: ''
schema: 2.0.0
ms.openlocfilehash: c12c5532a85bacb5cd854f4f2ad87ad0d8b68178
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940154"
---
# <span data-ttu-id="3a285-101">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="3a285-101">Remove-AzureRmDnsZone</span></span>

## <span data-ttu-id="3a285-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a285-102">SYNOPSIS</span></span>
<span data-ttu-id="3a285-103">Kaynak grubundan bir DNS bölgesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a285-103">Removes a DNS zone from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a285-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a285-104">SYNTAX</span></span>

### <span data-ttu-id="3a285-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="3a285-105">Fields</span></span>
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a285-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="3a285-106">Object</span></span>
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a285-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a285-107">DESCRIPTION</span></span>
<span data-ttu-id="3a285-108">**Remove-AzureRmDnsZone** cmdlet 'i, belirli bir kaynak grubundan etki alanı adı SISTEMI (DNS) bölgesini kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="3a285-108">The **Remove-AzureRmDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="3a285-109">Bölgede bulunan tüm kayıt kümeleri de silinir.</span><span class="sxs-lookup"><span data-stu-id="3a285-109">All record sets contained in the zone are also deleted.</span></span>

<span data-ttu-id="3a285-110">Name parametresini veya Pipeline işlecini kullanarak bir **dnsZone** nesnesini geçirebilir ya da bir alternatif olarak, *BölgeAdı* ve *resourcegroupname* parametrelerini belirtebilirsiniz *ZoneName* .</span><span class="sxs-lookup"><span data-stu-id="3a285-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="3a285-111">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için Confirm parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3a285-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="3a285-112">Bir **dnsZone** nesnesi (ardışık düzen veya *bölge* parametresi aracılığıyla geçirilir) kullanarak bölgeyi belirtirken, yerel **dnsZone** nesnesinin alındığı bu yana Azure DNS 'de DEĞIŞTIRILDIYSE bölge silinmez (yalnızca DNS bölge kaynak sayısı değiştiğinde, bölgedeki kayıt kümelerindeki işlemler).</span><span class="sxs-lookup"><span data-stu-id="3a285-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="3a285-113">Bu, eşzamanlı bölge değişiklikleri için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="3a285-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="3a285-114">Bu, yinelenen değişikliklerden bağımsız olarak bölgeyi silen, *overwrite* parametresi kullanılarak bastırılabilir.</span><span class="sxs-lookup"><span data-stu-id="3a285-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="3a285-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a285-115">EXAMPLES</span></span>

### <span data-ttu-id="3a285-116">Örnek 1: bölgeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="3a285-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="3a285-117">Bu komut, myzone.com adlı bölgeyi MyResourceGroup adlı kaynak grubundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a285-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="3a285-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a285-118">PARAMETERS</span></span>

### <span data-ttu-id="3a285-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3a285-119">-Force</span></span>
<span data-ttu-id="3a285-120">Bu parametre bu cmdlet için onaylanmaz.</span><span class="sxs-lookup"><span data-stu-id="3a285-120">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="3a285-121">Gelecek sürümde kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="3a285-121">It will be removed in a future release.</span></span>

<span data-ttu-id="3a285-122">Bu cmdlet 'in onaylamanız gerekip gerekmediğini denetlemek için, *Confirm* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3a285-122">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="3a285-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a285-123">-Name</span></span>
<span data-ttu-id="3a285-124">Bu cmdlet 'in kaldırıldığı DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a285-124">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="3a285-125">*Resourcegroupname* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3a285-125">You must also specify the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="3a285-126">Alternatif olarak, *bölge* PARAMETRESINI kullanarak DNS bölgesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3a285-126">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="3a285-127">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="3a285-127">-Overwrite</span></span>
<span data-ttu-id="3a285-128">Bir **dnsZone** nesnesi (ardışık düzen veya *bölge* parametresi aracılığıyla geçirilir) kullanarak bölgeyi belirtirken, yerel **dnsZone** nesnesinin alındığı bu yana Azure DNS 'de DEĞIŞTIRILDIYSE bölge silinmez (yalnızca DNS bölge kaynak sayısı değiştiğinde, bölgedeki kayıt kümelerindeki işlemler).</span><span class="sxs-lookup"><span data-stu-id="3a285-128">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="3a285-129">Bu, eşzamanlı bölge değişiklikleri için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="3a285-129">This provides protection for concurrent zone changes.</span></span>

<span data-ttu-id="3a285-130">Bu, yinelenen değişikliklerden bağımsız olarak bölgeyi silen, *overwrite* parametresi kullanılarak bastırılabilir.</span><span class="sxs-lookup"><span data-stu-id="3a285-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="3a285-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3a285-131">-PassThru</span></span>
<span data-ttu-id="3a285-132">geçiş</span><span class="sxs-lookup"><span data-stu-id="3a285-132">passthru</span></span>

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

### <span data-ttu-id="3a285-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a285-133">-ResourceGroupName</span></span>
<span data-ttu-id="3a285-134">Kaldırılacak bölgeyi içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a285-134">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="3a285-135">Ayrıca, *BölgeAdı* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3a285-135">You must also specify the *ZoneName* parameter.</span></span>

<span data-ttu-id="3a285-136">Alternatif olarak, ardışık düzen veya *bölge* parametresi aracılığıyla geçen bir **dnsZone** nesnesi kullanarak DNS bölgesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3a285-136">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="3a285-137">-Bölge</span><span class="sxs-lookup"><span data-stu-id="3a285-137">-Zone</span></span>
<span data-ttu-id="3a285-138">Silinecek DNS bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a285-138">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="3a285-139">Geçirilen **dnsZone** nesnesi ardışık düzen aracılığıyla da iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="3a285-139">The **DnsZone** object passed can also be passed via the pipeline.</span></span>

<span data-ttu-id="3a285-140">Alternatif olarak, *BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak silinecek DNS bölgesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3a285-140">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a285-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="3a285-141">-Confirm</span></span>
<span data-ttu-id="3a285-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a285-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a285-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a285-143">-WhatIf</span></span>
<span data-ttu-id="3a285-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a285-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a285-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3a285-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a285-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a285-146">CommonParameters</span></span>
<span data-ttu-id="3a285-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a285-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a285-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a285-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a285-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a285-149">INPUTS</span></span>

### <span data-ttu-id="3a285-150">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="3a285-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="3a285-151">Bir **dnsZone** nesnesini bu cmdlet 'e boru edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3a285-151">You can pipe a **DnsZone** object to this cmdlet.</span></span>

## <span data-ttu-id="3a285-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a285-152">OUTPUTS</span></span>

### <span data-ttu-id="3a285-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3a285-153">None</span></span>
<span data-ttu-id="3a285-154">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="3a285-154">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="3a285-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a285-155">NOTES</span></span>
<span data-ttu-id="3a285-156">DNS bölgesini silmenin yüksek etkisi nedeniyle, varsayılan olarak bu cmdlet $ConfirmPreference Windows PowerShell değişkeninde hiçbiri dışında bir değer varsa onay ister.</span><span class="sxs-lookup"><span data-stu-id="3a285-156">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>

<span data-ttu-id="3a285-157">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a285-157">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="3a285-158">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="3a285-158">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="3a285-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a285-159">RELATED LINKS</span></span>

[<span data-ttu-id="3a285-160">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="3a285-160">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="3a285-161">Yeni-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="3a285-161">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="3a285-162">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="3a285-162">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
