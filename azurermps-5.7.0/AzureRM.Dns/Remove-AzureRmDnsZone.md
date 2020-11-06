---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
ms.openlocfilehash: ac3f65ed82f9b04eb49e26a8cb03a3dcd8c9bc34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593500"
---
# <span data-ttu-id="4be6c-101">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="4be6c-101">Remove-AzureRmDnsZone</span></span>

## <span data-ttu-id="4be6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4be6c-102">SYNOPSIS</span></span>
<span data-ttu-id="4be6c-103">Kaynak grubundan bir DNS bölgesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4be6c-103">Removes a DNS zone from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4be6c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4be6c-104">SYNTAX</span></span>

### <span data-ttu-id="4be6c-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="4be6c-105">Fields</span></span>
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4be6c-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="4be6c-106">Object</span></span>
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4be6c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4be6c-107">DESCRIPTION</span></span>
<span data-ttu-id="4be6c-108">**Remove-AzureRmDnsZone** cmdlet 'i, belirli bir kaynak grubundan etki alanı adı SISTEMI (DNS) bölgesini kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="4be6c-108">The **Remove-AzureRmDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="4be6c-109">Bölgede bulunan tüm kayıt kümeleri de silinir.</span><span class="sxs-lookup"><span data-stu-id="4be6c-109">All record sets contained in the zone are also deleted.</span></span>

<span data-ttu-id="4be6c-110">Name parametresini veya Pipeline işlecini kullanarak bir **dnsZone** nesnesini geçirebilir ya da bir alternatif olarak, *BölgeAdı* ve *resourcegroupname* parametrelerini belirtebilirsiniz *ZoneName* .</span><span class="sxs-lookup"><span data-stu-id="4be6c-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="4be6c-111">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için Confirm parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4be6c-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="4be6c-112">Bir **dnsZone** nesnesi (ardışık düzen veya *bölge* parametresi aracılığıyla geçirilir) kullanarak bölgeyi belirtirken, yerel **dnsZone** nesnesinin alındığı bu yana Azure DNS 'de DEĞIŞTIRILDIYSE bölge silinmez (yalnızca DNS bölge kaynak sayısı değiştiğinde, bölgedeki kayıt kümelerindeki işlemler).</span><span class="sxs-lookup"><span data-stu-id="4be6c-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="4be6c-113">Bu, eşzamanlı bölge değişiklikleri için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="4be6c-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="4be6c-114">Bu, yinelenen değişikliklerden bağımsız olarak bölgeyi silen, *overwrite* parametresi kullanılarak bastırılabilir.</span><span class="sxs-lookup"><span data-stu-id="4be6c-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="4be6c-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4be6c-115">EXAMPLES</span></span>

### <span data-ttu-id="4be6c-116">Örnek 1: bölgeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="4be6c-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="4be6c-117">Bu komut, myzone.com adlı bölgeyi MyResourceGroup adlı kaynak grubundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4be6c-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="4be6c-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4be6c-118">PARAMETERS</span></span>

### <span data-ttu-id="4be6c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4be6c-119">-DefaultProfile</span></span>
<span data-ttu-id="4be6c-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4be6c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4be6c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4be6c-121">-Force</span></span>
<span data-ttu-id="4be6c-122">Bu parametre bu cmdlet için onaylanmaz.</span><span class="sxs-lookup"><span data-stu-id="4be6c-122">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="4be6c-123">Gelecek sürümde kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="4be6c-123">It will be removed in a future release.</span></span>

