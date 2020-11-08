---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayipconfiguration
schema: 2.0.0
ms.openlocfilehash: 901d8209cc18a5d64285bf45f7169d55d3c7a41e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939906"
---
# <span data-ttu-id="8690c-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8690c-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="8690c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8690c-102">SYNOPSIS</span></span>
<span data-ttu-id="8690c-103">Uygulama ağ geçidinden IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8690c-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8690c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8690c-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8690c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8690c-105">DESCRIPTION</span></span>
<span data-ttu-id="8690c-106">**Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet 'i, bir Azure uygulama ağ geçidinden IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8690c-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="8690c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8690c-107">EXAMPLES</span></span>

### <span data-ttu-id="8690c-108">Örnek 1: Azure uygulama ağ geçidinden IP yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="8690c-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="8690c-109">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8690c-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="8690c-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden Subnet02 adlı IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8690c-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="8690c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8690c-111">PARAMETERS</span></span>

### <span data-ttu-id="8690c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8690c-112">-ApplicationGateway</span></span>
<span data-ttu-id="8690c-113">IP yapılandırmasının kaldırılacağı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8690c-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="8690c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8690c-114">-DefaultProfile</span></span>
<span data-ttu-id="8690c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8690c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8690c-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="8690c-116">-Name</span></span>
<span data-ttu-id="8690c-117">Kaldırılacak IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8690c-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="8690c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8690c-118">CommonParameters</span></span>
<span data-ttu-id="8690c-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8690c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8690c-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8690c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8690c-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8690c-121">INPUTS</span></span>

### <span data-ttu-id="8690c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="8690c-122">System.String</span></span>

## <span data-ttu-id="8690c-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8690c-123">OUTPUTS</span></span>

### <span data-ttu-id="8690c-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8690c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8690c-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8690c-125">NOTES</span></span>

## <span data-ttu-id="8690c-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8690c-126">RELATED LINKS</span></span>

[<span data-ttu-id="8690c-127">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8690c-127">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8690c-128">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8690c-128">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8690c-129">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8690c-129">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8690c-130">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8690c-130">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)

