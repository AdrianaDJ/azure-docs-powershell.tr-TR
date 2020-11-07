---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 7eb80c50674eeea374dcffbe2d6838d46bf2643e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932071"
---
# <span data-ttu-id="adb79-101">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="adb79-101">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="adb79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adb79-102">SYNOPSIS</span></span>
<span data-ttu-id="adb79-103">Uygulama ağ geçidinin otomatik ölçeklendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="adb79-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="adb79-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="adb79-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adb79-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="adb79-105">DESCRIPTION</span></span>
<span data-ttu-id="adb79-106">**Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet 'ı uygulama ağ geçidinin otomatik ölçeklendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="adb79-106">The **Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="adb79-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="adb79-107">EXAMPLES</span></span>

### <span data-ttu-id="adb79-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="adb79-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="adb79-109">İlk komut uygulama ağ geçidini alır ve $gw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="adb79-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="adb79-110">İkinci komut, uygulama ağ geçidinden otomatik ölçeklendirme yapılandırmasını ayıklar.</span><span class="sxs-lookup"><span data-stu-id="adb79-110">The second command extracts out the autoscale configuration from the application gateway.</span></span>

## <span data-ttu-id="adb79-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="adb79-111">PARAMETERS</span></span>

### <span data-ttu-id="adb79-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="adb79-112">-ApplicationGateway</span></span>
<span data-ttu-id="adb79-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="adb79-113">The applicationGateway</span></span>

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

### <span data-ttu-id="adb79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adb79-114">-DefaultProfile</span></span>
<span data-ttu-id="adb79-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="adb79-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adb79-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb79-116">CommonParameters</span></span>
<span data-ttu-id="adb79-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="adb79-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb79-118">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="adb79-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb79-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="adb79-119">INPUTS</span></span>

### <span data-ttu-id="adb79-120">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="adb79-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="adb79-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="adb79-121">OUTPUTS</span></span>

### <span data-ttu-id="adb79-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="adb79-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="adb79-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="adb79-123">NOTES</span></span>

## <span data-ttu-id="adb79-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="adb79-124">RELATED LINKS</span></span>

[<span data-ttu-id="adb79-125">Yeni-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="adb79-125">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="adb79-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="adb79-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="adb79-127">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="adb79-127">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
