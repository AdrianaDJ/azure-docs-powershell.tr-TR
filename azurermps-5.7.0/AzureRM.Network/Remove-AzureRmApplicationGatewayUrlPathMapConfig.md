---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 612e6b0cb5438dbb37a2e9d1c77da151c852fac1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589753"
---
# <span data-ttu-id="f89b1-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f89b1-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="f89b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f89b1-102">SYNOPSIS</span></span>
<span data-ttu-id="f89b1-103">URL yol eşlemelerini arka uç sunucu havuzuna kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f89b1-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f89b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f89b1-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f89b1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f89b1-105">DESCRIPTION</span></span>
<span data-ttu-id="f89b1-106">**Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet 'i arka uç sunucu havuzuna yönelik URL yol eşlemelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f89b1-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="f89b1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f89b1-107">EXAMPLES</span></span>

## <span data-ttu-id="f89b1-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f89b1-108">PARAMETERS</span></span>

### <span data-ttu-id="f89b1-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f89b1-109">-ApplicationGateway</span></span>
<span data-ttu-id="f89b1-110">Bu cmdlet 'in URL yol haritası yapılandırmasını kaldırdığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f89b1-110">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="f89b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f89b1-111">-DefaultProfile</span></span>
<span data-ttu-id="f89b1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f89b1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f89b1-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="f89b1-113">-Name</span></span>
<span data-ttu-id="f89b1-114">Bu cmdlet 'in arka uç sunucusundan kaldırdığı URL yol eşlem adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f89b1-114">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="f89b1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f89b1-115">CommonParameters</span></span>
<span data-ttu-id="f89b1-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f89b1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f89b1-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f89b1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f89b1-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f89b1-118">INPUTS</span></span>

### <span data-ttu-id="f89b1-119">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f89b1-119">PSApplicationGateway</span></span>
<span data-ttu-id="f89b1-120">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f89b1-120">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="f89b1-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f89b1-121">OUTPUTS</span></span>

### <span data-ttu-id="f89b1-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f89b1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f89b1-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f89b1-123">NOTES</span></span>

## <span data-ttu-id="f89b1-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f89b1-124">RELATED LINKS</span></span>

[<span data-ttu-id="f89b1-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f89b1-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f89b1-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f89b1-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f89b1-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f89b1-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f89b1-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f89b1-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


