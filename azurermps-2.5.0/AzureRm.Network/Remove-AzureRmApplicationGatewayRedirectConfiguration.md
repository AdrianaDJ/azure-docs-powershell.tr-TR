---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: ba979a12584d526ba7e3a36d13c44b51704b44f6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939100"
---
# <span data-ttu-id="e9850-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9850-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="e9850-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9850-102">SYNOPSIS</span></span>
<span data-ttu-id="e9850-103">Varolan bir uygulama ağ geçidinden yeniden yönlendirme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e9850-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9850-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9850-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9850-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9850-105">DESCRIPTION</span></span>
<span data-ttu-id="e9850-106">**Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet 'i, varolan bir uygulama ağ geçidinden yeniden yönlendirme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e9850-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="e9850-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9850-107">EXAMPLES</span></span>

### <span data-ttu-id="e9850-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e9850-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="e9850-109">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e9850-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="e9850-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden Redirect01 adlı yeniden yönlendirme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e9850-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="e9850-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9850-111">PARAMETERS</span></span>

### <span data-ttu-id="e9850-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9850-112">-ApplicationGateway</span></span>
<span data-ttu-id="e9850-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9850-113">The applicationGateway</span></span>

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

### <span data-ttu-id="e9850-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9850-114">-DefaultProfile</span></span>
<span data-ttu-id="e9850-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e9850-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9850-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="e9850-116">-Name</span></span>
<span data-ttu-id="e9850-117">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="e9850-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="e9850-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9850-118">CommonParameters</span></span>
<span data-ttu-id="e9850-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9850-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9850-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9850-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9850-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9850-121">INPUTS</span></span>

### <span data-ttu-id="e9850-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9850-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e9850-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9850-123">OUTPUTS</span></span>

### <span data-ttu-id="e9850-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9850-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e9850-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9850-125">NOTES</span></span>

## <span data-ttu-id="e9850-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9850-126">RELATED LINKS</span></span>
