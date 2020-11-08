---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: ec20d7caafe110f03e5a0ce3130247ec877d6af9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267983"
---
# <span data-ttu-id="f4f1c-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f4f1c-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="f4f1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4f1c-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f1c-103">Uygulama ağ geçidinden var olan bir sistem durumu araştırması yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="f4f1c-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="f4f1c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4f1c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4f1c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4f1c-105">DESCRIPTION</span></span>
<span data-ttu-id="f4f1c-106">Get-AzApplicationGatewayProbeConfig cmdlet 'i uygulama ağ geçidinden var olan bir sistem durumu araştırması yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="f4f1c-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="f4f1c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4f1c-107">EXAMPLES</span></span>

### <span data-ttu-id="f4f1c-108">Örnek 1: uygulama ağ geçidinden varolan bir araştırma alma</span><span class="sxs-lookup"><span data-stu-id="f4f1c-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="f4f1c-109">Bu komut ağ geçidi adlı uygulama ağ geçidinden Probe02 adlı sistem durumu araştırılmasını alır.</span><span class="sxs-lookup"><span data-stu-id="f4f1c-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="f4f1c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4f1c-110">PARAMETERS</span></span>

### <span data-ttu-id="f4f1c-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4f1c-111">-ApplicationGateway</span></span>
<span data-ttu-id="f4f1c-112">Bu cmdlet 'in yoklama yapılandırması aldığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4f1c-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="f4f1c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f1c-113">-DefaultProfile</span></span>
<span data-ttu-id="f4f1c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4f1c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4f1c-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="f4f1c-115">-Name</span></span>
<span data-ttu-id="f4f1c-116">Araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4f1c-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="f4f1c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f1c-117">CommonParameters</span></span>
<span data-ttu-id="f4f1c-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4f1c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f1c-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f4f1c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f1c-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4f1c-120">INPUTS</span></span>

### <span data-ttu-id="f4f1c-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4f1c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f4f1c-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4f1c-122">OUTPUTS</span></span>

### <span data-ttu-id="f4f1c-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="f4f1c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="f4f1c-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4f1c-124">NOTES</span></span>

## <span data-ttu-id="f4f1c-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4f1c-125">RELATED LINKS</span></span>

[<span data-ttu-id="f4f1c-126">Var olan uygulama ağ geçidine araştırma ekleme</span><span class="sxs-lookup"><span data-stu-id="f4f1c-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="f4f1c-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f4f1c-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="f4f1c-128">Yeni-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f4f1c-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="f4f1c-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f4f1c-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="f4f1c-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f4f1c-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

