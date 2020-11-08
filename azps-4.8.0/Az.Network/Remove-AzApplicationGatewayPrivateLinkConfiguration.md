---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 8d222f4eaaa9d37a4f87f5f19604bdef9cff9e39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109446"
---
# <span data-ttu-id="13b5f-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="13b5f-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="13b5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13b5f-102">SYNOPSIS</span></span>
<span data-ttu-id="13b5f-103">Bir uygulama ağ geçidinden privateLink yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="13b5f-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="13b5f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="13b5f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13b5f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="13b5f-105">DESCRIPTION</span></span>
<span data-ttu-id="13b5f-106">**Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet 'ı bir Azure uygulama ağ geçidinden Privatelink yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="13b5f-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="13b5f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="13b5f-107">EXAMPLES</span></span>

### <span data-ttu-id="13b5f-108">Örnek 1: bir uygulama ağ geçidi PrivateLink yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="13b5f-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="13b5f-109">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="13b5f-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="13b5f-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden privateLinkConfig01 adlı privateLink yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="13b5f-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="13b5f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="13b5f-111">PARAMETERS</span></span>

### <span data-ttu-id="13b5f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13b5f-112">-ApplicationGateway</span></span>
<span data-ttu-id="13b5f-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13b5f-113">The applicationGateway</span></span>

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

### <span data-ttu-id="13b5f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13b5f-114">-DefaultProfile</span></span>
<span data-ttu-id="13b5f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="13b5f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b5f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="13b5f-116">-Name</span></span>
<span data-ttu-id="13b5f-117">Uygulama ağ geçidi privateLink yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="13b5f-117">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="13b5f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b5f-118">CommonParameters</span></span>
<span data-ttu-id="13b5f-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="13b5f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b5f-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="13b5f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b5f-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="13b5f-121">INPUTS</span></span>

### <span data-ttu-id="13b5f-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13b5f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="13b5f-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="13b5f-123">OUTPUTS</span></span>

### <span data-ttu-id="13b5f-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13b5f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="13b5f-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="13b5f-125">NOTES</span></span>

## <span data-ttu-id="13b5f-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="13b5f-126">RELATED LINKS</span></span>

[<span data-ttu-id="13b5f-127">Yeni-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="13b5f-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="13b5f-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="13b5f-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="13b5f-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="13b5f-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="13b5f-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="13b5f-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)