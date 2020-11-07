---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 13829081952be7ab79c6d7badde4dc687aa845ed
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937045"
---
# <span data-ttu-id="eb37d-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="eb37d-101">Get-AzImage</span></span>

## <span data-ttu-id="eb37d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb37d-102">SYNOPSIS</span></span>
<span data-ttu-id="eb37d-103">Resmin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="eb37d-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="eb37d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb37d-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb37d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb37d-105">DESCRIPTION</span></span>
<span data-ttu-id="eb37d-106">**Get-Azgörüntü** cmdlet 'inin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="eb37d-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="eb37d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb37d-107">EXAMPLES</span></span>

### <span data-ttu-id="eb37d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="eb37d-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="eb37d-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Image01 ' adlı resmin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="eb37d-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="eb37d-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="eb37d-110">Example 2</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="eb37d-111">Bu komut, ' ResourceGroup01 ' kaynak grubundaki tüm görüntülerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="eb37d-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="eb37d-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="eb37d-112">Example 3</span></span>
```
PS C:\> Get-AzImage
```

<span data-ttu-id="eb37d-113">Bu komut, aboneliğin altındaki tüm görüntülerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="eb37d-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="eb37d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb37d-114">PARAMETERS</span></span>

### <span data-ttu-id="eb37d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb37d-115">-DefaultProfile</span></span>
<span data-ttu-id="eb37d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eb37d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb37d-117">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="eb37d-117">-Expand</span></span>
<span data-ttu-id="eb37d-118">Genişletme ifade sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb37d-118">Specifies the expand expression query.</span></span>

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

### <span data-ttu-id="eb37d-119">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="eb37d-119">-ImageName</span></span>
<span data-ttu-id="eb37d-120">Bir resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb37d-120">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="eb37d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb37d-121">-ResourceGroupName</span></span>
<span data-ttu-id="eb37d-122">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb37d-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="eb37d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb37d-123">CommonParameters</span></span>
<span data-ttu-id="eb37d-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb37d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb37d-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb37d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb37d-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb37d-126">INPUTS</span></span>

### <span data-ttu-id="eb37d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="eb37d-127">System.String</span></span>

## <span data-ttu-id="eb37d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb37d-128">OUTPUTS</span></span>

### <span data-ttu-id="eb37d-129">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="eb37d-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="eb37d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb37d-130">NOTES</span></span>

## <span data-ttu-id="eb37d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb37d-131">RELATED LINKS</span></span>

