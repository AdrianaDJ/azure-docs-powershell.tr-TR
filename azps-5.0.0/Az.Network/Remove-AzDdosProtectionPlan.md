---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
ms.openlocfilehash: c565c78e7f95e02d3449a04f0a53f4b84ef7a9f5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276398"
---
# <span data-ttu-id="783cd-101">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="783cd-101">Remove-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="783cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="783cd-102">SYNOPSIS</span></span>
<span data-ttu-id="783cd-103">Bir Vseçdos koruma planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="783cd-103">Removes a DDoS protection plan.</span></span>

## <span data-ttu-id="783cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="783cd-104">SYNTAX</span></span>

```
Remove-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="783cd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="783cd-105">DESCRIPTION</span></span>
<span data-ttu-id="783cd-106">Remove-AzDdosProtectionPlan cmdlet 'i, bir Vseçdos koruma planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="783cd-106">The Remove-AzDdosProtectionPlan cmdlet removes a DDoS protection plan.</span></span>

## <span data-ttu-id="783cd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="783cd-107">EXAMPLES</span></span>

### <span data-ttu-id="783cd-108">Örnek 1: boş bir Vseçdos koruma planını kaldırma</span><span class="sxs-lookup"><span data-stu-id="783cd-108">Example 1: Remove an empty DDoS protection plan</span></span>
```
D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="783cd-109">Bu durumda, bir Vseçdos koruma planını belirtildiği gibi kaldırdık.</span><span class="sxs-lookup"><span data-stu-id="783cd-109">In this case, we remove a DDoS protection plan as specified.</span></span>

### <span data-ttu-id="783cd-110">Örnek 2: sanal ağla ilişkili bir Vseçdos koruma planını kaldırma</span><span class="sxs-lookup"><span data-stu-id="783cd-110">Example 2: Remove a DDoS protection plan associated with a virtual network</span></span>
```
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = $null
D:\> $vnet.EnableDdosProtection = $false
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"65947351-747e-4686-aa8b-c40da58f6c8b"
ResourceGuid           : fcb7bc1e-ee0d-4005-b3f1-feda76e3756c
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "10.0.0.0/16"
                           ]
                         }
DhcpOptions            : {
                           "DnsServers": [
                             "8.8.8.8"
                           ]
                         }
Subnets                : [
                           {
                             "Name": "SubnetName",
                             "Etag": "W/\"65947351-747e-4686-aa8b-c40da58f6c8b\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
EnableVmProtection     : false


D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="783cd-111">Sanal ağla ilişkili olmaları durumunda, Vseçlanları koruma planları silinemez.</span><span class="sxs-lookup"><span data-stu-id="783cd-111">DDoS protection plans cannot be deleted if they are associated with a virtual network.</span></span> <span data-ttu-id="783cd-112">İlk adım, her iki nesnenin de ilişkisini, bu nedenle.</span><span class="sxs-lookup"><span data-stu-id="783cd-112">So the first step is to disassociate both objects.</span></span> <span data-ttu-id="783cd-113">Burada, planla ilişkili sanal ağın en güncel sürümünü aldık ve **Ddosprotectionplan** özelliğini boş bir değerle ayarladık **(Bu bayrak bir** plan olmadan true olamaz).</span><span class="sxs-lookup"><span data-stu-id="783cd-113">Here, we get the most updated version of the virtual network associated with the plan, and we set the property **DdosProtectionPlan** to an empty value and the flag **EnableDdosProtection** (this flag cannot be true without a plan).</span></span>
<span data-ttu-id="783cd-114">Ardından yerel değişkeni **set-AzVirtualNetwork** ' a geçirerek yeni durumu devam ediyoruz.</span><span class="sxs-lookup"><span data-stu-id="783cd-114">Then, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span> <span data-ttu-id="783cd-115">Bu aşamada, plan artık sanal ağla ilişkilendirilmez.</span><span class="sxs-lookup"><span data-stu-id="783cd-115">At this point, the plan is no longer associated with the virtual network.</span></span>
<span data-ttu-id="783cd-116">Bu, planla ilişkili son bir bu ise, Remove-Azvseçdosprotectionplan komutunu kullanarak Vseçdos koruma planını kaldırabiliriz.</span><span class="sxs-lookup"><span data-stu-id="783cd-116">If this is the last one associated with the plan, we can remove the DDoS protection plan by using the command Remove-AzDdosProtectionPlan.</span></span>

## <span data-ttu-id="783cd-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="783cd-117">PARAMETERS</span></span>

### <span data-ttu-id="783cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="783cd-118">-DefaultProfile</span></span>
<span data-ttu-id="783cd-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="783cd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="783cd-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="783cd-120">-Name</span></span>
<span data-ttu-id="783cd-121">Kaldırılacak olan Dsaprotection planının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="783cd-121">Specifies the name of the DDoS protection plan to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="783cd-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="783cd-122">-PassThru</span></span>
<span data-ttu-id="783cd-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="783cd-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="783cd-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="783cd-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="783cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="783cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="783cd-126">Kaldırılacak Vseçdos koruma planının kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="783cd-126">Specifies the resource group of the DDoS protection plan to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="783cd-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="783cd-127">-Confirm</span></span>
<span data-ttu-id="783cd-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="783cd-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="783cd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="783cd-129">-WhatIf</span></span>
<span data-ttu-id="783cd-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="783cd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="783cd-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="783cd-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="783cd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="783cd-132">CommonParameters</span></span>
<span data-ttu-id="783cd-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="783cd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="783cd-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="783cd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="783cd-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="783cd-135">INPUTS</span></span>

### <span data-ttu-id="783cd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="783cd-136">System.String</span></span>

## <span data-ttu-id="783cd-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="783cd-137">OUTPUTS</span></span>

### <span data-ttu-id="783cd-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="783cd-138">System.Boolean</span></span>

## <span data-ttu-id="783cd-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="783cd-139">NOTES</span></span>

## <span data-ttu-id="783cd-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="783cd-140">RELATED LINKS</span></span>

[<span data-ttu-id="783cd-141">Yeni-Azvadosprotectionplan</span><span class="sxs-lookup"><span data-stu-id="783cd-141">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="783cd-142">Get-Azvseçdosprotectionplan</span><span class="sxs-lookup"><span data-stu-id="783cd-142">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="783cd-143">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="783cd-143">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="783cd-144">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="783cd-144">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="783cd-145">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="783cd-145">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)