---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: 1a04ca9df307b8d6251c6a8378df86827a76d001
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935945"
---
# <span data-ttu-id="a80bd-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="a80bd-101">Update-AzImage</span></span>

## <span data-ttu-id="a80bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a80bd-102">SYNOPSIS</span></span>
<span data-ttu-id="a80bd-103">Bir resmi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a80bd-103">Updates an image.</span></span>

## <span data-ttu-id="a80bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a80bd-104">SYNTAX</span></span>

```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a80bd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a80bd-105">DESCRIPTION</span></span>
<span data-ttu-id="a80bd-106">**Update-Azgörüntü** cmdlet 'ini bir resmi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a80bd-106">The **Update-AzImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="a80bd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a80bd-107">EXAMPLES</span></span>

### <span data-ttu-id="a80bd-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a80bd-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="a80bd-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki varolan ' Image01 ' görüntüsünden mantıksal birim numarası 1 veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a80bd-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a80bd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a80bd-110">PARAMETERS</span></span>

### <span data-ttu-id="a80bd-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="a80bd-111">-AsJob</span></span>
<span data-ttu-id="a80bd-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a80bd-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a80bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a80bd-113">-DefaultProfile</span></span>
<span data-ttu-id="a80bd-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a80bd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a80bd-115">-Image</span><span class="sxs-lookup"><span data-stu-id="a80bd-115">-Image</span></span>
<span data-ttu-id="a80bd-116">Yerel bir resim nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a80bd-116">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a80bd-117">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="a80bd-117">-ImageName</span></span>
<span data-ttu-id="a80bd-118">Bir resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a80bd-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="a80bd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a80bd-119">-ResourceGroupName</span></span>
<span data-ttu-id="a80bd-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a80bd-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a80bd-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="a80bd-121">-Confirm</span></span>
<span data-ttu-id="a80bd-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a80bd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a80bd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a80bd-123">-WhatIf</span></span>
<span data-ttu-id="a80bd-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a80bd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a80bd-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a80bd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a80bd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a80bd-126">CommonParameters</span></span>
<span data-ttu-id="a80bd-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a80bd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a80bd-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a80bd-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a80bd-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a80bd-129">INPUTS</span></span>

### <span data-ttu-id="a80bd-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a80bd-130">System.String</span></span>
<span data-ttu-id="a80bd-131">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="a80bd-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="a80bd-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a80bd-132">OUTPUTS</span></span>

### <span data-ttu-id="a80bd-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="a80bd-133">System.Object</span></span>

## <span data-ttu-id="a80bd-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a80bd-134">NOTES</span></span>

## <span data-ttu-id="a80bd-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a80bd-135">RELATED LINKS</span></span>

