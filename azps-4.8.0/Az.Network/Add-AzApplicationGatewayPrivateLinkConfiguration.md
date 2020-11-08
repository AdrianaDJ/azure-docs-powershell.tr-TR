---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2083dd00c5163a67492ff9973fdf7399d67d7cb6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107716"
---
# <span data-ttu-id="19f1d-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="19f1d-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="19f1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="19f1d-103">Uygulama ağ geçidine özel bağlantı yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="19f1d-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="19f1d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19f1d-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19f1d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="19f1d-105">DESCRIPTION</span></span>
<span data-ttu-id="19f1d-106">**Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet 'i, bir uygulama ağ geçidine özel bağlantı yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="19f1d-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="19f1d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19f1d-107">EXAMPLES</span></span>

### <span data-ttu-id="19f1d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="19f1d-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="19f1d-109">İlk komut Privatelinkıp yapılandırması oluşturur ve $PrivateLinkIpConfiguration değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="19f1d-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="19f1d-110">İkinci komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="19f1d-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="19f1d-111">Üçüncü komut, $AppGw ağ geçidi için privateLinkConfig01 adlı özel bağlantı yapılandırmasını ekler</span><span class="sxs-lookup"><span data-stu-id="19f1d-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="19f1d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19f1d-112">PARAMETERS</span></span>

### <span data-ttu-id="19f1d-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19f1d-113">-ApplicationGateway</span></span>
<span data-ttu-id="19f1d-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19f1d-114">The applicationGateway</span></span>

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

### <span data-ttu-id="19f1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19f1d-115">-DefaultProfile</span></span>
<span data-ttu-id="19f1d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="19f1d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f1d-117">-IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="19f1d-117">-IpConfiguration</span></span>
<span data-ttu-id="19f1d-118">IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="19f1d-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19f1d-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="19f1d-119">-Name</span></span>
<span data-ttu-id="19f1d-120">PrivateLink yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="19f1d-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="19f1d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19f1d-121">CommonParameters</span></span>
<span data-ttu-id="19f1d-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19f1d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19f1d-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="19f1d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19f1d-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19f1d-124">INPUTS</span></span>

### <span data-ttu-id="19f1d-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19f1d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="19f1d-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="19f1d-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="19f1d-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19f1d-127">OUTPUTS</span></span>

### <span data-ttu-id="19f1d-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19f1d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="19f1d-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19f1d-129">NOTES</span></span>

## <span data-ttu-id="19f1d-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19f1d-130">RELATED LINKS</span></span>

[<span data-ttu-id="19f1d-131">Yeni-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="19f1d-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="19f1d-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="19f1d-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="19f1d-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="19f1d-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="19f1d-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="19f1d-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)