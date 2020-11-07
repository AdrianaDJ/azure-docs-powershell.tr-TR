---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 51428d44c2fc5ce29259924f71617317b163ac29
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935311"
---
# <span data-ttu-id="9e1b9-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9e1b9-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="9e1b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e1b9-102">SYNOPSIS</span></span>
<span data-ttu-id="9e1b9-103">URL yol eşlemelerini arka uç sunucu havuzuna kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="9e1b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e1b9-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e1b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e1b9-105">DESCRIPTION</span></span>
<span data-ttu-id="9e1b9-106">**Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet 'i arka uç sunucu havuzuna yönelik URL yol eşlemelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="9e1b9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e1b9-107">EXAMPLES</span></span>

### <span data-ttu-id="9e1b9-108">2</span><span class="sxs-lookup"><span data-stu-id="9e1b9-108">1:</span></span>
```

```

## <span data-ttu-id="9e1b9-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e1b9-109">PARAMETERS</span></span>

### <span data-ttu-id="9e1b9-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e1b9-110">-ApplicationGateway</span></span>
<span data-ttu-id="9e1b9-111">Bu cmdlet 'in URL yol haritası yapılandırmasını kaldırdığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-111">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="9e1b9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e1b9-112">-DefaultProfile</span></span>
<span data-ttu-id="9e1b9-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e1b9-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="9e1b9-114">-Name</span></span>
<span data-ttu-id="9e1b9-115">Bu cmdlet 'in arka uç sunucusundan kaldırdığı URL yol eşlem adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-115">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="9e1b9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e1b9-116">CommonParameters</span></span>
<span data-ttu-id="9e1b9-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e1b9-118">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e1b9-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e1b9-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e1b9-119">INPUTS</span></span>

### <span data-ttu-id="9e1b9-120">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e1b9-120">PSApplicationGateway</span></span>
<span data-ttu-id="9e1b9-121">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="9e1b9-121">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="9e1b9-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e1b9-122">OUTPUTS</span></span>

### <span data-ttu-id="9e1b9-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e1b9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9e1b9-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e1b9-124">NOTES</span></span>

## <span data-ttu-id="9e1b9-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e1b9-125">RELATED LINKS</span></span>

[<span data-ttu-id="9e1b9-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9e1b9-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9e1b9-127">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9e1b9-127">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9e1b9-128">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9e1b9-128">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9e1b9-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9e1b9-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


