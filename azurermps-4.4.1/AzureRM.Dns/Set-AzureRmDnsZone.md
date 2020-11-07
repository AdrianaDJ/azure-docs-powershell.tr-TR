---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
ms.openlocfilehash: 9d4e0e376e611e1373d30ab6b3aeafb51f363c31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764062"
---
# <span data-ttu-id="e7b40-101">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e7b40-101">Set-AzureRmDnsZone</span></span>

## <span data-ttu-id="e7b40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7b40-102">SYNOPSIS</span></span>
<span data-ttu-id="e7b40-103">DNS bölgesinin özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e7b40-103">Updates the properties of a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7b40-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7b40-104">SYNTAX</span></span>

### <span data-ttu-id="e7b40-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="e7b40-105">Fields</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7b40-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="e7b40-106">Object</span></span>
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7b40-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7b40-107">DESCRIPTION</span></span>
<span data-ttu-id="e7b40-108">**Set-AzureRmDnsZone** cmdlet 'ı, Azure DNS HIZMETINDE belirtilen DNS bölgesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e7b40-108">The **Set-AzureRmDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="e7b40-109">Bu cmdlet, bölgedeki kayıt kümelerini güncelleştirmez.</span><span class="sxs-lookup"><span data-stu-id="e7b40-109">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="e7b40-110">Bir **dnsZone** nesnesini parametre olarak veya Pipeline işlecini kullanarak geçirebilir ya da bir alternatif olarak, *BölgeAdı* ve *resourcegroupname* parametrelerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7b40-110">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="e7b40-111">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için *Confirm* parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7b40-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="e7b40-112">DNS bölgesini nesne olarak geçirirken (bölge nesnesini veya ardışık düzen aracılığıyla), yerel DnsZone nesnesinin alındığı bu yana Azure DNS 'de değiştirilmişse bu, güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="e7b40-112">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="e7b40-113">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="e7b40-113">This provides protection for concurrent changes.</span></span> <span data-ttu-id="e7b40-114">Bu *davranışı, eş* zamanlı değişikliklerden bağımsız olarak, bölgeyi güncelleyen parametreyle kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7b40-114">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="e7b40-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7b40-115">EXAMPLES</span></span>

### <span data-ttu-id="e7b40-116">Örnek 1: DNS bölgesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e7b40-116">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

<span data-ttu-id="e7b40-117">İlk komut, myzone.com adlı bölgeyi belirtilen kaynak grubundan alır ve $Zone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e7b40-117">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="e7b40-118">İkinci komut $Zone etiketlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e7b40-118">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="e7b40-119">Son komutu değişikliği kaydeder.</span><span class="sxs-lookup"><span data-stu-id="e7b40-119">The final command commits the change.</span></span>

### <span data-ttu-id="e7b40-120">Örnek 2: bir bölgeye ait etiketleri güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e7b40-120">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="e7b40-121">Bu komut, önce bölgeyi açıkça almadan myzone.com adındaki bölgenin etiketlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e7b40-121">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

## <span data-ttu-id="e7b40-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7b40-122">PARAMETERS</span></span>

### <span data-ttu-id="e7b40-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7b40-123">-Name</span></span>
<span data-ttu-id="e7b40-124">Güncelleştirilecek DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7b40-124">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b40-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="e7b40-125">-Overwrite</span></span>
<span data-ttu-id="e7b40-126">DNS bölgesini nesne olarak geçirirken (bölge nesnesini veya ardışık düzen aracılığıyla), yerel DnsZone nesnesinin alındığı bu yana Azure DNS 'de değiştirilmişse bu, güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="e7b40-126">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="e7b40-127">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="e7b40-127">This provides protection for concurrent changes.</span></span> <span data-ttu-id="e7b40-128">Bu *davranışı, eş* zamanlı değişikliklerden bağımsız olarak, bölgeyi güncelleyen parametreyle kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7b40-128">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b40-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7b40-129">-ResourceGroupName</span></span>
<span data-ttu-id="e7b40-130">Güncelleştirilecek bölgeyi içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7b40-130">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="e7b40-131">Ayrıca, BölgeAdı parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e7b40-131">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="e7b40-132">Alternatif olarak, bölgeyi *bölge* parametresi veya ardışık düzene sahip bir dnsZone nesnesi kullanarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7b40-132">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b40-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e7b40-133">-Tag</span></span>
<span data-ttu-id="e7b40-134">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="e7b40-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e7b40-135">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="e7b40-135">For example:</span></span>

<span data-ttu-id="e7b40-136">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="e7b40-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b40-137">-Bölge</span><span class="sxs-lookup"><span data-stu-id="e7b40-137">-Zone</span></span>
<span data-ttu-id="e7b40-138">Güncelleştirilecek DNS bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7b40-138">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="e7b40-139">Alternatif olarak, bölgeyi *BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7b40-139">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b40-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="e7b40-140">-Confirm</span></span>
<span data-ttu-id="e7b40-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e7b40-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7b40-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7b40-142">-WhatIf</span></span>
<span data-ttu-id="e7b40-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7b40-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7b40-144">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7b40-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7b40-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e7b40-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7b40-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7b40-146">-DefaultProfile</span></span>
<span data-ttu-id="e7b40-147">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7b40-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7b40-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7b40-148">CommonParameters</span></span>
<span data-ttu-id="e7b40-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7b40-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7b40-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7b40-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7b40-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7b40-151">INPUTS</span></span>

### <span data-ttu-id="e7b40-152">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="e7b40-152">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="e7b40-153">Bir DnsZone nesnesini bu cmdlet 'e boru edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7b40-153">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="e7b40-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7b40-154">OUTPUTS</span></span>

### <span data-ttu-id="e7b40-155">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="e7b40-155">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="e7b40-156">Bu cmdlet, yeni ETag ile güncelleştirilmiş DNS bölgesini temsil eden bir DnsZone nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="e7b40-156">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="e7b40-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7b40-157">NOTES</span></span>
<span data-ttu-id="e7b40-158">*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="e7b40-158">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="e7b40-159">Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.</span><span class="sxs-lookup"><span data-stu-id="e7b40-159">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="e7b40-160">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="e7b40-160">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="e7b40-161">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="e7b40-161">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e7b40-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7b40-162">RELATED LINKS</span></span>

[<span data-ttu-id="e7b40-163">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e7b40-163">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="e7b40-164">Yeni-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e7b40-164">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="e7b40-165">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e7b40-165">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
