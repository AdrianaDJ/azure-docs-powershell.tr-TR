---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 0d4e1977e0985dbe82731376bd78547ce21251e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592932"
---
# <span data-ttu-id="0e27a-101">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="0e27a-101">Set-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="0e27a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e27a-102">SYNOPSIS</span></span>
<span data-ttu-id="0e27a-103">Uygulama ağ geçidi SKU 'sunda değişiklik yapar.</span><span class="sxs-lookup"><span data-stu-id="0e27a-103">Modifies the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e27a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e27a-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 -Capacity <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e27a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e27a-105">DESCRIPTION</span></span>
<span data-ttu-id="0e27a-106">**Set-AzureRmApplicationGatewaySku** cmdlet 'i, bir uygulama ağ geçidinin stok tutma BIRIMINI (STB) değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0e27a-106">The **Set-AzureRmApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="0e27a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e27a-107">EXAMPLES</span></span>

### <span data-ttu-id="0e27a-108">Örnek 1: uygulama ağ geçidi SKU 'YU güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0e27a-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="0e27a-109">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0e27a-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="0e27a-110">İkinci komut, uygulama ağ geçidinin SKU adını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0e27a-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="0e27a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e27a-111">PARAMETERS</span></span>

### <span data-ttu-id="0e27a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e27a-112">-ApplicationGateway</span></span>
<span data-ttu-id="0e27a-113">Bu cmdlet 'in SKU 'YU ilişkilendiren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e27a-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="0e27a-114">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="0e27a-114">-Capacity</span></span>
<span data-ttu-id="0e27a-115">Uygulama ağ geçidinin örnek sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e27a-115">Specifies the instance count of the application gateway.</span></span>

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

### <span data-ttu-id="0e27a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e27a-116">-DefaultProfile</span></span>
<span data-ttu-id="0e27a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0e27a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e27a-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="0e27a-118">-Name</span></span>
<span data-ttu-id="0e27a-119">Uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e27a-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="0e27a-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0e27a-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0e27a-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="0e27a-121">Standard_Small</span></span>
- <span data-ttu-id="0e27a-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="0e27a-122">Standard_Medium</span></span>
- <span data-ttu-id="0e27a-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="0e27a-123">Standard_Large</span></span>
- <span data-ttu-id="0e27a-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="0e27a-124">WAF_Medium</span></span>
- <span data-ttu-id="0e27a-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="0e27a-125">WAF_Large</span></span>

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

### <span data-ttu-id="0e27a-126">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="0e27a-126">-Tier</span></span>
<span data-ttu-id="0e27a-127">Uygulama ağ geçidinin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e27a-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="0e27a-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0e27a-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0e27a-129">Ardından</span><span class="sxs-lookup"><span data-stu-id="0e27a-129">Standard</span></span>
- <span data-ttu-id="0e27a-130">WAF</span><span class="sxs-lookup"><span data-stu-id="0e27a-130">WAF</span></span>

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

### <span data-ttu-id="0e27a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e27a-131">CommonParameters</span></span>
<span data-ttu-id="0e27a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e27a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e27a-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e27a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e27a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e27a-134">INPUTS</span></span>

### <span data-ttu-id="0e27a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0e27a-135">System.String</span></span>

## <span data-ttu-id="0e27a-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e27a-136">OUTPUTS</span></span>

### <span data-ttu-id="0e27a-137">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e27a-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0e27a-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e27a-138">NOTES</span></span>

## <span data-ttu-id="0e27a-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e27a-139">RELATED LINKS</span></span>

[<span data-ttu-id="0e27a-140">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="0e27a-140">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="0e27a-141">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="0e27a-141">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)


