---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermimagedatadisk
schema: 2.0.0
ms.openlocfilehash: b7e691d3bfea45fc8fc45725ddfe782418c12ab7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939761"
---
# <span data-ttu-id="cd9fa-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="cd9fa-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="cd9fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd9fa-102">SYNOPSIS</span></span>
<span data-ttu-id="cd9fa-103">Bir resim nesnesinden veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cd9fa-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd9fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd9fa-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd9fa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd9fa-105">DESCRIPTION</span></span>
<span data-ttu-id="cd9fa-106">**Remove-Azurermimagedatadısk** cmdlet 'i, bir resim nesnesinden veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cd9fa-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="cd9fa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd9fa-107">EXAMPLES</span></span>

### <span data-ttu-id="cd9fa-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cd9fa-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="cd9fa-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki varolan ' Image01 ' görüntüsünden mantıksal birim numarası 1 veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cd9fa-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cd9fa-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd9fa-110">PARAMETERS</span></span>

### <span data-ttu-id="cd9fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd9fa-111">-DefaultProfile</span></span>
<span data-ttu-id="cd9fa-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd9fa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd9fa-113">-Image</span><span class="sxs-lookup"><span data-stu-id="cd9fa-113">-Image</span></span>
<span data-ttu-id="cd9fa-114">Yerel bir resim nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd9fa-114">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd9fa-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="cd9fa-115">-Lun</span></span>
<span data-ttu-id="cd9fa-116">Mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd9fa-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="cd9fa-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="cd9fa-117">-Confirm</span></span>
<span data-ttu-id="cd9fa-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cd9fa-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd9fa-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd9fa-119">-WhatIf</span></span>
<span data-ttu-id="cd9fa-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd9fa-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd9fa-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cd9fa-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd9fa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd9fa-122">CommonParameters</span></span>
<span data-ttu-id="cd9fa-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd9fa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd9fa-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd9fa-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd9fa-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd9fa-125">INPUTS</span></span>

### <span data-ttu-id="cd9fa-126">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="cd9fa-126">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="cd9fa-127">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cd9fa-127">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="cd9fa-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd9fa-128">OUTPUTS</span></span>

### <span data-ttu-id="cd9fa-129">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="cd9fa-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="cd9fa-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd9fa-130">NOTES</span></span>

## <span data-ttu-id="cd9fa-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd9fa-131">RELATED LINKS</span></span>

