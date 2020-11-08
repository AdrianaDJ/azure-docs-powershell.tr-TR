---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2c9f006c9e719380abd1f1f5dbb6c6233346a563
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279995"
---
# <span data-ttu-id="5b910-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b910-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="5b910-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b910-102">SYNOPSIS</span></span>
<span data-ttu-id="5b910-103">Uygulama ağ geçidinin özel bağlantı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="5b910-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="5b910-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b910-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b910-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b910-105">DESCRIPTION</span></span>
<span data-ttu-id="5b910-106">**Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet 'i, bir uygulama ağ geçidinin özel bağlantı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="5b910-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="5b910-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b910-107">EXAMPLES</span></span>

### <span data-ttu-id="5b910-108">Örnek 1: belirtilen özel bağlantı yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="5b910-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="5b910-109">İlk komut, ResourceGroup01 adındaki kaynak grubundan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5b910-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5b910-110">İkinci komut, $AppGw privateLinkConfig01 adındaki özel bağlantı yapılandırmasını alır ve bunu $PrivateLinkConfiguration değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5b910-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="5b910-111">Örnek 2: özel bağlantı yapılandırmasının listesini alma</span><span class="sxs-lookup"><span data-stu-id="5b910-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="5b910-112">İlk komut, ResourceGroup01 adındaki kaynak grubundan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5b910-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5b910-113">İkinci komut $AppGw 'dan tüm özel bağlantı yapılandırmalarını alır ve $PrivateLinkConfigurations değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5b910-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="5b910-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b910-114">PARAMETERS</span></span>

### <span data-ttu-id="5b910-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b910-115">-ApplicationGateway</span></span>
<span data-ttu-id="5b910-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b910-116">The applicationGateway</span></span>

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

### <span data-ttu-id="5b910-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b910-117">-DefaultProfile</span></span>
<span data-ttu-id="5b910-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5b910-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b910-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="5b910-119">-Name</span></span>
<span data-ttu-id="5b910-120">Uygulama ağ geçidi privateLink yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="5b910-120">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="5b910-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b910-121">CommonParameters</span></span>
<span data-ttu-id="5b910-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b910-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b910-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5b910-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b910-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b910-124">INPUTS</span></span>

### <span data-ttu-id="5b910-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b910-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5b910-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b910-126">OUTPUTS</span></span>

### <span data-ttu-id="5b910-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b910-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="5b910-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b910-128">NOTES</span></span>

## <span data-ttu-id="5b910-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b910-129">RELATED LINKS</span></span>

[<span data-ttu-id="5b910-130">Yeni-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b910-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="5b910-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b910-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="5b910-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b910-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="5b910-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b910-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)