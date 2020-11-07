---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d54dac2689fd751663ebf0046288c4d4ceeae928
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759767"
---
# <span data-ttu-id="f0bcf-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f0bcf-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="f0bcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="f0bcf-103">Kaynak grubundan özel bir DNS bölgesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="f0bcf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0bcf-104">SYNTAX</span></span>

### <span data-ttu-id="f0bcf-105">Alanlar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f0bcf-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0bcf-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="f0bcf-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0bcf-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="f0bcf-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0bcf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0bcf-108">DESCRIPTION</span></span>
<span data-ttu-id="f0bcf-109">**Remove-AzPrivateDnsZone** cmdlet 'i, belirli bir kaynak grubundan özel bir etki alanı adı SISTEMI (DNS) bölgesini kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="f0bcf-110">Bölgede bulunan tüm kayıt kümeleri de silinir.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="f0bcf-111">*Privatezone* parametresini veya Pipeline işlecini kullanarak bir **PrivateDnsZone** nesnesi geçirebilir ya da *Name* ve *resourcegroupname* parametrelerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="f0bcf-112">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için Confirm parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="f0bcf-113">Bir **PrivateDnsZone** nesnesi (ardışık düzen veya *bölge* parametresi aracılığıyla geçirilir) kullanarak bölgeyi belirtirken, yerel **PRIVATEDNSZONE** nesnesi alındıktan sonra Azure DNS 'de DEĞIŞTIRILMIŞ olan bölge silinmez (yalnızca DNS bölge kaynak sayısı değiştiğinde, bölgedeki kayıt kümelerindeki işlemler).</span><span class="sxs-lookup"><span data-stu-id="f0bcf-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="f0bcf-114">Bu, eşzamanlı bölge değişiklikleri için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="f0bcf-115">Bu, yinelenen değişikliklerden bağımsız olarak bölgeyi silen, *overwrite* parametresi kullanılarak bastırılabilir.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="f0bcf-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0bcf-116">EXAMPLES</span></span>

### <span data-ttu-id="f0bcf-117">Örnek 1: özel bölgeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="f0bcf-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="f0bcf-118">Bu komut, myzone.com adlı bölgeyi MyResourceGroup adlı kaynak grubundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="f0bcf-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0bcf-119">PARAMETERS</span></span>

### <span data-ttu-id="f0bcf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0bcf-120">-DefaultProfile</span></span>
<span data-ttu-id="f0bcf-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f0bcf-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0bcf-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f0bcf-122">-Name</span></span>
<span data-ttu-id="f0bcf-123">Bu cmdlet 'in kaldırıldığı özel DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="f0bcf-124">*Resourcegroupname* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="f0bcf-125">Alternatif olarak, *bölge* PARAMETRESINI kullanarak DNS bölgesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0bcf-126">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="f0bcf-126">-Overwrite</span></span>
<span data-ttu-id="f0bcf-127">Bir **PrivateDnsZone** nesnesi (ardışık düzen veya *bölge* parametresi aracılığıyla geçirilir) kullanarak bölgeyi belirtirken, yerel **PRIVATEDNSZONE** nesnesi alındıktan sonra Azure DNS 'de DEĞIŞTIRILMIŞ olan bölge silinmez (yalnızca DNS bölge kaynak sayısı değiştiğinde, bölgedeki kayıt kümelerindeki işlemler).</span><span class="sxs-lookup"><span data-stu-id="f0bcf-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="f0bcf-128">Bu, eşzamanlı bölge değişiklikleri için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="f0bcf-129">Bu, yinelenen değişikliklerden bağımsız olarak bölgeyi silen, *overwrite* parametresi kullanılarak bastırılabilir.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="f0bcf-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f0bcf-130">-PassThru</span></span>
<span data-ttu-id="f0bcf-131">İşlemin sonucunu geçirmek için kullanılır özel bölgesini daha aşağı doğru silme.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="f0bcf-132">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="f0bcf-132">-PrivateZone</span></span>
<span data-ttu-id="f0bcf-133">Silinecek özel bölge nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-133">The private zone object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0bcf-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0bcf-134">-ResourceGroupName</span></span>
<span data-ttu-id="f0bcf-135">Kaldırılacak bölgeyi içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="f0bcf-136">Ayrıca, *BölgeAdı* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="f0bcf-137">Alternatif olarak, **PrivateDnsZone** nesnesi kullanarak ardışık düzen veya *bölge* parametresi aracılığıyla DNS bölgesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0bcf-138">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f0bcf-138">-ResourceId</span></span>
<span data-ttu-id="f0bcf-139">Özel DNS bölge RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-139">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0bcf-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="f0bcf-140">-Confirm</span></span>
<span data-ttu-id="f0bcf-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0bcf-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0bcf-142">-WhatIf</span></span>
<span data-ttu-id="f0bcf-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0bcf-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0bcf-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0bcf-145">CommonParameters</span></span>
<span data-ttu-id="f0bcf-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0bcf-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0bcf-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0bcf-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0bcf-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0bcf-148">INPUTS</span></span>

### <span data-ttu-id="f0bcf-149">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f0bcf-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="f0bcf-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f0bcf-150">System.String</span></span>

## <span data-ttu-id="f0bcf-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0bcf-151">OUTPUTS</span></span>

### <span data-ttu-id="f0bcf-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f0bcf-152">System.Boolean</span></span>

## <span data-ttu-id="f0bcf-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0bcf-153">NOTES</span></span>

## <span data-ttu-id="f0bcf-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0bcf-154">RELATED LINKS</span></span>

[<span data-ttu-id="f0bcf-155">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f0bcf-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="f0bcf-156">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f0bcf-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="f0bcf-157">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f0bcf-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
