---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 42454d41281746e4b95399e74aa4cb7a9c3c7a77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752022"
---
# <span data-ttu-id="c09bd-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c09bd-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="c09bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c09bd-102">SYNOPSIS</span></span>
<span data-ttu-id="c09bd-103">DNS bölgesinin özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c09bd-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="c09bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c09bd-104">SYNTAX</span></span>

### <span data-ttu-id="c09bd-105">Alanlar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c09bd-105">Fields (Default)</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c09bd-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="c09bd-106">FieldsObjects</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c09bd-107">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="c09bd-107">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c09bd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c09bd-108">DESCRIPTION</span></span>
<span data-ttu-id="c09bd-109">**Set-AzDnsZone** cmdlet 'ı, Azure DNS HIZMETINDE belirtilen DNS bölgesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c09bd-109">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="c09bd-110">Bu cmdlet, bölgedeki kayıt kümelerini güncelleştirmez.</span><span class="sxs-lookup"><span data-stu-id="c09bd-110">This cmdlet does not update the record sets in the zone.</span></span>
<span data-ttu-id="c09bd-111">Bir **dnsZone** nesnesini parametre olarak veya Pipeline işlecini kullanarak geçirebilir ya da bir alternatif olarak, *BölgeAdı* ve *resourcegroupname* parametrelerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c09bd-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="c09bd-112">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için *Confirm* parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c09bd-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="c09bd-113">DNS bölgesini nesne olarak geçirirken (bölge nesnesini veya ardışık düzen aracılığıyla), yerel DnsZone nesnesinin alındığı bu yana Azure DNS 'de değiştirilmişse bu, güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="c09bd-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="c09bd-114">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="c09bd-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="c09bd-115">Bu *davranışı, eş* zamanlı değişikliklerden bağımsız olarak, bölgeyi güncelleyen parametreyle kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c09bd-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="c09bd-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c09bd-116">EXAMPLES</span></span>

### <span data-ttu-id="c09bd-117">Örnek 1: DNS bölgesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c09bd-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="c09bd-118">İlk komut, myzone.com adlı bölgeyi belirtilen kaynak grubundan alır ve $Zone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c09bd-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>
<span data-ttu-id="c09bd-119">İkinci komut $Zone etiketlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c09bd-119">The second command updates the tags for $Zone.</span></span>
<span data-ttu-id="c09bd-120">Son komutu değişikliği kaydeder.</span><span class="sxs-lookup"><span data-stu-id="c09bd-120">The final command commits the change.</span></span>

### <span data-ttu-id="c09bd-121">Örnek 2: bir bölgeye ait etiketleri güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c09bd-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="c09bd-122">Bu komut, önce bölgeyi açıkça almadan myzone.com adındaki bölgenin etiketlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c09bd-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="c09bd-123">Örnek 3: KIMLIĞINI belirterek özel bir bölgeyi sanal bir ağla Ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="c09bd-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="c09bd-124">Bu komut, KIMLIĞI belirterek özel DNS bölgesini bir kayıt ağı olarak myvnet myprivatezone.com ile ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="c09bd-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="c09bd-125">Örnek 4: ağ nesnesini belirterek özel bir bölgeyi sanal bir ağla Ilişkilendirme.</span><span class="sxs-lookup"><span data-stu-id="c09bd-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="c09bd-126">Bu komut, $vnet değişkeni ile temsil edilen sanal ağ nesnesini Set-AzDnsZone cmdlet 'ine geçirerek, özel DNS bölgesini bir kayıt ağı olarak myvnet ile ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="c09bd-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzDnsZone cmdlet.</span></span>

## <span data-ttu-id="c09bd-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c09bd-127">PARAMETERS</span></span>

