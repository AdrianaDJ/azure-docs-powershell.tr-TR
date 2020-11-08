---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2c73be940e887b4cd1ca96da1442f8ae007ab6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104088"
---
# <span data-ttu-id="8d09c-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8d09c-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="8d09c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d09c-102">SYNOPSIS</span></span>
<span data-ttu-id="8d09c-103">URL yol eşlemelerini arka uç sunucu havuzuna kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8d09c-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="8d09c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d09c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d09c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d09c-105">DESCRIPTION</span></span>
<span data-ttu-id="8d09c-106">**Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet 'i arka uç sunucu havuzuna yönelik URL yol eşlemelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8d09c-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="8d09c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d09c-107">EXAMPLES</span></span>

### <span data-ttu-id="8d09c-108">Örnek 1: uygulama ağ geçidinden URL yolu eşlemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="8d09c-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="8d09c-109">İlk komut appGwName adlı uygulama ağ geçidini alır ve sonucu $appgw değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="8d09c-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="8d09c-110">İkinci komut map01 adındaki URL yol eşlemesini uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8d09c-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="8d09c-111">Üçüncü komut, uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8d09c-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="8d09c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d09c-112">PARAMETERS</span></span>

### <span data-ttu-id="8d09c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d09c-113">-ApplicationGateway</span></span>
<span data-ttu-id="8d09c-114">Bu cmdlet 'in URL yol haritası yapılandırmasını kaldırdığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d09c-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="8d09c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d09c-115">-DefaultProfile</span></span>
<span data-ttu-id="8d09c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8d09c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d09c-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="8d09c-117">-Name</span></span>
<span data-ttu-id="8d09c-118">Bu cmdlet 'in arka uç sunucusundan kaldırdığı URL yol eşlem adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d09c-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="8d09c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d09c-119">CommonParameters</span></span>
<span data-ttu-id="8d09c-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d09c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d09c-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d09c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d09c-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d09c-122">INPUTS</span></span>

### <span data-ttu-id="8d09c-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d09c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8d09c-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d09c-124">OUTPUTS</span></span>

### <span data-ttu-id="8d09c-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d09c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8d09c-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d09c-126">NOTES</span></span>

## <span data-ttu-id="8d09c-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d09c-127">RELATED LINKS</span></span>

[<span data-ttu-id="8d09c-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8d09c-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="8d09c-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8d09c-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="8d09c-130">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8d09c-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="8d09c-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8d09c-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


