---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 320588b81791c033b94a07261f769fa0886d2f2c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935321"
---
# <span data-ttu-id="6cb62-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6cb62-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="6cb62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cb62-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb62-103">Var olan uygulama ağ geçidinden sistem durumu araştır'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6cb62-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="6cb62-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6cb62-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cb62-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6cb62-105">DESCRIPTION</span></span>
<span data-ttu-id="6cb62-106">Remove-AzApplicationGatewayProbeConfig cmdlet, var olan uygulama ağ geçidinden bir üst bir araştırma kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6cb62-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="6cb62-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6cb62-107">EXAMPLES</span></span>

### <span data-ttu-id="6cb62-108">Örnek 1: var olan uygulama ağ geçidinden sistem durumu araştırması kaldırma</span><span class="sxs-lookup"><span data-stu-id="6cb62-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="6cb62-109">Bu komut, Probe04 adındaki uygulama ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="6cb62-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="6cb62-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6cb62-110">PARAMETERS</span></span>

### <span data-ttu-id="6cb62-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6cb62-111">-ApplicationGateway</span></span>
<span data-ttu-id="6cb62-112">Bu cmdlet 'in bir araştırın kaldırıldığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6cb62-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="6cb62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb62-113">-DefaultProfile</span></span>
<span data-ttu-id="6cb62-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6cb62-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cb62-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="6cb62-115">-Name</span></span>
<span data-ttu-id="6cb62-116">Bu cmdlet 'in kaldırıldığı araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6cb62-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="6cb62-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb62-117">CommonParameters</span></span>
<span data-ttu-id="6cb62-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6cb62-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb62-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cb62-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb62-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6cb62-120">INPUTS</span></span>

### <span data-ttu-id="6cb62-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6cb62-121">PSApplicationGateway</span></span>
<span data-ttu-id="6cb62-122">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6cb62-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="6cb62-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6cb62-123">OUTPUTS</span></span>

### <span data-ttu-id="6cb62-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6cb62-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6cb62-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6cb62-125">NOTES</span></span>

## <span data-ttu-id="6cb62-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6cb62-126">RELATED LINKS</span></span>

[<span data-ttu-id="6cb62-127">Var olan uygulama ağ geçidinden bir araştırın kaldırma</span><span class="sxs-lookup"><span data-stu-id="6cb62-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="6cb62-128">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6cb62-128">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="6cb62-129">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6cb62-129">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="6cb62-130">Yeni-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6cb62-130">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="6cb62-131">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6cb62-131">Set-AzApplicationGatewayProbeConfig</span></span>]()

