---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: 15b1316940c42534844245eaaf1aee3e450adc4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587625"
---
# <span data-ttu-id="9ff88-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="9ff88-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="9ff88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ff88-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff88-103">Azure uzantısının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="9ff88-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ff88-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ff88-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String> [<CommonParameters>]
```

## <span data-ttu-id="9ff88-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ff88-105">DESCRIPTION</span></span>
<span data-ttu-id="9ff88-106">**Get-Azurermvmextensionımagetype** cmdlet 'i, bir Azure uzantısının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="9ff88-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="9ff88-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ff88-107">EXAMPLES</span></span>

### <span data-ttu-id="9ff88-108">Örnek 1: uzantı resim türünü alma</span><span class="sxs-lookup"><span data-stu-id="9ff88-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="9ff88-109">Bu komut belirtilen yayımcının ve konumun uzantı resim türünü alır.</span><span class="sxs-lookup"><span data-stu-id="9ff88-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="9ff88-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ff88-110">PARAMETERS</span></span>

### <span data-ttu-id="9ff88-111">-Konum</span><span class="sxs-lookup"><span data-stu-id="9ff88-111">-Location</span></span>
<span data-ttu-id="9ff88-112">Bir uzantının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ff88-112">Specifies the location of an extension.</span></span>
<span data-ttu-id="9ff88-113">Bu cmdlet, bu parametrenin belirttiği konumda uzantının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="9ff88-113">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="9ff88-114">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9ff88-114">-PublisherName</span></span>
<span data-ttu-id="9ff88-115">Bir uzantının yayıncısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ff88-115">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="9ff88-116">Uzantı yayımcısı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9ff88-116">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="9ff88-117">Bu cmdlet, bu parametrenin belirttiği yayımcının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="9ff88-117">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="9ff88-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff88-118">CommonParameters</span></span>
<span data-ttu-id="9ff88-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ff88-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff88-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ff88-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff88-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ff88-121">INPUTS</span></span>

### <span data-ttu-id="9ff88-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9ff88-122">None</span></span>
<span data-ttu-id="9ff88-123">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="9ff88-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9ff88-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ff88-124">OUTPUTS</span></span>

## <span data-ttu-id="9ff88-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ff88-125">NOTES</span></span>

## <span data-ttu-id="9ff88-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ff88-126">RELATED LINKS</span></span>

[<span data-ttu-id="9ff88-127">Get-Azurermvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="9ff88-127">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="9ff88-128">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="9ff88-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


