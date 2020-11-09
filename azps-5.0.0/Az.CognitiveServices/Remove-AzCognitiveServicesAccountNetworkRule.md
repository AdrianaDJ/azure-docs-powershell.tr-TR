---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 2faf890cda0c87d15704a14f9c4ae12c5b3d81c2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323950"
---
# <span data-ttu-id="942cd-101">Remove-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="942cd-101">Remove-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="942cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="942cd-102">SYNOPSIS</span></span>
<span data-ttu-id="942cd-103">Bir öğretici hizmet hesabının NetWorkRule özelliğinden ıprules veya VirtualNetworkRules 'ı kaldırın</span><span class="sxs-lookup"><span data-stu-id="942cd-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="942cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="942cd-104">SYNTAX</span></span>

### <span data-ttu-id="942cd-105">NetWorkRuleString (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="942cd-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="942cd-106">Ipruleobject</span><span class="sxs-lookup"><span data-stu-id="942cd-106">IpRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpRule <PSIpRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="942cd-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="942cd-107">NetworkRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="942cd-108">Iprulestring</span><span class="sxs-lookup"><span data-stu-id="942cd-108">IpRuleString</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="942cd-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="942cd-109">DESCRIPTION</span></span>
<span data-ttu-id="942cd-110">**Remove-azbir ınitialveservicesaccountnetworkrule** cmdlet 'i, bir öğretici hizmet hesabının networkrule özelliğinden ıprules veya virtualnetworkrules öğesini kaldırıyor</span><span class="sxs-lookup"><span data-stu-id="942cd-110">The **Remove-AzCognitiveServicesAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="942cd-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="942cd-111">EXAMPLES</span></span>

### <span data-ttu-id="942cd-112">Örnek 1: ıpaddressorrange ile birkaç Ipkuralı kaldırın</span><span class="sxs-lookup"><span data-stu-id="942cd-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="942cd-113">Bu komut, ıpaddressorrange ile birkaç Ipkuralı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="942cd-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="942cd-114">Örnek 2: JSON ile VirtualNetworkRule nesne girişiyle VirtualNetworkRule öğesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="942cd-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"})
```

<span data-ttu-id="942cd-115">Bu komut, JSON ile VirtualNetworkRule nesne girişiyle VirtualNetworkRule öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="942cd-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="942cd-116">Örnek 3: birinci ıprule 'i ardışık düzene çıkarma</span><span class="sxs-lookup"><span data-stu-id="942cd-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount").IpRules[0] | Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="942cd-117">Bu komut ilk ıprule 'i ardışık düzene çıkarın.</span><span class="sxs-lookup"><span data-stu-id="942cd-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="942cd-118">Örnek 4: Virtualnetworkresourceıd ile birkaç VirtualNetworkRules 'ı kaldırma</span><span class="sxs-lookup"><span data-stu-id="942cd-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="942cd-119">Bu komut Virtualnetworkresourceıd ile birkaç VirtualNetworkRules 'ı kaldırın.</span><span class="sxs-lookup"><span data-stu-id="942cd-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span> 

## <span data-ttu-id="942cd-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="942cd-120">PARAMETERS</span></span>

### <span data-ttu-id="942cd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="942cd-121">-DefaultProfile</span></span>
<span data-ttu-id="942cd-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="942cd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="942cd-123">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="942cd-123">-IpAddressOrRange</span></span>
<span data-ttu-id="942cd-124">Öğrenme Hizmetleri hesap NetworkRule ıprules, String 'teki.</span><span class="sxs-lookup"><span data-stu-id="942cd-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="942cd-125">-Iprule</span><span class="sxs-lookup"><span data-stu-id="942cd-125">-IpRule</span></span>
<span data-ttu-id="942cd-126">Öğrenme Hizmetleri hesap NetworkRule ıprules.</span><span class="sxs-lookup"><span data-stu-id="942cd-126">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="942cd-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="942cd-127">-Name</span></span>
<span data-ttu-id="942cd-128">Öğretici hizmetler hesap adı.</span><span class="sxs-lookup"><span data-stu-id="942cd-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="942cd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="942cd-129">-ResourceGroupName</span></span>
<span data-ttu-id="942cd-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="942cd-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="942cd-131">-Virtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="942cd-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="942cd-132">Öğrenme Hizmetleri hesap NetworkRule Virtualnetworkrule Virtualnetworkresourceıd ın String.</span><span class="sxs-lookup"><span data-stu-id="942cd-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="942cd-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="942cd-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="942cd-134">Öğretici Hizmetler hesabı NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="942cd-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="942cd-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="942cd-135">-Confirm</span></span>
<span data-ttu-id="942cd-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="942cd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="942cd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="942cd-137">-WhatIf</span></span>
<span data-ttu-id="942cd-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="942cd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="942cd-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="942cd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="942cd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="942cd-140">CommonParameters</span></span>
<span data-ttu-id="942cd-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="942cd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="942cd-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="942cd-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="942cd-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="942cd-143">INPUTS</span></span>

### <span data-ttu-id="942cd-144">System. String</span><span class="sxs-lookup"><span data-stu-id="942cd-144">System.String</span></span>

### <span data-ttu-id="942cd-145">Microsoft. Azure. Commands. Management. öğretici Bveservices. modeller. Psıprule []</span><span class="sxs-lookup"><span data-stu-id="942cd-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="942cd-146">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="942cd-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="942cd-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="942cd-147">OUTPUTS</span></span>

### <span data-ttu-id="942cd-148">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="942cd-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="942cd-149">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psıprule</span><span class="sxs-lookup"><span data-stu-id="942cd-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="942cd-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="942cd-150">NOTES</span></span>

## <span data-ttu-id="942cd-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="942cd-151">RELATED LINKS</span></span>
