---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: ecee205ee831c5ba7a2fa78c00f005af3303a13a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939103"
---
# <span data-ttu-id="36d92-101">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="36d92-101">Remove-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="36d92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36d92-102">SYNOPSIS</span></span>
<span data-ttu-id="36d92-103">Uygulama ağ geçidinden ön uç bağlantı noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="36d92-103">Removes a front-end port from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36d92-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36d92-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36d92-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="36d92-105">DESCRIPTION</span></span>
<span data-ttu-id="36d92-106">**Remove-AzureRmApplicationGatewayFrontendPort** cmdlet 'ı bir Azure uygulama ağ geçidinden ön uç bağlantı noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="36d92-106">The **Remove-AzureRmApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="36d92-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36d92-107">EXAMPLES</span></span>

### <span data-ttu-id="36d92-108">Örnek: uygulama ağ geçidinden ön uç bağlantı noktasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="36d92-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="36d92-109">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve ağ geçidini $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="36d92-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>

<span data-ttu-id="36d92-110">İkinci komut FrontEndPort02 adındaki bağlantı noktasını uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="36d92-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="36d92-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36d92-111">PARAMETERS</span></span>

### <span data-ttu-id="36d92-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36d92-112">-ApplicationGateway</span></span>
<span data-ttu-id="36d92-113">Ön uç bağlantı noktasının kaldırılacağı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="36d92-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="36d92-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d92-114">-DefaultProfile</span></span>
<span data-ttu-id="36d92-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36d92-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36d92-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="36d92-116">-Name</span></span>
<span data-ttu-id="36d92-117">Kaldırılacak ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36d92-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="36d92-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d92-118">CommonParameters</span></span>
<span data-ttu-id="36d92-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36d92-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d92-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36d92-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d92-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36d92-121">INPUTS</span></span>

### <span data-ttu-id="36d92-122">System. String</span><span class="sxs-lookup"><span data-stu-id="36d92-122">System.String</span></span>

## <span data-ttu-id="36d92-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36d92-123">OUTPUTS</span></span>

### <span data-ttu-id="36d92-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36d92-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="36d92-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36d92-125">NOTES</span></span>

## <span data-ttu-id="36d92-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36d92-126">RELATED LINKS</span></span>

[<span data-ttu-id="36d92-127">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="36d92-127">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="36d92-128">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="36d92-128">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="36d92-129">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="36d92-129">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="36d92-130">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="36d92-130">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


