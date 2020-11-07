---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
ms.openlocfilehash: 054462398a0f7b3e8710928000f9c10fb42f04db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762546"
---
# <span data-ttu-id="55b8f-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="55b8f-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="55b8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="55b8f-103">Bir resmi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="55b8f-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55b8f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55b8f-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55b8f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="55b8f-105">DESCRIPTION</span></span>
<span data-ttu-id="55b8f-106">**Remove-AzureRmImage** cmdlet 'ini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="55b8f-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="55b8f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55b8f-107">EXAMPLES</span></span>

### <span data-ttu-id="55b8f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="55b8f-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="55b8f-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Image01 ' adındaki resmi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="55b8f-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="55b8f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55b8f-110">PARAMETERS</span></span>

### <span data-ttu-id="55b8f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="55b8f-111">-Force</span></span>
<span data-ttu-id="55b8f-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="55b8f-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55b8f-113">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="55b8f-113">-ImageName</span></span>
<span data-ttu-id="55b8f-114">Bir resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55b8f-114">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="55b8f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55b8f-115">-ResourceGroupName</span></span>
<span data-ttu-id="55b8f-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55b8f-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="55b8f-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="55b8f-117">-Confirm</span></span>
<span data-ttu-id="55b8f-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="55b8f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55b8f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55b8f-119">-WhatIf</span></span>
<span data-ttu-id="55b8f-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55b8f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55b8f-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="55b8f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55b8f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b8f-122">CommonParameters</span></span>
<span data-ttu-id="55b8f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55b8f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b8f-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55b8f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b8f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55b8f-125">INPUTS</span></span>

### <span data-ttu-id="55b8f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="55b8f-126">System.String</span></span>

## <span data-ttu-id="55b8f-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55b8f-127">OUTPUTS</span></span>

### <span data-ttu-id="55b8f-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="55b8f-128">System.Object</span></span>

## <span data-ttu-id="55b8f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55b8f-129">NOTES</span></span>

## <span data-ttu-id="55b8f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55b8f-130">RELATED LINKS</span></span>

