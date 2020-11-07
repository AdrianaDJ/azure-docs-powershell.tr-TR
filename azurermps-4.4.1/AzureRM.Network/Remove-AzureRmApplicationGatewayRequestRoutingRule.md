---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 5b4f0568574b6ec6994d0c195568306e9d2e4a86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764806"
---
# <span data-ttu-id="576d8-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="576d8-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="576d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="576d8-102">SYNOPSIS</span></span>
<span data-ttu-id="576d8-103">Uygulama ağ geçidinden istek yönlendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="576d8-103">Removes a request routing rule from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="576d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="576d8-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="576d8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="576d8-105">DESCRIPTION</span></span>
<span data-ttu-id="576d8-106">**Remove-AzureRmApplicationGatewayRequestRoutingRule** cmdlet 'ı bir Azure uygulama ağ geçidinden istek yönlendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="576d8-106">The **Remove-AzureRmApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="576d8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="576d8-107">EXAMPLES</span></span>

### <span data-ttu-id="576d8-108">Örnek 1: uygulama ağ geçidinden istek yönlendirme kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="576d8-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="576d8-109">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="576d8-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="576d8-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden Rule02 adındaki istek yönlendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="576d8-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="576d8-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="576d8-111">PARAMETERS</span></span>

### <span data-ttu-id="576d8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="576d8-112">-ApplicationGateway</span></span>
<span data-ttu-id="576d8-113">İstek yönlendirme kuralının kaldırılacağı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="576d8-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="576d8-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="576d8-114">-Name</span></span>
<span data-ttu-id="576d8-115">Bu cmdlet 'in kaldırıldığı istek yönlendirme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="576d8-115">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="576d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="576d8-116">-DefaultProfile</span></span>
<span data-ttu-id="576d8-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="576d8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="576d8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="576d8-118">CommonParameters</span></span>
<span data-ttu-id="576d8-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="576d8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="576d8-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="576d8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="576d8-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="576d8-121">INPUTS</span></span>

### <span data-ttu-id="576d8-122">System. String</span><span class="sxs-lookup"><span data-stu-id="576d8-122">System.String</span></span>

## <span data-ttu-id="576d8-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="576d8-123">OUTPUTS</span></span>

### <span data-ttu-id="576d8-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="576d8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="576d8-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="576d8-125">NOTES</span></span>

## <span data-ttu-id="576d8-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="576d8-126">RELATED LINKS</span></span>

[<span data-ttu-id="576d8-127">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="576d8-127">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="576d8-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="576d8-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="576d8-129">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="576d8-129">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="576d8-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="576d8-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