<span data-ttu-id="4be6c-124">Bu cmdlet 'in onaylamanız gerekip gerekmediğini denetlemek için, *Confirm* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4be6c-124">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="4be6c-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="4be6c-125">-Name</span></span>
<span data-ttu-id="4be6c-126">Bu cmdlet 'in kaldırıldığı DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4be6c-126">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="4be6c-127">*Resourcegroupname* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4be6c-127">You must also specify the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="4be6c-128">Alternatif olarak, *bölge* PARAMETRESINI kullanarak DNS bölgesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4be6c-128">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="4be6c-129">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="4be6c-129">-Overwrite</span></span>
<span data-ttu-id="4be6c-130">Bir **dnsZone** nesnesi (ardışık düzen veya *bölge* parametresi aracılığıyla geçirilir) kullanarak bölgeyi belirtirken, yerel **dnsZone** nesnesinin alındığı bu yana Azure DNS 'de DEĞIŞTIRILDIYSE bölge silinmez (yalnızca DNS bölge kaynak sayısı değiştiğinde, bölgedeki kayıt kümelerindeki işlemler).</span><span class="sxs-lookup"><span data-stu-id="4be6c-130">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="4be6c-131">Bu, eşzamanlı bölge değişiklikleri için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="4be6c-131">This provides protection for concurrent zone changes.</span></span>

<span data-ttu-id="4be6c-132">Bu, yinelenen değişikliklerden bağımsız olarak bölgeyi silen, *overwrite* parametresi kullanılarak bastırılabilir.</span><span class="sxs-lookup"><span data-stu-id="4be6c-132">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="4be6c-133">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4be6c-133">-PassThru</span></span>
<span data-ttu-id="4be6c-134">geçiş</span><span class="sxs-lookup"><span data-stu-id="4be6c-134">passthru</span></span>

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

### <span data-ttu-id="4be6c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4be6c-135">-ResourceGroupName</span></span>
<span data-ttu-id="4be6c-136">Kaldırılacak bölgeyi içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4be6c-136">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="4be6c-137">Ayrıca, *BölgeAdı* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4be6c-137">You must also specify the *ZoneName* parameter.</span></span>

<span data-ttu-id="4be6c-138">Alternatif olarak, ardışık düzen veya *bölge* parametresi aracılığıyla geçen bir **dnsZone** nesnesi kullanarak DNS bölgesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4be6c-138">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="4be6c-139">-Bölge</span><span class="sxs-lookup"><span data-stu-id="4be6c-139">-Zone</span></span>
<span data-ttu-id="4be6c-140">Silinecek DNS bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4be6c-140">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="4be6c-141">Geçirilen **dnsZone** nesnesi ardışık düzen aracılığıyla da iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="4be6c-141">The **DnsZone** object passed can also be passed via the pipeline.</span></span>

<span data-ttu-id="4be6c-142">Alternatif olarak, *BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak silinecek DNS bölgesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4be6c-142">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="4be6c-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="4be6c-143">-Confirm</span></span>
<span data-ttu-id="4be6c-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4be6c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4be6c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4be6c-145">-WhatIf</span></span>
<span data-ttu-id="4be6c-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4be6c-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4be6c-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4be6c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4be6c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be6c-148">CommonParameters</span></span>
<span data-ttu-id="4be6c-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4be6c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be6c-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4be6c-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be6c-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4be6c-151">INPUTS</span></span>

### <span data-ttu-id="4be6c-152">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="4be6c-152">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="4be6c-153">Bir **dnsZone** nesnesini bu cmdlet 'e boru edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4be6c-153">You can pipe a **DnsZone** object to this cmdlet.</span></span>

## <span data-ttu-id="4be6c-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4be6c-154">OUTPUTS</span></span>

### <span data-ttu-id="4be6c-155">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4be6c-155">None</span></span>
<span data-ttu-id="4be6c-156">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="4be6c-156">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="4be6c-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4be6c-157">NOTES</span></span>
<span data-ttu-id="4be6c-158">DNS bölgesini silmenin yüksek etkisi nedeniyle, varsayılan olarak bu cmdlet $ConfirmPreference Windows PowerShell değişkeninde hiçbiri dışında bir değer varsa onay ister.</span><span class="sxs-lookup"><span data-stu-id="4be6c-158">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>

<span data-ttu-id="4be6c-159">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="4be6c-159">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="4be6c-160">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="4be6c-160">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="4be6c-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4be6c-161">RELATED LINKS</span></span>

[<span data-ttu-id="4be6c-162">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="4be6c-162">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="4be6c-163">Yeni-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="4be6c-163">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="4be6c-164">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="4be6c-164">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
