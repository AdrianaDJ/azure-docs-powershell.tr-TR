---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
ms.openlocfilehash: 7d6d130f639265cd2b7e2885f117d2e29899b8c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594296"
---
# <span data-ttu-id="f458d-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="f458d-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="f458d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f458d-102">SYNOPSIS</span></span>
<span data-ttu-id="f458d-103">Bir resmi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f458d-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f458d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f458d-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f458d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f458d-105">DESCRIPTION</span></span>
<span data-ttu-id="f458d-106">**Remove-AzureRmImage** cmdlet 'ini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f458d-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="f458d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f458d-107">EXAMPLES</span></span>

### <span data-ttu-id="f458d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f458d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="f458d-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Image01 ' adındaki resmi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f458d-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f458d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f458d-110">PARAMETERS</span></span>

### <span data-ttu-id="f458d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f458d-111">-DefaultProfile</span></span>
<span data-ttu-id="f458d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f458d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f458d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f458d-113">-Force</span></span>
<span data-ttu-id="f458d-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f458d-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f458d-115">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="f458d-115">-ImageName</span></span>
<span data-ttu-id="f458d-116">Bir resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f458d-116">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="f458d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f458d-117">-ResourceGroupName</span></span>
<span data-ttu-id="f458d-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f458d-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f458d-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="f458d-119">-Confirm</span></span>
<span data-ttu-id="f458d-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f458d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f458d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f458d-121">-WhatIf</span></span>
<span data-ttu-id="f458d-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f458d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f458d-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f458d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f458d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f458d-124">CommonParameters</span></span>
<span data-ttu-id="f458d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f458d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f458d-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f458d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f458d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f458d-127">INPUTS</span></span>

### <span data-ttu-id="f458d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f458d-128">System.String</span></span>

## <span data-ttu-id="f458d-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f458d-129">OUTPUTS</span></span>

### <span data-ttu-id="f458d-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="f458d-130">System.Object</span></span>

## <span data-ttu-id="f458d-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f458d-131">NOTES</span></span>

## <span data-ttu-id="f458d-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f458d-132">RELATED LINKS</span></span>

