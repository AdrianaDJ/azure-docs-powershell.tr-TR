---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 63fbe26fa0a9ac7ca5eb985a3806886adeb2a2f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096490"
---
# <span data-ttu-id="2dbee-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="2dbee-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="2dbee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dbee-102">SYNOPSIS</span></span>
<span data-ttu-id="2dbee-103">Kaynak grubundan sanal ağ bağlantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2dbee-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="2dbee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2dbee-104">SYNTAX</span></span>

### <span data-ttu-id="2dbee-105">Alanlar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2dbee-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dbee-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="2dbee-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dbee-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="2dbee-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dbee-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2dbee-108">DESCRIPTION</span></span>
<span data-ttu-id="2dbee-109">**Remove-AzPrivateDnsVirtualNetworkLink** cmdlet 'i, belirli bir kaynak grubundan özel bir etki alanı adı SISTEMI (DNS) bağlantısını kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="2dbee-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="2dbee-110">*Link* parametresini kullanarak veya Pipeline Işlecini kullanarak **Psprivatednsvirtualnetworklink** nesnesini geçirebilir ya da *ad BölgeAdı* *ZoneName* ve *resourcegroupname* parametrelerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2dbee-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="2dbee-111">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için Confirm parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2dbee-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="2dbee-112">Bir **Psprivatednsvirtualnetworklink** nesnesi (ardışık düzen veya *bağlantı* parametresi aracılığıyla gönderilir) kullanarak bağlantıyı belirtirken, yerel **Psprivatednsvirtualnetworklink** nesnesi alındıktan sonra Azure özel DNS 'de değiştirilmişse bağlantı silinmez.</span><span class="sxs-lookup"><span data-stu-id="2dbee-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="2dbee-113">Bu, eşzamanlı bölge değişiklikleri için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="2dbee-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="2dbee-114">Bu, yinelenen değişikliklerden bağımsız olarak bölgeyi silen, *overwrite* parametresi kullanılarak bastırılabilir.</span><span class="sxs-lookup"><span data-stu-id="2dbee-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="2dbee-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2dbee-115">EXAMPLES</span></span>

### <span data-ttu-id="2dbee-116">Örnek 1: bağlantı kaldırma</span><span class="sxs-lookup"><span data-stu-id="2dbee-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="2dbee-117">Bu komut MyResourceGroup adlı kaynak grubundan bölge myzone.com bağlantılı MyLink adındaki bağlantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2dbee-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="2dbee-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2dbee-118">PARAMETERS</span></span>

### <span data-ttu-id="2dbee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dbee-119">-DefaultProfile</span></span>
<span data-ttu-id="2dbee-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2dbee-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2dbee-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2dbee-121">-InputObject</span></span>
<span data-ttu-id="2dbee-122">Kaldırılacak sanal ağ bağlantısı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2dbee-122">The virtual network link object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dbee-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="2dbee-123">-Name</span></span>
<span data-ttu-id="2dbee-124">Silinecek bağlantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2dbee-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="2dbee-125">Ayrıca, *Resourcegroupname* ve *BölgeAdı* parametresini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2dbee-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="2dbee-126">Alternatif olarak, *bağlantı parametresini kullanarak bağlantıyı belirtebilirsiniz* .</span><span class="sxs-lookup"><span data-stu-id="2dbee-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="2dbee-127">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="2dbee-127">-Overwrite</span></span>
<span data-ttu-id="2dbee-128">Bir **Psprivatednsvirtualnetworklink** nesnesi (Pipeline veya *Link* parametresi aracılığıyla geçirilir) kullanarak bölgeyi belirtirken, yerel **Psprivatednsvirtualnetworklink** nesnesi ALıNDıKTAN sonra, bu bölge Azure DNS 'de değiştirilmişse bu bölge silinmez.</span><span class="sxs-lookup"><span data-stu-id="2dbee-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="2dbee-129">Bu, eşzamanlı bölge değişiklikleri için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="2dbee-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="2dbee-130">Bu, yinelenen değişikliklerden bağımsız olarak bölgeyi silen, *overwrite* parametresi kullanılarak bastırılabilir.</span><span class="sxs-lookup"><span data-stu-id="2dbee-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="2dbee-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2dbee-131">-PassThru</span></span>
<span data-ttu-id="2dbee-132">İşlemin sonucunu geçirmek için kullanılır sanal ağ bağlantısını silme</span><span class="sxs-lookup"><span data-stu-id="2dbee-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="2dbee-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dbee-133">-ResourceGroupName</span></span>
<span data-ttu-id="2dbee-134">Kaldırılacak bağlantıyı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2dbee-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="2dbee-135">Ayrıca, *BölgeAdı* ve *ad* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2dbee-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="2dbee-136">Alternatif olarak, ardışık düzen veya *bağlantı* parametresi aracılığıyla bir **Psprivatednsvirtualnetworklink** nesnesi kullanarak DNS bölgesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2dbee-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="2dbee-137">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2dbee-137">-ResourceId</span></span>
<span data-ttu-id="2dbee-138">Bağlantının ARM kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2dbee-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="2dbee-139">-BölgeAdı</span><span class="sxs-lookup"><span data-stu-id="2dbee-139">-ZoneName</span></span>
<span data-ttu-id="2dbee-140">Bağlantının ilişkilendirildiği özel DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2dbee-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="2dbee-141">*Resourcegroupname* ve *Name* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2dbee-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="2dbee-142">Alternatif olarak, *bağlantı parametresini kullanarak bağlantıyı belirtebilirsiniz* .</span><span class="sxs-lookup"><span data-stu-id="2dbee-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="2dbee-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="2dbee-143">-Confirm</span></span>
<span data-ttu-id="2dbee-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2dbee-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dbee-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dbee-145">-WhatIf</span></span>
<span data-ttu-id="2dbee-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2dbee-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dbee-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2dbee-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dbee-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dbee-148">CommonParameters</span></span>
<span data-ttu-id="2dbee-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2dbee-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dbee-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dbee-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dbee-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2dbee-151">INPUTS</span></span>

### <span data-ttu-id="2dbee-152">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="2dbee-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="2dbee-153">System. String</span><span class="sxs-lookup"><span data-stu-id="2dbee-153">System.String</span></span>

## <span data-ttu-id="2dbee-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2dbee-154">OUTPUTS</span></span>

### <span data-ttu-id="2dbee-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2dbee-155">System.Boolean</span></span>

## <span data-ttu-id="2dbee-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2dbee-156">NOTES</span></span>

## <span data-ttu-id="2dbee-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2dbee-157">RELATED LINKS</span></span>

[<span data-ttu-id="2dbee-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="2dbee-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="2dbee-159">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="2dbee-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="2dbee-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="2dbee-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
