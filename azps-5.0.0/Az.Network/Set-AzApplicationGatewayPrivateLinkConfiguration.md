---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 78af871cf476ee80c57e22e2469b48bb4d4337a1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325228"
---
# <span data-ttu-id="da841-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="da841-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="da841-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da841-102">SYNOPSIS</span></span>
<span data-ttu-id="da841-103">Bir uygulama ağ geçidi için PrivateLink yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="da841-103">Modifies an PrivateLink Configuration for an application gateway.</span></span>

## <span data-ttu-id="da841-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="da841-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da841-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="da841-105">DESCRIPTION</span></span>
<span data-ttu-id="da841-106">**Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet 'i, bir Azure uygulama ağ geçidi Için Privatelink yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="da841-106">The **Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet modifies an privateLink configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="da841-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="da841-107">EXAMPLES</span></span>

### <span data-ttu-id="da841-108">Örnek 1: PrivateLink yapılandırması ayarlama</span><span class="sxs-lookup"><span data-stu-id="da841-108">Example 1: Set a PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration01
```

<span data-ttu-id="da841-109">İlk komut, ApplicationGateway01 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="da841-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="da841-110">İkinci komut, ad privateLinkConfig01 ile privateLink yapılandırmasını ayarlar 01 ' $privateLinkIpConfiguration de depolanan IP yapılandırmasını kullanacak şekilde ayarlar</span><span class="sxs-lookup"><span data-stu-id="da841-110">The second command sets the privateLink configuration with name privateLinkConfig01 to use the ip configuration stored in $privateLinkIpConfiguration01</span></span>

## <span data-ttu-id="da841-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="da841-111">PARAMETERS</span></span>

### <span data-ttu-id="da841-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="da841-112">-ApplicationGateway</span></span>
<span data-ttu-id="da841-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="da841-113">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da841-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da841-114">-DefaultProfile</span></span>
<span data-ttu-id="da841-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="da841-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da841-116">-IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="da841-116">-IpConfiguration</span></span>
<span data-ttu-id="da841-117">IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="da841-117">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da841-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="da841-118">-Name</span></span>
<span data-ttu-id="da841-119">PrivateLink yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="da841-119">The name of the privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da841-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="da841-120">-Confirm</span></span>
<span data-ttu-id="da841-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="da841-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da841-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da841-122">-WhatIf</span></span>
<span data-ttu-id="da841-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="da841-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da841-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="da841-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da841-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da841-125">CommonParameters</span></span>
<span data-ttu-id="da841-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="da841-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da841-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="da841-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da841-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="da841-128">INPUTS</span></span>

### <span data-ttu-id="da841-129">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="da841-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="da841-130">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="da841-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="da841-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="da841-131">OUTPUTS</span></span>

### <span data-ttu-id="da841-132">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="da841-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="da841-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="da841-133">NOTES</span></span>

## <span data-ttu-id="da841-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="da841-134">RELATED LINKS</span></span>

[<span data-ttu-id="da841-135">Yeni-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="da841-135">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="da841-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="da841-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="da841-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="da841-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="da841-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="da841-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)