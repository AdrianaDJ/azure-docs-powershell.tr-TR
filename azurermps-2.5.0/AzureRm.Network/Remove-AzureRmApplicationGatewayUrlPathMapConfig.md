---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: a0885534311dfef4498c9fc71be7f82d16b05277
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939091"
---
# <span data-ttu-id="e2768-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e2768-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="e2768-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2768-102">SYNOPSIS</span></span>
<span data-ttu-id="e2768-103">URL yol eşlemelerini arka uç sunucu havuzuna kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e2768-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2768-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2768-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2768-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2768-105">DESCRIPTION</span></span>
<span data-ttu-id="e2768-106">**Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet 'i arka uç sunucu havuzuna yönelik URL yol eşlemelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e2768-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="e2768-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2768-107">EXAMPLES</span></span>

### <span data-ttu-id="e2768-108">2</span><span class="sxs-lookup"><span data-stu-id="e2768-108">1:</span></span>
```

```

## <span data-ttu-id="e2768-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2768-109">PARAMETERS</span></span>

### <span data-ttu-id="e2768-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2768-110">-ApplicationGateway</span></span>
<span data-ttu-id="e2768-111">Bu cmdlet 'in URL yol haritası yapılandırmasını kaldırdığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2768-111">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="e2768-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2768-112">-DefaultProfile</span></span>
<span data-ttu-id="e2768-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2768-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2768-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="e2768-114">-Name</span></span>
<span data-ttu-id="e2768-115">Bu cmdlet 'in arka uç sunucusundan kaldırdığı URL yol eşlem adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2768-115">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="e2768-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2768-116">CommonParameters</span></span>
<span data-ttu-id="e2768-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2768-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2768-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2768-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2768-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2768-119">INPUTS</span></span>

### <span data-ttu-id="e2768-120">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2768-120">PSApplicationGateway</span></span>
<span data-ttu-id="e2768-121">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e2768-121">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="e2768-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2768-122">OUTPUTS</span></span>

### <span data-ttu-id="e2768-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2768-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2768-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2768-124">NOTES</span></span>

## <span data-ttu-id="e2768-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2768-125">RELATED LINKS</span></span>

[<span data-ttu-id="e2768-126">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e2768-126">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e2768-127">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e2768-127">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e2768-128">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e2768-128">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e2768-129">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e2768-129">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


