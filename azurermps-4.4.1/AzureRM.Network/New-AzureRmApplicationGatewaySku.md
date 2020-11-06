---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: eb1f0dadd905ff4b57a58c46f763f3c2dd51f256
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593528"
---
# <span data-ttu-id="6a3c4-101">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6a3c4-101">New-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="6a3c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a3c4-102">SYNOPSIS</span></span>
<span data-ttu-id="6a3c4-103">Uygulama ağ geçidi için SKU oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6a3c4-103">Creates a SKU for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a3c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a3c4-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a3c4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a3c4-105">DESCRIPTION</span></span>
<span data-ttu-id="6a3c4-106">**New-AzureRmApplicationGatewaySku** cmdlet 'ı bir Azure uygulama ağ geçidi için bir stok saklama BIRIMI (SKU) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6a3c4-106">The **New-AzureRmApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="6a3c4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a3c4-107">EXAMPLES</span></span>

### <span data-ttu-id="6a3c4-108">Örnek 1: Azure uygulaması ağ geçidi için SKU oluşturma</span><span class="sxs-lookup"><span data-stu-id="6a3c4-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="6a3c4-109">Bu komut, Azure Application Gateway için Standard_Small adlı bir SKU oluşturur ve sonucu $SKU adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="6a3c4-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="6a3c4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a3c4-110">PARAMETERS</span></span>

### <span data-ttu-id="6a3c4-111">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="6a3c4-111">-Capacity</span></span>
<span data-ttu-id="6a3c4-112">Uygulama ağ geçidi örneklerinin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a3c4-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="6a3c4-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="6a3c4-113">-Name</span></span>
<span data-ttu-id="6a3c4-114">SKU 'nun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a3c4-114">Specifies the name of the SKU.</span></span>

<span data-ttu-id="6a3c4-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6a3c4-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a3c4-116">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="6a3c4-116">Standard_Small</span></span>
- <span data-ttu-id="6a3c4-117">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="6a3c4-117">Standard_Medium</span></span>
- <span data-ttu-id="6a3c4-118">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="6a3c4-118">Standard_Large</span></span>
- <span data-ttu-id="6a3c4-119">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="6a3c4-119">WAF_Medium</span></span>
- <span data-ttu-id="6a3c4-120">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="6a3c4-120">WAF_Large</span></span>

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

### <span data-ttu-id="6a3c4-121">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="6a3c4-121">-Tier</span></span>
<span data-ttu-id="6a3c4-122">SKU 'nun katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a3c4-122">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="6a3c4-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6a3c4-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a3c4-124">Ardından</span><span class="sxs-lookup"><span data-stu-id="6a3c4-124">Standard</span></span>
- <span data-ttu-id="6a3c4-125">WAF</span><span class="sxs-lookup"><span data-stu-id="6a3c4-125">WAF</span></span>

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

### <span data-ttu-id="6a3c4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a3c4-126">-DefaultProfile</span></span>
<span data-ttu-id="6a3c4-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a3c4-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a3c4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a3c4-128">CommonParameters</span></span>
<span data-ttu-id="6a3c4-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a3c4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a3c4-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a3c4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a3c4-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a3c4-131">INPUTS</span></span>

### <span data-ttu-id="6a3c4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6a3c4-132">System.String</span></span>

## <span data-ttu-id="6a3c4-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a3c4-133">OUTPUTS</span></span>

### <span data-ttu-id="6a3c4-134">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6a3c4-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="6a3c4-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a3c4-135">NOTES</span></span>

## <span data-ttu-id="6a3c4-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a3c4-136">RELATED LINKS</span></span>

[<span data-ttu-id="6a3c4-137">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6a3c4-137">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="6a3c4-138">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6a3c4-138">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


