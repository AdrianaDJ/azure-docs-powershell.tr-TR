---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: b9782d56fb18f0f00c52e9ff37ef0d62a609f980
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935299"
---
# <span data-ttu-id="aca1c-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="aca1c-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="aca1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aca1c-102">SYNOPSIS</span></span>
<span data-ttu-id="aca1c-103">Bir yük dengeleyiciden ön uç IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="aca1c-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="aca1c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aca1c-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aca1c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aca1c-105">DESCRIPTION</span></span>
<span data-ttu-id="aca1c-106">**Remove-Azloadbalancerfrontendıconfıg** cmdlet 'i, bir Azure yük dengeleyiciden ön uç IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="aca1c-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="aca1c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aca1c-107">EXAMPLES</span></span>

### <span data-ttu-id="aca1c-108">Örnek 1: yük dengeleyiciden ön uç IP yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="aca1c-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="aca1c-109">İlk komut, kaldırmak istediğiniz ön uç IP yapılandırmasıyla ilişkili yük dengeleyicın alır ve $loadbalancer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="aca1c-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="aca1c-110">İkinci komut $loadbalancer ' da yük dengeleyiciden ilişkili ön uç IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="aca1c-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="aca1c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aca1c-111">PARAMETERS</span></span>

### <span data-ttu-id="aca1c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aca1c-112">-DefaultProfile</span></span>
<span data-ttu-id="aca1c-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aca1c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aca1c-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aca1c-114">-LoadBalancer</span></span>
<span data-ttu-id="aca1c-115">Kaldırılacak ön uç IP yapılandırmasını içeren yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="aca1c-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aca1c-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="aca1c-116">-Name</span></span>
<span data-ttu-id="aca1c-117">Kaldırılacak ön uç IP adresi yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aca1c-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aca1c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aca1c-118">CommonParameters</span></span>
<span data-ttu-id="aca1c-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aca1c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aca1c-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aca1c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aca1c-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aca1c-121">INPUTS</span></span>

### <span data-ttu-id="aca1c-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aca1c-122">PSLoadBalancer</span></span>
<span data-ttu-id="aca1c-123">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="aca1c-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="aca1c-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aca1c-124">OUTPUTS</span></span>

### <span data-ttu-id="aca1c-125">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aca1c-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="aca1c-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aca1c-126">NOTES</span></span>

## <span data-ttu-id="aca1c-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aca1c-127">RELATED LINKS</span></span>

[<span data-ttu-id="aca1c-128">Add-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="aca1c-128">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="aca1c-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aca1c-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="aca1c-130">Get-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="aca1c-130">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="aca1c-131">Yeni-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="aca1c-131">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="aca1c-132">Set-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="aca1c-132">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


