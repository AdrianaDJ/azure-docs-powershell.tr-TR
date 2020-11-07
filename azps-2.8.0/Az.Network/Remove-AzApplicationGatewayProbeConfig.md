---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: eedb3eb0df28b3f02690a2462b9367995235fcc7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918120"
---
# <span data-ttu-id="e3687-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e3687-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="e3687-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3687-102">SYNOPSIS</span></span>
<span data-ttu-id="e3687-103">Var olan uygulama ağ geçidinden sistem durumu araştır'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e3687-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="e3687-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3687-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3687-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3687-105">DESCRIPTION</span></span>
<span data-ttu-id="e3687-106">Remove-AzApplicationGatewayProbeConfig cmdlet, var olan uygulama ağ geçidinden bir üst bir araştırma kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e3687-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="e3687-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3687-107">EXAMPLES</span></span>

### <span data-ttu-id="e3687-108">Örnek 1: var olan uygulama ağ geçidinden sistem durumu araştırması kaldırma</span><span class="sxs-lookup"><span data-stu-id="e3687-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="e3687-109">Bu komut, Probe04 adındaki uygulama ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="e3687-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="e3687-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3687-110">PARAMETERS</span></span>

### <span data-ttu-id="e3687-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3687-111">-ApplicationGateway</span></span>
<span data-ttu-id="e3687-112">Bu cmdlet 'in bir araştırın kaldırıldığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3687-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="e3687-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3687-113">-DefaultProfile</span></span>
<span data-ttu-id="e3687-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e3687-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3687-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e3687-115">-Name</span></span>
<span data-ttu-id="e3687-116">Bu cmdlet 'in kaldırıldığı araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3687-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="e3687-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3687-117">CommonParameters</span></span>
<span data-ttu-id="e3687-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3687-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3687-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3687-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3687-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3687-120">INPUTS</span></span>

### <span data-ttu-id="e3687-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3687-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e3687-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3687-122">OUTPUTS</span></span>

### <span data-ttu-id="e3687-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3687-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e3687-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3687-124">NOTES</span></span>

## <span data-ttu-id="e3687-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3687-125">RELATED LINKS</span></span>

[<span data-ttu-id="e3687-126">Var olan uygulama ağ geçidinden bir araştırın kaldırma</span><span class="sxs-lookup"><span data-stu-id="e3687-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="e3687-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e3687-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="e3687-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e3687-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="e3687-129">Yeni-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e3687-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="e3687-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e3687-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

