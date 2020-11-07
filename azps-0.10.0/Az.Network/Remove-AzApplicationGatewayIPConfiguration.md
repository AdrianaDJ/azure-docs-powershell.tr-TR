---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 68fa8e24d9cdc5e5dbf04ed132e1eac4909973d4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935329"
---
# <span data-ttu-id="82dfe-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="82dfe-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="82dfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82dfe-102">SYNOPSIS</span></span>
<span data-ttu-id="82dfe-103">Uygulama ağ geçidinden IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="82dfe-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="82dfe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="82dfe-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82dfe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="82dfe-105">DESCRIPTION</span></span>
<span data-ttu-id="82dfe-106">**Remove-Azapplicationgatewayıpconfiguration** cmdlet 'i, bir Azure uygulama ağ geçidinden IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="82dfe-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="82dfe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="82dfe-107">EXAMPLES</span></span>

### <span data-ttu-id="82dfe-108">Örnek 1: Azure uygulama ağ geçidinden IP yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="82dfe-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="82dfe-109">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="82dfe-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="82dfe-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden Subnet02 adlı IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="82dfe-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="82dfe-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="82dfe-111">PARAMETERS</span></span>

### <span data-ttu-id="82dfe-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82dfe-112">-ApplicationGateway</span></span>
<span data-ttu-id="82dfe-113">IP yapılandırmasının kaldırılacağı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="82dfe-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="82dfe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82dfe-114">-DefaultProfile</span></span>
<span data-ttu-id="82dfe-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="82dfe-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82dfe-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="82dfe-116">-Name</span></span>
<span data-ttu-id="82dfe-117">Kaldırılacak IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="82dfe-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="82dfe-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82dfe-118">CommonParameters</span></span>
<span data-ttu-id="82dfe-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="82dfe-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82dfe-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82dfe-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82dfe-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="82dfe-121">INPUTS</span></span>

### <span data-ttu-id="82dfe-122">System. String</span><span class="sxs-lookup"><span data-stu-id="82dfe-122">System.String</span></span>

## <span data-ttu-id="82dfe-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="82dfe-123">OUTPUTS</span></span>

### <span data-ttu-id="82dfe-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82dfe-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="82dfe-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="82dfe-125">NOTES</span></span>

## <span data-ttu-id="82dfe-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="82dfe-126">RELATED LINKS</span></span>

[<span data-ttu-id="82dfe-127">Add-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="82dfe-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="82dfe-128">Get-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="82dfe-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="82dfe-129">Yeni-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="82dfe-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="82dfe-130">Set-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="82dfe-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


