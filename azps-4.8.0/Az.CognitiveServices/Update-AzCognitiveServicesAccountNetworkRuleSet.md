---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 0f094ba8bdfa8dbf40f2af8495ee2f8cfa6fca16
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267898"
---
# <span data-ttu-id="edaba-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="edaba-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="edaba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edaba-102">SYNOPSIS</span></span>
<span data-ttu-id="edaba-103">Bir öğretici hizmetler hesabının NetworkRule özelliğini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="edaba-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="edaba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="edaba-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="edaba-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="edaba-105">DESCRIPTION</span></span>
<span data-ttu-id="edaba-106">**Güncelleştirme-Azöğretici Iveservicesaccountnetworkruleset** cmdlet 'i, bir öğretici hizmet hesabının networkrule özelliğini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="edaba-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="edaba-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="edaba-107">EXAMPLES</span></span>

### <span data-ttu-id="edaba-108">Örnek 1: NetworkRule 'un tüm özelliklerini güncelleştir, JSON ile giriş kuralları</span><span class="sxs-lookup"><span data-stu-id="edaba-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="edaba-109">Bu komut, tüm NetworkRule özelliklerini, JSON ile giriş kurallarını güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="edaba-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="edaba-110">Örnek 2: NetworkRule 'un güncelleştirme atlama özelliği</span><span class="sxs-lookup"><span data-stu-id="edaba-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="edaba-111">Bu komut, NetworkRule 'un bypass özelliğini güncelleyin (diğer özellikler değişmez).</span><span class="sxs-lookup"><span data-stu-id="edaba-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="edaba-112">Örnek 3: bir öğretici hizmet hesabının NetworkRule kurallarını Temizleme</span><span class="sxs-lookup"><span data-stu-id="edaba-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="edaba-113">Bu komut, bir öğretici hizmet hesabının (diğer özellikler değiştirmeyeceği) NetworkRule kurallarını temizler.</span><span class="sxs-lookup"><span data-stu-id="edaba-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="edaba-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="edaba-114">PARAMETERS</span></span>

### <span data-ttu-id="edaba-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="edaba-115">-DefaultAction</span></span>
<span data-ttu-id="edaba-116">Öğretici hizmetler hesap NetworkRule Defaultatransaction.</span><span class="sxs-lookup"><span data-stu-id="edaba-116">Cognitive Services Account NetworkRule DefaultAction.</span></span> <span data-ttu-id="edaba-117">Varsayılan değer `Deny` .</span><span class="sxs-lookup"><span data-stu-id="edaba-117">Default value `Deny`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edaba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edaba-118">-DefaultProfile</span></span>
<span data-ttu-id="edaba-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="edaba-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edaba-120">-Iprule</span><span class="sxs-lookup"><span data-stu-id="edaba-120">-IpRule</span></span>
<span data-ttu-id="edaba-121">Öğrenme Hizmetleri hesap NetworkRule ıprules.</span><span class="sxs-lookup"><span data-stu-id="edaba-121">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edaba-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="edaba-122">-Name</span></span>
<span data-ttu-id="edaba-123">Öğretici hizmetler hesap adı.</span><span class="sxs-lookup"><span data-stu-id="edaba-123">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edaba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edaba-124">-ResourceGroupName</span></span>
<span data-ttu-id="edaba-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="edaba-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edaba-126">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="edaba-126">-VirtualNetworkRule</span></span>
<span data-ttu-id="edaba-127">Öğretici Hizmetler hesabı NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="edaba-127">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edaba-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="edaba-128">-Confirm</span></span>
<span data-ttu-id="edaba-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="edaba-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edaba-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edaba-130">-WhatIf</span></span>
<span data-ttu-id="edaba-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="edaba-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edaba-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="edaba-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edaba-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edaba-133">CommonParameters</span></span>
<span data-ttu-id="edaba-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="edaba-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edaba-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="edaba-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edaba-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="edaba-136">INPUTS</span></span>

### <span data-ttu-id="edaba-137">System. String</span><span class="sxs-lookup"><span data-stu-id="edaba-137">System.String</span></span>

### <span data-ttu-id="edaba-138">Microsoft. Azure. Commands. Management. öğretici Bveservices. modeller. Psıprule []</span><span class="sxs-lookup"><span data-stu-id="edaba-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="edaba-139">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="edaba-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="edaba-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="edaba-140">OUTPUTS</span></span>

### <span data-ttu-id="edaba-141">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="edaba-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="edaba-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="edaba-142">NOTES</span></span>

## <span data-ttu-id="edaba-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="edaba-143">RELATED LINKS</span></span>
