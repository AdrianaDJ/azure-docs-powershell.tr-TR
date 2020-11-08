---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 212ba438a701b9abbd2fd290f4fb0f867b551497
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274383"
---
# <span data-ttu-id="d5e4f-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="d5e4f-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="d5e4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="d5e4f-103">Uygulama ağ geçidi için SKU oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d5e4f-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="d5e4f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5e4f-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5e4f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5e4f-105">DESCRIPTION</span></span>
<span data-ttu-id="d5e4f-106">**Yeni-AzApplicationGatewaySku** cmdlet 'i, bir Azure uygulama ağ geçidi için bir stok saklama BIRIMI (SKU) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d5e4f-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="d5e4f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5e4f-107">EXAMPLES</span></span>

### <span data-ttu-id="d5e4f-108">Örnek 1: Azure uygulaması ağ geçidi için SKU oluşturma</span><span class="sxs-lookup"><span data-stu-id="d5e4f-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="d5e4f-109">Bu komut, Azure Application Gateway için Standard_Small adlı bir SKU oluşturur ve sonucu $SKU adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="d5e4f-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="d5e4f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5e4f-110">PARAMETERS</span></span>

### <span data-ttu-id="d5e4f-111">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="d5e4f-111">-Capacity</span></span>
<span data-ttu-id="d5e4f-112">Uygulama ağ geçidi örneklerinin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5e4f-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="d5e4f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5e4f-113">-DefaultProfile</span></span>
<span data-ttu-id="d5e4f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d5e4f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5e4f-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d5e4f-115">-Name</span></span>
<span data-ttu-id="d5e4f-116">SKU 'nun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5e4f-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="d5e4f-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d5e4f-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d5e4f-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="d5e4f-118">Standard_Small</span></span>
- <span data-ttu-id="d5e4f-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="d5e4f-119">Standard_Medium</span></span>
- <span data-ttu-id="d5e4f-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="d5e4f-120">Standard_Large</span></span>
- <span data-ttu-id="d5e4f-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="d5e4f-121">WAF_Medium</span></span>
- <span data-ttu-id="d5e4f-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="d5e4f-122">WAF_Large</span></span>
- <span data-ttu-id="d5e4f-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="d5e4f-123">Standard_v2</span></span>
- <span data-ttu-id="d5e4f-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="d5e4f-124">WAF_v2</span></span>

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

### <span data-ttu-id="d5e4f-125">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="d5e4f-125">-Tier</span></span>
<span data-ttu-id="d5e4f-126">SKU 'nun katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5e4f-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="d5e4f-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d5e4f-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d5e4f-128">Ardından</span><span class="sxs-lookup"><span data-stu-id="d5e4f-128">Standard</span></span>
- <span data-ttu-id="d5e4f-129">WAF</span><span class="sxs-lookup"><span data-stu-id="d5e4f-129">WAF</span></span>
- <span data-ttu-id="d5e4f-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="d5e4f-130">Standard_v2</span></span>
- <span data-ttu-id="d5e4f-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="d5e4f-131">WAF_v2</span></span>

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

### <span data-ttu-id="d5e4f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5e4f-132">CommonParameters</span></span>
<span data-ttu-id="d5e4f-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5e4f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5e4f-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5e4f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5e4f-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5e4f-135">INPUTS</span></span>

### <span data-ttu-id="d5e4f-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d5e4f-136">None</span></span>

## <span data-ttu-id="d5e4f-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5e4f-137">OUTPUTS</span></span>

### <span data-ttu-id="d5e4f-138">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="d5e4f-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="d5e4f-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5e4f-139">NOTES</span></span>

## <span data-ttu-id="d5e4f-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5e4f-140">RELATED LINKS</span></span>

[<span data-ttu-id="d5e4f-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="d5e4f-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="d5e4f-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="d5e4f-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


