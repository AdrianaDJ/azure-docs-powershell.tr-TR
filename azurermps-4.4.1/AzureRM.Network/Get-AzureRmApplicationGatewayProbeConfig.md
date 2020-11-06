---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 6583856eb6d44fa170b53a855e43db71602534a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587865"
---
# <span data-ttu-id="b23dc-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b23dc-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="b23dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b23dc-102">SYNOPSIS</span></span>
<span data-ttu-id="b23dc-103">Uygulama ağ geçidinden var olan bir sistem durumu araştırması yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="b23dc-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b23dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b23dc-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b23dc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b23dc-105">DESCRIPTION</span></span>
<span data-ttu-id="b23dc-106">Get-AzureRmApplicationGatewayProbeConfig cmdlet 'i uygulama ağ geçidinden var olan bir sistem durumu araştırması yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="b23dc-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="b23dc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b23dc-107">EXAMPLES</span></span>

### <span data-ttu-id="b23dc-108">Örnek 1: uygulama ağ geçidinden varolan bir araştırma alma</span><span class="sxs-lookup"><span data-stu-id="b23dc-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="b23dc-109">Bu komut ağ geçidi adlı uygulama ağ geçidinden Probe02 adlı sistem durumu araştırılmasını alır.</span><span class="sxs-lookup"><span data-stu-id="b23dc-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="b23dc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b23dc-110">PARAMETERS</span></span>

### <span data-ttu-id="b23dc-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b23dc-111">-ApplicationGateway</span></span>
<span data-ttu-id="b23dc-112">Bu cmdlet 'in yoklama yapılandırması aldığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b23dc-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="b23dc-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="b23dc-113">-Name</span></span>
<span data-ttu-id="b23dc-114">Araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b23dc-114">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="b23dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b23dc-115">-DefaultProfile</span></span>
<span data-ttu-id="b23dc-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b23dc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b23dc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b23dc-117">CommonParameters</span></span>
<span data-ttu-id="b23dc-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b23dc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b23dc-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b23dc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b23dc-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b23dc-120">INPUTS</span></span>

### <span data-ttu-id="b23dc-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b23dc-121">PSApplicationGateway</span></span>
<span data-ttu-id="b23dc-122">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b23dc-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="b23dc-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b23dc-123">OUTPUTS</span></span>

### <span data-ttu-id="b23dc-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="b23dc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="b23dc-125">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="b23dc-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="b23dc-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b23dc-126">NOTES</span></span>

## <span data-ttu-id="b23dc-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b23dc-127">RELATED LINKS</span></span>

[<span data-ttu-id="b23dc-128">Var olan uygulama ağ geçidine araştırma ekleme</span><span class="sxs-lookup"><span data-stu-id="b23dc-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="b23dc-129">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b23dc-129">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="b23dc-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b23dc-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="b23dc-131">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b23dc-131">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="b23dc-132">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b23dc-132">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

