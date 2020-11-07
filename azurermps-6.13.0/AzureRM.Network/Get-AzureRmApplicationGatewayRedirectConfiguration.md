---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 23815c5b4d0977f27f09f002f32e1658a8515d61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763456"
---
# <span data-ttu-id="bffce-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bffce-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="bffce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bffce-102">SYNOPSIS</span></span>
<span data-ttu-id="bffce-103">Uygulama ağ geçidinden varolan bir yönlendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="bffce-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bffce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bffce-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bffce-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bffce-105">DESCRIPTION</span></span>
<span data-ttu-id="bffce-106">**Get-AzureRmApplicationGatewayRedirectConfiguration** cmdlet 'ı uygulama ağ geçidinden varolan bir yönlendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="bffce-106">The **Get-AzureRmApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="bffce-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bffce-107">EXAMPLES</span></span>

### <span data-ttu-id="bffce-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bffce-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="bffce-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="bffce-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="bffce-110">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden Redirect01 adındaki yeniden yönlendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="bffce-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="bffce-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bffce-111">PARAMETERS</span></span>

### <span data-ttu-id="bffce-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bffce-112">-ApplicationGateway</span></span>
<span data-ttu-id="bffce-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bffce-113">The applicationGateway</span></span>

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

### <span data-ttu-id="bffce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bffce-114">-DefaultProfile</span></span>
<span data-ttu-id="bffce-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bffce-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bffce-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="bffce-116">-Name</span></span>
<span data-ttu-id="bffce-117">İstek yönlendirme kuralının adı</span><span class="sxs-lookup"><span data-stu-id="bffce-117">The name of the request routing rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bffce-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bffce-118">CommonParameters</span></span>
<span data-ttu-id="bffce-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bffce-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bffce-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bffce-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bffce-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bffce-121">INPUTS</span></span>

### <span data-ttu-id="bffce-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bffce-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="bffce-123">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bffce-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="bffce-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bffce-124">OUTPUTS</span></span>

### <span data-ttu-id="bffce-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bffce-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="bffce-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bffce-126">NOTES</span></span>

## <span data-ttu-id="bffce-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bffce-127">RELATED LINKS</span></span>
