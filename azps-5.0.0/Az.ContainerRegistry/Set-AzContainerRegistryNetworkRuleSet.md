---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/set-azcontainerregistrynetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
ms.openlocfilehash: 4a2292b0b573a5357466f3b240ba3b6df7cf0a1e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275578"
---
# <span data-ttu-id="ac5c1-101">Set-AzContainerRegistryNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac5c1-101">Set-AzContainerRegistryNetworkRuleSet</span></span>

## <span data-ttu-id="ac5c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac5c1-102">SYNOPSIS</span></span>
<span data-ttu-id="ac5c1-103">Ağ kural kümesi oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="ac5c1-103">Create or update a network rule set.</span></span> <span data-ttu-id="ac5c1-104">Kural kümesi yalnızca "Premium" kayıt defterine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="ac5c1-104">Rule set can only be applied to "Premium" registry.</span></span>

## <span data-ttu-id="ac5c1-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ac5c1-105">SYNTAX</span></span>

### <span data-ttu-id="ac5c1-106">AddAddNetworkRuleWithoutInputObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ac5c1-106">AddAddNetworkRuleWithoutInputObject (Default)</span></span>
```
Set-AzContainerRegistryNetworkRuleSet -DefaultAction <String> [-NetworkRule <IPSNetworkRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac5c1-107">AddNetworkRuleWithInputObject</span><span class="sxs-lookup"><span data-stu-id="ac5c1-107">AddNetworkRuleWithInputObject</span></span>
```
Set-AzContainerRegistryNetworkRuleSet [-DefaultAction <String>] [-NetworkRule <IPSNetworkRule[]>]
 -InputObject <PSNetworkRuleSet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac5c1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac5c1-108">DESCRIPTION</span></span>
<span data-ttu-id="ac5c1-109">Ağ kural kümesi oluşturma veya güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ac5c1-109">Create or update a network rule set</span></span>

## <span data-ttu-id="ac5c1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ac5c1-110">EXAMPLES</span></span>

### <span data-ttu-id="ac5c1-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ac5c1-111">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
PS C:\> $set = Set-AzContainerRegistryNetworkRuleSet -DefaultAction "Allow" -NetworkRule $rule
```

<span data-ttu-id="ac5c1-112">Yeni bir ağ kuralı kümesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ac5c1-112">Create a new network rule set.</span></span>

## <span data-ttu-id="ac5c1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ac5c1-113">PARAMETERS</span></span>

### <span data-ttu-id="ac5c1-114">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="ac5c1-114">-DefaultAction</span></span>
<span data-ttu-id="ac5c1-115">Varsayılan eylem ' Izin ver ' veya ' Reddet ' olabilir</span><span class="sxs-lookup"><span data-stu-id="ac5c1-115">Default action, could be 'Allow' or 'Deny'</span></span>

```yaml
Type: System.String
Parameter Sets: AddAddNetworkRuleWithoutInputObject
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac5c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac5c1-116">-DefaultProfile</span></span>
<span data-ttu-id="ac5c1-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ac5c1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac5c1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac5c1-118">-InputObject</span></span>
<span data-ttu-id="ac5c1-119">Giriş PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac5c1-119">Input PSNetworkRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac5c1-120">-NetworkRule</span><span class="sxs-lookup"><span data-stu-id="ac5c1-120">-NetworkRule</span></span>
<span data-ttu-id="ac5c1-121">Ağ kuralları listesi</span><span class="sxs-lookup"><span data-stu-id="ac5c1-121">List of Network rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac5c1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac5c1-122">CommonParameters</span></span>
<span data-ttu-id="ac5c1-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ac5c1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac5c1-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ac5c1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac5c1-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ac5c1-125">INPUTS</span></span>

### <span data-ttu-id="ac5c1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ac5c1-126">System.String</span></span>

### <span data-ttu-id="ac5c1-127">Microsoft. Azure. Commands. ContainerRegistry. model. IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ac5c1-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="ac5c1-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ac5c1-128">OUTPUTS</span></span>

### <span data-ttu-id="ac5c1-129">Microsoft. Azure. Commands. ContainerRegistry. modeller. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac5c1-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="ac5c1-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ac5c1-130">NOTES</span></span>

## <span data-ttu-id="ac5c1-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ac5c1-131">RELATED LINKS</span></span>
