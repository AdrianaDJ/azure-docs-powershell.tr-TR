---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: c7912f1a5d0539a0c81aff930cd94cb944e45bb7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935585"
---
# <span data-ttu-id="7e14c-101">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e14c-101">Get-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="7e14c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e14c-102">SYNOPSIS</span></span>
<span data-ttu-id="7e14c-103">Uygulama ağ geçidinin IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="7e14c-103">Gets the IP configuration of an application gateway.</span></span>

## <span data-ttu-id="7e14c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e14c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e14c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e14c-105">DESCRIPTION</span></span>
<span data-ttu-id="7e14c-106">**Get-Azapplicationgatewayıp** yapılandırması cmdlet 'i, bir uygulama ağ geçidinin IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="7e14c-106">The **Get-AzApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="7e14c-107">IP yapılandırması, uygulama ağ geçidinin dağıtıldığı alt ağı içerir.</span><span class="sxs-lookup"><span data-stu-id="7e14c-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="7e14c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e14c-108">EXAMPLES</span></span>

### <span data-ttu-id="7e14c-109">Örnek 1: belirli bir IP yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="7e14c-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="7e14c-110">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar. İkinci komut, $AppGw depolanan ağ geçidinden GateSubnet01 adlı bir IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="7e14c-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="7e14c-111">Örnek 2: IP yapılandırmalarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="7e14c-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="7e14c-112">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar. İkinci komut, tüm IP yapılandırmalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="7e14c-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="7e14c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e14c-113">PARAMETERS</span></span>

### <span data-ttu-id="7e14c-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e14c-114">-ApplicationGateway</span></span>
<span data-ttu-id="7e14c-115">IP yapılandırmasını içeren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e14c-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="7e14c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e14c-116">-DefaultProfile</span></span>
<span data-ttu-id="7e14c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e14c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e14c-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="7e14c-118">-Name</span></span>
<span data-ttu-id="7e14c-119">Bu cmdlet 'in aldığı IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e14c-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

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

### <span data-ttu-id="7e14c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e14c-120">CommonParameters</span></span>
<span data-ttu-id="7e14c-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e14c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e14c-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e14c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e14c-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e14c-123">INPUTS</span></span>

### <span data-ttu-id="7e14c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7e14c-124">System.String</span></span>

## <span data-ttu-id="7e14c-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e14c-125">OUTPUTS</span></span>

### <span data-ttu-id="7e14c-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e14c-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="7e14c-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e14c-127">NOTES</span></span>

## <span data-ttu-id="7e14c-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e14c-128">RELATED LINKS</span></span>

[<span data-ttu-id="7e14c-129">Add-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="7e14c-129">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="7e14c-130">Yeni-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="7e14c-130">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="7e14c-131">Remove-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="7e14c-131">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="7e14c-132">Set-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="7e14c-132">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)

