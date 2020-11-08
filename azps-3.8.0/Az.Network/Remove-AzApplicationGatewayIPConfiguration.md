---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 87f6f441220f1f8ab47fee5356bddca8d02b96c0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095828"
---
# <span data-ttu-id="ba332-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba332-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="ba332-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba332-102">SYNOPSIS</span></span>
<span data-ttu-id="ba332-103">Uygulama ağ geçidinden IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ba332-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="ba332-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba332-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba332-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba332-105">DESCRIPTION</span></span>
<span data-ttu-id="ba332-106">**Remove-Azapplicationgatewayıpconfiguration** cmdlet 'i, bir Azure uygulama ağ geçidinden IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ba332-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="ba332-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba332-107">EXAMPLES</span></span>

### <span data-ttu-id="ba332-108">Örnek 1: Azure uygulama ağ geçidinden IP yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="ba332-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="ba332-109">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ba332-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ba332-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden Subnet02 adlı IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ba332-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="ba332-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba332-111">PARAMETERS</span></span>

### <span data-ttu-id="ba332-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ba332-112">-ApplicationGateway</span></span>
<span data-ttu-id="ba332-113">IP yapılandırmasının kaldırılacağı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba332-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba332-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba332-114">-DefaultProfile</span></span>
<span data-ttu-id="ba332-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba332-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba332-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="ba332-116">-Name</span></span>
<span data-ttu-id="ba332-117">Kaldırılacak IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba332-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="ba332-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba332-118">CommonParameters</span></span>
<span data-ttu-id="ba332-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba332-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba332-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba332-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba332-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba332-121">INPUTS</span></span>

### <span data-ttu-id="ba332-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ba332-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ba332-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba332-123">OUTPUTS</span></span>

### <span data-ttu-id="ba332-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ba332-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ba332-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba332-125">NOTES</span></span>

## <span data-ttu-id="ba332-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba332-126">RELATED LINKS</span></span>

[<span data-ttu-id="ba332-127">Add-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="ba332-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ba332-128">Get-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="ba332-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ba332-129">Yeni-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="ba332-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ba332-130">Set-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="ba332-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


