---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: b7c5155706b968973bef6a5cf1ce2285caee819d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586765"
---
# <span data-ttu-id="ecca0-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="ecca0-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="ecca0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecca0-102">SYNOPSIS</span></span>
<span data-ttu-id="ecca0-103">Bir resmi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ecca0-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecca0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ecca0-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <Image> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecca0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ecca0-105">DESCRIPTION</span></span>
<span data-ttu-id="ecca0-106">**Güncelleştirme-AzureRmImage** cmdlet 'i, bir resmi günceller.</span><span class="sxs-lookup"><span data-stu-id="ecca0-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="ecca0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ecca0-107">EXAMPLES</span></span>

### <span data-ttu-id="ecca0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ecca0-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="ecca0-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki varolan ' Image01 ' görüntüsünden mantıksal birim numarası 1 veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ecca0-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ecca0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ecca0-110">PARAMETERS</span></span>

### <span data-ttu-id="ecca0-111">-Image</span><span class="sxs-lookup"><span data-stu-id="ecca0-111">-Image</span></span>
<span data-ttu-id="ecca0-112">Yerel bir resim nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ecca0-112">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecca0-113">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="ecca0-113">-ImageName</span></span>
<span data-ttu-id="ecca0-114">Bir resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ecca0-114">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecca0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecca0-115">-ResourceGroupName</span></span>
<span data-ttu-id="ecca0-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ecca0-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecca0-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="ecca0-117">-Confirm</span></span>
<span data-ttu-id="ecca0-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ecca0-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecca0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecca0-119">-WhatIf</span></span>
<span data-ttu-id="ecca0-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ecca0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecca0-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ecca0-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecca0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecca0-122">CommonParameters</span></span>
<span data-ttu-id="ecca0-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ecca0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecca0-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecca0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecca0-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ecca0-125">INPUTS</span></span>

### <span data-ttu-id="ecca0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ecca0-126">System.String</span></span>
<span data-ttu-id="ecca0-127">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="ecca0-127">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="ecca0-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ecca0-128">OUTPUTS</span></span>

### <span data-ttu-id="ecca0-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="ecca0-129">System.Object</span></span>

## <span data-ttu-id="ecca0-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ecca0-130">NOTES</span></span>

## <span data-ttu-id="ecca0-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ecca0-131">RELATED LINKS</span></span>

