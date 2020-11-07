---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 14d1aea928923d9da4eee089ae1e95c75289eb3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764703"
---
# <span data-ttu-id="f05d2-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f05d2-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="f05d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f05d2-102">SYNOPSIS</span></span>
<span data-ttu-id="f05d2-103">Var olan uygulama ağ geçidinden sistem durumu araştır'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f05d2-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f05d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f05d2-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f05d2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f05d2-105">DESCRIPTION</span></span>
<span data-ttu-id="f05d2-106">Remove-AzureRmApplicationGatewayProbeConfig cmdlet, var olan uygulama ağ geçidinden bir üst bir araştırma kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f05d2-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="f05d2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f05d2-107">EXAMPLES</span></span>

### <span data-ttu-id="f05d2-108">Örnek 1: var olan uygulama ağ geçidinden sistem durumu araştırması kaldırma</span><span class="sxs-lookup"><span data-stu-id="f05d2-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="f05d2-109">Bu komut, Probe04 adındaki uygulama ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="f05d2-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="f05d2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f05d2-110">PARAMETERS</span></span>

### <span data-ttu-id="f05d2-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f05d2-111">-ApplicationGateway</span></span>
<span data-ttu-id="f05d2-112">Bu cmdlet 'in bir araştırın kaldırıldığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f05d2-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="f05d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f05d2-113">-DefaultProfile</span></span>
<span data-ttu-id="f05d2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f05d2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f05d2-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="f05d2-115">-Name</span></span>
<span data-ttu-id="f05d2-116">Bu cmdlet 'in kaldırıldığı araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f05d2-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="f05d2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f05d2-117">CommonParameters</span></span>
<span data-ttu-id="f05d2-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f05d2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f05d2-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f05d2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f05d2-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f05d2-120">INPUTS</span></span>

### <span data-ttu-id="f05d2-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f05d2-121">PSApplicationGateway</span></span>
<span data-ttu-id="f05d2-122">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f05d2-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="f05d2-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f05d2-123">OUTPUTS</span></span>

### <span data-ttu-id="f05d2-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f05d2-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f05d2-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f05d2-125">NOTES</span></span>

## <span data-ttu-id="f05d2-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f05d2-126">RELATED LINKS</span></span>

[<span data-ttu-id="f05d2-127">Var olan uygulama ağ geçidinden bir araştırın kaldırma</span><span class="sxs-lookup"><span data-stu-id="f05d2-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="f05d2-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f05d2-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="f05d2-129">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f05d2-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="f05d2-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f05d2-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="f05d2-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f05d2-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

