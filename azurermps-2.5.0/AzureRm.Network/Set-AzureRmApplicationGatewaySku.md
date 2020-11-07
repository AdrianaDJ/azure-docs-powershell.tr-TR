---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysku
schema: 2.0.0
ms.openlocfilehash: ccefc75d28ee49f12dd1f72d03512e3850298986
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939267"
---
# <span data-ttu-id="c36e0-101">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="c36e0-101">Set-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="c36e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c36e0-102">SYNOPSIS</span></span>
<span data-ttu-id="c36e0-103">Uygulama ağ geçidi SKU 'sunda değişiklik yapar.</span><span class="sxs-lookup"><span data-stu-id="c36e0-103">Modifies the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c36e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c36e0-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 -Capacity <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c36e0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c36e0-105">DESCRIPTION</span></span>
<span data-ttu-id="c36e0-106">**Set-AzureRmApplicationGatewaySku** cmdlet 'i, bir uygulama ağ geçidinin stok tutma BIRIMINI (STB) değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c36e0-106">The **Set-AzureRmApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="c36e0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c36e0-107">EXAMPLES</span></span>

### <span data-ttu-id="c36e0-108">Örnek 1: uygulama ağ geçidi SKU 'YU güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c36e0-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="c36e0-109">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c36e0-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="c36e0-110">İkinci komut, uygulama ağ geçidinin SKU adını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c36e0-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="c36e0-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c36e0-111">PARAMETERS</span></span>

### <span data-ttu-id="c36e0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c36e0-112">-ApplicationGateway</span></span>
<span data-ttu-id="c36e0-113">Bu cmdlet 'in SKU 'YU ilişkilendiren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c36e0-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="c36e0-114">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="c36e0-114">-Capacity</span></span>
<span data-ttu-id="c36e0-115">Uygulama ağ geçidinin örnek sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c36e0-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c36e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c36e0-116">-DefaultProfile</span></span>
<span data-ttu-id="c36e0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c36e0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c36e0-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="c36e0-118">-Name</span></span>
<span data-ttu-id="c36e0-119">Uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c36e0-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="c36e0-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c36e0-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c36e0-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="c36e0-121">Standard_Small</span></span>
- <span data-ttu-id="c36e0-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="c36e0-122">Standard_Medium</span></span>
- <span data-ttu-id="c36e0-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="c36e0-123">Standard_Large</span></span>
- <span data-ttu-id="c36e0-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="c36e0-124">WAF_Medium</span></span>
- <span data-ttu-id="c36e0-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="c36e0-125">WAF_Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c36e0-126">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="c36e0-126">-Tier</span></span>
<span data-ttu-id="c36e0-127">Uygulama ağ geçidinin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c36e0-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="c36e0-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c36e0-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c36e0-129">Ardından</span><span class="sxs-lookup"><span data-stu-id="c36e0-129">Standard</span></span>
- <span data-ttu-id="c36e0-130">WAF</span><span class="sxs-lookup"><span data-stu-id="c36e0-130">WAF</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c36e0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c36e0-131">CommonParameters</span></span>
<span data-ttu-id="c36e0-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c36e0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c36e0-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c36e0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c36e0-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c36e0-134">INPUTS</span></span>

### <span data-ttu-id="c36e0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c36e0-135">System.String</span></span>

## <span data-ttu-id="c36e0-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c36e0-136">OUTPUTS</span></span>

### <span data-ttu-id="c36e0-137">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c36e0-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c36e0-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c36e0-138">NOTES</span></span>

## <span data-ttu-id="c36e0-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c36e0-139">RELATED LINKS</span></span>

[<span data-ttu-id="c36e0-140">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="c36e0-140">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="c36e0-141">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="c36e0-141">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)


