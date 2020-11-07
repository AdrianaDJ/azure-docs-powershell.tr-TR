---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 3c7399e3eec760e8d4a40d58a8ea9a56e744cfd4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936929"
---
# <span data-ttu-id="9920e-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="9920e-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="9920e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9920e-102">SYNOPSIS</span></span>
<span data-ttu-id="9920e-103">Bir resim nesnesinden veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9920e-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="9920e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9920e-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9920e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9920e-105">DESCRIPTION</span></span>
<span data-ttu-id="9920e-106">**Remove-Azımagedatadısk** cmdlet 'i, bir resim nesnesinden veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9920e-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="9920e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9920e-107">EXAMPLES</span></span>

### <span data-ttu-id="9920e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9920e-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="9920e-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki varolan ' Image01 ' görüntüsünden mantıksal birim numarası 1 veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9920e-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="9920e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9920e-110">PARAMETERS</span></span>

### <span data-ttu-id="9920e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9920e-111">-DefaultProfile</span></span>
<span data-ttu-id="9920e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9920e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9920e-113">-Image</span><span class="sxs-lookup"><span data-stu-id="9920e-113">-Image</span></span>
<span data-ttu-id="9920e-114">Yerel bir resim nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9920e-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="9920e-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="9920e-115">-Lun</span></span>
<span data-ttu-id="9920e-116">Mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="9920e-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="9920e-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="9920e-117">-Confirm</span></span>
<span data-ttu-id="9920e-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9920e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9920e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9920e-119">-WhatIf</span></span>
<span data-ttu-id="9920e-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9920e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9920e-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9920e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9920e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9920e-122">CommonParameters</span></span>
<span data-ttu-id="9920e-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9920e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9920e-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9920e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9920e-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9920e-125">INPUTS</span></span>

### <span data-ttu-id="9920e-126">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="9920e-126">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="9920e-127">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9920e-127">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9920e-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9920e-128">OUTPUTS</span></span>

### <span data-ttu-id="9920e-129">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="9920e-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="9920e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9920e-130">NOTES</span></span>

## <span data-ttu-id="9920e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9920e-131">RELATED LINKS</span></span>

