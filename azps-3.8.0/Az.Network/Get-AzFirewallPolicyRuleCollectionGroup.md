---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8ce5369605f419821994c771dc9200e138e5ad7a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098822"
---
# <span data-ttu-id="614e8-101">Get-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="614e8-101">Get-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="614e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="614e8-102">SYNOPSIS</span></span>
<span data-ttu-id="614e8-103">Azure Güvenlik Duvarı Ilkesi kuralı koleksiyon grubunu alır</span><span class="sxs-lookup"><span data-stu-id="614e8-103">Gets a Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="614e8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="614e8-104">SYNTAX</span></span>

### <span data-ttu-id="614e8-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="614e8-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="614e8-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="614e8-106">GetByInputObjectParameterSet</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -Name <String> -AzureFirewallPolicy <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="614e8-107">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="614e8-107">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="614e8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="614e8-108">DESCRIPTION</span></span>
<span data-ttu-id="614e8-109">**Get-AzFirewallPolicyRuleCollectionGroup** cmdlet 'i, bir güvenlik duvarı Ilkesinden belirtilen rulecollectiongroup öğesini alır</span><span class="sxs-lookup"><span data-stu-id="614e8-109">The **Get-AzFirewallPolicyRuleCollectionGroup** cmdlet gets the RuleCollectionGroup mentioned from a Firewall Policy</span></span>

## <span data-ttu-id="614e8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="614e8-110">EXAMPLES</span></span>

### <span data-ttu-id="614e8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="614e8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicyRuleCollectionGroup -Name rg1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="614e8-112">Bu örnekte, $fp</span><span class="sxs-lookup"><span data-stu-id="614e8-112">This example get the rule collectionGroup in the firewall policy $fp</span></span>

## <span data-ttu-id="614e8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="614e8-113">PARAMETERS</span></span>

### <span data-ttu-id="614e8-114">-AzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="614e8-114">-AzureFirewallPolicy</span></span>
<span data-ttu-id="614e8-115">Güvenlik Duvarı Ilkesi.</span><span class="sxs-lookup"><span data-stu-id="614e8-115">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="614e8-116">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="614e8-116">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="614e8-117">Güvenlik Duvarı ilke adı</span><span class="sxs-lookup"><span data-stu-id="614e8-117">The Firewall policy name</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="614e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="614e8-118">-DefaultProfile</span></span>
<span data-ttu-id="614e8-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="614e8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="614e8-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="614e8-120">-Name</span></span>
<span data-ttu-id="614e8-121">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="614e8-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="614e8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="614e8-122">-ResourceGroupName</span></span>
<span data-ttu-id="614e8-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="614e8-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="614e8-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="614e8-124">-ResourceId</span></span>
<span data-ttu-id="614e8-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="614e8-125">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="614e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="614e8-126">CommonParameters</span></span>
<span data-ttu-id="614e8-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="614e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="614e8-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="614e8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="614e8-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="614e8-129">INPUTS</span></span>

### <span data-ttu-id="614e8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="614e8-130">System.String</span></span>

### <span data-ttu-id="614e8-131">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="614e8-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="614e8-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="614e8-132">OUTPUTS</span></span>

### <span data-ttu-id="614e8-133">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="614e8-133">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="614e8-134">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall, Microsoft. Azure. PowerShell. cmdlet. Network, Version = 1.12.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="614e8-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="614e8-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="614e8-135">NOTES</span></span>

## <span data-ttu-id="614e8-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="614e8-136">RELATED LINKS</span></span>
