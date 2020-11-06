---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 4ef644fb92bf3f872a9e80aef2674a3ffb56747b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590735"
---
# <span data-ttu-id="4c118-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c118-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="4c118-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c118-102">SYNOPSIS</span></span>
<span data-ttu-id="4c118-103">Uygulama ağ geçidinden IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4c118-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c118-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c118-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c118-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c118-105">DESCRIPTION</span></span>
<span data-ttu-id="4c118-106">**Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet 'i, bir Azure uygulama ağ geçidinden IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4c118-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="4c118-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c118-107">EXAMPLES</span></span>

### <span data-ttu-id="4c118-108">Örnek 1: Azure uygulama ağ geçidinden IP yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="4c118-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="4c118-109">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4c118-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="4c118-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden Subnet02 adlı IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4c118-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="4c118-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c118-111">PARAMETERS</span></span>

### <span data-ttu-id="4c118-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c118-112">-ApplicationGateway</span></span>
<span data-ttu-id="4c118-113">IP yapılandırmasının kaldırılacağı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c118-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="4c118-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="4c118-114">-Name</span></span>
<span data-ttu-id="4c118-115">Kaldırılacak IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c118-115">Specifies the name of the IP configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c118-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c118-116">-DefaultProfile</span></span>
<span data-ttu-id="4c118-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c118-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c118-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c118-118">CommonParameters</span></span>
<span data-ttu-id="4c118-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c118-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c118-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c118-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c118-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c118-121">INPUTS</span></span>

### <span data-ttu-id="4c118-122">System. String</span><span class="sxs-lookup"><span data-stu-id="4c118-122">System.String</span></span>

## <span data-ttu-id="4c118-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c118-123">OUTPUTS</span></span>

### <span data-ttu-id="4c118-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c118-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4c118-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c118-125">NOTES</span></span>

## <span data-ttu-id="4c118-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c118-126">RELATED LINKS</span></span>

[<span data-ttu-id="4c118-127">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c118-127">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4c118-128">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c118-128">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4c118-129">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c118-129">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4c118-130">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c118-130">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


