---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
ms.openlocfilehash: 00213d4829d4b389f19a01ad9748517608657136
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937528"
---
# <span data-ttu-id="ac3fa-101">Remove-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="ac3fa-101">Remove-AzEventHubIPRule</span></span>

## <span data-ttu-id="ac3fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac3fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ac3fa-103">Verilen ad alanının NetworkRuleSet öğesine tek bir IP kuralı kaldırma</span><span class="sxs-lookup"><span data-stu-id="ac3fa-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="ac3fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ac3fa-104">SYNTAX</span></span>

### <span data-ttu-id="ac3fa-105">Iprulepropertiesparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ac3fa-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac3fa-106">Ipruleinputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="ac3fa-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac3fa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac3fa-107">DESCRIPTION</span></span>
<span data-ttu-id="ac3fa-108">Verilen ad alanının NetworkRuleSet öğesine tek bir IP kuralı kaldırma</span><span class="sxs-lookup"><span data-stu-id="ac3fa-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="ac3fa-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ac3fa-109">EXAMPLES</span></span>

### <span data-ttu-id="ac3fa-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ac3fa-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="ac3fa-111">Verilen ad alanının NetworkRuleSet 'in IPMask öğesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="ac3fa-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="ac3fa-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ac3fa-112">PARAMETERS</span></span>

### <span data-ttu-id="ac3fa-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="ac3fa-113">-AsJob</span></span>
<span data-ttu-id="ac3fa-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ac3fa-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac3fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac3fa-115">-DefaultProfile</span></span>
<span data-ttu-id="ac3fa-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ac3fa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac3fa-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="ac3fa-117">-IpMask</span></span>
<span data-ttu-id="ac3fa-118">Alt ağ kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="ac3fa-118">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac3fa-119">-Ipruleobject</span><span class="sxs-lookup"><span data-stu-id="ac3fa-119">-IpRuleObject</span></span>
<span data-ttu-id="ac3fa-120">Iprule yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="ac3fa-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac3fa-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ac3fa-121">-Name</span></span>
<span data-ttu-id="ac3fa-122">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="ac3fa-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac3fa-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ac3fa-123">-PassThru</span></span>
<span data-ttu-id="ac3fa-124">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="ac3fa-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ac3fa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac3fa-125">-ResourceGroupName</span></span>
<span data-ttu-id="ac3fa-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ac3fa-126">Resource Group Name</span></span>

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

### <span data-ttu-id="ac3fa-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="ac3fa-127">-Confirm</span></span>
<span data-ttu-id="ac3fa-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ac3fa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac3fa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac3fa-129">-WhatIf</span></span>
<span data-ttu-id="ac3fa-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac3fa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac3fa-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ac3fa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac3fa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac3fa-132">CommonParameters</span></span>
<span data-ttu-id="ac3fa-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ac3fa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ac3fa-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac3fa-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac3fa-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ac3fa-135">INPUTS</span></span>

### <span data-ttu-id="ac3fa-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ac3fa-136">System.String</span></span>

### <span data-ttu-id="ac3fa-137">Microsoft. Azure. Commands. EventHub. model. Psnwrulesetıprulesattributes</span><span class="sxs-lookup"><span data-stu-id="ac3fa-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="ac3fa-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ac3fa-138">OUTPUTS</span></span>

### <span data-ttu-id="ac3fa-139">Microsoft. Azure. Commands. EventHub. model. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="ac3fa-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="ac3fa-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ac3fa-140">NOTES</span></span>

## <span data-ttu-id="ac3fa-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ac3fa-141">RELATED LINKS</span></span>