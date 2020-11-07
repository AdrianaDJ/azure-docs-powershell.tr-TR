---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 286afc05e9b7c825f183aabe7a78c965c790cb02
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940095"
---
# <span data-ttu-id="2b0b1-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b0b1-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="2b0b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b0b1-102">SYNOPSIS</span></span>
<span data-ttu-id="2b0b1-103">Uygulama ağ geçidinden varolan bir yönlendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="2b0b1-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b0b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b0b1-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b0b1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b0b1-105">DESCRIPTION</span></span>
<span data-ttu-id="2b0b1-106">**Get-AzureRmApplicationGatewayRedirectConfiguration** cmdlet 'ı uygulama ağ geçidinden varolan bir yönlendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="2b0b1-106">The **Get-AzureRmApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="2b0b1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b0b1-107">EXAMPLES</span></span>

### <span data-ttu-id="2b0b1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2b0b1-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="2b0b1-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="2b0b1-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="2b0b1-110">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden Redirect01 adındaki yeniden yönlendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="2b0b1-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="2b0b1-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b0b1-111">PARAMETERS</span></span>

### <span data-ttu-id="2b0b1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b0b1-112">-ApplicationGateway</span></span>
<span data-ttu-id="2b0b1-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b0b1-113">The applicationGateway</span></span>

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

### <span data-ttu-id="2b0b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b0b1-114">-DefaultProfile</span></span>
<span data-ttu-id="2b0b1-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b0b1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b0b1-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="2b0b1-116">-Name</span></span>
<span data-ttu-id="2b0b1-117">İstek yönlendirme kuralının adı</span><span class="sxs-lookup"><span data-stu-id="2b0b1-117">The name of the request routing rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b0b1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b0b1-118">CommonParameters</span></span>
<span data-ttu-id="2b0b1-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b0b1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b0b1-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b0b1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b0b1-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b0b1-121">INPUTS</span></span>

### <span data-ttu-id="2b0b1-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b0b1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2b0b1-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b0b1-123">OUTPUTS</span></span>

### <span data-ttu-id="2b0b1-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b0b1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="2b0b1-125">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2b0b1-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2b0b1-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b0b1-126">NOTES</span></span>

## <span data-ttu-id="2b0b1-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b0b1-127">RELATED LINKS</span></span>

