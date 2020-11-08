---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 212ba438a701b9abbd2fd290f4fb0f867b551497
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104775"
---
# <span data-ttu-id="e781f-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e781f-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="e781f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e781f-102">SYNOPSIS</span></span>
<span data-ttu-id="e781f-103">Uygulama ağ geçidi için SKU oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e781f-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="e781f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e781f-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e781f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e781f-105">DESCRIPTION</span></span>
<span data-ttu-id="e781f-106">**Yeni-AzApplicationGatewaySku** cmdlet 'i, bir Azure uygulama ağ geçidi için bir stok saklama BIRIMI (SKU) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e781f-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="e781f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e781f-107">EXAMPLES</span></span>

### <span data-ttu-id="e781f-108">Örnek 1: Azure uygulaması ağ geçidi için SKU oluşturma</span><span class="sxs-lookup"><span data-stu-id="e781f-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="e781f-109">Bu komut, Azure Application Gateway için Standard_Small adlı bir SKU oluşturur ve sonucu $SKU adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="e781f-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="e781f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e781f-110">PARAMETERS</span></span>

### <span data-ttu-id="e781f-111">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="e781f-111">-Capacity</span></span>
<span data-ttu-id="e781f-112">Uygulama ağ geçidi örneklerinin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e781f-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="e781f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e781f-113">-DefaultProfile</span></span>
<span data-ttu-id="e781f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e781f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e781f-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e781f-115">-Name</span></span>
<span data-ttu-id="e781f-116">SKU 'nun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e781f-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="e781f-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e781f-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e781f-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="e781f-118">Standard_Small</span></span>
- <span data-ttu-id="e781f-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="e781f-119">Standard_Medium</span></span>
- <span data-ttu-id="e781f-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="e781f-120">Standard_Large</span></span>
- <span data-ttu-id="e781f-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="e781f-121">WAF_Medium</span></span>
- <span data-ttu-id="e781f-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="e781f-122">WAF_Large</span></span>
- <span data-ttu-id="e781f-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="e781f-123">Standard_v2</span></span>
- <span data-ttu-id="e781f-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="e781f-124">WAF_v2</span></span>

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

### <span data-ttu-id="e781f-125">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="e781f-125">-Tier</span></span>
<span data-ttu-id="e781f-126">SKU 'nun katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e781f-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="e781f-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e781f-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e781f-128">Ardından</span><span class="sxs-lookup"><span data-stu-id="e781f-128">Standard</span></span>
- <span data-ttu-id="e781f-129">WAF</span><span class="sxs-lookup"><span data-stu-id="e781f-129">WAF</span></span>
- <span data-ttu-id="e781f-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="e781f-130">Standard_v2</span></span>
- <span data-ttu-id="e781f-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="e781f-131">WAF_v2</span></span>

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

### <span data-ttu-id="e781f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e781f-132">CommonParameters</span></span>
<span data-ttu-id="e781f-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e781f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e781f-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e781f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e781f-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e781f-135">INPUTS</span></span>

### <span data-ttu-id="e781f-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e781f-136">None</span></span>

## <span data-ttu-id="e781f-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e781f-137">OUTPUTS</span></span>

### <span data-ttu-id="e781f-138">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e781f-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="e781f-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e781f-139">NOTES</span></span>

## <span data-ttu-id="e781f-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e781f-140">RELATED LINKS</span></span>

[<span data-ttu-id="e781f-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e781f-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="e781f-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e781f-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


