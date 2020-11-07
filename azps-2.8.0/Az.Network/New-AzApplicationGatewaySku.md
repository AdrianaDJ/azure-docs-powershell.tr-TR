---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 1d737733deb167510196555af4ad7b357cc60154
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918332"
---
# <span data-ttu-id="cb43b-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="cb43b-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="cb43b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb43b-102">SYNOPSIS</span></span>
<span data-ttu-id="cb43b-103">Uygulama ağ geçidi için SKU oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb43b-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="cb43b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb43b-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb43b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb43b-105">DESCRIPTION</span></span>
<span data-ttu-id="cb43b-106">**Yeni-AzApplicationGatewaySku** cmdlet 'i, bir Azure uygulama ağ geçidi için bir stok saklama BIRIMI (SKU) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb43b-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="cb43b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb43b-107">EXAMPLES</span></span>

### <span data-ttu-id="cb43b-108">Örnek 1: Azure uygulaması ağ geçidi için SKU oluşturma</span><span class="sxs-lookup"><span data-stu-id="cb43b-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="cb43b-109">Bu komut, Azure Application Gateway için Standard_Small adlı bir SKU oluşturur ve sonucu $SKU adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="cb43b-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="cb43b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb43b-110">PARAMETERS</span></span>

### <span data-ttu-id="cb43b-111">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="cb43b-111">-Capacity</span></span>
<span data-ttu-id="cb43b-112">Uygulama ağ geçidi örneklerinin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb43b-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="cb43b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb43b-113">-DefaultProfile</span></span>
<span data-ttu-id="cb43b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb43b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb43b-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb43b-115">-Name</span></span>
<span data-ttu-id="cb43b-116">SKU 'nun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb43b-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="cb43b-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="cb43b-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cb43b-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="cb43b-118">Standard_Small</span></span>
- <span data-ttu-id="cb43b-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="cb43b-119">Standard_Medium</span></span>
- <span data-ttu-id="cb43b-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="cb43b-120">Standard_Large</span></span>
- <span data-ttu-id="cb43b-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="cb43b-121">WAF_Medium</span></span>
- <span data-ttu-id="cb43b-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="cb43b-122">WAF_Large</span></span>

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

### <span data-ttu-id="cb43b-123">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="cb43b-123">-Tier</span></span>
<span data-ttu-id="cb43b-124">SKU 'nun katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb43b-124">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="cb43b-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="cb43b-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cb43b-126">Ardından</span><span class="sxs-lookup"><span data-stu-id="cb43b-126">Standard</span></span>
- <span data-ttu-id="cb43b-127">WAF</span><span class="sxs-lookup"><span data-stu-id="cb43b-127">WAF</span></span>

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

### <span data-ttu-id="cb43b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb43b-128">CommonParameters</span></span>
<span data-ttu-id="cb43b-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb43b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb43b-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb43b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb43b-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb43b-131">INPUTS</span></span>

### <span data-ttu-id="cb43b-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cb43b-132">None</span></span>

## <span data-ttu-id="cb43b-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb43b-133">OUTPUTS</span></span>

### <span data-ttu-id="cb43b-134">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="cb43b-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="cb43b-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb43b-135">NOTES</span></span>

## <span data-ttu-id="cb43b-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb43b-136">RELATED LINKS</span></span>

[<span data-ttu-id="cb43b-137">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="cb43b-137">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="cb43b-138">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="cb43b-138">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


