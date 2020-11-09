---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: cfe9fb07854fcc5850e1c5f73f4da7fe43f172a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323263"
---
# <span data-ttu-id="3aaee-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="3aaee-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="3aaee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3aaee-102">SYNOPSIS</span></span>
<span data-ttu-id="3aaee-103">Kaynak için bir ağ sanal gereç SKU 'su tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="3aaee-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="3aaee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3aaee-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3aaee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3aaee-105">DESCRIPTION</span></span>
<span data-ttu-id="3aaee-106">New-AzVirtualApplianceSkuProperties komutu, ağ sanal gereç kaynağı için bir SKU tanımlar.</span><span class="sxs-lookup"><span data-stu-id="3aaee-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="3aaee-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3aaee-107">EXAMPLES</span></span>

### <span data-ttu-id="3aaee-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3aaee-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="3aaee-109">New-AzNetworkVirtualAppliance komutuyla kullanılacak sanal bir gereç özellik nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3aaee-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="3aaee-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3aaee-110">PARAMETERS</span></span>

### <span data-ttu-id="3aaee-111">-Paketleme</span><span class="sxs-lookup"><span data-stu-id="3aaee-111">-BundledScaleUnit</span></span>
<span data-ttu-id="3aaee-112">Paketlenmiş ölçeklendirme birimi.</span><span class="sxs-lookup"><span data-stu-id="3aaee-112">The bundled scale unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aaee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aaee-113">-DefaultProfile</span></span>
<span data-ttu-id="3aaee-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3aaee-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3aaee-115">-Pazar Placeversion</span><span class="sxs-lookup"><span data-stu-id="3aaee-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="3aaee-116">Pazar yeri sürümü.</span><span class="sxs-lookup"><span data-stu-id="3aaee-116">The market place version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aaee-117">-SatıcıAdı</span><span class="sxs-lookup"><span data-stu-id="3aaee-117">-VendorName</span></span>
<span data-ttu-id="3aaee-118">Satıcının adı.</span><span class="sxs-lookup"><span data-stu-id="3aaee-118">The name of the vendor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aaee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aaee-119">CommonParameters</span></span>
<span data-ttu-id="3aaee-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3aaee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aaee-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3aaee-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aaee-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3aaee-122">INPUTS</span></span>

### <span data-ttu-id="3aaee-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3aaee-123">None</span></span>

## <span data-ttu-id="3aaee-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3aaee-124">OUTPUTS</span></span>

### <span data-ttu-id="3aaee-125">Microsoft. Azure. Commands. Network. model. PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="3aaee-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="3aaee-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3aaee-126">NOTES</span></span>

## <span data-ttu-id="3aaee-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3aaee-127">RELATED LINKS</span></span>
