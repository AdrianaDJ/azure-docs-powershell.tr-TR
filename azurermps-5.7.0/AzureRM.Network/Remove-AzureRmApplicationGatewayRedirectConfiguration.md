---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: f5a0c703640d540dfd5a47f643694f56f87e0438
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763580"
---
# <span data-ttu-id="0642a-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0642a-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="0642a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0642a-102">SYNOPSIS</span></span>
<span data-ttu-id="0642a-103">Varolan bir uygulama ağ geçidinden yeniden yönlendirme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0642a-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0642a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0642a-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0642a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0642a-105">DESCRIPTION</span></span>
<span data-ttu-id="0642a-106">**Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet 'i, varolan bir uygulama ağ geçidinden yeniden yönlendirme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0642a-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="0642a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0642a-107">EXAMPLES</span></span>

### <span data-ttu-id="0642a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0642a-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="0642a-109">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0642a-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="0642a-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden Redirect01 adlı yeniden yönlendirme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0642a-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="0642a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0642a-111">PARAMETERS</span></span>

### <span data-ttu-id="0642a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0642a-112">-ApplicationGateway</span></span>
<span data-ttu-id="0642a-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0642a-113">The applicationGateway</span></span>

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

### <span data-ttu-id="0642a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0642a-114">-DefaultProfile</span></span>
<span data-ttu-id="0642a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0642a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0642a-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="0642a-116">-Name</span></span>
<span data-ttu-id="0642a-117">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="0642a-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="0642a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0642a-118">CommonParameters</span></span>
<span data-ttu-id="0642a-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0642a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0642a-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0642a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0642a-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0642a-121">INPUTS</span></span>

### <span data-ttu-id="0642a-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0642a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0642a-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0642a-123">OUTPUTS</span></span>

### <span data-ttu-id="0642a-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0642a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0642a-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0642a-125">NOTES</span></span>

## <span data-ttu-id="0642a-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0642a-126">RELATED LINKS</span></span>

