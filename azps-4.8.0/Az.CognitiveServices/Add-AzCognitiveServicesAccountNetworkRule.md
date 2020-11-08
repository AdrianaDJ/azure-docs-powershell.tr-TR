---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/add-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 039a3e4bf676f29d55f48e7e0883f5818e7367b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110044"
---
# <span data-ttu-id="9dbca-101">Add-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9dbca-101">Add-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="9dbca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dbca-102">SYNOPSIS</span></span>
<span data-ttu-id="9dbca-103">Bir öğretici hizmet hesabının NetworkRule özelliğine ıprules veya VirtualNetworkRules ekleme</span><span class="sxs-lookup"><span data-stu-id="9dbca-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="9dbca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9dbca-104">SYNTAX</span></span>

### <span data-ttu-id="9dbca-105">NetWorkRuleString (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9dbca-105">NetWorkRuleString (Default)</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9dbca-106">Ipruleobject</span><span class="sxs-lookup"><span data-stu-id="9dbca-106">IpRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IpRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dbca-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="9dbca-107">NetworkRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9dbca-108">Iprulestring</span><span class="sxs-lookup"><span data-stu-id="9dbca-108">IpRuleString</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9dbca-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="9dbca-109">DESCRIPTION</span></span>
<span data-ttu-id="9dbca-110">**Add-Azöğretici Iveservicesaccountnetworkrule** cmdlet 'i, bir öğretici hizmet hesabının networkrule özelliğine ıprules veya virtualnetworkrules ekler</span><span class="sxs-lookup"><span data-stu-id="9dbca-110">The **Add-AzCognitiveServicesAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="9dbca-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9dbca-111">EXAMPLES</span></span>

### <span data-ttu-id="9dbca-112">Örnek 1: ıpaddressorrange ile birkaç IpRules ekleme</span><span class="sxs-lookup"><span data-stu-id="9dbca-112">Example 1: Add several IpRules with IpAddressOrRange</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "200.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="9dbca-113">Bu komut, ıpaddressorrange ile birkaç ıprules ekler.</span><span class="sxs-lookup"><span data-stu-id="9dbca-113">This command add several IpRules with IpAddressOrRange.</span></span>

### <span data-ttu-id="9dbca-114">Örnek 2: Virtualnetworkresourceıd ile VirtualNetworkRule ekleme</span><span class="sxs-lookup"><span data-stu-id="9dbca-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="9dbca-115">Bu komut Virtualnetworkresourceıd ile VirtualNetworkRule öğesini ekler.</span><span class="sxs-lookup"><span data-stu-id="9dbca-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="9dbca-116">Örnek 3: başka bir hesaptan VirtualNetworkRule nesneleriyle VirtualNetworkRules ekleme</span><span class="sxs-lookup"><span data-stu-id="9dbca-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount1"
PS C:\> Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="9dbca-117">Bu komut, başka bir hesaptan VirtualNetworkRule nesneleriyle VirtualNetworkRules öğesini ekler.</span><span class="sxs-lookup"><span data-stu-id="9dbca-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="9dbca-118">Örnek 4: ıprule nesneleri olan birkaç ıprule ekleme, JSON ile giriş</span><span class="sxs-lookup"><span data-stu-id="9dbca-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
```

<span data-ttu-id="9dbca-119">Bu komut, ıprule nesneleri</span><span class="sxs-lookup"><span data-stu-id="9dbca-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="9dbca-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9dbca-120">PARAMETERS</span></span>

### <span data-ttu-id="9dbca-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dbca-121">-DefaultProfile</span></span>
<span data-ttu-id="9dbca-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9dbca-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dbca-123">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="9dbca-123">-IpAddressOrRange</span></span>
<span data-ttu-id="9dbca-124">Öğrenme Hizmetleri hesap NetworkRule ıprules, String 'teki.</span><span class="sxs-lookup"><span data-stu-id="9dbca-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="9dbca-125">-Iprule</span><span class="sxs-lookup"><span data-stu-id="9dbca-125">-IpRule</span></span>
<span data-ttu-id="9dbca-126">Öğrenme Hizmetleri hesap NetworkRule ıprules.</span><span class="sxs-lookup"><span data-stu-id="9dbca-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="9dbca-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="9dbca-127">-Name</span></span>
<span data-ttu-id="9dbca-128">Öğretici hizmetler hesap adı.</span><span class="sxs-lookup"><span data-stu-id="9dbca-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="9dbca-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dbca-129">-ResourceGroupName</span></span>
<span data-ttu-id="9dbca-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9dbca-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="9dbca-131">-Virtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="9dbca-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="9dbca-132">Öğrenme Hizmetleri hesap NetworkRule Virtualnetworkrule Virtualnetworkresourceıd ın String.</span><span class="sxs-lookup"><span data-stu-id="9dbca-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="9dbca-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9dbca-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="9dbca-134">Öğretici Hizmetler hesabı NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="9dbca-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="9dbca-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="9dbca-135">-Confirm</span></span>
<span data-ttu-id="9dbca-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9dbca-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dbca-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dbca-137">-WhatIf</span></span>
<span data-ttu-id="9dbca-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9dbca-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dbca-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9dbca-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dbca-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dbca-140">CommonParameters</span></span>
<span data-ttu-id="9dbca-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9dbca-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dbca-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9dbca-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dbca-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9dbca-143">INPUTS</span></span>

### <span data-ttu-id="9dbca-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9dbca-144">System.String</span></span>

### <span data-ttu-id="9dbca-145">Microsoft. Azure. Commands. Management. öğretici Bveservices. modeller. Psıprule []</span><span class="sxs-lookup"><span data-stu-id="9dbca-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="9dbca-146">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="9dbca-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="9dbca-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9dbca-147">OUTPUTS</span></span>

### <span data-ttu-id="9dbca-148">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9dbca-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="9dbca-149">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psıprule</span><span class="sxs-lookup"><span data-stu-id="9dbca-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="9dbca-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9dbca-150">NOTES</span></span>

## <span data-ttu-id="9dbca-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9dbca-151">RELATED LINKS</span></span>
