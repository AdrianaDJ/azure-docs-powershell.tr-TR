---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: 39ce61f4a1e973dfdac8104a6364bdd3d8b9151a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939901"
---
# <span data-ttu-id="24453-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="24453-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="24453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24453-102">SYNOPSIS</span></span>
<span data-ttu-id="24453-103">Var olan uygulama ağ geçidinden sistem durumu araştır'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="24453-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24453-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24453-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24453-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="24453-105">DESCRIPTION</span></span>
<span data-ttu-id="24453-106">Remove-AzureRmApplicationGatewayProbeConfig cmdlet, var olan uygulama ağ geçidinden bir üst bir araştırma kaldırır.</span><span class="sxs-lookup"><span data-stu-id="24453-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="24453-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24453-107">EXAMPLES</span></span>

### <span data-ttu-id="24453-108">Örnek 1: var olan uygulama ağ geçidinden sistem durumu araştırması kaldırma</span><span class="sxs-lookup"><span data-stu-id="24453-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="24453-109">Bu komut, Probe04 adındaki uygulama ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="24453-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="24453-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24453-110">PARAMETERS</span></span>

### <span data-ttu-id="24453-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24453-111">-ApplicationGateway</span></span>
<span data-ttu-id="24453-112">Bu cmdlet 'in bir araştırın kaldırıldığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="24453-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="24453-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24453-113">-DefaultProfile</span></span>
<span data-ttu-id="24453-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="24453-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24453-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="24453-115">-Name</span></span>
<span data-ttu-id="24453-116">Bu cmdlet 'in kaldırıldığı araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24453-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="24453-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24453-117">CommonParameters</span></span>
<span data-ttu-id="24453-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24453-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24453-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24453-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24453-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24453-120">INPUTS</span></span>

### <span data-ttu-id="24453-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24453-121">PSApplicationGateway</span></span>
<span data-ttu-id="24453-122">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="24453-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="24453-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24453-123">OUTPUTS</span></span>

### <span data-ttu-id="24453-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24453-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="24453-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24453-125">NOTES</span></span>

## <span data-ttu-id="24453-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24453-126">RELATED LINKS</span></span>

[<span data-ttu-id="24453-127">Var olan uygulama ağ geçidinden bir araştırın kaldırma</span><span class="sxs-lookup"><span data-stu-id="24453-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="24453-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="24453-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="24453-129">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="24453-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="24453-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="24453-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="24453-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="24453-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

