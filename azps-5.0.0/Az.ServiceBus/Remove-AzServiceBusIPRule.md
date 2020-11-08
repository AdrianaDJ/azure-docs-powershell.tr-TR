---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: 90c832d36017aa02a05d972a7b6e26fffd93937e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278170"
---
# <span data-ttu-id="6f8d1-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="6f8d1-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="6f8d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f8d1-102">SYNOPSIS</span></span>
<span data-ttu-id="6f8d1-103">Verilen ad alanının NetworkRuleSet öğesine tek bir IP kuralı kaldırma</span><span class="sxs-lookup"><span data-stu-id="6f8d1-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="6f8d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f8d1-104">SYNTAX</span></span>

### <span data-ttu-id="6f8d1-105">Iprulepropertiesparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6f8d1-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f8d1-106">Ipruleinputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="6f8d1-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f8d1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f8d1-107">DESCRIPTION</span></span>
<span data-ttu-id="6f8d1-108">Verilen ad alanının NetworkRuleSet öğesine tek bir IP kuralı kaldırma</span><span class="sxs-lookup"><span data-stu-id="6f8d1-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="6f8d1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f8d1-109">EXAMPLES</span></span>

### <span data-ttu-id="6f8d1-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6f8d1-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="6f8d1-111">Verilen ad alanının NetworkRuleSet 'in IPMask öğesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="6f8d1-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="6f8d1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f8d1-112">PARAMETERS</span></span>

### <span data-ttu-id="6f8d1-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="6f8d1-113">-AsJob</span></span>
<span data-ttu-id="6f8d1-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6f8d1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f8d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f8d1-115">-DefaultProfile</span></span>
<span data-ttu-id="6f8d1-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6f8d1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f8d1-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="6f8d1-117">-IpMask</span></span>
<span data-ttu-id="6f8d1-118">Alt ağ kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="6f8d1-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="6f8d1-119">-Ipruleobject</span><span class="sxs-lookup"><span data-stu-id="6f8d1-119">-IpRuleObject</span></span>
<span data-ttu-id="6f8d1-120">Iprule yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="6f8d1-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f8d1-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="6f8d1-121">-Name</span></span>
<span data-ttu-id="6f8d1-122">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="6f8d1-122">Namespace Name</span></span>

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

### <span data-ttu-id="6f8d1-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6f8d1-123">-PassThru</span></span>
<span data-ttu-id="6f8d1-124">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="6f8d1-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6f8d1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f8d1-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f8d1-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6f8d1-126">Resource Group Name</span></span>

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

### <span data-ttu-id="6f8d1-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="6f8d1-127">-Confirm</span></span>
<span data-ttu-id="6f8d1-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6f8d1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f8d1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f8d1-129">-WhatIf</span></span>
<span data-ttu-id="6f8d1-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6f8d1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f8d1-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6f8d1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f8d1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f8d1-132">CommonParameters</span></span>
<span data-ttu-id="6f8d1-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f8d1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6f8d1-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f8d1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f8d1-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f8d1-135">INPUTS</span></span>

### <span data-ttu-id="6f8d1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6f8d1-136">System.String</span></span>

### <span data-ttu-id="6f8d1-137">Microsoft. Azure. Commands. ServiceBus. modeller. Psnwrulesetıprulesattributes</span><span class="sxs-lookup"><span data-stu-id="6f8d1-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="6f8d1-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f8d1-138">OUTPUTS</span></span>

### <span data-ttu-id="6f8d1-139">Microsoft. Azure. Commands. ServiceBus. modeller. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="6f8d1-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="6f8d1-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f8d1-140">NOTES</span></span>

## <span data-ttu-id="6f8d1-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f8d1-141">RELATED LINKS</span></span>
