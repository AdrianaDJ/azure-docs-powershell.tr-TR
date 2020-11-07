---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermimage
schema: 2.0.0
ms.openlocfilehash: f1309453384f028c51bea20703d6ec75cc8a3a36
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940155"
---
# <span data-ttu-id="65ed7-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="65ed7-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="65ed7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="65ed7-103">Bir resmi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="65ed7-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65ed7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65ed7-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65ed7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="65ed7-105">DESCRIPTION</span></span>
<span data-ttu-id="65ed7-106">**Güncelleştirme-AzureRmImage** cmdlet 'i, bir resmi günceller.</span><span class="sxs-lookup"><span data-stu-id="65ed7-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="65ed7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65ed7-107">EXAMPLES</span></span>

### <span data-ttu-id="65ed7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="65ed7-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="65ed7-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki varolan ' Image01 ' görüntüsünden mantıksal birim numarası 1 veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="65ed7-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="65ed7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65ed7-110">PARAMETERS</span></span>

### <span data-ttu-id="65ed7-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="65ed7-111">-AsJob</span></span>
<span data-ttu-id="65ed7-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="65ed7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65ed7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ed7-113">-DefaultProfile</span></span>
<span data-ttu-id="65ed7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="65ed7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65ed7-115">-Image</span><span class="sxs-lookup"><span data-stu-id="65ed7-115">-Image</span></span>
<span data-ttu-id="65ed7-116">Yerel bir resim nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="65ed7-116">Specifies a local image object.</span></span>

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

### <span data-ttu-id="65ed7-117">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="65ed7-117">-ImageName</span></span>
<span data-ttu-id="65ed7-118">Bir resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65ed7-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="65ed7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65ed7-119">-ResourceGroupName</span></span>
<span data-ttu-id="65ed7-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65ed7-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="65ed7-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="65ed7-121">-Confirm</span></span>
<span data-ttu-id="65ed7-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="65ed7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65ed7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65ed7-123">-WhatIf</span></span>
<span data-ttu-id="65ed7-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="65ed7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65ed7-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="65ed7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65ed7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ed7-126">CommonParameters</span></span>
<span data-ttu-id="65ed7-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65ed7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ed7-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65ed7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ed7-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65ed7-129">INPUTS</span></span>

### <span data-ttu-id="65ed7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="65ed7-130">System.String</span></span>
<span data-ttu-id="65ed7-131">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="65ed7-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="65ed7-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65ed7-132">OUTPUTS</span></span>

### <span data-ttu-id="65ed7-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="65ed7-133">System.Object</span></span>

## <span data-ttu-id="65ed7-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65ed7-134">NOTES</span></span>

## <span data-ttu-id="65ed7-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65ed7-135">RELATED LINKS</span></span>

