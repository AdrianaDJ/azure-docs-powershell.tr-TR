---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: ccca83cdbebcf73df9059807dc5b030e4ab21736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763124"
---
# <span data-ttu-id="14124-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="14124-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="14124-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14124-102">SYNOPSIS</span></span>
<span data-ttu-id="14124-103">Bir resmi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="14124-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14124-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14124-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14124-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="14124-105">DESCRIPTION</span></span>
<span data-ttu-id="14124-106">**Güncelleştirme-AzureRmImage** cmdlet 'i, bir resmi günceller.</span><span class="sxs-lookup"><span data-stu-id="14124-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="14124-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14124-107">EXAMPLES</span></span>

### <span data-ttu-id="14124-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="14124-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="14124-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki varolan ' Image01 ' görüntüsünden mantıksal birim numarası 1 veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="14124-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="14124-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14124-110">PARAMETERS</span></span>

### <span data-ttu-id="14124-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14124-111">-DefaultProfile</span></span>
<span data-ttu-id="14124-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="14124-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14124-113">-Image</span><span class="sxs-lookup"><span data-stu-id="14124-113">-Image</span></span>
<span data-ttu-id="14124-114">Yerel bir resim nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="14124-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14124-115">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="14124-115">-ImageName</span></span>
<span data-ttu-id="14124-116">Bir resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="14124-116">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14124-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14124-117">-ResourceGroupName</span></span>
<span data-ttu-id="14124-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="14124-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14124-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="14124-119">-Confirm</span></span>
<span data-ttu-id="14124-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="14124-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14124-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14124-121">-WhatIf</span></span>
<span data-ttu-id="14124-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="14124-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14124-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="14124-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14124-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14124-124">CommonParameters</span></span>
<span data-ttu-id="14124-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14124-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14124-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14124-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14124-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14124-127">INPUTS</span></span>

### <span data-ttu-id="14124-128">System. String</span><span class="sxs-lookup"><span data-stu-id="14124-128">System.String</span></span>
<span data-ttu-id="14124-129">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="14124-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="14124-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14124-130">OUTPUTS</span></span>

### <span data-ttu-id="14124-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="14124-131">System.Object</span></span>

## <span data-ttu-id="14124-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14124-132">NOTES</span></span>

## <span data-ttu-id="14124-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14124-133">RELATED LINKS</span></span>
