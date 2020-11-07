---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: d0a149f5ee2e03345cd433952d49748886c066ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752636"
---
# <span data-ttu-id="50232-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="50232-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="50232-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50232-102">SYNOPSIS</span></span>
<span data-ttu-id="50232-103">Galeri görüntüsü tanımını güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="50232-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="50232-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50232-104">SYNTAX</span></span>

### <span data-ttu-id="50232-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="50232-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>]
 [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>]
 [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50232-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="50232-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50232-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="50232-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>]
 [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>]
 [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>]
 [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50232-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="50232-108">DESCRIPTION</span></span>
<span data-ttu-id="50232-109">Galeri görüntüsü tanımını güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="50232-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="50232-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50232-110">EXAMPLES</span></span>

### <span data-ttu-id="50232-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="50232-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="50232-112">Galeri görüntüsü tanımını güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="50232-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="50232-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50232-113">PARAMETERS</span></span>

### <span data-ttu-id="50232-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="50232-114">-AsJob</span></span>
<span data-ttu-id="50232-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="50232-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50232-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50232-116">-DefaultProfile</span></span>
<span data-ttu-id="50232-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="50232-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50232-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="50232-118">-Description</span></span>
<span data-ttu-id="50232-119">Galeri görüntüsü tanım kaynağının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="50232-119">The description of the gallery image Definition resource.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50232-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="50232-120">-DisallowedDiskType</span></span>
<span data-ttu-id="50232-121">İzin verilmeyen disk türleri.</span><span class="sxs-lookup"><span data-stu-id="50232-121">The disallowed disk types.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50232-122">-Endofyaşam tarihi</span><span class="sxs-lookup"><span data-stu-id="50232-122">-EndOfLifeDate</span></span>
<span data-ttu-id="50232-123">Galeri görüntüsü tanımının kullanım ömrünün sonu</span><span class="sxs-lookup"><span data-stu-id="50232-123">The end of life date of the gallery Image Definition</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50232-124">-EULA</span><span class="sxs-lookup"><span data-stu-id="50232-124">-Eula</span></span>
<span data-ttu-id="50232-125">Galeri resmi tanımı için EULA sözleşmesi.</span><span class="sxs-lookup"><span data-stu-id="50232-125">The Eula agreement for the gallery Image Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50232-126">-Gallertadı</span><span class="sxs-lookup"><span data-stu-id="50232-126">-GalleryName</span></span>
<span data-ttu-id="50232-127">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="50232-127">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50232-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50232-128">-InputObject</span></span>
<span data-ttu-id="50232-129">PS Galerisi görüntü tanımı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="50232-129">The PS Gallery Image Definition Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50232-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="50232-130">-MaximumMemory</span></span>
<span data-ttu-id="50232-131">Önerilen belleğin en yüksek değeri</span><span class="sxs-lookup"><span data-stu-id="50232-131">The maximum of the recommended memory</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50232-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="50232-132">-MaximumVCPU</span></span>
<span data-ttu-id="50232-133">Önerilen CPU çekirdeğin en yüksek değeri</span><span class="sxs-lookup"><span data-stu-id="50232-133">The maximum of the recommended CPU core</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50232-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="50232-134">-MinimumMemory</span></span>
<span data-ttu-id="50232-135">Önerilen belleğin en küçüğü</span><span class="sxs-lookup"><span data-stu-id="50232-135">The minimum of the recommended memory</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50232-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="50232-136">-MinimumVCPU</span></span>
<span data-ttu-id="50232-137">Önerilen CPU çekirdeğin en küçüğü</span><span class="sxs-lookup"><span data-stu-id="50232-137">The minimum of the recommended CPU core</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50232-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="50232-138">-Name</span></span>
<span data-ttu-id="50232-139">Galeri resim tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="50232-139">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50232-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="50232-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="50232-141">Gizlilik bildirimi URI 'si.</span><span class="sxs-lookup"><span data-stu-id="50232-141">The privacy statement uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50232-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="50232-142">-PurchasePlanName</span></span>
<span data-ttu-id="50232-143">Satın alma planının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="50232-143">The ID for the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50232-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="50232-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="50232-145">Satın alma planının ürün KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="50232-145">The product ID for the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50232-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="50232-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="50232-147">Satın alma planının Yayımcı Kımlığı.</span><span class="sxs-lookup"><span data-stu-id="50232-147">The publisher ID for the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50232-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="50232-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="50232-149">Sürüm notu URI 'si.</span><span class="sxs-lookup"><span data-stu-id="50232-149">The release note uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50232-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50232-150">-ResourceGroupName</span></span>
<span data-ttu-id="50232-151">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="50232-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="50232-152">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="50232-152">-ResourceId</span></span>
<span data-ttu-id="50232-153">Görüntü tanımı için kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="50232-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="50232-154">Etiketli</span><span class="sxs-lookup"><span data-stu-id="50232-154">-Tag</span></span>
<span data-ttu-id="50232-155">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="50232-155">Resource tags</span></span>

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

### <span data-ttu-id="50232-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="50232-156">-Confirm</span></span>
<span data-ttu-id="50232-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="50232-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50232-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50232-158">-WhatIf</span></span>
<span data-ttu-id="50232-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="50232-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50232-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="50232-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50232-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50232-161">CommonParameters</span></span>
<span data-ttu-id="50232-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50232-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50232-163">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="50232-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50232-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50232-164">INPUTS</span></span>

### <span data-ttu-id="50232-165">System. String</span><span class="sxs-lookup"><span data-stu-id="50232-165">System.String</span></span>

### <span data-ttu-id="50232-166">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerimage</span><span class="sxs-lookup"><span data-stu-id="50232-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="50232-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="50232-167">System.DateTime</span></span>

### <span data-ttu-id="50232-168">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="50232-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="50232-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="50232-169">System.Int32</span></span>

### <span data-ttu-id="50232-170">System. String []</span><span class="sxs-lookup"><span data-stu-id="50232-170">System.String[]</span></span>

## <span data-ttu-id="50232-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50232-171">OUTPUTS</span></span>

### <span data-ttu-id="50232-172">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerimage</span><span class="sxs-lookup"><span data-stu-id="50232-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="50232-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50232-173">NOTES</span></span>

## <span data-ttu-id="50232-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50232-174">RELATED LINKS</span></span>
