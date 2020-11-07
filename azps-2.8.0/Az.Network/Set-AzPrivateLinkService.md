---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: 4401ae153fc237d1f1bc9ccfa870e5cecc1e2c33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932756"
---
# <span data-ttu-id="fc0e1-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fc0e1-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="fc0e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc0e1-102">SYNOPSIS</span></span>
<span data-ttu-id="fc0e1-103">Özel bir bağlantı hizmetini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-103">Updates a private link service.</span></span>

## <span data-ttu-id="fc0e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc0e1-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc0e1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc0e1-105">DESCRIPTION</span></span>
<span data-ttu-id="fc0e1-106">**Set-AzPrivateLinkService** cmdlet 'i özel bir bağlantı hizmetini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="fc0e1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc0e1-107">EXAMPLES</span></span>

### <span data-ttu-id="fc0e1-108">1: özel bir bağlantı hizmeti oluşturur ve</span><span class="sxs-lookup"><span data-stu-id="fc0e1-108">1: Creates a private link service and update its</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
$privateLinkService = New-AzPrivateLinkService -ServiceName "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig

$newIPConfig = New-AzPrivateLinkServiceIpConfig -Name "New-IP-Config" -Subnet $vnet.subnets[0] 
$privateLinkService.IpConfigurations[0] = $newIPConfig
$privateLinkService | Set-AzPrivateLinkService
```

<span data-ttu-id="fc0e1-109">Bu örnek, mypls.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="fc0e1-110">Ardından onun IP yapılandırmalarını bellek içi ıpconfiguratiuon nesnesinden değiştirin.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="fc0e1-111">Ardından, hizmet tarafında değiştirilmiş özel bağlantı hizmeti durumunu yazmak için Set-AzPrivateLinkService cmdlet 'i kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="fc0e1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc0e1-112">PARAMETERS</span></span>

### <span data-ttu-id="fc0e1-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="fc0e1-113">-AsJob</span></span>
<span data-ttu-id="fc0e1-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fc0e1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc0e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc0e1-115">-DefaultProfile</span></span>
<span data-ttu-id="fc0e1-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc0e1-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fc0e1-117">-PrivateLinkService</span></span>
<span data-ttu-id="fc0e1-118">Özel bağlantı hizmetinin ayarlanması gereken durumu temsil eden bir özel bağlantı hizmeti nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0e1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc0e1-119">CommonParameters</span></span>
<span data-ttu-id="fc0e1-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc0e1-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc0e1-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc0e1-122">INPUTS</span></span>

### <span data-ttu-id="fc0e1-123">Microsoft. Azure. Commands. Network. model. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fc0e1-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="fc0e1-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc0e1-124">OUTPUTS</span></span>

### <span data-ttu-id="fc0e1-125">Microsoft. Azure. Commands. Network. model. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fc0e1-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="fc0e1-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc0e1-126">NOTES</span></span>

## <span data-ttu-id="fc0e1-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc0e1-127">RELATED LINKS</span></span>

[<span data-ttu-id="fc0e1-128">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fc0e1-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="fc0e1-129">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fc0e1-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="fc0e1-130">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fc0e1-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)


