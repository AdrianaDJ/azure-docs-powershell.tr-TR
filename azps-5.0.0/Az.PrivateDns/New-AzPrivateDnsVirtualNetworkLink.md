---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/New-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: be1480b68c4b0fd66328a7ff417517ee86cb88df
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322193"
---
# <span data-ttu-id="36d50-101">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="36d50-101">New-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="36d50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36d50-102">SYNOPSIS</span></span>
<span data-ttu-id="36d50-103">Yeni bir özel DNS sanal ağ bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36d50-103">Creates a new private DNS virtual network link.</span></span>

## <span data-ttu-id="36d50-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36d50-104">SYNTAX</span></span>

### <span data-ttu-id="36d50-105">Virtualnetworkıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="36d50-105">VirtualNetworkId (Default)</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36d50-106">VirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="36d50-106">VirtualNetworkObject</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetwork <VirtualNetwork> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36d50-107">Remotevirtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="36d50-107">RemoteVirtualNetworkId</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36d50-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="36d50-108">DESCRIPTION</span></span>
<span data-ttu-id="36d50-109">**New-AzPrivateDnsVirtualNetworkLink** cmdlet 'i, belirtilen kaynak grubunda ve özel bölgede yeni bir özel etki alanı adı SISTEMI (DNS) sanal ağ bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36d50-109">The **New-AzPrivateDnsVirtualNetworkLink** cmdlet creates a new private Domain Name System (DNS) virtual network link in the specified resource group and private zone.</span></span> <span data-ttu-id="36d50-110">*Name* parametresi için benzersiz bir bağlantı adı belirtmelisiniz veya cmdlet hata döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="36d50-110">You must specify a unique link name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="36d50-111">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için *Confirm* parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="36d50-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="36d50-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36d50-112">EXAMPLES</span></span>

### <span data-ttu-id="36d50-113">Örnek 1: özel DNS sanal ağ bağlantısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="36d50-113">Example 1: Create a Private DNS virtual network link</span></span>
```
PS C:\>$Link = New-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -VirtualNetworkId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork" -EnableRegistration

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

<span data-ttu-id="36d50-114">Bu komut, myzone.com ve sanal ağ "myvirtualnetwork" (kaynak grubunda zaten oluşturulmuş) adlı özel DNS bölgesiyle ilişkili olarak belirtilen kaynak grubundaki yeni bir sanal ağ bağlantısı oluşturur ve $Link değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="36d50-114">This command creates a new virtual network link associated with the private DNS zone named myzone.com and virtual network "myvirtualnetwork" (which has already been created in the resource group) in the specified resource group, and then stores it in the $Link variable.</span></span>

## <span data-ttu-id="36d50-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36d50-115">PARAMETERS</span></span>

### <span data-ttu-id="36d50-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d50-116">-DefaultProfile</span></span>
<span data-ttu-id="36d50-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="36d50-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36d50-118">-EnableRegistration</span><span class="sxs-lookup"><span data-stu-id="36d50-118">-EnableRegistration</span></span>
<span data-ttu-id="36d50-119">Bağlantının kayıt özelliğinin etkin olup olmadığını gösteren Switch parametresi.</span><span class="sxs-lookup"><span data-stu-id="36d50-119">Switch parameter that represents if the link is registration enabled or not.</span></span>

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

### <span data-ttu-id="36d50-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="36d50-120">-Name</span></span>
<span data-ttu-id="36d50-121">Oluşturulacak sanal ağ bağlantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36d50-121">Specifies the name of the virtual network link to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d50-122">-Remotevirtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="36d50-122">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="36d50-123">Başka bir Kiracıdaki sanal ağın kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="36d50-123">The resource id of the virtual network in another tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoteVirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d50-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36d50-124">-ResourceGroupName</span></span>
<span data-ttu-id="36d50-125">Bağlantının oluşturulacağı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="36d50-125">Specifies the resource group in which to create the link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d50-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="36d50-126">-Tag</span></span>
<span data-ttu-id="36d50-127">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="36d50-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="36d50-128">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="36d50-128">-VirtualNetwork</span></span>
<span data-ttu-id="36d50-129">Bağlantıyla ilişkili sanal ağ nesnesi.</span><span class="sxs-lookup"><span data-stu-id="36d50-129">The virtual network object associated with the link.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IVirtualNetwork
Parameter Sets: VirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d50-130">-Virtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="36d50-130">-VirtualNetworkId</span></span>
<span data-ttu-id="36d50-131">Bağlantıyla ilişkili sanal ağın kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="36d50-131">The resource id of the virtual network associated with the link.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d50-132">-BölgeAdı</span><span class="sxs-lookup"><span data-stu-id="36d50-132">-ZoneName</span></span>
<span data-ttu-id="36d50-133">Sanal ağ bağlantısına bağlanacak bölgenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36d50-133">Specifies the name of the zone which will be linked to the virtual network link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d50-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="36d50-134">-Confirm</span></span>
<span data-ttu-id="36d50-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="36d50-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36d50-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36d50-136">-WhatIf</span></span>
<span data-ttu-id="36d50-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="36d50-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36d50-138">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="36d50-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36d50-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="36d50-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36d50-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d50-140">CommonParameters</span></span>
<span data-ttu-id="36d50-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36d50-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d50-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="36d50-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d50-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36d50-143">INPUTS</span></span>

### <span data-ttu-id="36d50-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="36d50-144">None</span></span>

## <span data-ttu-id="36d50-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36d50-145">OUTPUTS</span></span>

### <span data-ttu-id="36d50-146">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="36d50-146">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="36d50-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36d50-147">NOTES</span></span>

## <span data-ttu-id="36d50-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36d50-148">RELATED LINKS</span></span>

[<span data-ttu-id="36d50-149">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="36d50-149">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="36d50-150">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="36d50-150">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="36d50-151">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="36d50-151">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)
