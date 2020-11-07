---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 9b6d84f9007a872db0e41efa78d8e16d7269eb02
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935911"
---
# <span data-ttu-id="6141b-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6141b-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="6141b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6141b-102">SYNOPSIS</span></span>
<span data-ttu-id="6141b-103">DNS bölgesinin özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6141b-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="6141b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6141b-104">SYNTAX</span></span>

### <span data-ttu-id="6141b-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="6141b-105">Fields</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6141b-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="6141b-106">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6141b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6141b-107">DESCRIPTION</span></span>
<span data-ttu-id="6141b-108">**Set-AzDnsZone** cmdlet 'ı, Azure DNS HIZMETINDE belirtilen DNS bölgesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6141b-108">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="6141b-109">Bu cmdlet, bölgedeki kayıt kümelerini güncelleştirmez.</span><span class="sxs-lookup"><span data-stu-id="6141b-109">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="6141b-110">Bir **dnsZone** nesnesini parametre olarak veya Pipeline işlecini kullanarak geçirebilir ya da bir alternatif olarak, *BölgeAdı* ve *resourcegroupname* parametrelerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6141b-110">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="6141b-111">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için *Confirm* parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6141b-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="6141b-112">DNS bölgesini nesne olarak geçirirken (bölge nesnesini veya ardışık düzen aracılığıyla), yerel DnsZone nesnesinin alındığı bu yana Azure DNS 'de değiştirilmişse bu, güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="6141b-112">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="6141b-113">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="6141b-113">This provides protection for concurrent changes.</span></span> <span data-ttu-id="6141b-114">Bu *davranışı, eş* zamanlı değişikliklerden bağımsız olarak, bölgeyi güncelleyen parametreyle kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6141b-114">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="6141b-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6141b-115">EXAMPLES</span></span>

### <span data-ttu-id="6141b-116">Örnek 1: DNS bölgesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="6141b-116">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="6141b-117">İlk komut, myzone.com adlı bölgeyi belirtilen kaynak grubundan alır ve $Zone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6141b-117">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="6141b-118">İkinci komut $Zone etiketlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6141b-118">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="6141b-119">Son komutu değişikliği kaydeder.</span><span class="sxs-lookup"><span data-stu-id="6141b-119">The final command commits the change.</span></span>

### <span data-ttu-id="6141b-120">Örnek 2: bir bölgeye ait etiketleri güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="6141b-120">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="6141b-121">Bu komut, önce bölgeyi açıkça almadan myzone.com adındaki bölgenin etiketlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6141b-121">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

## <span data-ttu-id="6141b-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6141b-122">PARAMETERS</span></span>

### <span data-ttu-id="6141b-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="6141b-123">-Name</span></span>
<span data-ttu-id="6141b-124">Güncelleştirilecek DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6141b-124">Specifies the name of the DNS zone to update.</span></span>

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

### <span data-ttu-id="6141b-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="6141b-125">-Overwrite</span></span>
<span data-ttu-id="6141b-126">DNS bölgesini nesne olarak geçirirken (bölge nesnesini veya ardışık düzen aracılığıyla), yerel DnsZone nesnesinin alındığı bu yana Azure DNS 'de değiştirilmişse bu, güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="6141b-126">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="6141b-127">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="6141b-127">This provides protection for concurrent changes.</span></span> <span data-ttu-id="6141b-128">Bu *davranışı, eş* zamanlı değişikliklerden bağımsız olarak, bölgeyi güncelleyen parametreyle kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6141b-128">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="6141b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6141b-129">-ResourceGroupName</span></span>
<span data-ttu-id="6141b-130">Güncelleştirilecek bölgeyi içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6141b-130">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="6141b-131">Ayrıca, BölgeAdı parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6141b-131">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="6141b-132">Alternatif olarak, bölgeyi *bölge* parametresi veya ardışık düzene sahip bir dnsZone nesnesi kullanarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6141b-132">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

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

### <span data-ttu-id="6141b-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6141b-133">-Tag</span></span>
<span data-ttu-id="6141b-134">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="6141b-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6141b-135">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="6141b-135">For example:</span></span>

<span data-ttu-id="6141b-136">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="6141b-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6141b-137">-Bölge</span><span class="sxs-lookup"><span data-stu-id="6141b-137">-Zone</span></span>
<span data-ttu-id="6141b-138">Güncelleştirilecek DNS bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6141b-138">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="6141b-139">Alternatif olarak, bölgeyi *BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6141b-139">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="6141b-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="6141b-140">-Confirm</span></span>
<span data-ttu-id="6141b-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6141b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6141b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6141b-142">-WhatIf</span></span>
<span data-ttu-id="6141b-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6141b-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6141b-144">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6141b-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6141b-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6141b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6141b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6141b-146">CommonParameters</span></span>
<span data-ttu-id="6141b-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6141b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6141b-148">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6141b-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6141b-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6141b-149">INPUTS</span></span>

### <span data-ttu-id="6141b-150">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="6141b-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="6141b-151">Bir DnsZone nesnesini bu cmdlet 'e boru edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6141b-151">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="6141b-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6141b-152">OUTPUTS</span></span>

### <span data-ttu-id="6141b-153">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="6141b-153">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="6141b-154">Bu cmdlet, yeni ETag ile güncelleştirilmiş DNS bölgesini temsil eden bir DnsZone nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="6141b-154">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="6141b-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6141b-155">NOTES</span></span>
<span data-ttu-id="6141b-156">*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="6141b-156">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="6141b-157">Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.</span><span class="sxs-lookup"><span data-stu-id="6141b-157">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="6141b-158">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="6141b-158">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="6141b-159">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="6141b-159">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6141b-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6141b-160">RELATED LINKS</span></span>

[<span data-ttu-id="6141b-161">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6141b-161">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="6141b-162">Yeni-Azdnzone</span><span class="sxs-lookup"><span data-stu-id="6141b-162">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="6141b-163">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6141b-163">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)