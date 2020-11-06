---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: cc9a79b424d6ad81804aaed0d941ca017463abba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591348"
---
# <span data-ttu-id="47092-101">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47092-101">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="47092-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47092-102">SYNOPSIS</span></span>
<span data-ttu-id="47092-103">Bir yük dengeleyiciden giden kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="47092-103">Removes an outbound rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47092-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47092-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47092-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="47092-105">DESCRIPTION</span></span>
<span data-ttu-id="47092-106">**Remove-AzureRmLoadBalancerOutboundRuleConfig** cmdlet 'i, bir Azure yük dengeleyiciden giden kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="47092-106">The **Remove-AzureRmLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="47092-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47092-107">EXAMPLES</span></span>

### <span data-ttu-id="47092-108">Örnek 1: Azure yük dengeleyiciden giden kuralı silme</span><span class="sxs-lookup"><span data-stu-id="47092-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzureRmLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzureRmLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="47092-109">İlk komut, kaldırmak istediğiniz giden kuralı yapılandırmasıyla ilişkili yük dengeleyiciden alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="47092-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="47092-110">İkinci komut, yük dengeleyiciden ilişkili giden kuralı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="47092-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="47092-111">Üçüncü komut yük dengeleyiciden günceller.</span><span class="sxs-lookup"><span data-stu-id="47092-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="47092-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47092-112">PARAMETERS</span></span>

### <span data-ttu-id="47092-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47092-113">-DefaultProfile</span></span>
<span data-ttu-id="47092-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47092-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47092-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="47092-115">-LoadBalancer</span></span>
<span data-ttu-id="47092-116">Yük dengeleyici kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="47092-116">The reference of the load balancer resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47092-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="47092-117">-Name</span></span>
<span data-ttu-id="47092-118">Giden kuralının adı</span><span class="sxs-lookup"><span data-stu-id="47092-118">The Name of outbound rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47092-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="47092-119">-Confirm</span></span>
<span data-ttu-id="47092-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47092-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47092-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47092-121">-WhatIf</span></span>
<span data-ttu-id="47092-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47092-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47092-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47092-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47092-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47092-124">CommonParameters</span></span>
<span data-ttu-id="47092-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47092-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47092-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47092-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47092-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47092-127">INPUTS</span></span>

### <span data-ttu-id="47092-128">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="47092-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="47092-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47092-129">OUTPUTS</span></span>

### <span data-ttu-id="47092-130">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="47092-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="47092-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47092-131">NOTES</span></span>

## <span data-ttu-id="47092-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47092-132">RELATED LINKS</span></span>