### <span data-ttu-id="c09bd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c09bd-128">-DefaultProfile</span></span>
<span data-ttu-id="c09bd-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c09bd-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c09bd-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="c09bd-130">-Name</span></span>
<span data-ttu-id="c09bd-131">Güncelleştirilecek DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c09bd-131">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c09bd-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="c09bd-132">-Overwrite</span></span>
<span data-ttu-id="c09bd-133">DNS bölgesini nesne olarak geçirirken (bölge nesnesini veya ardışık düzen aracılığıyla), yerel DnsZone nesnesinin alındığı bu yana Azure DNS 'de değiştirilmişse bu, güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="c09bd-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="c09bd-134">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="c09bd-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="c09bd-135">Bu *davranışı, eş* zamanlı değişikliklerden bağımsız olarak, bölgeyi güncelleyen parametreyle kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c09bd-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="c09bd-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c09bd-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="c09bd-137">Bu DNS bölgesindeki sanal makine ana bilgisayar adları kayıtlarını kaydeden sanal ağların listesi, yalnızca özel bölgeler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c09bd-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c09bd-138">-Registrationvirtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="c09bd-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="c09bd-139">Bu DNS bölgesindeki sanal makine ana bilgisayar adları kayıtlarını kaydeden sanal ağ kimliklerinin listesi, yalnızca özel bölgeler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c09bd-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c09bd-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c09bd-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="c09bd-141">Bu DNS bölgesindeki kayıtları çözümleyebileceğiniz sanal ağların listesi, yalnızca özel bölgeler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c09bd-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c09bd-142">-Resolutionvirtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="c09bd-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="c09bd-143">Bu DNS bölgesindeki kayıtları çözümleyemeyecek sanal ağ kimliklerinin listesi, yalnızca özel bölgeler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c09bd-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c09bd-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c09bd-144">-ResourceGroupName</span></span>
<span data-ttu-id="c09bd-145">Güncelleştirilecek bölgeyi içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c09bd-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="c09bd-146">Ayrıca, BölgeAdı parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c09bd-146">You must also specify the ZoneName parameter.</span></span>
<span data-ttu-id="c09bd-147">Alternatif olarak, bölgeyi *bölge* parametresi veya ardışık düzene sahip bir dnsZone nesnesi kullanarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c09bd-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c09bd-148">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c09bd-148">-Tag</span></span>
<span data-ttu-id="c09bd-149">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="c09bd-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c09bd-150">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="c09bd-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c09bd-151">-Bölge</span><span class="sxs-lookup"><span data-stu-id="c09bd-151">-Zone</span></span>
<span data-ttu-id="c09bd-152">Güncelleştirilecek DNS bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c09bd-152">Specifies the DNS zone to update.</span></span>
<span data-ttu-id="c09bd-153">Alternatif olarak, bölgeyi *BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c09bd-153">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="c09bd-154">-Onay</span><span class="sxs-lookup"><span data-stu-id="c09bd-154">-Confirm</span></span>
<span data-ttu-id="c09bd-155">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c09bd-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c09bd-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c09bd-156">-WhatIf</span></span>
<span data-ttu-id="c09bd-157">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c09bd-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c09bd-158">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c09bd-158">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c09bd-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c09bd-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c09bd-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c09bd-160">CommonParameters</span></span>
<span data-ttu-id="c09bd-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c09bd-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c09bd-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c09bd-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c09bd-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c09bd-163">INPUTS</span></span>

### <span data-ttu-id="c09bd-164">System. String</span><span class="sxs-lookup"><span data-stu-id="c09bd-164">System.String</span></span>

### <span data-ttu-id="c09bd-165">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c09bd-165">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c09bd-166">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0</span><span class="sxs-lookup"><span data-stu-id="c09bd-166">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c09bd-167">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. Internal. Network. Common. IResourceReference, Microsoft. Azure. PowerShell. clients. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c09bd-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="c09bd-168">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="c09bd-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="c09bd-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c09bd-169">OUTPUTS</span></span>

### <span data-ttu-id="c09bd-170">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="c09bd-170">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="c09bd-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c09bd-171">NOTES</span></span>
<span data-ttu-id="c09bd-172">*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="c09bd-172">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="c09bd-173">Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.</span><span class="sxs-lookup"><span data-stu-id="c09bd-173">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="c09bd-174">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="c09bd-174">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="c09bd-175">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="c09bd-175">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c09bd-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c09bd-176">RELATED LINKS</span></span>

[<span data-ttu-id="c09bd-177">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c09bd-177">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="c09bd-178">Yeni-Azdnzone</span><span class="sxs-lookup"><span data-stu-id="c09bd-178">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="c09bd-179">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c09bd-179">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
