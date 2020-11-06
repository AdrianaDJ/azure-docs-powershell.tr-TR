---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 29f9d1b13704f190a94bffaa70b900bc5a3b29e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593072"
---
# <span data-ttu-id="2cfb9-101">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="2cfb9-101">Get-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="2cfb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cfb9-102">SYNOPSIS</span></span>
<span data-ttu-id="2cfb9-103">Uygulama ağ geçidinin SSL ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="2cfb9-103">Gets the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cfb9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2cfb9-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cfb9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2cfb9-105">DESCRIPTION</span></span>
<span data-ttu-id="2cfb9-106">**Get-AzureRmApplicationGatewaySslPolicy** cmdlet 'i, bir uygulama ağ geçidinin SSL ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="2cfb9-106">The **Get-AzureRmApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="2cfb9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2cfb9-107">EXAMPLES</span></span>

### <span data-ttu-id="2cfb9-108">2</span><span class="sxs-lookup"><span data-stu-id="2cfb9-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="2cfb9-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="2cfb9-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="2cfb9-110">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden SSL ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="2cfb9-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="2cfb9-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2cfb9-111">PARAMETERS</span></span>

### <span data-ttu-id="2cfb9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2cfb9-112">-ApplicationGateway</span></span>
<span data-ttu-id="2cfb9-113">Bu cmdlet 'in aldığı SSL ilkesinin uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cfb9-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2cfb9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cfb9-114">-DefaultProfile</span></span>
<span data-ttu-id="2cfb9-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2cfb9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cfb9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cfb9-116">CommonParameters</span></span>
<span data-ttu-id="2cfb9-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2cfb9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cfb9-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cfb9-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cfb9-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2cfb9-119">INPUTS</span></span>

### <span data-ttu-id="2cfb9-120">System. String</span><span class="sxs-lookup"><span data-stu-id="2cfb9-120">System.String</span></span>

## <span data-ttu-id="2cfb9-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2cfb9-121">OUTPUTS</span></span>

### <span data-ttu-id="2cfb9-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="2cfb9-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="2cfb9-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2cfb9-123">NOTES</span></span>
* <span data-ttu-id="2cfb9-124">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="2cfb9-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2cfb9-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2cfb9-125">RELATED LINKS</span></span>

[<span data-ttu-id="2cfb9-126">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="2cfb9-126">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="2cfb9-127">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="2cfb9-127">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


