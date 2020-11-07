---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 0b87119ccec521b85a210dc8685874bd4ba4b9ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935421"
---
# <span data-ttu-id="e0891-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e0891-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="e0891-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0891-102">SYNOPSIS</span></span>
<span data-ttu-id="e0891-103">Uygulama ağ geçidi için SKU oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0891-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="e0891-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0891-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0891-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0891-105">DESCRIPTION</span></span>
<span data-ttu-id="e0891-106">**Yeni-AzApplicationGatewaySku** cmdlet 'i, bir Azure uygulama ağ geçidi için bir stok saklama BIRIMI (SKU) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0891-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="e0891-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0891-107">EXAMPLES</span></span>

### <span data-ttu-id="e0891-108">Örnek 1: Azure uygulaması ağ geçidi için SKU oluşturma</span><span class="sxs-lookup"><span data-stu-id="e0891-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="e0891-109">Bu komut, Azure Application Gateway için Standard_Small adlı bir SKU oluşturur ve sonucu $SKU adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="e0891-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="e0891-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0891-110">PARAMETERS</span></span>

### <span data-ttu-id="e0891-111">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="e0891-111">-Capacity</span></span>
<span data-ttu-id="e0891-112">Uygulama ağ geçidi örneklerinin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0891-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="e0891-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0891-113">-DefaultProfile</span></span>
<span data-ttu-id="e0891-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0891-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0891-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e0891-115">-Name</span></span>
<span data-ttu-id="e0891-116">SKU 'nun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0891-116">Specifies the name of the SKU.</span></span>

<span data-ttu-id="e0891-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e0891-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e0891-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="e0891-118">Standard_Small</span></span>
- <span data-ttu-id="e0891-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="e0891-119">Standard_Medium</span></span>
- <span data-ttu-id="e0891-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="e0891-120">Standard_Large</span></span>
- <span data-ttu-id="e0891-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="e0891-121">WAF_Medium</span></span>
- <span data-ttu-id="e0891-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="e0891-122">WAF_Large</span></span>

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

### <span data-ttu-id="e0891-123">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="e0891-123">-Tier</span></span>
<span data-ttu-id="e0891-124">SKU 'nun katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0891-124">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="e0891-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e0891-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e0891-126">Ardından</span><span class="sxs-lookup"><span data-stu-id="e0891-126">Standard</span></span>
- <span data-ttu-id="e0891-127">WAF</span><span class="sxs-lookup"><span data-stu-id="e0891-127">WAF</span></span>

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

### <span data-ttu-id="e0891-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0891-128">CommonParameters</span></span>
<span data-ttu-id="e0891-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0891-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0891-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0891-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0891-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0891-131">INPUTS</span></span>

### <span data-ttu-id="e0891-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e0891-132">System.String</span></span>

## <span data-ttu-id="e0891-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0891-133">OUTPUTS</span></span>

### <span data-ttu-id="e0891-134">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e0891-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="e0891-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0891-135">NOTES</span></span>

## <span data-ttu-id="e0891-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0891-136">RELATED LINKS</span></span>

[<span data-ttu-id="e0891-137">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e0891-137">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="e0891-138">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e0891-138">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


