---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
ms.openlocfilehash: c1d7a7128c0fd4774c99799695e0d041a08c8053
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764574"
---
# <span data-ttu-id="911c7-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="911c7-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="911c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="911c7-102">SYNOPSIS</span></span>
<span data-ttu-id="911c7-103">Resmin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="911c7-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="911c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="911c7-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="911c7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="911c7-105">DESCRIPTION</span></span>
<span data-ttu-id="911c7-106">**Get-AzureRmImage** cmdlet 'inin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="911c7-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="911c7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="911c7-107">EXAMPLES</span></span>

### <span data-ttu-id="911c7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="911c7-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="911c7-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Image01 ' adlı resmin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="911c7-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="911c7-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="911c7-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="911c7-111">Bu komut, ' ResourceGroup01 ' kaynak grubundaki tüm görüntülerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="911c7-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="911c7-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="911c7-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="911c7-113">Bu komut, aboneliğin altındaki tüm görüntülerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="911c7-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="911c7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="911c7-114">PARAMETERS</span></span>

### <span data-ttu-id="911c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="911c7-115">-DefaultProfile</span></span>
<span data-ttu-id="911c7-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="911c7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="911c7-117">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="911c7-117">-Expand</span></span>
<span data-ttu-id="911c7-118">Genişletme ifade sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="911c7-118">Specifies the expand expression query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="911c7-119">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="911c7-119">-ImageName</span></span>
<span data-ttu-id="911c7-120">Bir resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="911c7-120">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="911c7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="911c7-121">-ResourceGroupName</span></span>
<span data-ttu-id="911c7-122">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="911c7-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="911c7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="911c7-123">CommonParameters</span></span>
<span data-ttu-id="911c7-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="911c7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="911c7-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="911c7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="911c7-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="911c7-126">INPUTS</span></span>

### <span data-ttu-id="911c7-127">System. String</span><span class="sxs-lookup"><span data-stu-id="911c7-127">System.String</span></span>

## <span data-ttu-id="911c7-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="911c7-128">OUTPUTS</span></span>

### <span data-ttu-id="911c7-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="911c7-129">System.Object</span></span>

## <span data-ttu-id="911c7-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="911c7-130">NOTES</span></span>

## <span data-ttu-id="911c7-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="911c7-131">RELATED LINKS</span></span>

