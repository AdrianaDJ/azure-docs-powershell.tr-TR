---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: bae8fb04e71700d1572b8742f8cccbb2ebe8e331
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587628"
---
# <span data-ttu-id="178c2-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="178c2-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="178c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="178c2-102">SYNOPSIS</span></span>
<span data-ttu-id="178c2-103">Bir Azure uzantısı için tüm sürümleri alır.</span><span class="sxs-lookup"><span data-stu-id="178c2-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="178c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="178c2-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [<CommonParameters>]
```

## <span data-ttu-id="178c2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="178c2-105">DESCRIPTION</span></span>
<span data-ttu-id="178c2-106">**Get-Azurermvmextensionımage** cmdlet 'ı bir Azure uzantısı için tüm sürümleri alır.</span><span class="sxs-lookup"><span data-stu-id="178c2-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="178c2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="178c2-107">EXAMPLES</span></span>

### <span data-ttu-id="178c2-108">Örnek 1: uzantı resminin sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="178c2-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="178c2-109">Bu komut, belirtilen konum, yayıncı ve tür için uzantı resminin tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="178c2-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="178c2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="178c2-110">PARAMETERS</span></span>

### <span data-ttu-id="178c2-111">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="178c2-111">-FilterExpression</span></span>
<span data-ttu-id="178c2-112">Filtre ifadesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="178c2-112">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c2-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="178c2-113">-Location</span></span>
<span data-ttu-id="178c2-114">Bir uzantının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="178c2-114">Specifies the location of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="178c2-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="178c2-115">-PublisherName</span></span>
<span data-ttu-id="178c2-116">Uzantı yayıncısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="178c2-116">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="178c2-117">Uzantı yayımcısı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="178c2-117">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="178c2-118">-Tür</span><span class="sxs-lookup"><span data-stu-id="178c2-118">-Type</span></span>
<span data-ttu-id="178c2-119">Uzantının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="178c2-119">Specifies the type of the extension.</span></span>
<span data-ttu-id="178c2-120">Uzantı türü edinmek için Get-AzureRmVMExtensionImageType cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="178c2-120">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="178c2-121">-Version</span><span class="sxs-lookup"><span data-stu-id="178c2-121">-Version</span></span>
<span data-ttu-id="178c2-122">Bu cmdlet 'in aldığı uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="178c2-122">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="178c2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178c2-123">CommonParameters</span></span>
<span data-ttu-id="178c2-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="178c2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="178c2-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="178c2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178c2-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="178c2-126">INPUTS</span></span>

### <span data-ttu-id="178c2-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="178c2-127">None</span></span>
<span data-ttu-id="178c2-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="178c2-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="178c2-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="178c2-129">OUTPUTS</span></span>

## <span data-ttu-id="178c2-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="178c2-130">NOTES</span></span>

## <span data-ttu-id="178c2-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="178c2-131">RELATED LINKS</span></span>

[<span data-ttu-id="178c2-132">Get-Azurermvmextensionımagetype</span><span class="sxs-lookup"><span data-stu-id="178c2-132">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="178c2-133">Get-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="178c2-133">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="178c2-134">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="178c2-134">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


