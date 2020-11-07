---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 62d58803f4b1c7cae39e41e5f903cbfaf022e632
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932053"
---
# <span data-ttu-id="04b82-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="04b82-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="04b82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04b82-102">SYNOPSIS</span></span>
<span data-ttu-id="04b82-103">Uygulama ağ geçidinden var olan bir sistem durumu araştırması yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="04b82-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="04b82-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04b82-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04b82-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="04b82-105">DESCRIPTION</span></span>
<span data-ttu-id="04b82-106">Get-AzApplicationGatewayProbeConfig cmdlet 'i uygulama ağ geçidinden var olan bir sistem durumu araştırması yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="04b82-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="04b82-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04b82-107">EXAMPLES</span></span>

### <span data-ttu-id="04b82-108">Örnek 1: uygulama ağ geçidinden varolan bir araştırma alma</span><span class="sxs-lookup"><span data-stu-id="04b82-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="04b82-109">Bu komut ağ geçidi adlı uygulama ağ geçidinden Probe02 adlı sistem durumu araştırılmasını alır.</span><span class="sxs-lookup"><span data-stu-id="04b82-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="04b82-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04b82-110">PARAMETERS</span></span>

### <span data-ttu-id="04b82-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04b82-111">-ApplicationGateway</span></span>
<span data-ttu-id="04b82-112">Bu cmdlet 'in yoklama yapılandırması aldığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="04b82-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="04b82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04b82-113">-DefaultProfile</span></span>
<span data-ttu-id="04b82-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="04b82-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04b82-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="04b82-115">-Name</span></span>
<span data-ttu-id="04b82-116">Araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04b82-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="04b82-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b82-117">CommonParameters</span></span>
<span data-ttu-id="04b82-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04b82-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b82-119">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="04b82-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b82-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04b82-120">INPUTS</span></span>

### <span data-ttu-id="04b82-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04b82-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="04b82-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04b82-122">OUTPUTS</span></span>

### <span data-ttu-id="04b82-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="04b82-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="04b82-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04b82-124">NOTES</span></span>

## <span data-ttu-id="04b82-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04b82-125">RELATED LINKS</span></span>

[<span data-ttu-id="04b82-126">Var olan uygulama ağ geçidine araştırma ekleme</span><span class="sxs-lookup"><span data-stu-id="04b82-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="04b82-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="04b82-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="04b82-128">Yeni-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="04b82-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="04b82-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="04b82-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="04b82-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="04b82-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)
