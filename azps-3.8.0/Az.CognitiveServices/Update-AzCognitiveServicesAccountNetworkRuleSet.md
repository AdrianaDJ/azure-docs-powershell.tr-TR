---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 5c01b692e47c3d246982be353093c436a91d6b64
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095777"
---
# <span data-ttu-id="1d7fe-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d7fe-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="1d7fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d7fe-102">SYNOPSIS</span></span>
<span data-ttu-id="1d7fe-103">Bir öğretici hizmetler hesabının NetworkRule özelliğini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1d7fe-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="1d7fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d7fe-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d7fe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d7fe-105">DESCRIPTION</span></span>
<span data-ttu-id="1d7fe-106">**Güncelleştirme-Azöğretici Iveservicesaccountnetworkruleset** cmdlet 'i, bir öğretici hizmet hesabının networkrule özelliğini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="1d7fe-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="1d7fe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d7fe-107">EXAMPLES</span></span>

### <span data-ttu-id="1d7fe-108">Örnek 1: NetworkRule 'un tüm özelliklerini güncelleştir, JSON ile giriş kuralları</span><span class="sxs-lookup"><span data-stu-id="1d7fe-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="1d7fe-109">Bu komut, tüm NetworkRule özelliklerini, JSON ile giriş kurallarını güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="1d7fe-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="1d7fe-110">Örnek 2: NetworkRule 'un güncelleştirme atlama özelliği</span><span class="sxs-lookup"><span data-stu-id="1d7fe-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="1d7fe-111">Bu komut, NetworkRule 'un bypass özelliğini güncelleyin (diğer özellikler değişmez).</span><span class="sxs-lookup"><span data-stu-id="1d7fe-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="1d7fe-112">Örnek 3: bir öğretici hizmet hesabının NetworkRule kurallarını Temizleme</span><span class="sxs-lookup"><span data-stu-id="1d7fe-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="1d7fe-113">Bu komut, bir öğretici hizmet hesabının (diğer özellikler değiştirmeyeceği) NetworkRule kurallarını temizler.</span><span class="sxs-lookup"><span data-stu-id="1d7fe-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="1d7fe-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d7fe-114">PARAMETERS</span></span>

### <span data-ttu-id="1d7fe-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="1d7fe-115">-DefaultAction</span></span>
<span data-ttu-id="1d7fe-116">Öğretici hizmetler hesap NetworkRule Defaultatransaction.</span><span class="sxs-lookup"><span data-stu-id="1d7fe-116">Cognitive Services Account NetworkRule DefaultAction.</span></span>

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

### <span data-ttu-id="1d7fe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d7fe-117">-DefaultProfile</span></span>
<span data-ttu-id="1d7fe-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1d7fe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d7fe-119">-Iprule</span><span class="sxs-lookup"><span data-stu-id="1d7fe-119">-IpRule</span></span>
<span data-ttu-id="1d7fe-120">Öğrenme Hizmetleri hesap NetworkRule ıprules.</span><span class="sxs-lookup"><span data-stu-id="1d7fe-120">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="1d7fe-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="1d7fe-121">-Name</span></span>
<span data-ttu-id="1d7fe-122">Öğretici hizmetler hesap adı.</span><span class="sxs-lookup"><span data-stu-id="1d7fe-122">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="1d7fe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d7fe-123">-ResourceGroupName</span></span>
<span data-ttu-id="1d7fe-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1d7fe-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="1d7fe-125">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1d7fe-125">-VirtualNetworkRule</span></span>
<span data-ttu-id="1d7fe-126">Öğretici Hizmetler hesabı NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="1d7fe-126">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="1d7fe-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="1d7fe-127">-Confirm</span></span>
<span data-ttu-id="1d7fe-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1d7fe-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d7fe-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d7fe-129">-WhatIf</span></span>
<span data-ttu-id="1d7fe-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d7fe-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d7fe-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1d7fe-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d7fe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d7fe-132">CommonParameters</span></span>
<span data-ttu-id="1d7fe-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d7fe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d7fe-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1d7fe-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d7fe-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d7fe-135">INPUTS</span></span>

### <span data-ttu-id="1d7fe-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1d7fe-136">System.String</span></span>

### <span data-ttu-id="1d7fe-137">Microsoft. Azure. Commands. Management. öğretici Bveservices. modeller. Psıprule []</span><span class="sxs-lookup"><span data-stu-id="1d7fe-137">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="1d7fe-138">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="1d7fe-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="1d7fe-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d7fe-139">OUTPUTS</span></span>

### <span data-ttu-id="1d7fe-140">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d7fe-140">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="1d7fe-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d7fe-141">NOTES</span></span>

## <span data-ttu-id="1d7fe-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d7fe-142">RELATED LINKS</span></span>
