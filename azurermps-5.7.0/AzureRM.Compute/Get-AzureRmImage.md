---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
ms.openlocfilehash: 3976418d89076b290500343775ca42e2fb975659
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591066"
---
# <span data-ttu-id="13f64-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="13f64-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="13f64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13f64-102">SYNOPSIS</span></span>
<span data-ttu-id="13f64-103">Resmin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="13f64-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13f64-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="13f64-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="13f64-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="13f64-105">DESCRIPTION</span></span>
<span data-ttu-id="13f64-106">**Get-AzureRmImage** cmdlet 'inin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="13f64-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="13f64-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="13f64-107">EXAMPLES</span></span>

### <span data-ttu-id="13f64-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="13f64-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="13f64-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Image01 ' adlı resmin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="13f64-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="13f64-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="13f64-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="13f64-111">Bu komut, ' ResourceGroup01 ' kaynak grubundaki tüm görüntülerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="13f64-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="13f64-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="13f64-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="13f64-113">Bu komut, aboneliğin altındaki tüm görüntülerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="13f64-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="13f64-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="13f64-114">PARAMETERS</span></span>

### <span data-ttu-id="13f64-115">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="13f64-115">-Expand</span></span>
<span data-ttu-id="13f64-116">Genişletme ifade sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="13f64-116">Specifies the expand expression query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13f64-117">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="13f64-117">-ImageName</span></span>
<span data-ttu-id="13f64-118">Bir resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="13f64-118">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13f64-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13f64-119">-ResourceGroupName</span></span>
<span data-ttu-id="13f64-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="13f64-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13f64-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f64-121">CommonParameters</span></span>
<span data-ttu-id="13f64-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="13f64-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f64-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13f64-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f64-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="13f64-124">INPUTS</span></span>

### <span data-ttu-id="13f64-125">System. String</span><span class="sxs-lookup"><span data-stu-id="13f64-125">System.String</span></span>

## <span data-ttu-id="13f64-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="13f64-126">OUTPUTS</span></span>

### <span data-ttu-id="13f64-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="13f64-127">System.Object</span></span>

## <span data-ttu-id="13f64-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="13f64-128">NOTES</span></span>

## <span data-ttu-id="13f64-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="13f64-129">RELATED LINKS</span></span>

