---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: aaba7580e2ffd00a2e5a9e61dd087e6af6359513
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096042"
---
# <span data-ttu-id="7bc30-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="7bc30-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="7bc30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bc30-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc30-103">Galeri resmi tanımı oluşturma.</span><span class="sxs-lookup"><span data-stu-id="7bc30-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="7bc30-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7bc30-104">SYNTAX</span></span>

```
New-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Location] <String> -Publisher <String> -Offer <String> -Sku <String> -OsState <OperatingSystemStateTypes>
 -OsType <OperatingSystemTypes> [-Description <String>] [-DisallowedDiskType <String[]>]
 [-EndOfLifeDate <DateTime>] [-Eula <String>] [-HyperVGeneration <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7bc30-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7bc30-105">DESCRIPTION</span></span>
<span data-ttu-id="7bc30-106">Galeri resmi tanımı oluşturma.</span><span class="sxs-lookup"><span data-stu-id="7bc30-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="7bc30-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7bc30-107">EXAMPLES</span></span>

### <span data-ttu-id="7bc30-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7bc30-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="7bc30-109">Galeri resmi tanımı oluşturma.</span><span class="sxs-lookup"><span data-stu-id="7bc30-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="7bc30-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7bc30-110">PARAMETERS</span></span>

### <span data-ttu-id="7bc30-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="7bc30-111">-AsJob</span></span>
<span data-ttu-id="7bc30-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7bc30-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7bc30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc30-113">-DefaultProfile</span></span>
<span data-ttu-id="7bc30-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7bc30-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bc30-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="7bc30-115">-Description</span></span>
<span data-ttu-id="7bc30-116">Galeri görüntüsü tanım kaynağının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="7bc30-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="7bc30-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="7bc30-117">-DisallowedDiskType</span></span>
<span data-ttu-id="7bc30-118">İzin verilmeyen disk türleri.</span><span class="sxs-lookup"><span data-stu-id="7bc30-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="7bc30-119">-Endofyaşam tarihi</span><span class="sxs-lookup"><span data-stu-id="7bc30-119">-EndOfLifeDate</span></span>
<span data-ttu-id="7bc30-120">Galeri görüntüsü tanımının kullanım ömrünün sonu</span><span class="sxs-lookup"><span data-stu-id="7bc30-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="7bc30-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="7bc30-121">-Eula</span></span>
<span data-ttu-id="7bc30-122">Galeri resmi tanımı için EULA sözleşmesi.</span><span class="sxs-lookup"><span data-stu-id="7bc30-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="7bc30-123">-Gallertadı</span><span class="sxs-lookup"><span data-stu-id="7bc30-123">-GalleryName</span></span>
<span data-ttu-id="7bc30-124">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="7bc30-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="7bc30-125">-Hiper VCR</span><span class="sxs-lookup"><span data-stu-id="7bc30-125">-HyperVGeneration</span></span>
<span data-ttu-id="7bc30-126">Sanal makinenin Hiper Yöneticisi üretimi.</span><span class="sxs-lookup"><span data-stu-id="7bc30-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="7bc30-127">Yalnızca işletim sistemi disklerine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="7bc30-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="7bc30-128">İzin verilen değerler v1 ve v2.</span><span class="sxs-lookup"><span data-stu-id="7bc30-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="7bc30-129">-Konum</span><span class="sxs-lookup"><span data-stu-id="7bc30-129">-Location</span></span>
<span data-ttu-id="7bc30-130">Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="7bc30-130">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc30-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="7bc30-131">-MaximumMemory</span></span>
<span data-ttu-id="7bc30-132">Önerilen belleğin en yüksek değeri</span><span class="sxs-lookup"><span data-stu-id="7bc30-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="7bc30-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="7bc30-133">-MaximumVCPU</span></span>
<span data-ttu-id="7bc30-134">Önerilen CPU çekirdeğin en yüksek değeri</span><span class="sxs-lookup"><span data-stu-id="7bc30-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="7bc30-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="7bc30-135">-MinimumMemory</span></span>
<span data-ttu-id="7bc30-136">Önerilen belleğin en küçüğü</span><span class="sxs-lookup"><span data-stu-id="7bc30-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="7bc30-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="7bc30-137">-MinimumVCPU</span></span>
<span data-ttu-id="7bc30-138">Önerilen CPU çekirdeğin en küçüğü</span><span class="sxs-lookup"><span data-stu-id="7bc30-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="7bc30-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="7bc30-139">-Name</span></span>
<span data-ttu-id="7bc30-140">Galeri resim tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="7bc30-140">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc30-141">-Teklif</span><span class="sxs-lookup"><span data-stu-id="7bc30-141">-Offer</span></span>
<span data-ttu-id="7bc30-142">Galeri görüntüsü tanım teklifinin adı.</span><span class="sxs-lookup"><span data-stu-id="7bc30-142">The name of the gallery Image Definition offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc30-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="7bc30-143">-OsState</span></span>
<span data-ttu-id="7bc30-144">İşletim sisteminin durumu</span><span class="sxs-lookup"><span data-stu-id="7bc30-144">The state of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc30-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="7bc30-145">-OsType</span></span>
<span data-ttu-id="7bc30-146">İşletim sisteminin türü</span><span class="sxs-lookup"><span data-stu-id="7bc30-146">The type of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc30-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="7bc30-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="7bc30-148">Gizlilik bildirimi URI 'si.</span><span class="sxs-lookup"><span data-stu-id="7bc30-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="7bc30-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="7bc30-149">-Publisher</span></span>
<span data-ttu-id="7bc30-150">Galeri görüntüsü tanım yayımcısının adı.</span><span class="sxs-lookup"><span data-stu-id="7bc30-150">The name of the gallery Image Definition publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc30-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="7bc30-151">-PurchasePlanName</span></span>
<span data-ttu-id="7bc30-152">Satın alma planının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7bc30-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="7bc30-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="7bc30-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="7bc30-154">Satın alma planının ürün KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7bc30-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="7bc30-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="7bc30-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="7bc30-156">Satın alma planının Yayımcı Kımlığı.</span><span class="sxs-lookup"><span data-stu-id="7bc30-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="7bc30-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="7bc30-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="7bc30-158">Sürüm notu URI 'si.</span><span class="sxs-lookup"><span data-stu-id="7bc30-158">The release note uri.</span></span>

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

### <span data-ttu-id="7bc30-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bc30-159">-ResourceGroupName</span></span>
<span data-ttu-id="7bc30-160">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7bc30-160">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc30-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="7bc30-161">-Sku</span></span>
<span data-ttu-id="7bc30-162">Galeri görüntüsü tanım SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="7bc30-162">The name of the gallery Image Definition SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc30-163">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7bc30-163">-Tag</span></span>
<span data-ttu-id="7bc30-164">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="7bc30-164">Resource tags</span></span>

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

### <span data-ttu-id="7bc30-165">-Onay</span><span class="sxs-lookup"><span data-stu-id="7bc30-165">-Confirm</span></span>
<span data-ttu-id="7bc30-166">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7bc30-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bc30-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bc30-167">-WhatIf</span></span>
<span data-ttu-id="7bc30-168">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7bc30-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bc30-169">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7bc30-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bc30-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc30-170">CommonParameters</span></span>
<span data-ttu-id="7bc30-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7bc30-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc30-172">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7bc30-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc30-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7bc30-173">INPUTS</span></span>

### <span data-ttu-id="7bc30-174">System. String</span><span class="sxs-lookup"><span data-stu-id="7bc30-174">System.String</span></span>

### <span data-ttu-id="7bc30-175">Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="7bc30-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="7bc30-176">Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="7bc30-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="7bc30-177">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="7bc30-177">System.DateTime</span></span>

### <span data-ttu-id="7bc30-178">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7bc30-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7bc30-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7bc30-179">System.Int32</span></span>

### <span data-ttu-id="7bc30-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="7bc30-180">System.String[]</span></span>

## <span data-ttu-id="7bc30-181">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7bc30-181">OUTPUTS</span></span>

### <span data-ttu-id="7bc30-182">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerimage</span><span class="sxs-lookup"><span data-stu-id="7bc30-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="7bc30-183">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7bc30-183">NOTES</span></span>

## <span data-ttu-id="7bc30-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7bc30-184">RELATED LINKS</span></span>