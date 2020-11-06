---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 40a7e63150384ac3fa2c330c079d5377c836d52e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589456"
---
# <span data-ttu-id="ea12b-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ea12b-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="ea12b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea12b-102">SYNOPSIS</span></span>
<span data-ttu-id="ea12b-103">Var olan uygulama ağ geçidinden sistem durumu araştır'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ea12b-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea12b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea12b-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea12b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea12b-105">DESCRIPTION</span></span>
<span data-ttu-id="ea12b-106">Remove-AzureRmApplicationGatewayProbeConfig cmdlet, var olan uygulama ağ geçidinden bir üst bir araştırma kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ea12b-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="ea12b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea12b-107">EXAMPLES</span></span>

### <span data-ttu-id="ea12b-108">Örnek 1: var olan uygulama ağ geçidinden sistem durumu araştırması kaldırma</span><span class="sxs-lookup"><span data-stu-id="ea12b-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="ea12b-109">Bu komut, Probe04 adındaki uygulama ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="ea12b-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="ea12b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea12b-110">PARAMETERS</span></span>

### <span data-ttu-id="ea12b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ea12b-111">-ApplicationGateway</span></span>
<span data-ttu-id="ea12b-112">Bu cmdlet 'in bir araştırın kaldırıldığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea12b-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="ea12b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea12b-113">-DefaultProfile</span></span>
<span data-ttu-id="ea12b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea12b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea12b-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ea12b-115">-Name</span></span>
<span data-ttu-id="ea12b-116">Bu cmdlet 'in kaldırıldığı araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea12b-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="ea12b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea12b-117">CommonParameters</span></span>
<span data-ttu-id="ea12b-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea12b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea12b-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea12b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea12b-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea12b-120">INPUTS</span></span>

### <span data-ttu-id="ea12b-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ea12b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="ea12b-122">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ea12b-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="ea12b-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea12b-123">OUTPUTS</span></span>

### <span data-ttu-id="ea12b-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ea12b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ea12b-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea12b-125">NOTES</span></span>

## <span data-ttu-id="ea12b-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea12b-126">RELATED LINKS</span></span>

[<span data-ttu-id="ea12b-127">Var olan uygulama ağ geçidinden bir araştırın kaldırma</span><span class="sxs-lookup"><span data-stu-id="ea12b-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="ea12b-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ea12b-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ea12b-129">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ea12b-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ea12b-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ea12b-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ea12b-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ea12b-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

