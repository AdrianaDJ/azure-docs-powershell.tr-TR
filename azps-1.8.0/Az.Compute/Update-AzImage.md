---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: 10302f75bcbdb24c838f7785804368fd4716da87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917180"
---
# <span data-ttu-id="f74f1-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="f74f1-101">Update-AzImage</span></span>

## <span data-ttu-id="f74f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f74f1-102">SYNOPSIS</span></span>
<span data-ttu-id="f74f1-103">Bir resmi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f74f1-103">Updates an image.</span></span>

## <span data-ttu-id="f74f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f74f1-104">SYNTAX</span></span>

### <span data-ttu-id="f74f1-105">ObjectParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f74f1-105">ObjectParameter (Default)</span></span>
```
Update-AzImage [-Image] <PSImage> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74f1-106">DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="f74f1-106">DefaultParameter</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [[-Image] <PSImage>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74f1-107">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="f74f1-107">ResourceIdParameter</span></span>
```
Update-AzImage [-ResourceId] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f74f1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f74f1-108">DESCRIPTION</span></span>
<span data-ttu-id="f74f1-109">**Update-Azgörüntü** cmdlet 'ini bir resmi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f74f1-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="f74f1-110">Şu anda yalnızca Etiketler güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="f74f1-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="f74f1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f74f1-111">EXAMPLES</span></span>

### <span data-ttu-id="f74f1-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f74f1-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="f74f1-113">Bu komut, ' ResourceGroup01 ' kaynak grubundaki mevcut ' Image01 ' resminin etiket değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f74f1-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f74f1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f74f1-114">PARAMETERS</span></span>

### <span data-ttu-id="f74f1-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="f74f1-115">-AsJob</span></span>
<span data-ttu-id="f74f1-116">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f74f1-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f74f1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f74f1-117">-DefaultProfile</span></span>
<span data-ttu-id="f74f1-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f74f1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f74f1-119">-Image</span><span class="sxs-lookup"><span data-stu-id="f74f1-119">-Image</span></span>
<span data-ttu-id="f74f1-120">Yerel bir resim nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f74f1-120">Specifies a local image object.</span></span>

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

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f74f1-121">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="f74f1-121">-ImageName</span></span>
<span data-ttu-id="f74f1-122">Bir resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f74f1-122">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="f74f1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f74f1-123">-ResourceGroupName</span></span>
<span data-ttu-id="f74f1-124">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f74f1-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f74f1-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f74f1-125">-ResourceId</span></span>
<span data-ttu-id="f74f1-126">Resmin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="f74f1-126">The resource Id for the image</span></span>

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

### <span data-ttu-id="f74f1-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f74f1-127">-Tag</span></span>
<span data-ttu-id="f74f1-128">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="f74f1-128">Resource tags</span></span>

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

### <span data-ttu-id="f74f1-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="f74f1-129">-Confirm</span></span>
<span data-ttu-id="f74f1-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f74f1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f74f1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f74f1-131">-WhatIf</span></span>
<span data-ttu-id="f74f1-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f74f1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f74f1-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f74f1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f74f1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f74f1-134">CommonParameters</span></span>
<span data-ttu-id="f74f1-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f74f1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f74f1-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f74f1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f74f1-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f74f1-137">INPUTS</span></span>

### <span data-ttu-id="f74f1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f74f1-138">System.String</span></span>

### <span data-ttu-id="f74f1-139">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="f74f1-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="f74f1-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f74f1-140">OUTPUTS</span></span>

### <span data-ttu-id="f74f1-141">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="f74f1-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="f74f1-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f74f1-142">NOTES</span></span>

## <span data-ttu-id="f74f1-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f74f1-143">RELATED LINKS</span></span>
