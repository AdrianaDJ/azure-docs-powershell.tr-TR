---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 9e3a9a515f7b33e23cb7444baa281e083c3c10ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590738"
---
# <span data-ttu-id="c7f6f-101">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c7f6f-101">Remove-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="c7f6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f6f-103">Uygulama ağ geçidinden ön uç bağlantı noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-103">Removes a front-end port from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7f6f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7f6f-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7f6f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7f6f-105">DESCRIPTION</span></span>
<span data-ttu-id="c7f6f-106">**Remove-AzureRmApplicationGatewayFrontendPort** cmdlet 'ı bir Azure uygulama ağ geçidinden ön uç bağlantı noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-106">The **Remove-AzureRmApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="c7f6f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7f6f-107">EXAMPLES</span></span>

### <span data-ttu-id="c7f6f-108">Örnek: uygulama ağ geçidinden ön uç bağlantı noktasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="c7f6f-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="c7f6f-109">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve ağ geçidini $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>

<span data-ttu-id="c7f6f-110">İkinci komut FrontEndPort02 adındaki bağlantı noktasını uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="c7f6f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7f6f-111">PARAMETERS</span></span>

### <span data-ttu-id="c7f6f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7f6f-112">-ApplicationGateway</span></span>
<span data-ttu-id="c7f6f-113">Ön uç bağlantı noktasının kaldırılacağı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="c7f6f-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="c7f6f-114">-Name</span></span>
<span data-ttu-id="c7f6f-115">Kaldırılacak ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-115">Specifies name of the frontend port to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7f6f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f6f-116">-DefaultProfile</span></span>
<span data-ttu-id="c7f6f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7f6f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f6f-118">CommonParameters</span></span>
<span data-ttu-id="c7f6f-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f6f-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7f6f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f6f-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7f6f-121">INPUTS</span></span>

### <span data-ttu-id="c7f6f-122">System. String</span><span class="sxs-lookup"><span data-stu-id="c7f6f-122">System.String</span></span>

## <span data-ttu-id="c7f6f-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7f6f-123">OUTPUTS</span></span>

### <span data-ttu-id="c7f6f-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7f6f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c7f6f-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7f6f-125">NOTES</span></span>

## <span data-ttu-id="c7f6f-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7f6f-126">RELATED LINKS</span></span>

[<span data-ttu-id="c7f6f-127">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c7f6f-127">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c7f6f-128">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c7f6f-128">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c7f6f-129">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c7f6f-129">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c7f6f-130">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c7f6f-130">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


