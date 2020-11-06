---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 00e9e91736be664610bef5562c0c5416ea5fc7c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592298"
---
# <span data-ttu-id="07e26-101">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="07e26-101">New-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="07e26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07e26-102">SYNOPSIS</span></span>
<span data-ttu-id="07e26-103">Uygulama ağ geçidi için SKU oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07e26-103">Creates a SKU for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07e26-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07e26-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07e26-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="07e26-105">DESCRIPTION</span></span>
<span data-ttu-id="07e26-106">**New-AzureRmApplicationGatewaySku** cmdlet 'ı bir Azure uygulama ağ geçidi için bir stok saklama BIRIMI (SKU) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07e26-106">The **New-AzureRmApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="07e26-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07e26-107">EXAMPLES</span></span>

### <span data-ttu-id="07e26-108">Örnek 1: Azure uygulaması ağ geçidi için SKU oluşturma</span><span class="sxs-lookup"><span data-stu-id="07e26-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="07e26-109">Bu komut, Azure Application Gateway için Standard_Small adlı bir SKU oluşturur ve sonucu $SKU adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="07e26-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="07e26-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07e26-110">PARAMETERS</span></span>

### <span data-ttu-id="07e26-111">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="07e26-111">-Capacity</span></span>
<span data-ttu-id="07e26-112">Uygulama ağ geçidi örneklerinin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07e26-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="07e26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e26-113">-DefaultProfile</span></span>
<span data-ttu-id="07e26-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07e26-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07e26-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="07e26-115">-Name</span></span>
<span data-ttu-id="07e26-116">SKU 'nun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07e26-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="07e26-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="07e26-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="07e26-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="07e26-118">Standard_Small</span></span>
- <span data-ttu-id="07e26-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="07e26-119">Standard_Medium</span></span>
- <span data-ttu-id="07e26-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="07e26-120">Standard_Large</span></span>
- <span data-ttu-id="07e26-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="07e26-121">WAF_Medium</span></span>
- <span data-ttu-id="07e26-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="07e26-122">WAF_Large</span></span>

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

### <span data-ttu-id="07e26-123">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="07e26-123">-Tier</span></span>
<span data-ttu-id="07e26-124">SKU 'nun katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07e26-124">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="07e26-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="07e26-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="07e26-126">Ardından</span><span class="sxs-lookup"><span data-stu-id="07e26-126">Standard</span></span>
- <span data-ttu-id="07e26-127">WAF</span><span class="sxs-lookup"><span data-stu-id="07e26-127">WAF</span></span>

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

### <span data-ttu-id="07e26-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e26-128">CommonParameters</span></span>
<span data-ttu-id="07e26-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07e26-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07e26-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07e26-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e26-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07e26-131">INPUTS</span></span>

### <span data-ttu-id="07e26-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="07e26-132">None</span></span>

## <span data-ttu-id="07e26-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07e26-133">OUTPUTS</span></span>

### <span data-ttu-id="07e26-134">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="07e26-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="07e26-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07e26-135">NOTES</span></span>

## <span data-ttu-id="07e26-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07e26-136">RELATED LINKS</span></span>

[<span data-ttu-id="07e26-137">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="07e26-137">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="07e26-138">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="07e26-138">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


