---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
ms.openlocfilehash: 1d37af16fcb84db8247ac5db495abb1f41319c6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594295"
---
# <span data-ttu-id="c7cd9-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="c7cd9-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="c7cd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7cd9-102">SYNOPSIS</span></span>
<span data-ttu-id="c7cd9-103">Bir resim nesnesinden veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c7cd9-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7cd9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7cd9-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7cd9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7cd9-105">DESCRIPTION</span></span>
<span data-ttu-id="c7cd9-106">**Remove-Azurermimagedatadısk** cmdlet 'i, bir resim nesnesinden veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c7cd9-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="c7cd9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7cd9-107">EXAMPLES</span></span>

### <span data-ttu-id="c7cd9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c7cd9-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="c7cd9-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki varolan ' Image01 ' görüntüsünden mantıksal birim numarası 1 veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c7cd9-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c7cd9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7cd9-110">PARAMETERS</span></span>

### <span data-ttu-id="c7cd9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7cd9-111">-DefaultProfile</span></span>
<span data-ttu-id="c7cd9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c7cd9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7cd9-113">-Image</span><span class="sxs-lookup"><span data-stu-id="c7cd9-113">-Image</span></span>
<span data-ttu-id="c7cd9-114">Yerel bir resim nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7cd9-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7cd9-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="c7cd9-115">-Lun</span></span>
<span data-ttu-id="c7cd9-116">Mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7cd9-116">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7cd9-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="c7cd9-117">-Confirm</span></span>
<span data-ttu-id="c7cd9-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c7cd9-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7cd9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7cd9-119">-WhatIf</span></span>
<span data-ttu-id="c7cd9-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7cd9-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7cd9-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c7cd9-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7cd9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7cd9-122">CommonParameters</span></span>
<span data-ttu-id="c7cd9-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7cd9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7cd9-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7cd9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7cd9-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7cd9-125">INPUTS</span></span>

### <span data-ttu-id="c7cd9-126">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="c7cd9-126">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="c7cd9-127">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c7cd9-127">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="c7cd9-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7cd9-128">OUTPUTS</span></span>

### <span data-ttu-id="c7cd9-129">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="c7cd9-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="c7cd9-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7cd9-130">NOTES</span></span>

## <span data-ttu-id="c7cd9-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7cd9-131">RELATED LINKS</span></span>

