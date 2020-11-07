---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 4079d8b6859a2860116520c52928d13c7e3fa29e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764924"
---
# <span data-ttu-id="89a5e-101">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="89a5e-101">Remove-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="89a5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="89a5e-103">Uygulama ağ geçidinden HTTP dinleyicisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="89a5e-103">Removes an HTTP listener from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89a5e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89a5e-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89a5e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="89a5e-105">DESCRIPTION</span></span>
<span data-ttu-id="89a5e-106">**Remove-AzureRmApplicationGatewayHttpListener** cmdlet 'ı bir Azure uygulama ağ geçidinden HTTP dinleyicisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="89a5e-106">The **Remove-AzureRmApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="89a5e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89a5e-107">EXAMPLES</span></span>

### <span data-ttu-id="89a5e-108">Örnek 1: uygulama ağ geçidi HTTP dinleyicisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="89a5e-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="89a5e-109">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="89a5e-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="89a5e-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden Listener02 adlı HTTP dinleyicisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="89a5e-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="89a5e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89a5e-111">PARAMETERS</span></span>

### <span data-ttu-id="89a5e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89a5e-112">-ApplicationGateway</span></span>
<span data-ttu-id="89a5e-113">HTTP dinleyicisinin kaldırılacağı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="89a5e-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="89a5e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89a5e-114">-DefaultProfile</span></span>
<span data-ttu-id="89a5e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89a5e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89a5e-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="89a5e-116">-Name</span></span>
<span data-ttu-id="89a5e-117">Bu cmdlet 'in kaldırıldığı HTTP dinleyicisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89a5e-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="89a5e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89a5e-118">CommonParameters</span></span>
<span data-ttu-id="89a5e-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89a5e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89a5e-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89a5e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89a5e-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89a5e-121">INPUTS</span></span>

### <span data-ttu-id="89a5e-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89a5e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="89a5e-123">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="89a5e-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="89a5e-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89a5e-124">OUTPUTS</span></span>

### <span data-ttu-id="89a5e-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="89a5e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="89a5e-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89a5e-126">NOTES</span></span>

## <span data-ttu-id="89a5e-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89a5e-127">RELATED LINKS</span></span>

[<span data-ttu-id="89a5e-128">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="89a5e-128">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="89a5e-129">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="89a5e-129">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="89a5e-130">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="89a5e-130">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="89a5e-131">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="89a5e-131">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


