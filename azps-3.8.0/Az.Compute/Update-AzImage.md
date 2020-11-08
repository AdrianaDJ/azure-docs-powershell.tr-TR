---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: b829321dc3d091549ff0b8a89a5ad564867db478
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098141"
---
# <span data-ttu-id="13212-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="13212-101">Update-AzImage</span></span>

## <span data-ttu-id="13212-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13212-102">SYNOPSIS</span></span>
<span data-ttu-id="13212-103">Bir resmi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="13212-103">Updates an image.</span></span>

## <span data-ttu-id="13212-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="13212-104">SYNTAX</span></span>

### <span data-ttu-id="13212-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="13212-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13212-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="13212-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13212-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="13212-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13212-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="13212-108">DESCRIPTION</span></span>
<span data-ttu-id="13212-109">**Update-Azgörüntü** cmdlet 'ini bir resmi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="13212-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="13212-110">Şu anda yalnızca Etiketler güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="13212-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="13212-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="13212-111">EXAMPLES</span></span>

### <span data-ttu-id="13212-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="13212-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="13212-113">Bu komut, ' ResourceGroup01 ' kaynak grubundaki mevcut ' Image01 ' resminin etiket değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="13212-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="13212-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="13212-114">PARAMETERS</span></span>

### <span data-ttu-id="13212-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="13212-115">-AsJob</span></span>
<span data-ttu-id="13212-116">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="13212-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="13212-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13212-117">-DefaultProfile</span></span>
<span data-ttu-id="13212-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="13212-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13212-119">-Image</span><span class="sxs-lookup"><span data-stu-id="13212-119">-Image</span></span>
<span data-ttu-id="13212-120">Yerel bir resim nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="13212-120">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13212-121">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="13212-121">-ImageName</span></span>
<span data-ttu-id="13212-122">Bir resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="13212-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13212-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13212-123">-ResourceGroupName</span></span>
<span data-ttu-id="13212-124">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="13212-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13212-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="13212-125">-ResourceId</span></span>
<span data-ttu-id="13212-126">Resmin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="13212-126">The resource Id for the image</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13212-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="13212-127">-Tag</span></span>
<span data-ttu-id="13212-128">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="13212-128">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13212-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="13212-129">-Confirm</span></span>
<span data-ttu-id="13212-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="13212-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13212-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13212-131">-WhatIf</span></span>
<span data-ttu-id="13212-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="13212-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13212-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="13212-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13212-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13212-134">CommonParameters</span></span>
<span data-ttu-id="13212-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="13212-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13212-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="13212-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13212-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="13212-137">INPUTS</span></span>

### <span data-ttu-id="13212-138">System. String</span><span class="sxs-lookup"><span data-stu-id="13212-138">System.String</span></span>

### <span data-ttu-id="13212-139">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="13212-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="13212-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="13212-140">OUTPUTS</span></span>

### <span data-ttu-id="13212-141">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="13212-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="13212-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="13212-142">NOTES</span></span>

## <span data-ttu-id="13212-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="13212-143">RELATED LINKS</span></span>
