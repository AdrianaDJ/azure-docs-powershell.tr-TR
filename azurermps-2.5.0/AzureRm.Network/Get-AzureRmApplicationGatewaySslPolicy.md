---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpolicy
schema: 2.0.0
ms.openlocfilehash: 237df37605581adeeb45fdfbb7bae6449128aa7b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940089"
---
# <span data-ttu-id="03563-101">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="03563-101">Get-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="03563-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03563-102">SYNOPSIS</span></span>
<span data-ttu-id="03563-103">Uygulama ağ geçidinin SSL ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="03563-103">Gets the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03563-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03563-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03563-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="03563-105">DESCRIPTION</span></span>
<span data-ttu-id="03563-106">**Get-AzureRmApplicationGatewaySslPolicy** cmdlet 'i, bir uygulama ağ geçidinin SSL ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="03563-106">The **Get-AzureRmApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="03563-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03563-107">EXAMPLES</span></span>

### <span data-ttu-id="03563-108">2</span><span class="sxs-lookup"><span data-stu-id="03563-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="03563-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="03563-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="03563-110">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden SSL ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="03563-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="03563-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03563-111">PARAMETERS</span></span>

### <span data-ttu-id="03563-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="03563-112">-ApplicationGateway</span></span>
<span data-ttu-id="03563-113">Bu cmdlet 'in aldığı SSL ilkesinin uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="03563-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="03563-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03563-114">-DefaultProfile</span></span>
<span data-ttu-id="03563-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="03563-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03563-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03563-116">CommonParameters</span></span>
<span data-ttu-id="03563-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03563-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03563-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03563-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03563-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03563-119">INPUTS</span></span>

### <span data-ttu-id="03563-120">System. String</span><span class="sxs-lookup"><span data-stu-id="03563-120">System.String</span></span>

## <span data-ttu-id="03563-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03563-121">OUTPUTS</span></span>

### <span data-ttu-id="03563-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="03563-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="03563-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03563-123">NOTES</span></span>
* <span data-ttu-id="03563-124">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="03563-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="03563-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03563-125">RELATED LINKS</span></span>

[<span data-ttu-id="03563-126">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="03563-126">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="03563-127">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="03563-127">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


