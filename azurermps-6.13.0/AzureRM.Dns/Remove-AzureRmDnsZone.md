---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
ms.openlocfilehash: f5dd34c15745707df8bb0b91f7a4716e5c0bba6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591961"
---
# <span data-ttu-id="43970-101">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="43970-101">Remove-AzureRmDnsZone</span></span>

## <span data-ttu-id="43970-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43970-102">SYNOPSIS</span></span>
<span data-ttu-id="43970-103">Kaynak grubundan bir DNS bölgesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="43970-103">Removes a DNS zone from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43970-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43970-104">SYNTAX</span></span>

### <span data-ttu-id="43970-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="43970-105">Fields</span></span>
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43970-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="43970-106">Object</span></span>
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43970-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="43970-107">DESCRIPTION</span></span>
<span data-ttu-id="43970-108">**Remove-AzureRmDnsZone** cmdlet 'i, belirli bir kaynak grubundan etki alanı adı SISTEMI (DNS) bölgesini kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="43970-108">The **Remove-AzureRmDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="43970-109">Bölgede bulunan tüm kayıt kümeleri de silinir.</span><span class="sxs-lookup"><span data-stu-id="43970-109">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="43970-110">Name parametresini veya Pipeline işlecini kullanarak bir **dnsZone** nesnesini geçirebilir ya da bir alternatif olarak, *BölgeAdı* ve *resourcegroupname* parametrelerini belirtebilirsiniz *ZoneName* .</span><span class="sxs-lookup"><span data-stu-id="43970-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="43970-111">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için Confirm parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="43970-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="43970-112">Bir **dnsZone** nesnesi (ardışık düzen veya *bölge* parametresi aracılığıyla geçirilir) kullanarak bölgeyi belirtirken, yerel **dnsZone** nesnesinin alındığı bu yana Azure DNS 'de DEĞIŞTIRILDIYSE bölge silinmez (yalnızca DNS bölge kaynak sayısı değiştiğinde, bölgedeki kayıt kümelerindeki işlemler).</span><span class="sxs-lookup"><span data-stu-id="43970-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="43970-113">Bu, eşzamanlı bölge değişiklikleri için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="43970-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="43970-114">Bu, yinelenen değişikliklerden bağımsız olarak bölgeyi silen, *overwrite* parametresi kullanılarak bastırılabilir.</span><span class="sxs-lookup"><span data-stu-id="43970-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="43970-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43970-115">EXAMPLES</span></span>

### <span data-ttu-id="43970-116">Örnek 1: bölgeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="43970-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="43970-117">Bu komut, myzone.com adlı bölgeyi MyResourceGroup adlı kaynak grubundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="43970-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="43970-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43970-118">PARAMETERS</span></span>

### <span data-ttu-id="43970-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43970-119">-DefaultProfile</span></span>
<span data-ttu-id="43970-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="43970-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43970-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="43970-121">-Name</span></span>
<span data-ttu-id="43970-122">Bu cmdlet 'in kaldırıldığı DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43970-122">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="43970-123">*Resourcegroupname* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="43970-123">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="43970-124">Alternatif olarak, *bölge* PARAMETRESINI kullanarak DNS bölgesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="43970-124">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="43970-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="43970-125">-Overwrite</span></span>
<span data-ttu-id="43970-126">Bir **dnsZone** nesnesi (ardışık düzen veya *bölge* parametresi aracılığıyla geçirilir) kullanarak bölgeyi belirtirken, yerel **dnsZone** nesnesinin alındığı bu yana Azure DNS 'de DEĞIŞTIRILDIYSE bölge silinmez (yalnızca DNS bölge kaynak sayısı değiştiğinde, bölgedeki kayıt kümelerindeki işlemler).</span><span class="sxs-lookup"><span data-stu-id="43970-126">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="43970-127">Bu, eşzamanlı bölge değişiklikleri için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="43970-127">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="43970-128">Bu, yinelenen değişikliklerden bağımsız olarak bölgeyi silen, *overwrite* parametresi kullanılarak bastırılabilir.</span><span class="sxs-lookup"><span data-stu-id="43970-128">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="43970-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="43970-129">-PassThru</span></span>
<span data-ttu-id="43970-130">geçiş</span><span class="sxs-lookup"><span data-stu-id="43970-130">passthru</span></span>

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

### <span data-ttu-id="43970-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43970-131">-ResourceGroupName</span></span>
<span data-ttu-id="43970-132">Kaldırılacak bölgeyi içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43970-132">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="43970-133">Ayrıca, *BölgeAdı* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="43970-133">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="43970-134">Alternatif olarak, ardışık düzen veya *bölge* parametresi aracılığıyla geçen bir **dnsZone** nesnesi kullanarak DNS bölgesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="43970-134">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="43970-135">-Bölge</span><span class="sxs-lookup"><span data-stu-id="43970-135">-Zone</span></span>
<span data-ttu-id="43970-136">Silinecek DNS bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="43970-136">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="43970-137">Geçirilen **dnsZone** nesnesi ardışık düzen aracılığıyla da iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="43970-137">The **DnsZone** object passed can also be passed via the pipeline.</span></span>
<span data-ttu-id="43970-138">Alternatif olarak, *BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak silinecek DNS bölgesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="43970-138">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="43970-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="43970-139">-Confirm</span></span>
<span data-ttu-id="43970-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="43970-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43970-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43970-141">-WhatIf</span></span>
<span data-ttu-id="43970-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="43970-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43970-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="43970-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43970-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43970-144">CommonParameters</span></span>
<span data-ttu-id="43970-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43970-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43970-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43970-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43970-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43970-147">INPUTS</span></span>

### <span data-ttu-id="43970-148">System. String</span><span class="sxs-lookup"><span data-stu-id="43970-148">System.String</span></span>

### <span data-ttu-id="43970-149">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="43970-149">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="43970-150">Parametreler: bölge (ByValue)</span><span class="sxs-lookup"><span data-stu-id="43970-150">Parameters: Zone (ByValue)</span></span>

## <span data-ttu-id="43970-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43970-151">OUTPUTS</span></span>

### <span data-ttu-id="43970-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43970-152">System.Boolean</span></span>

## <span data-ttu-id="43970-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43970-153">NOTES</span></span>
<span data-ttu-id="43970-154">DNS bölgesini silmenin yüksek etkisi nedeniyle, varsayılan olarak bu cmdlet $ConfirmPreference Windows PowerShell değişkeninde hiçbiri dışında bir değer varsa onay ister.</span><span class="sxs-lookup"><span data-stu-id="43970-154">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>
<span data-ttu-id="43970-155">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="43970-155">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="43970-156">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="43970-156">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="43970-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43970-157">RELATED LINKS</span></span>

[<span data-ttu-id="43970-158">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="43970-158">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="43970-159">Yeni-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="43970-159">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="43970-160">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="43970-160">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
