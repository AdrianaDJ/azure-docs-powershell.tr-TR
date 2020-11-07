---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 2297eb3d1734938f6c04b22472b02add19f634f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762564"
---
# <span data-ttu-id="6b06d-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6b06d-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="6b06d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b06d-102">SYNOPSIS</span></span>
<span data-ttu-id="6b06d-103">URL yol eşlemelerini arka uç sunucu havuzuna kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6b06d-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b06d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b06d-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b06d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b06d-105">DESCRIPTION</span></span>
<span data-ttu-id="6b06d-106">**Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet 'i arka uç sunucu havuzuna yönelik URL yol eşlemelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6b06d-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="6b06d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b06d-107">EXAMPLES</span></span>

## <span data-ttu-id="6b06d-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b06d-108">PARAMETERS</span></span>

### <span data-ttu-id="6b06d-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b06d-109">-ApplicationGateway</span></span>
<span data-ttu-id="6b06d-110">Bu cmdlet 'in URL yol haritası yapılandırmasını kaldırdığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b06d-110">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="6b06d-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="6b06d-111">-Name</span></span>
<span data-ttu-id="6b06d-112">Bu cmdlet 'in arka uç sunucusundan kaldırdığı URL yol eşlem adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b06d-112">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="6b06d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b06d-113">-DefaultProfile</span></span>
<span data-ttu-id="6b06d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b06d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b06d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b06d-115">CommonParameters</span></span>
<span data-ttu-id="6b06d-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b06d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b06d-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b06d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b06d-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b06d-118">INPUTS</span></span>

### <span data-ttu-id="6b06d-119">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b06d-119">PSApplicationGateway</span></span>
<span data-ttu-id="6b06d-120">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6b06d-120">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="6b06d-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b06d-121">OUTPUTS</span></span>

### <span data-ttu-id="6b06d-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b06d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6b06d-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b06d-123">NOTES</span></span>

## <span data-ttu-id="6b06d-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b06d-124">RELATED LINKS</span></span>

[<span data-ttu-id="6b06d-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6b06d-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6b06d-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6b06d-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6b06d-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6b06d-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6b06d-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6b06d-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


