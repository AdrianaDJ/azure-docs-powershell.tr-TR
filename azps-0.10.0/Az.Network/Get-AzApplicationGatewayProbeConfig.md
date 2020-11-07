---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: b3e2b3ea03ca0bae0db1bea1606e4ae6b94a597e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935584"
---
# <span data-ttu-id="271f2-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="271f2-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="271f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="271f2-102">SYNOPSIS</span></span>
<span data-ttu-id="271f2-103">Uygulama ağ geçidinden var olan bir sistem durumu araştırması yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="271f2-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="271f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="271f2-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="271f2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="271f2-105">DESCRIPTION</span></span>
<span data-ttu-id="271f2-106">Get-AzApplicationGatewayProbeConfig cmdlet 'i uygulama ağ geçidinden var olan bir sistem durumu araştırması yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="271f2-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="271f2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="271f2-107">EXAMPLES</span></span>

### <span data-ttu-id="271f2-108">Örnek 1: uygulama ağ geçidinden varolan bir araştırma alma</span><span class="sxs-lookup"><span data-stu-id="271f2-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="271f2-109">Bu komut ağ geçidi adlı uygulama ağ geçidinden Probe02 adlı sistem durumu araştırılmasını alır.</span><span class="sxs-lookup"><span data-stu-id="271f2-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="271f2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="271f2-110">PARAMETERS</span></span>

### <span data-ttu-id="271f2-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="271f2-111">-ApplicationGateway</span></span>
<span data-ttu-id="271f2-112">Bu cmdlet 'in yoklama yapılandırması aldığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="271f2-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="271f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="271f2-113">-DefaultProfile</span></span>
<span data-ttu-id="271f2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="271f2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="271f2-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="271f2-115">-Name</span></span>
<span data-ttu-id="271f2-116">Araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="271f2-116">Specifies the name of the probe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="271f2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="271f2-117">CommonParameters</span></span>
<span data-ttu-id="271f2-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="271f2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="271f2-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="271f2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="271f2-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="271f2-120">INPUTS</span></span>

### <span data-ttu-id="271f2-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="271f2-121">PSApplicationGateway</span></span>
<span data-ttu-id="271f2-122">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="271f2-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="271f2-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="271f2-123">OUTPUTS</span></span>

### <span data-ttu-id="271f2-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="271f2-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="271f2-125">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="271f2-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="271f2-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="271f2-126">NOTES</span></span>

## <span data-ttu-id="271f2-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="271f2-127">RELATED LINKS</span></span>

[<span data-ttu-id="271f2-128">Var olan uygulama ağ geçidine araştırma ekleme</span><span class="sxs-lookup"><span data-stu-id="271f2-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="271f2-129">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="271f2-129">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="271f2-130">Yeni-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="271f2-130">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="271f2-131">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="271f2-131">Remove-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="271f2-132">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="271f2-132">Set-AzApplicationGatewayProbeConfig</span></span>]()

