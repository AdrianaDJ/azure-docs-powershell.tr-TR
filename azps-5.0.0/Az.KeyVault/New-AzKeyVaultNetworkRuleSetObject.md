---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultnetworkrulesetobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
ms.openlocfilehash: 318d5915e07ac55430dbe8e1788d862673dc5998
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280212"
---
# <span data-ttu-id="13089-101">New-AzKeyVaultNetworkRuleSetObject</span><span class="sxs-lookup"><span data-stu-id="13089-101">New-AzKeyVaultNetworkRuleSetObject</span></span>

## <span data-ttu-id="13089-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13089-102">SYNOPSIS</span></span>
<span data-ttu-id="13089-103">Ağ kuralı ayarlarını temsil eden bir nesne oluşturun.</span><span class="sxs-lookup"><span data-stu-id="13089-103">Create an object representing the network rule settings.</span></span>

## <span data-ttu-id="13089-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="13089-104">SYNTAX</span></span>

```
New-AzKeyVaultNetworkRuleSetObject [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>]
 [-Bypass <PSKeyVaultNetworkRuleBypassEnum>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13089-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="13089-105">DESCRIPTION</span></span>
<span data-ttu-id="13089-106">Kasa oluştururken kullanılabilecek ağ kuralı ayarlarını temsil eden bir nesne oluşturun.</span><span class="sxs-lookup"><span data-stu-id="13089-106">Create an object representing the network rule settings that can be used when creating a vault.</span></span>

## <span data-ttu-id="13089-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="13089-107">EXAMPLES</span></span>

### <span data-ttu-id="13089-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="13089-108">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="13089-109">Yeni bir kasa oluşturun ve $myNetworkResId ile belirtilen sanal ağdan belirtilen IP adresine erişim izni vermek için ağ kurallarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="13089-109">Creating a new vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="13089-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="13089-110">PARAMETERS</span></span>

### <span data-ttu-id="13089-111">-Bypass</span><span class="sxs-lookup"><span data-stu-id="13089-111">-Bypass</span></span>
<span data-ttu-id="13089-112">Ağ kuralının atlanmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="13089-112">Specifies bypass of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13089-113">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="13089-113">-DefaultAction</span></span>
<span data-ttu-id="13089-114">Ağ kuralının varsayılan eylemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="13089-114">Specifies default action of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13089-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13089-115">-DefaultProfile</span></span>
<span data-ttu-id="13089-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="13089-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13089-117">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="13089-117">-IpAddressRange</span></span>
<span data-ttu-id="13089-118">Ağ kuralının ağ adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="13089-118">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13089-119">-Virtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="13089-119">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="13089-120">Ağ kuralının sanal ağ kaynağı tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="13089-120">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13089-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13089-121">CommonParameters</span></span>
<span data-ttu-id="13089-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="13089-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13089-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="13089-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13089-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="13089-124">INPUTS</span></span>

### <span data-ttu-id="13089-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="13089-125">None</span></span>

## <span data-ttu-id="13089-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="13089-126">OUTPUTS</span></span>

### <span data-ttu-id="13089-127">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="13089-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="13089-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="13089-128">NOTES</span></span>

## <span data-ttu-id="13089-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="13089-129">RELATED LINKS</span></span>
