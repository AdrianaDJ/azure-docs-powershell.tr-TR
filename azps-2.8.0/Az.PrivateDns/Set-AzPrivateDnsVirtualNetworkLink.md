---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: d2d00df48cbaf4bff1d6e9dac648004d73e65f2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933071"
---
# <span data-ttu-id="01f00-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="01f00-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="01f00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01f00-102">SYNOPSIS</span></span>
<span data-ttu-id="01f00-103">Özel bir bölgeyle ve bir kaynak grubuyla ilişkilendirilmiş sanal ağ bağlantısını güncelleştirir/ayarlar.</span><span class="sxs-lookup"><span data-stu-id="01f00-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="01f00-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01f00-104">SYNTAX</span></span>

### <span data-ttu-id="01f00-105">Alanlar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="01f00-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01f00-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="01f00-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01f00-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="01f00-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01f00-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="01f00-108">DESCRIPTION</span></span>
<span data-ttu-id="01f00-109">**Set-AzPrivateDnsVirtualNetworkLink** cmdlet 'i, belirtilen kaynak grubundaki bir bölgeyle ilişkili bağlantıyı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="01f00-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="01f00-110">*Link* parametresini kullanarak veya Pipeline Işlecini kullanarak **Psprivatednsvirtualnetworklink** nesnesini geçirebilir ya da *ad BölgeAdı* *ZoneName* ve *resourcegroupname* parametrelerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01f00-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="01f00-111">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için Confirm parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01f00-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="01f00-112">Bir **Psprivatednsvirtualnetworklink** nesnesi (ardışık düzen veya *bağlantı* parametresi aracılığıyla gönderilir) kullanarak bölgeyi belirtirken, yerel **Psprivatednsvirtualnetworklink** nesnesi alındıktan sonra Azure DNS 'de değiştirilmişse bağlantı güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="01f00-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="01f00-113">Bu, eşzamanlı bağlantı değişiklikleri için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="01f00-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="01f00-114">Bu, eşzamanlı değişikliklerden bağımsız olarak bağlantıyı güncelleştiren, *overwrite* parametresi kullanılarak bastırılabilir.</span><span class="sxs-lookup"><span data-stu-id="01f00-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="01f00-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01f00-115">EXAMPLES</span></span>

### <span data-ttu-id="01f00-116">Örnek 1: bağlantı ayarlama</span><span class="sxs-lookup"><span data-stu-id="01f00-116">Example 1: Set a link</span></span>
```
PS C:\>Set-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -Tag @{} -IsRegistrationEnabled $true

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="01f00-117">Bu komut MyLink adındaki myzone.com adlı bölgeyle MyResourceGroup adındaki bağlantı için ısaregistrationenabled değerini true olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="01f00-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="01f00-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01f00-118">PARAMETERS</span></span>

### <span data-ttu-id="01f00-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01f00-119">-DefaultProfile</span></span>
<span data-ttu-id="01f00-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="01f00-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01f00-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01f00-121">-InputObject</span></span>
<span data-ttu-id="01f00-122">Ayarlanacak sanal ağ bağlantısı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="01f00-122">The virtual network link object to set.</span></span>

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

### <span data-ttu-id="01f00-123">-Isregistrationenabled</span><span class="sxs-lookup"><span data-stu-id="01f00-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="01f00-124">Sanal ağ bağlantısında kaydın etkinleştirilip etkinleştirilmediğini temsil eden Boole değeri.</span><span class="sxs-lookup"><span data-stu-id="01f00-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01f00-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="01f00-125">-Name</span></span>
<span data-ttu-id="01f00-126">Bu cmdlet 'in kaldırdığı bağlantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01f00-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="01f00-127">Ayrıca, *Resourcegroupname* ve *BölgeAdı* parametresini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="01f00-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="01f00-128">Alternatif olarak, *bağlantı* parametresini kullanarak özel DNS bağlantısını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01f00-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="01f00-129">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="01f00-129">-Overwrite</span></span>
<span data-ttu-id="01f00-130">Bir **Psprivatednsvirtualnetworklink** nesnesi (ardışık düzen veya *bağlantı* parametresi aracılığıyla gönderilir) kullanarak bağlantıyı belirtirken, yerel **psprivatednsvirtualnetworklink** NESNESI alındıktan sonra, bağlantı Azure DNS 'de değiştirilmişse bu bağlantı silinmez.</span><span class="sxs-lookup"><span data-stu-id="01f00-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="01f00-131">Bu, eşzamanlı bağlantı değişiklikleri için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="01f00-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="01f00-132">Bu, eşzamanlı değişikliklerden bağımsız olarak bağlantıyı silen, *overwrite* parametresi kullanılarak bastırılabilir.</span><span class="sxs-lookup"><span data-stu-id="01f00-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="01f00-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01f00-133">-ResourceGroupName</span></span>
<span data-ttu-id="01f00-134">Kaldırılacak bağlantıyı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01f00-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="01f00-135">Ayrıca, *BölgeAdı* ve *ad* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="01f00-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="01f00-136">Alternatif olarak, ardışık düzen veya *bağlantı* parametresi aracılığıyla bir **Psprivatednsvirtualnetworklink** nesnesi kullanarak sanal ağ bağlantısını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01f00-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="01f00-137">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="01f00-137">-ResourceId</span></span>
<span data-ttu-id="01f00-138">Özel DNS bölge RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="01f00-138">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="01f00-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="01f00-139">-Tag</span></span>
<span data-ttu-id="01f00-140">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="01f00-140">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01f00-141">-BölgeAdı</span><span class="sxs-lookup"><span data-stu-id="01f00-141">-ZoneName</span></span>
<span data-ttu-id="01f00-142">Bu cmdlet 'in kaldırıldığı DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01f00-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="01f00-143">*Name* ve *resourcegroupname* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="01f00-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="01f00-144">Alternatif olarak, *bağlantı* parametresini kullanarak özel DNS bağlantısını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01f00-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="01f00-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="01f00-145">-Confirm</span></span>
<span data-ttu-id="01f00-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="01f00-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01f00-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01f00-147">-WhatIf</span></span>
<span data-ttu-id="01f00-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="01f00-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01f00-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="01f00-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01f00-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f00-150">CommonParameters</span></span>
<span data-ttu-id="01f00-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01f00-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f00-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01f00-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f00-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01f00-153">INPUTS</span></span>

### <span data-ttu-id="01f00-154">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="01f00-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="01f00-155">System. String</span><span class="sxs-lookup"><span data-stu-id="01f00-155">System.String</span></span>

## <span data-ttu-id="01f00-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01f00-156">OUTPUTS</span></span>

### <span data-ttu-id="01f00-157">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="01f00-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="01f00-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01f00-158">NOTES</span></span>

## <span data-ttu-id="01f00-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01f00-159">RELATED LINKS</span></span>

[<span data-ttu-id="01f00-160">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="01f00-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="01f00-161">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="01f00-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="01f00-162">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="01f00-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)