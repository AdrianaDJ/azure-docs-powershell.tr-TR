---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 1a71b48387948d65ba0db24fdb2c236a11a9a44d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594850"
---
# <span data-ttu-id="968d5-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="968d5-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="968d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="968d5-102">SYNOPSIS</span></span>
<span data-ttu-id="968d5-103">Bir yük dengeleyiciden ön uç IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="968d5-103">Removes a front-end IP configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="968d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="968d5-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="968d5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="968d5-105">DESCRIPTION</span></span>
<span data-ttu-id="968d5-106">**Remove-Azurermloadbalancerfrontendıcaconfig** cmdlet 'i, bir Azure yük dengeleyiciden ön uç IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="968d5-106">The **Remove-AzureRmLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="968d5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="968d5-107">EXAMPLES</span></span>

### <span data-ttu-id="968d5-108">Örnek 1: yük dengeleyiciden ön uç IP yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="968d5-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="968d5-109">İlk komut, kaldırmak istediğiniz ön uç IP yapılandırmasıyla ilişkili yük dengeleyicın alır ve $loadbalancer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="968d5-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="968d5-110">İkinci komut $loadbalancer ' da yük dengeleyiciden ilişkili ön uç IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="968d5-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="968d5-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="968d5-111">PARAMETERS</span></span>

### <span data-ttu-id="968d5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="968d5-112">-DefaultProfile</span></span>
<span data-ttu-id="968d5-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="968d5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="968d5-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="968d5-114">-LoadBalancer</span></span>
<span data-ttu-id="968d5-115">Kaldırılacak ön uç IP yapılandırmasını içeren yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="968d5-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="968d5-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="968d5-116">-Name</span></span>
<span data-ttu-id="968d5-117">Kaldırılacak ön uç IP adresi yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="968d5-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="968d5-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="968d5-118">-Confirm</span></span>
<span data-ttu-id="968d5-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="968d5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="968d5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="968d5-120">-WhatIf</span></span>
<span data-ttu-id="968d5-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="968d5-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="968d5-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="968d5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="968d5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="968d5-123">CommonParameters</span></span>
<span data-ttu-id="968d5-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="968d5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="968d5-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="968d5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="968d5-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="968d5-126">INPUTS</span></span>

### <span data-ttu-id="968d5-127">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="968d5-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="968d5-128">Parametreler: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="968d5-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="968d5-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="968d5-129">OUTPUTS</span></span>

### <span data-ttu-id="968d5-130">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="968d5-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="968d5-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="968d5-131">NOTES</span></span>

## <span data-ttu-id="968d5-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="968d5-132">RELATED LINKS</span></span>

[<span data-ttu-id="968d5-133">Add-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="968d5-133">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="968d5-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="968d5-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="968d5-135">Get-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="968d5-135">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="968d5-136">Yeni-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="968d5-136">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="968d5-137">Set-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="968d5-137">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


