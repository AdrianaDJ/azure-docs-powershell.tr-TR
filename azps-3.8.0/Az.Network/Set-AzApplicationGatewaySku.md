---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
ms.openlocfilehash: bfaf9773582b201de8f6066a30a55c0fd5f5b7ac
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937332"
---
# <span data-ttu-id="77daf-101">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="77daf-101">Set-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="77daf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77daf-102">SYNOPSIS</span></span>
<span data-ttu-id="77daf-103">Uygulama ağ geçidi SKU 'sunda değişiklik yapar.</span><span class="sxs-lookup"><span data-stu-id="77daf-103">Modifies the SKU of an application gateway.</span></span>

## <span data-ttu-id="77daf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="77daf-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77daf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="77daf-105">DESCRIPTION</span></span>
<span data-ttu-id="77daf-106">**Set-AzApplicationGatewaySku** cmdlet 'i, bir uygulama ağ geçidinin stok tutma BIRIMINI (SKU) değiştirir.</span><span class="sxs-lookup"><span data-stu-id="77daf-106">The **Set-AzApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="77daf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="77daf-107">EXAMPLES</span></span>

### <span data-ttu-id="77daf-108">Örnek 1: uygulama ağ geçidi SKU 'YU güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="77daf-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="77daf-109">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="77daf-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="77daf-110">İkinci komut, uygulama ağ geçidinin SKU adını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="77daf-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="77daf-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="77daf-111">PARAMETERS</span></span>

### <span data-ttu-id="77daf-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="77daf-112">-ApplicationGateway</span></span>
<span data-ttu-id="77daf-113">Bu cmdlet 'in SKU 'YU ilişkilendiren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="77daf-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="77daf-114">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="77daf-114">-Capacity</span></span>
<span data-ttu-id="77daf-115">Uygulama ağ geçidinin örnek sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="77daf-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77daf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77daf-116">-DefaultProfile</span></span>
<span data-ttu-id="77daf-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="77daf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77daf-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="77daf-118">-Name</span></span>
<span data-ttu-id="77daf-119">Uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="77daf-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="77daf-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="77daf-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="77daf-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="77daf-121">Standard_Small</span></span>
- <span data-ttu-id="77daf-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="77daf-122">Standard_Medium</span></span>
- <span data-ttu-id="77daf-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="77daf-123">Standard_Large</span></span>
- <span data-ttu-id="77daf-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="77daf-124">WAF_Medium</span></span>
- <span data-ttu-id="77daf-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="77daf-125">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77daf-126">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="77daf-126">-Tier</span></span>
<span data-ttu-id="77daf-127">Uygulama ağ geçidinin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="77daf-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="77daf-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="77daf-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="77daf-129">Ardından</span><span class="sxs-lookup"><span data-stu-id="77daf-129">Standard</span></span>
- <span data-ttu-id="77daf-130">WAF</span><span class="sxs-lookup"><span data-stu-id="77daf-130">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, WAF, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77daf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77daf-131">CommonParameters</span></span>
<span data-ttu-id="77daf-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="77daf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77daf-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77daf-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77daf-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="77daf-134">INPUTS</span></span>

### <span data-ttu-id="77daf-135">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="77daf-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="77daf-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="77daf-136">OUTPUTS</span></span>

### <span data-ttu-id="77daf-137">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="77daf-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="77daf-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="77daf-138">NOTES</span></span>

## <span data-ttu-id="77daf-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="77daf-139">RELATED LINKS</span></span>

[<span data-ttu-id="77daf-140">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="77daf-140">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="77daf-141">Yeni-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="77daf-141">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

