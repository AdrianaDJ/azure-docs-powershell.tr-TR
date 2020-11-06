---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
ms.openlocfilehash: 4115cabbeeb2a7c458ce52e80eb251cb972491f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587607"
---
# <span data-ttu-id="291bc-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="291bc-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="291bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="291bc-102">SYNOPSIS</span></span>
<span data-ttu-id="291bc-103">Bir resim nesnesinden veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="291bc-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="291bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="291bc-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <Image> [-Lun] <Int32> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="291bc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="291bc-105">DESCRIPTION</span></span>
<span data-ttu-id="291bc-106">**Remove-Azurermimagedatadısk** cmdlet 'i, bir resim nesnesinden veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="291bc-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="291bc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="291bc-107">EXAMPLES</span></span>

### <span data-ttu-id="291bc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="291bc-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="291bc-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki varolan ' Image01 ' görüntüsünden mantıksal birim numarası 1 veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="291bc-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="291bc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="291bc-110">PARAMETERS</span></span>

### <span data-ttu-id="291bc-111">-Image</span><span class="sxs-lookup"><span data-stu-id="291bc-111">-Image</span></span>
<span data-ttu-id="291bc-112">Yerel bir resim nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="291bc-112">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="291bc-113">-LUN</span><span class="sxs-lookup"><span data-stu-id="291bc-113">-Lun</span></span>
<span data-ttu-id="291bc-114">Mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="291bc-114">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="291bc-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="291bc-115">-Confirm</span></span>
<span data-ttu-id="291bc-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="291bc-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="291bc-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="291bc-117">-WhatIf</span></span>
<span data-ttu-id="291bc-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="291bc-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="291bc-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="291bc-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="291bc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="291bc-120">CommonParameters</span></span>
<span data-ttu-id="291bc-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="291bc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="291bc-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="291bc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="291bc-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="291bc-123">INPUTS</span></span>

### <span data-ttu-id="291bc-124">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="291bc-124">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="291bc-125">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="291bc-125">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="291bc-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="291bc-126">OUTPUTS</span></span>

### <span data-ttu-id="291bc-127">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="291bc-127">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="291bc-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="291bc-128">NOTES</span></span>

## <span data-ttu-id="291bc-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="291bc-129">RELATED LINKS</span></span>

