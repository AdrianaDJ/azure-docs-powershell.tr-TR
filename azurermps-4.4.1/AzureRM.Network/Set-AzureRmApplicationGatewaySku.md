---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: b1680d18e11851718ca6d9d49acf4dc9501e1aad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590720"
---
# <span data-ttu-id="cad27-101">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="cad27-101">Set-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="cad27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cad27-102">SYNOPSIS</span></span>
<span data-ttu-id="cad27-103">Uygulama ağ geçidi SKU 'sunda değişiklik yapar.</span><span class="sxs-lookup"><span data-stu-id="cad27-103">Modifies the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cad27-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cad27-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 -Capacity <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cad27-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cad27-105">DESCRIPTION</span></span>
<span data-ttu-id="cad27-106">**Set-AzureRmApplicationGatewaySku** cmdlet 'i, bir uygulama ağ geçidinin stok tutma BIRIMINI (STB) değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cad27-106">The **Set-AzureRmApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="cad27-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cad27-107">EXAMPLES</span></span>

### <span data-ttu-id="cad27-108">Örnek 1: uygulama ağ geçidi SKU 'YU güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="cad27-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="cad27-109">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cad27-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="cad27-110">İkinci komut, uygulama ağ geçidinin SKU adını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cad27-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="cad27-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cad27-111">PARAMETERS</span></span>

### <span data-ttu-id="cad27-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cad27-112">-ApplicationGateway</span></span>
<span data-ttu-id="cad27-113">Bu cmdlet 'in SKU 'YU ilişkilendiren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cad27-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="cad27-114">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="cad27-114">-Capacity</span></span>
<span data-ttu-id="cad27-115">Uygulama ağ geçidinin örnek sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cad27-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad27-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="cad27-116">-Name</span></span>
<span data-ttu-id="cad27-117">Uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cad27-117">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="cad27-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="cad27-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cad27-119">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="cad27-119">Standard_Small</span></span>
- <span data-ttu-id="cad27-120">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="cad27-120">Standard_Medium</span></span>
- <span data-ttu-id="cad27-121">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="cad27-121">Standard_Large</span></span>
- <span data-ttu-id="cad27-122">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="cad27-122">WAF_Medium</span></span>
- <span data-ttu-id="cad27-123">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="cad27-123">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad27-124">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="cad27-124">-Tier</span></span>
<span data-ttu-id="cad27-125">Uygulama ağ geçidinin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cad27-125">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="cad27-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="cad27-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cad27-127">Ardından</span><span class="sxs-lookup"><span data-stu-id="cad27-127">Standard</span></span>
- <span data-ttu-id="cad27-128">WAF</span><span class="sxs-lookup"><span data-stu-id="cad27-128">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad27-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cad27-129">-DefaultProfile</span></span>
<span data-ttu-id="cad27-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cad27-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cad27-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cad27-131">CommonParameters</span></span>
<span data-ttu-id="cad27-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cad27-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cad27-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cad27-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cad27-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cad27-134">INPUTS</span></span>

### <span data-ttu-id="cad27-135">System. String</span><span class="sxs-lookup"><span data-stu-id="cad27-135">System.String</span></span>

## <span data-ttu-id="cad27-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cad27-136">OUTPUTS</span></span>

### <span data-ttu-id="cad27-137">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cad27-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cad27-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cad27-138">NOTES</span></span>

## <span data-ttu-id="cad27-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cad27-139">RELATED LINKS</span></span>

[<span data-ttu-id="cad27-140">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="cad27-140">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="cad27-141">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="cad27-141">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

