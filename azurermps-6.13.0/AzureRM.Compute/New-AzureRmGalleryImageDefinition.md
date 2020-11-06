---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 8dcfe4adedd7da375e888dade108125d7899d7d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594447"
---
# <span data-ttu-id="be7cf-101">New-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="be7cf-101">New-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="be7cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be7cf-102">SYNOPSIS</span></span>
<span data-ttu-id="be7cf-103">Galeri resmi tanımı oluşturma.</span><span class="sxs-lookup"><span data-stu-id="be7cf-103">Create a gallery image definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be7cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be7cf-104">SYNTAX</span></span>

```
New-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String>
 [-AsJob] [-Location] <String> -Publisher <String> -Offer <String> -Sku <String>
 -OsState <OperatingSystemStateTypes> -OsType <OperatingSystemTypes> [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be7cf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="be7cf-105">DESCRIPTION</span></span>
<span data-ttu-id="be7cf-106">Galeri resmi tanımı oluşturma.</span><span class="sxs-lookup"><span data-stu-id="be7cf-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="be7cf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be7cf-107">EXAMPLES</span></span>

### <span data-ttu-id="be7cf-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="be7cf-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="be7cf-109">Galeri resmi tanımı oluşturma.</span><span class="sxs-lookup"><span data-stu-id="be7cf-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="be7cf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be7cf-110">PARAMETERS</span></span>

### <span data-ttu-id="be7cf-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="be7cf-111">-AsJob</span></span>
<span data-ttu-id="be7cf-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="be7cf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="be7cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be7cf-113">-DefaultProfile</span></span>
<span data-ttu-id="be7cf-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be7cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be7cf-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="be7cf-115">-Description</span></span>
<span data-ttu-id="be7cf-116">Galeri görüntüsü tanım kaynağının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="be7cf-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="be7cf-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="be7cf-117">-DisallowedDiskType</span></span>
<span data-ttu-id="be7cf-118">İzin verilmeyen disk türleri.</span><span class="sxs-lookup"><span data-stu-id="be7cf-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="be7cf-119">-Endofyaşam tarihi</span><span class="sxs-lookup"><span data-stu-id="be7cf-119">-EndOfLifeDate</span></span>
<span data-ttu-id="be7cf-120">Galeri görüntüsü tanımının kullanım ömrünün sonu</span><span class="sxs-lookup"><span data-stu-id="be7cf-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="be7cf-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="be7cf-121">-Eula</span></span>
<span data-ttu-id="be7cf-122">Galeri resmi tanımı için EULA sözleşmesi.</span><span class="sxs-lookup"><span data-stu-id="be7cf-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="be7cf-123">-Gallertadı</span><span class="sxs-lookup"><span data-stu-id="be7cf-123">-GalleryName</span></span>
<span data-ttu-id="be7cf-124">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="be7cf-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="be7cf-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="be7cf-125">-Location</span></span>
<span data-ttu-id="be7cf-126">Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="be7cf-126">Resource location</span></span>

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

### <span data-ttu-id="be7cf-127">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="be7cf-127">-MaximumMemory</span></span>
<span data-ttu-id="be7cf-128">Önerilen belleğin en yüksek değeri</span><span class="sxs-lookup"><span data-stu-id="be7cf-128">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="be7cf-129">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="be7cf-129">-MaximumVCPU</span></span>
<span data-ttu-id="be7cf-130">Önerilen CPU çekirdeğin en yüksek değeri</span><span class="sxs-lookup"><span data-stu-id="be7cf-130">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="be7cf-131">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="be7cf-131">-MinimumMemory</span></span>
<span data-ttu-id="be7cf-132">Önerilen belleğin en küçüğü</span><span class="sxs-lookup"><span data-stu-id="be7cf-132">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="be7cf-133">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="be7cf-133">-MinimumVCPU</span></span>
<span data-ttu-id="be7cf-134">Önerilen CPU çekirdeğin en küçüğü</span><span class="sxs-lookup"><span data-stu-id="be7cf-134">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="be7cf-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="be7cf-135">-Name</span></span>
<span data-ttu-id="be7cf-136">Galeri resim tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="be7cf-136">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="be7cf-137">-Teklif</span><span class="sxs-lookup"><span data-stu-id="be7cf-137">-Offer</span></span>
<span data-ttu-id="be7cf-138">Galeri görüntüsü tanım teklifinin adı.</span><span class="sxs-lookup"><span data-stu-id="be7cf-138">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="be7cf-139">-OsState</span><span class="sxs-lookup"><span data-stu-id="be7cf-139">-OsState</span></span>
<span data-ttu-id="be7cf-140">İşletim sisteminin durumu</span><span class="sxs-lookup"><span data-stu-id="be7cf-140">The state of OS</span></span>

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

### <span data-ttu-id="be7cf-141">-OsType</span><span class="sxs-lookup"><span data-stu-id="be7cf-141">-OsType</span></span>
<span data-ttu-id="be7cf-142">İşletim sisteminin türü</span><span class="sxs-lookup"><span data-stu-id="be7cf-142">The type of OS</span></span>

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

### <span data-ttu-id="be7cf-143">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="be7cf-143">-PrivacyStatementUri</span></span>
<span data-ttu-id="be7cf-144">Gizlilik bildirimi URI 'si.</span><span class="sxs-lookup"><span data-stu-id="be7cf-144">The privacy statement uri.</span></span>

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

### <span data-ttu-id="be7cf-145">-Publisher</span><span class="sxs-lookup"><span data-stu-id="be7cf-145">-Publisher</span></span>
<span data-ttu-id="be7cf-146">Galeri görüntüsü tanım yayımcısının adı.</span><span class="sxs-lookup"><span data-stu-id="be7cf-146">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="be7cf-147">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="be7cf-147">-PurchasePlanName</span></span>
<span data-ttu-id="be7cf-148">Satın alma planının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="be7cf-148">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="be7cf-149">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="be7cf-149">-PurchasePlanProduct</span></span>
<span data-ttu-id="be7cf-150">Satın alma planının ürün KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="be7cf-150">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="be7cf-151">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="be7cf-151">-PurchasePlanPublisher</span></span>
<span data-ttu-id="be7cf-152">Satın alma planının Yayımcı Kımlığı.</span><span class="sxs-lookup"><span data-stu-id="be7cf-152">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="be7cf-153">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="be7cf-153">-ReleaseNoteUri</span></span>
<span data-ttu-id="be7cf-154">Sürüm notu URI 'si.</span><span class="sxs-lookup"><span data-stu-id="be7cf-154">The release note uri.</span></span>

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

### <span data-ttu-id="be7cf-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be7cf-155">-ResourceGroupName</span></span>
<span data-ttu-id="be7cf-156">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="be7cf-156">The name of the resource group.</span></span>

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

### <span data-ttu-id="be7cf-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="be7cf-157">-Sku</span></span>
<span data-ttu-id="be7cf-158">Galeri görüntüsü tanım SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="be7cf-158">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="be7cf-159">Etiketli</span><span class="sxs-lookup"><span data-stu-id="be7cf-159">-Tag</span></span>
<span data-ttu-id="be7cf-160">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="be7cf-160">Resource tags</span></span>

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

### <span data-ttu-id="be7cf-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="be7cf-161">-Confirm</span></span>
<span data-ttu-id="be7cf-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="be7cf-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be7cf-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be7cf-163">-WhatIf</span></span>
<span data-ttu-id="be7cf-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="be7cf-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be7cf-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="be7cf-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be7cf-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be7cf-166">CommonParameters</span></span>
<span data-ttu-id="be7cf-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be7cf-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be7cf-168">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be7cf-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be7cf-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be7cf-169">INPUTS</span></span>

### <span data-ttu-id="be7cf-170">System. String</span><span class="sxs-lookup"><span data-stu-id="be7cf-170">System.String</span></span>

### <span data-ttu-id="be7cf-171">Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="be7cf-171">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="be7cf-172">Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="be7cf-172">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="be7cf-173">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="be7cf-173">System.DateTime</span></span>

### <span data-ttu-id="be7cf-174">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="be7cf-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="be7cf-175">System. Int32</span><span class="sxs-lookup"><span data-stu-id="be7cf-175">System.Int32</span></span>

### <span data-ttu-id="be7cf-176">System. String []</span><span class="sxs-lookup"><span data-stu-id="be7cf-176">System.String[]</span></span>

## <span data-ttu-id="be7cf-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be7cf-177">OUTPUTS</span></span>

### <span data-ttu-id="be7cf-178">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerimage</span><span class="sxs-lookup"><span data-stu-id="be7cf-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="be7cf-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be7cf-179">NOTES</span></span>

## <span data-ttu-id="be7cf-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be7cf-180">RELATED LINKS</span></span>
