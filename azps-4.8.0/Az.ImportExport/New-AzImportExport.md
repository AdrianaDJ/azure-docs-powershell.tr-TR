---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: 9b0cf40b090111a6bd32bc87b6e72bc542eae5ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267697"
---
# <span data-ttu-id="b7868-101">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="b7868-101">New-AzImportExport</span></span>

## <span data-ttu-id="b7868-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7868-102">SYNOPSIS</span></span>
<span data-ttu-id="b7868-103">Belirtilen abonelikte yeni bir iş oluşturur veya mevcut işi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b7868-103">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="b7868-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7868-104">SYNTAX</span></span>

```
New-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-ClientTenantId <String>] [-BackupDriveManifest] [-BlobListBlobPath <String[]>]
 [-BlobListBlobPathPrefix <String[]>] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DiagnosticsPath <String>] [-DriveList <IDriveStatus[]>]
 [-ExportBlobListblobPath <String>] [-IncompleteBlobListUri <String>] [-JobType <String>] [-Location <String>]
 [-LogLevel <String>] [-PercentComplete <Int32>] [-ProvisioningState <String>] [-ReturnAddressCity <String>]
 [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>]
 [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnPackageCarrierName <String>]
 [-ReturnPackageDriveCount <Int32>] [-ReturnPackageShipDate <String>] [-ReturnPackageTrackingNumber <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>]
 [-ShippingInformationCity <String>] [-ShippingInformationCountryOrRegion <String>]
 [-ShippingInformationPhone <String>] [-ShippingInformationPostalCode <String>]
 [-ShippingInformationRecipientName <String>] [-ShippingInformationStateOrProvince <String>]
 [-ShippingInformationStreetAddress1 <String>] [-ShippingInformationStreetAddress2 <String>] [-State <String>]
 [-StorageAccountId <String>] [-Tag <IPutJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b7868-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7868-105">DESCRIPTION</span></span>
<span data-ttu-id="b7868-106">Belirtilen abonelikte yeni bir iş oluşturur veya mevcut işi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b7868-106">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="b7868-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7868-107">EXAMPLES</span></span>

### <span data-ttu-id="b7868-108">Örnek 1: yeni bir ımportexport işi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b7868-108">Example 1: Create a new ImportExport job</span></span>
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="b7868-109">Bu cmdlet 'ler yeni bir ımportexport işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b7868-109">These cmdlets create a new ImportExport job.</span></span>

## <span data-ttu-id="b7868-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7868-110">PARAMETERS</span></span>

### <span data-ttu-id="b7868-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="b7868-111">-AcceptLanguage</span></span>
<span data-ttu-id="b7868-112">Yanıtın tercih ettiği dili belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7868-112">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-113">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="b7868-113">-BackupDriveManifest</span></span>
<span data-ttu-id="b7868-114">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="b7868-114">Default value is false.</span></span>
<span data-ttu-id="b7868-115">Sürücülerdeki bildirim dosyalarının blob 'ları engellemek için kopyalanıp kopyalanmaması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7868-115">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="b7868-116">-BlobListBlobPath</span><span class="sxs-lookup"><span data-stu-id="b7868-116">-BlobListBlobPath</span></span>
<span data-ttu-id="b7868-117">Blob-yol dizelerinin koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="b7868-117">A collection of blob-path strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-118">-BlobListBlobPathPrefix</span><span class="sxs-lookup"><span data-stu-id="b7868-118">-BlobListBlobPathPrefix</span></span>
<span data-ttu-id="b7868-119">Blob-önek dizeleri koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="b7868-119">A collection of blob-prefix strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-120">-Cancelisteniyor</span><span class="sxs-lookup"><span data-stu-id="b7868-120">-CancelRequested</span></span>
<span data-ttu-id="b7868-121">İşi iptal etmek üzere bir isteğin gönderilip gönderilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b7868-121">Indicates whether a request has been submitted to cancel the job.</span></span>

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

### <span data-ttu-id="b7868-122">-Clienttenantıd</span><span class="sxs-lookup"><span data-stu-id="b7868-122">-ClientTenantId</span></span>
<span data-ttu-id="b7868-123">İsteği yapan istemcinin kiracı KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b7868-123">The tenant ID of the client making the request.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7868-124">-DefaultProfile</span></span>
<span data-ttu-id="b7868-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b7868-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-126">-Bir Ypackagecvarername</span><span class="sxs-lookup"><span data-stu-id="b7868-126">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="b7868-127">İçeri veya dışarı aktarma sürücülerini sevk etmek için kullanılan taşıyıcının adı.</span><span class="sxs-lookup"><span data-stu-id="b7868-127">The name of the carrier that is used to ship the import or export drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-128">-Bir değer</span><span class="sxs-lookup"><span data-stu-id="b7868-128">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="b7868-129">Pakete dahil edilen sürücü sayısı.</span><span class="sxs-lookup"><span data-stu-id="b7868-129">The number of drives included in the package.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-130">-Eypackageshipdate</span><span class="sxs-lookup"><span data-stu-id="b7868-130">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="b7868-131">Paketin gönderildiği tarih.</span><span class="sxs-lookup"><span data-stu-id="b7868-131">The date when the package is shipped.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-132">-, Sayı</span><span class="sxs-lookup"><span data-stu-id="b7868-132">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="b7868-133">Paketin izleme numarası.</span><span class="sxs-lookup"><span data-stu-id="b7868-133">The tracking number of the package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-134">-DiagnosticsPath</span><span class="sxs-lookup"><span data-stu-id="b7868-134">-DiagnosticsPath</span></span>
<span data-ttu-id="b7868-135">Kopyalama günlüklerinin ve sürücü bildirim dosyalarının (etkinleştirilmişse) yedeklemelerinin saklanacağı sanal blob dizini saklanır.</span><span class="sxs-lookup"><span data-stu-id="b7868-135">The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="b7868-136">-DriveList</span></span>
<span data-ttu-id="b7868-137">İşi oluşturan on taneye kadar sürücünün listesi.</span><span class="sxs-lookup"><span data-stu-id="b7868-137">List of up to ten drives that comprise the job.</span></span>
<span data-ttu-id="b7868-138">Sürücü listesi, içeri aktarma işi için gerekli bir öğedir; dışarı aktarma işleri için belirtilmez.</span><span class="sxs-lookup"><span data-stu-id="b7868-138">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
<span data-ttu-id="b7868-139">Oluşturmak için, sürücü LISTESI özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b7868-139">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-140">-ExportBlobListblobPath</span><span class="sxs-lookup"><span data-stu-id="b7868-140">-ExportBlobListblobPath</span></span>
<span data-ttu-id="b7868-141">Kapsayıcı adından başlayarak yukarıda tanımlanan blob yollarının veya blob yolu öneklerinin listesini içeren blok blob 'una göreli URI.</span><span class="sxs-lookup"><span data-stu-id="b7868-141">The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name.</span></span>
<span data-ttu-id="b7868-142">Blob kök kapsayıcıda yer alıyorsa URI $root ile başlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="b7868-142">If the blob is in root container, the URI must begin with $root.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-143">-IncompleteBlobListUri</span><span class="sxs-lookup"><span data-stu-id="b7868-143">-IncompleteBlobListUri</span></span>
<span data-ttu-id="b7868-144">Yetersiz sürücü alanı nedeniyle verilemeyen blob adları listesini içeren bir blok blob 'unu gösteren blob yolu.</span><span class="sxs-lookup"><span data-stu-id="b7868-144">A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space.</span></span>
<span data-ttu-id="b7868-145">Tüm blob 'lar başarıyla verilirse, bu öğe yanıta dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="b7868-145">If all blobs were exported successfully, then this element is not included in the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-146">-JobType</span><span class="sxs-lookup"><span data-stu-id="b7868-146">-JobType</span></span>
<span data-ttu-id="b7868-147">İşin türü</span><span class="sxs-lookup"><span data-stu-id="b7868-147">The type of job</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-148">-Konum</span><span class="sxs-lookup"><span data-stu-id="b7868-148">-Location</span></span>
<span data-ttu-id="b7868-149">İşin oluşturulması gereken Azure konumunu belirtir</span><span class="sxs-lookup"><span data-stu-id="b7868-149">Specifies the supported Azure location where the job should be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-150">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="b7868-150">-LogLevel</span></span>
<span data-ttu-id="b7868-151">Varsayılan değer Error değeridir.</span><span class="sxs-lookup"><span data-stu-id="b7868-151">Default value is Error.</span></span>
<span data-ttu-id="b7868-152">Hata günlüğünün etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b7868-152">Indicates whether error logging or verbose logging will be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-153">-Ad</span><span class="sxs-lookup"><span data-stu-id="b7868-153">-Name</span></span>
<span data-ttu-id="b7868-154">İçeri/dışarı aktarma işinin adı.</span><span class="sxs-lookup"><span data-stu-id="b7868-154">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-155">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="b7868-155">-PercentComplete</span></span>
<span data-ttu-id="b7868-156">İş için tamamlanan tüm yüzde.</span><span class="sxs-lookup"><span data-stu-id="b7868-156">Overall percentage completed for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-157">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="b7868-157">-ProvisioningState</span></span>
<span data-ttu-id="b7868-158">İşin hazırlık durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7868-158">Specifies the provisioning state of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7868-159">-ResourceGroupName</span></span>
<span data-ttu-id="b7868-160">Kaynak grubu adı, kullanıcı aboneliği içinde kaynak grubunu benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b7868-160">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-161">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="b7868-161">-ReturnAddressCity</span></span>
<span data-ttu-id="b7868-162">Sürücüleri döndürürken kullanılacak şehir adı.</span><span class="sxs-lookup"><span data-stu-id="b7868-162">The city name to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-163">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="b7868-163">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="b7868-164">Sürücüleri döndürürken kullanılacak ülke veya bölge.</span><span class="sxs-lookup"><span data-stu-id="b7868-164">The country or region to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-165">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="b7868-165">-ReturnAddressEmail</span></span>
<span data-ttu-id="b7868-166">Döndürülen sürücüler alıcısının e-posta adresi.</span><span class="sxs-lookup"><span data-stu-id="b7868-166">Email address of the recipient of the returned drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-167">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="b7868-167">-ReturnAddressPhone</span></span>
<span data-ttu-id="b7868-168">Döndürülen sürücüler alıcısının telefon numarası.</span><span class="sxs-lookup"><span data-stu-id="b7868-168">Phone number of the recipient of the returned drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-169">-Returnaddresspostakodu</span><span class="sxs-lookup"><span data-stu-id="b7868-169">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="b7868-170">Sürücüleri döndürürken kullanılacak posta kodu.</span><span class="sxs-lookup"><span data-stu-id="b7868-170">The postal code to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-171">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="b7868-171">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="b7868-172">İade edildiğinde sabit sürücüleri alacak olan alıcının adı.</span><span class="sxs-lookup"><span data-stu-id="b7868-172">The name of the recipient who will receive the hard drives when they are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-173">-Returnaddressstateorili</span><span class="sxs-lookup"><span data-stu-id="b7868-173">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="b7868-174">Sürücüleri döndürürken kullanılacak eyalet veya bölge.</span><span class="sxs-lookup"><span data-stu-id="b7868-174">The state or province to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-175">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="b7868-175">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="b7868-176">Sürücülerin döndürülmesi sırasında kullanılacak sokak adresinin ilk satırı.</span><span class="sxs-lookup"><span data-stu-id="b7868-176">The first line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-177">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="b7868-177">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="b7868-178">Sürücülerin döndürülmesi sırasında kullanılacak sokak adresinin ikinci satırı.</span><span class="sxs-lookup"><span data-stu-id="b7868-178">The second line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-179">-Returnpackagecvarış Ername</span><span class="sxs-lookup"><span data-stu-id="b7868-179">-ReturnPackageCarrierName</span></span>
<span data-ttu-id="b7868-180">İçeri veya dışarı aktarma sürücülerini sevk etmek için kullanılan taşıyıcının adı.</span><span class="sxs-lookup"><span data-stu-id="b7868-180">The name of the carrier that is used to ship the import or export drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-181">-ReturnPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="b7868-181">-ReturnPackageDriveCount</span></span>
<span data-ttu-id="b7868-182">Pakete dahil edilen sürücü sayısı.</span><span class="sxs-lookup"><span data-stu-id="b7868-182">The number of drives included in the package.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-183">-ReturnPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="b7868-183">-ReturnPackageShipDate</span></span>
<span data-ttu-id="b7868-184">Paketin gönderildiği tarih.</span><span class="sxs-lookup"><span data-stu-id="b7868-184">The date when the package is shipped.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-185">-Returnpackapracnumber</span><span class="sxs-lookup"><span data-stu-id="b7868-185">-ReturnPackageTrackingNumber</span></span>
<span data-ttu-id="b7868-186">Paketin izleme numarası.</span><span class="sxs-lookup"><span data-stu-id="b7868-186">The tracking number of the package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-187">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="b7868-187">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="b7868-188">Taşıyıcıda müşterinin hesap numarası.</span><span class="sxs-lookup"><span data-stu-id="b7868-188">The customer's account number with the carrier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-189">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="b7868-189">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="b7868-190">Taşıyıcı adı.</span><span class="sxs-lookup"><span data-stu-id="b7868-190">The carrier's name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-191">-Shippingınformationcity</span><span class="sxs-lookup"><span data-stu-id="b7868-191">-ShippingInformationCity</span></span>
<span data-ttu-id="b7868-192">Sürücüleri döndürürken kullanılacak şehir adı.</span><span class="sxs-lookup"><span data-stu-id="b7868-192">The city name to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-193">-Shippingınformationcountryorregion</span><span class="sxs-lookup"><span data-stu-id="b7868-193">-ShippingInformationCountryOrRegion</span></span>
<span data-ttu-id="b7868-194">Sürücüleri döndürürken kullanılacak ülke veya bölge.</span><span class="sxs-lookup"><span data-stu-id="b7868-194">The country or region to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-195">-Shippingınformationphone</span><span class="sxs-lookup"><span data-stu-id="b7868-195">-ShippingInformationPhone</span></span>
<span data-ttu-id="b7868-196">Döndürülen sürücüler alıcısının telefon numarası.</span><span class="sxs-lookup"><span data-stu-id="b7868-196">Phone number of the recipient of the returned drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-197">-Shippingınformationpostakodu</span><span class="sxs-lookup"><span data-stu-id="b7868-197">-ShippingInformationPostalCode</span></span>
<span data-ttu-id="b7868-198">Sürücüleri döndürürken kullanılacak posta kodu.</span><span class="sxs-lookup"><span data-stu-id="b7868-198">The postal code to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-199">-Shippingınformationrecipientname</span><span class="sxs-lookup"><span data-stu-id="b7868-199">-ShippingInformationRecipientName</span></span>
<span data-ttu-id="b7868-200">İade edildiğinde sabit sürücüleri alacak olan alıcının adı.</span><span class="sxs-lookup"><span data-stu-id="b7868-200">The name of the recipient who will receive the hard drives when they are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-201">-Shippingınformationstateoreyalet</span><span class="sxs-lookup"><span data-stu-id="b7868-201">-ShippingInformationStateOrProvince</span></span>
<span data-ttu-id="b7868-202">Sürücüleri döndürürken kullanılacak eyalet veya bölge.</span><span class="sxs-lookup"><span data-stu-id="b7868-202">The state or province to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-203">-ShippingInformationStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="b7868-203">-ShippingInformationStreetAddress1</span></span>
<span data-ttu-id="b7868-204">Sürücülerin döndürülmesi sırasında kullanılacak sokak adresinin ilk satırı.</span><span class="sxs-lookup"><span data-stu-id="b7868-204">The first line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-205">-ShippingInformationStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="b7868-205">-ShippingInformationStreetAddress2</span></span>
<span data-ttu-id="b7868-206">Sürücülerin döndürülmesi sırasında kullanılacak sokak adresinin ikinci satırı.</span><span class="sxs-lookup"><span data-stu-id="b7868-206">The second line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-207">Durumlu</span><span class="sxs-lookup"><span data-stu-id="b7868-207">-State</span></span>
<span data-ttu-id="b7868-208">İşin geçerli durumu.</span><span class="sxs-lookup"><span data-stu-id="b7868-208">Current state of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-209">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="b7868-209">-StorageAccountId</span></span>
<span data-ttu-id="b7868-210">Verilerin aktarılacağı veya alınacağı depolama hesabının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="b7868-210">The resource identifier of the storage account where data will be imported to or exported from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-211">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b7868-211">-SubscriptionId</span></span>
<span data-ttu-id="b7868-212">Azure kullanıcısına ait abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b7868-212">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-213">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b7868-213">-Tag</span></span>
<span data-ttu-id="b7868-214">İşe atanacak etiketleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7868-214">Specifies the tags that will be assigned to the job.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IPutJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-215">-Onay</span><span class="sxs-lookup"><span data-stu-id="b7868-215">-Confirm</span></span>
<span data-ttu-id="b7868-216">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b7868-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7868-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7868-217">-WhatIf</span></span>
<span data-ttu-id="b7868-218">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b7868-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7868-219">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b7868-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7868-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7868-220">CommonParameters</span></span>
<span data-ttu-id="b7868-221">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7868-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7868-222">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b7868-222">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7868-223">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7868-223">INPUTS</span></span>

## <span data-ttu-id="b7868-224">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7868-224">OUTPUTS</span></span>

### <span data-ttu-id="b7868-225">Microsoft. Azure. PowerShell. cmdlet. ımportexport. modeller. Api20161101. ıjobresponse</span><span class="sxs-lookup"><span data-stu-id="b7868-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="b7868-226">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7868-226">NOTES</span></span>

<span data-ttu-id="b7868-227">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="b7868-227">ALIASES</span></span>

<span data-ttu-id="b7868-228">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="b7868-228">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b7868-229">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b7868-229">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7868-230">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b7868-230">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b7868-231">DRIVELIST <IDriveStatus [] >: işi oluşturan en çok on sürücü listesi.</span><span class="sxs-lookup"><span data-stu-id="b7868-231">DRIVELIST <IDriveStatus[]>: List of up to ten drives that comprise the job.</span></span> <span data-ttu-id="b7868-232">Sürücü listesi, içeri aktarma işi için gerekli bir öğedir; dışarı aktarma işleri için belirtilmez.</span><span class="sxs-lookup"><span data-stu-id="b7868-232">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
  - <span data-ttu-id="b7868-233">`[BitLockerKey <String>]`: Sürücüyü şifrelemek için kullanılan BitLocker anahtarı.</span><span class="sxs-lookup"><span data-stu-id="b7868-233">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="b7868-234">`[BytesSucceeded <Int64?>]`: Sürücü için bayt başarıyla aktarıldı.</span><span class="sxs-lookup"><span data-stu-id="b7868-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="b7868-235">`[CopyStatus <String>]`: Veri aktarım süreci hakkında ayrıntılı durum.</span><span class="sxs-lookup"><span data-stu-id="b7868-235">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="b7868-236">Bu alan, sürücü aktarma durumunda olana kadar yanıtta döndürülmez.</span><span class="sxs-lookup"><span data-stu-id="b7868-236">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="b7868-237">`[DriveHeaderHash <String>]`: Sürücü üstbilgisi karma değeri.</span><span class="sxs-lookup"><span data-stu-id="b7868-237">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="b7868-238">`[DriveId <String>]`: Sürücünün boşluksuz donanım seri numarası.</span><span class="sxs-lookup"><span data-stu-id="b7868-238">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="b7868-239">`[ErrorLogUri <String>]`: Veri aktarma işlemi için hata günlüğünü içeren blob 'a işaret eden bir URI.</span><span class="sxs-lookup"><span data-stu-id="b7868-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="b7868-240">`[ManifestFile <String>]`: Sürücüdeki bildirim dosyasının göreli yolu.</span><span class="sxs-lookup"><span data-stu-id="b7868-240">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="b7868-241">`[ManifestHash <String>]`: Sürücüdeki bildirim dosyasının Base16 ile kodlanmış MD5 karması.</span><span class="sxs-lookup"><span data-stu-id="b7868-241">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="b7868-242">`[ManifestUri <String>]`: Sürücü bildirim dosyasını içeren blob 'a işaret eden bir URI.</span><span class="sxs-lookup"><span data-stu-id="b7868-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="b7868-243">`[PercentComplete <Int32?>]`: Sürücü için yüzde tamamlandı.</span><span class="sxs-lookup"><span data-stu-id="b7868-243">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="b7868-244">`[State <DriveState?>]`: Sürücünün geçerli durumu.</span><span class="sxs-lookup"><span data-stu-id="b7868-244">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="b7868-245">`[VerboseLogUri <String>]`: Veri aktarma işlemi için ayrıntılı günlüğü içeren blob 'a işaret eden bir URI.</span><span class="sxs-lookup"><span data-stu-id="b7868-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

## <span data-ttu-id="b7868-246">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7868-246">RELATED LINKS</span></span>

