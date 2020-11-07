---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: 34c4eefe2792de239b2f3ae2a9348704497a4bd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762987"
---
# <span data-ttu-id="f4a81-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="f4a81-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="f4a81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4a81-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a81-103">Bir resmi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f4a81-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4a81-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4a81-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4a81-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4a81-105">DESCRIPTION</span></span>
<span data-ttu-id="f4a81-106">**Güncelleştirme-AzureRmImage** cmdlet 'i, bir resmi günceller.</span><span class="sxs-lookup"><span data-stu-id="f4a81-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="f4a81-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4a81-107">EXAMPLES</span></span>

### <span data-ttu-id="f4a81-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f4a81-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="f4a81-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki varolan ' Image01 ' görüntüsünden mantıksal birim numarası 1 veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f4a81-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f4a81-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4a81-110">PARAMETERS</span></span>

### <span data-ttu-id="f4a81-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="f4a81-111">-AsJob</span></span>
<span data-ttu-id="f4a81-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f4a81-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4a81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4a81-113">-DefaultProfile</span></span>
<span data-ttu-id="f4a81-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4a81-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4a81-115">-Image</span><span class="sxs-lookup"><span data-stu-id="f4a81-115">-Image</span></span>
<span data-ttu-id="f4a81-116">Yerel bir resim nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4a81-116">Specifies a local image object.</span></span>

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

### <span data-ttu-id="f4a81-117">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="f4a81-117">-ImageName</span></span>
<span data-ttu-id="f4a81-118">Bir resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4a81-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="f4a81-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4a81-119">-ResourceGroupName</span></span>
<span data-ttu-id="f4a81-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4a81-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f4a81-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="f4a81-121">-Confirm</span></span>
<span data-ttu-id="f4a81-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f4a81-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4a81-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4a81-123">-WhatIf</span></span>
<span data-ttu-id="f4a81-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f4a81-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4a81-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f4a81-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4a81-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a81-126">CommonParameters</span></span>
<span data-ttu-id="f4a81-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4a81-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4a81-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4a81-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a81-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4a81-129">INPUTS</span></span>

### <span data-ttu-id="f4a81-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f4a81-130">System.String</span></span>

### <span data-ttu-id="f4a81-131">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="f4a81-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>
<span data-ttu-id="f4a81-132">Parametreler: Image (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f4a81-132">Parameters: Image (ByValue)</span></span>

## <span data-ttu-id="f4a81-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4a81-133">OUTPUTS</span></span>

### <span data-ttu-id="f4a81-134">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="f4a81-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="f4a81-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4a81-135">NOTES</span></span>

## <span data-ttu-id="f4a81-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4a81-136">RELATED LINKS</span></span>
