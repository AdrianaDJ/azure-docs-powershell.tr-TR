---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 347f590ecd6e2825264e6bb0b980dd94450b0f06
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939391"
---
# <span data-ttu-id="0d6df-101">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="0d6df-101">Set-AzureRmDnsZone</span></span>

## <span data-ttu-id="0d6df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d6df-102">SYNOPSIS</span></span>
<span data-ttu-id="0d6df-103">DNS bölgesinin özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0d6df-103">Updates the properties of a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d6df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d6df-104">SYNTAX</span></span>

### <span data-ttu-id="0d6df-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="0d6df-105">Fields</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d6df-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="0d6df-106">Object</span></span>
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d6df-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d6df-107">DESCRIPTION</span></span>
<span data-ttu-id="0d6df-108">**Set-AzureRmDnsZone** cmdlet 'ı, Azure DNS HIZMETINDE belirtilen DNS bölgesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0d6df-108">The **Set-AzureRmDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="0d6df-109">Bu cmdlet, bölgedeki kayıt kümelerini güncelleştirmez.</span><span class="sxs-lookup"><span data-stu-id="0d6df-109">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="0d6df-110">Bir **dnsZone** nesnesini parametre olarak veya Pipeline işlecini kullanarak geçirebilir ya da bir alternatif olarak, *BölgeAdı* ve *resourcegroupname* parametrelerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d6df-110">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="0d6df-111">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için *Confirm* parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d6df-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="0d6df-112">DNS bölgesini nesne olarak geçirirken (bölge nesnesini veya ardışık düzen aracılığıyla), yerel DnsZone nesnesinin alındığı bu yana Azure DNS 'de değiştirilmişse bu, güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="0d6df-112">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="0d6df-113">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="0d6df-113">This provides protection for concurrent changes.</span></span> <span data-ttu-id="0d6df-114">Bu *davranışı, eş* zamanlı değişikliklerden bağımsız olarak, bölgeyi güncelleyen parametreyle kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d6df-114">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="0d6df-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d6df-115">EXAMPLES</span></span>

### <span data-ttu-id="0d6df-116">Örnek 1: DNS bölgesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0d6df-116">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

<span data-ttu-id="0d6df-117">İlk komut, myzone.com adlı bölgeyi belirtilen kaynak grubundan alır ve $Zone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0d6df-117">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="0d6df-118">İkinci komut $Zone etiketlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0d6df-118">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="0d6df-119">Son komutu değişikliği kaydeder.</span><span class="sxs-lookup"><span data-stu-id="0d6df-119">The final command commits the change.</span></span>

### <span data-ttu-id="0d6df-120">Örnek 2: bir bölgeye ait etiketleri güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0d6df-120">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="0d6df-121">Bu komut, önce bölgeyi açıkça almadan myzone.com adındaki bölgenin etiketlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0d6df-121">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

## <span data-ttu-id="0d6df-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d6df-122">PARAMETERS</span></span>

### <span data-ttu-id="0d6df-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d6df-123">-Name</span></span>
<span data-ttu-id="0d6df-124">Güncelleştirilecek DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d6df-124">Specifies the name of the DNS zone to update.</span></span>

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

### <span data-ttu-id="0d6df-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="0d6df-125">-Overwrite</span></span>
<span data-ttu-id="0d6df-126">DNS bölgesini nesne olarak geçirirken (bölge nesnesini veya ardışık düzen aracılığıyla), yerel DnsZone nesnesinin alındığı bu yana Azure DNS 'de değiştirilmişse bu, güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="0d6df-126">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="0d6df-127">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="0d6df-127">This provides protection for concurrent changes.</span></span> <span data-ttu-id="0d6df-128">Bu *davranışı, eş* zamanlı değişikliklerden bağımsız olarak, bölgeyi güncelleyen parametreyle kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d6df-128">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="0d6df-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d6df-129">-ResourceGroupName</span></span>
<span data-ttu-id="0d6df-130">Güncelleştirilecek bölgeyi içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d6df-130">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="0d6df-131">Ayrıca, BölgeAdı parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="0d6df-131">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="0d6df-132">Alternatif olarak, bölgeyi *bölge* parametresi veya ardışık düzene sahip bir dnsZone nesnesi kullanarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d6df-132">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

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

### <span data-ttu-id="0d6df-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0d6df-133">-Tag</span></span>
<span data-ttu-id="0d6df-134">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="0d6df-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0d6df-135">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="0d6df-135">For example:</span></span>

<span data-ttu-id="0d6df-136">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="0d6df-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0d6df-137">-Bölge</span><span class="sxs-lookup"><span data-stu-id="0d6df-137">-Zone</span></span>
<span data-ttu-id="0d6df-138">Güncelleştirilecek DNS bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d6df-138">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="0d6df-139">Alternatif olarak, bölgeyi *BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d6df-139">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="0d6df-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="0d6df-140">-Confirm</span></span>
<span data-ttu-id="0d6df-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0d6df-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d6df-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d6df-142">-WhatIf</span></span>
<span data-ttu-id="0d6df-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d6df-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d6df-144">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d6df-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d6df-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0d6df-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d6df-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d6df-146">CommonParameters</span></span>
<span data-ttu-id="0d6df-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d6df-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d6df-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d6df-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d6df-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d6df-149">INPUTS</span></span>

### <span data-ttu-id="0d6df-150">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="0d6df-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="0d6df-151">Bir DnsZone nesnesini bu cmdlet 'e boru edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d6df-151">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="0d6df-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d6df-152">OUTPUTS</span></span>

### <span data-ttu-id="0d6df-153">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="0d6df-153">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="0d6df-154">Bu cmdlet, yeni ETag ile güncelleştirilmiş DNS bölgesini temsil eden bir DnsZone nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="0d6df-154">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="0d6df-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d6df-155">NOTES</span></span>
<span data-ttu-id="0d6df-156">*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="0d6df-156">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="0d6df-157">Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.</span><span class="sxs-lookup"><span data-stu-id="0d6df-157">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="0d6df-158">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="0d6df-158">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="0d6df-159">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="0d6df-159">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0d6df-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d6df-160">RELATED LINKS</span></span>

[<span data-ttu-id="0d6df-161">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="0d6df-161">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="0d6df-162">Yeni-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="0d6df-162">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="0d6df-163">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="0d6df-163">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)