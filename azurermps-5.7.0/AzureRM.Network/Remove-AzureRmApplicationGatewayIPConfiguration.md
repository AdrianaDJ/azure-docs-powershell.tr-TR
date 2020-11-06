---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 823b4ce458e4308965b4c5bea1ad5739708f7aff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594467"
---
# <span data-ttu-id="12be0-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="12be0-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="12be0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12be0-102">SYNOPSIS</span></span>
<span data-ttu-id="12be0-103">Uygulama ağ geçidinden IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="12be0-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12be0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12be0-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12be0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="12be0-105">DESCRIPTION</span></span>
<span data-ttu-id="12be0-106">**Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet 'i, bir Azure uygulama ağ geçidinden IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="12be0-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="12be0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12be0-107">EXAMPLES</span></span>

### <span data-ttu-id="12be0-108">Örnek 1: Azure uygulama ağ geçidinden IP yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="12be0-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="12be0-109">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="12be0-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="12be0-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden Subnet02 adlı IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="12be0-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="12be0-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12be0-111">PARAMETERS</span></span>

### <span data-ttu-id="12be0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12be0-112">-ApplicationGateway</span></span>
<span data-ttu-id="12be0-113">IP yapılandırmasının kaldırılacağı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="12be0-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="12be0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12be0-114">-DefaultProfile</span></span>
<span data-ttu-id="12be0-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="12be0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12be0-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="12be0-116">-Name</span></span>
<span data-ttu-id="12be0-117">Kaldırılacak IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="12be0-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="12be0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12be0-118">CommonParameters</span></span>
<span data-ttu-id="12be0-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12be0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12be0-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12be0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12be0-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12be0-121">INPUTS</span></span>

### <span data-ttu-id="12be0-122">System. String</span><span class="sxs-lookup"><span data-stu-id="12be0-122">System.String</span></span>

## <span data-ttu-id="12be0-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12be0-123">OUTPUTS</span></span>

### <span data-ttu-id="12be0-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12be0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="12be0-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12be0-125">NOTES</span></span>

## <span data-ttu-id="12be0-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12be0-126">RELATED LINKS</span></span>

[<span data-ttu-id="12be0-127">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="12be0-127">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="12be0-128">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="12be0-128">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="12be0-129">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="12be0-129">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="12be0-130">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="12be0-130">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


