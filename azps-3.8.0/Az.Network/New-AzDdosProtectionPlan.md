---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
ms.openlocfilehash: 39d45085c7f53bfeec6e18f38602fca48a3cefa3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104756"
---
# <span data-ttu-id="441b4-101">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="441b4-101">New-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="441b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="441b4-102">SYNOPSIS</span></span>
<span data-ttu-id="441b4-103">Bir Vseçdos koruma planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="441b4-103">Creates a DDoS protection plan.</span></span>

## <span data-ttu-id="441b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="441b4-104">SYNTAX</span></span>

```
New-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="441b4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="441b4-105">DESCRIPTION</span></span>
<span data-ttu-id="441b4-106">New-AzDdosProtectionPlan cmdlet 'i bir Vseçdos koruma planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="441b4-106">The New-AzDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="441b4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="441b4-107">EXAMPLES</span></span>

### <span data-ttu-id="441b4-108">Örnek 1: yeni bir sanal ağla bir Vseçdos koruma planı oluşturma ve ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="441b4-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="441b4-109">İlk olarak, **New-Azvseçdosprotectionplan** komutunu içeren yeni bir Vseçdos koruma planı oluşturduk.</span><span class="sxs-lookup"><span data-stu-id="441b4-109">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="441b4-110">Ardından, **New-AzVirtualNetwork** ile yeni bir sanal ağ yaratıyoruz ve yeni oluşturulan planın kimliğini **Vseçdosprotectionplanıd** parametresinde belirtiyoruz.</span><span class="sxs-lookup"><span data-stu-id="441b4-110">Then, we create a new virtual network with **New-AzVirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="441b4-111">Bu durumda, sanal ağı planla ilişkilendirdiğimiz için, **Etkindosprotection** parametresini de belirleyebiliriz.</span><span class="sxs-lookup"><span data-stu-id="441b4-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="441b4-112">Örnek 2: var olan bir sanal ağla bir Vseçdos koruma planı oluşturma ve ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="441b4-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = New-Object Microsoft.Azure.Commands.Network.Models.PSResourceId
D:\> $vnet.DdosProtectionPlan.Id = $ddosProtectionPlan.Id
D:\> $vnet.EnableDdosProtection = $true
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb"
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
                             "Etag": "W/\"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : true
DdosProtectionPlan     : {
                           "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName"
                         }
EnableVmProtection     : false
```

<span data-ttu-id="441b4-113">İlk olarak, **New-Azvseçdosprotectionplan** komutunu içeren yeni bir Vseçdos koruma planı oluşturduk.</span><span class="sxs-lookup"><span data-stu-id="441b4-113">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="441b4-114">İkincisi, planla ilişkilendirmek istediğimiz sanal ağın en güncel sürümünü hazırlıyoruz.</span><span class="sxs-lookup"><span data-stu-id="441b4-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="441b4-115">Yeni oluşturulan planın KIMLIĞINE başvuru içeren bir **Psresourceıd** nesnesiyle **Vseçdosprotectionplan** özelliğini güncelleştirdik.</span><span class="sxs-lookup"><span data-stu-id="441b4-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="441b4-116">Bu durumda, sanal ağı bir Vseçdos koruma planıyla ilişkilendirmemiz için, **etkin**</span><span class="sxs-lookup"><span data-stu-id="441b4-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="441b4-117">Son olarak, yerel değişkeni **set-AzVirtualNetwork** ' a geçirerek yeni durumu devam ediyoruz.</span><span class="sxs-lookup"><span data-stu-id="441b4-117">Finally, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span>

## <span data-ttu-id="441b4-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="441b4-118">PARAMETERS</span></span>

### <span data-ttu-id="441b4-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="441b4-119">-AsJob</span></span>
<span data-ttu-id="441b4-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="441b4-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="441b4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="441b4-121">-DefaultProfile</span></span>
<span data-ttu-id="441b4-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="441b4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="441b4-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="441b4-123">-Location</span></span>
<span data-ttu-id="441b4-124">Oluşturulacak Vados koruma planının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="441b4-124">Specifies the location of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="441b4-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="441b4-125">-Name</span></span>
<span data-ttu-id="441b4-126">Oluşturulacak Vados koruma planının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="441b4-126">Specifies the name of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="441b4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="441b4-127">-ResourceGroupName</span></span>
<span data-ttu-id="441b4-128">Oluşturulacak Vseçdos koruma planının kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="441b4-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="441b4-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="441b4-129">-Tag</span></span>
<span data-ttu-id="441b4-130">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="441b4-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441b4-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="441b4-131">-Confirm</span></span>
<span data-ttu-id="441b4-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="441b4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="441b4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="441b4-133">-WhatIf</span></span>
<span data-ttu-id="441b4-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="441b4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="441b4-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="441b4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="441b4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="441b4-136">CommonParameters</span></span>
<span data-ttu-id="441b4-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="441b4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="441b4-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="441b4-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="441b4-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="441b4-139">INPUTS</span></span>

### <span data-ttu-id="441b4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="441b4-140">System.String</span></span>

### <span data-ttu-id="441b4-141">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="441b4-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="441b4-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="441b4-142">OUTPUTS</span></span>

### <span data-ttu-id="441b4-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="441b4-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="441b4-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="441b4-144">NOTES</span></span>

## <span data-ttu-id="441b4-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="441b4-145">RELATED LINKS</span></span>

[<span data-ttu-id="441b4-146">Get-Azvseçdosprotectionplan</span><span class="sxs-lookup"><span data-stu-id="441b4-146">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="441b4-147">Remove-Azvseçdosprotectionplan</span><span class="sxs-lookup"><span data-stu-id="441b4-147">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="441b4-148">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="441b4-148">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="441b4-149">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="441b4-149">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="441b4-150">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="441b4-150">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)