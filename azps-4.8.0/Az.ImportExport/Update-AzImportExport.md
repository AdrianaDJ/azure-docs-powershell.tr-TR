---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: d6ed55cef91dc93f0ce9101adf94d9dc6931d07c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267691"
---
# <span data-ttu-id="0ce10-101">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="0ce10-101">Update-AzImportExport</span></span>

## <span data-ttu-id="0ce10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ce10-102">SYNOPSIS</span></span>
<span data-ttu-id="0ce10-103">İşin belirli özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0ce10-103">Updates specific properties of a job.</span></span>
<span data-ttu-id="0ce10-104">İçeri/dışarı aktarma hizmetine, içeri veya dışarı aktarma işi yapan sabit sürücülerin Microsoft veri merkezine sevk edilmiş olduğunu bildirmek için bu işlemi arayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0ce10-104">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="0ce10-105">Var olan bir işi iptal etmek için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0ce10-105">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="0ce10-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ce10-106">SYNTAX</span></span>

### <span data-ttu-id="0ce10-107">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0ce10-107">UpdateExpanded (Default)</span></span>
```
Update-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-BackupDriveManifest] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>] [-LogLevel <String>]
 [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>]
 [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnShippingCarrierAccountNumber <String>]
 [-ReturnShippingCarrierName <String>] [-State <String>] [-Tag <IUpdateJobParametersTags>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0ce10-108">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="0ce10-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>] [-BackupDriveManifest]
 [-CancelRequested] [-DeliveryPackageCarrierName <String>] [-DeliveryPackageDriveCount <Int32>]
 [-DeliveryPackageShipDate <String>] [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>]
 [-LogLevel <String>] [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>]
 [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>]
 [-ReturnAddressRecipientName <String>] [-ReturnAddressStateOrProvince <String>]
 [-ReturnAddressStreetAddress1 <String>] [-ReturnAddressStreetAddress2 <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>] [-State <String>]
 [-Tag <IUpdateJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0ce10-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ce10-109">DESCRIPTION</span></span>
<span data-ttu-id="0ce10-110">İşin belirli özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0ce10-110">Updates specific properties of a job.</span></span>
<span data-ttu-id="0ce10-111">İçeri/dışarı aktarma hizmetine, içeri veya dışarı aktarma işi yapan sabit sürücülerin Microsoft veri merkezine sevk edilmiş olduğunu bildirmek için bu işlemi arayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0ce10-111">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="0ce10-112">Var olan bir işi iptal etmek için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0ce10-112">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="0ce10-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ce10-113">EXAMPLES</span></span>

### <span data-ttu-id="0ce10-114">Örnek 1: kaynak grubuna ve sunucu adına göre ımportexport işini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0ce10-114">Example 1: Update ImportExport job by resource group and server name</span></span>
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="0ce10-115">Bu cmdlet, kaynak grubu ve sunucu adına göre ımportexport işini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0ce10-115">This cmdlet updates ImportExport job by resource group and server name.</span></span>

### <span data-ttu-id="0ce10-116">Örnek 2: ımportexport işini Identity olarak güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="0ce10-116">Example 2: Update ImportExport job by identity.</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="0ce10-117">Bu cmdlet, ımportexport işini Identity 'ye güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0ce10-117">This cmdlet updates ImportExport job by identity.</span></span>

## <span data-ttu-id="0ce10-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ce10-118">PARAMETERS</span></span>

### <span data-ttu-id="0ce10-119">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="0ce10-119">-AcceptLanguage</span></span>
<span data-ttu-id="0ce10-120">Yanıtın tercih ettiği dili belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ce10-120">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="0ce10-121">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="0ce10-121">-BackupDriveManifest</span></span>
<span data-ttu-id="0ce10-122">Sürücülerdeki bildirim dosyalarının blob 'ları engellemek için kopyalanıp kopyalanmaması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ce10-122">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="0ce10-123">-Cancelisteniyor</span><span class="sxs-lookup"><span data-stu-id="0ce10-123">-CancelRequested</span></span>
<span data-ttu-id="0ce10-124">Belirtilmişse değer doğru olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0ce10-124">If specified, the value must be true.</span></span>
<span data-ttu-id="0ce10-125">Hizmet işi iptal etmeye çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="0ce10-125">The service will attempt to cancel the job.</span></span>

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

### <span data-ttu-id="0ce10-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ce10-126">-DefaultProfile</span></span>
<span data-ttu-id="0ce10-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0ce10-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ce10-128">-Bir Ypackagecvarername</span><span class="sxs-lookup"><span data-stu-id="0ce10-128">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="0ce10-129">İçeri veya dışarı aktarma sürücülerini sevk etmek için kullanılan taşıyıcının adı.</span><span class="sxs-lookup"><span data-stu-id="0ce10-129">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="0ce10-130">-Bir değer</span><span class="sxs-lookup"><span data-stu-id="0ce10-130">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="0ce10-131">Pakete dahil edilen sürücü sayısı.</span><span class="sxs-lookup"><span data-stu-id="0ce10-131">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="0ce10-132">-Eypackageshipdate</span><span class="sxs-lookup"><span data-stu-id="0ce10-132">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="0ce10-133">Paketin gönderildiği tarih.</span><span class="sxs-lookup"><span data-stu-id="0ce10-133">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="0ce10-134">-, Sayı</span><span class="sxs-lookup"><span data-stu-id="0ce10-134">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="0ce10-135">Paketin izleme numarası.</span><span class="sxs-lookup"><span data-stu-id="0ce10-135">The tracking number of the package.</span></span>

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

### <span data-ttu-id="0ce10-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="0ce10-136">-DriveList</span></span>
<span data-ttu-id="0ce10-137">İşi oluşturan sürücülerin listesi.</span><span class="sxs-lookup"><span data-stu-id="0ce10-137">List of drives that comprise the job.</span></span>
<span data-ttu-id="0ce10-138">Oluşturmak için, sürücü LISTESI özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0ce10-138">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="0ce10-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ce10-139">-InputObject</span></span>
<span data-ttu-id="0ce10-140">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0ce10-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ce10-141">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="0ce10-141">-LogLevel</span></span>
<span data-ttu-id="0ce10-142">Hata günlüğünün etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0ce10-142">Indicates whether error logging or verbose logging is enabled.</span></span>

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

### <span data-ttu-id="0ce10-143">-Ad</span><span class="sxs-lookup"><span data-stu-id="0ce10-143">-Name</span></span>
<span data-ttu-id="0ce10-144">İçeri/dışarı aktarma işinin adı.</span><span class="sxs-lookup"><span data-stu-id="0ce10-144">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ce10-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ce10-145">-ResourceGroupName</span></span>
<span data-ttu-id="0ce10-146">Kaynak grubu adı, kullanıcı aboneliği içinde kaynak grubunu benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="0ce10-146">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ce10-147">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="0ce10-147">-ReturnAddressCity</span></span>
<span data-ttu-id="0ce10-148">Sürücüleri döndürürken kullanılacak şehir adı.</span><span class="sxs-lookup"><span data-stu-id="0ce10-148">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="0ce10-149">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="0ce10-149">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="0ce10-150">Sürücüleri döndürürken kullanılacak ülke veya bölge.</span><span class="sxs-lookup"><span data-stu-id="0ce10-150">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="0ce10-151">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="0ce10-151">-ReturnAddressEmail</span></span>
<span data-ttu-id="0ce10-152">Döndürülen sürücüler alıcısının e-posta adresi.</span><span class="sxs-lookup"><span data-stu-id="0ce10-152">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="0ce10-153">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="0ce10-153">-ReturnAddressPhone</span></span>
<span data-ttu-id="0ce10-154">Döndürülen sürücüler alıcısının telefon numarası.</span><span class="sxs-lookup"><span data-stu-id="0ce10-154">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="0ce10-155">-Returnaddresspostakodu</span><span class="sxs-lookup"><span data-stu-id="0ce10-155">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="0ce10-156">Sürücüleri döndürürken kullanılacak posta kodu.</span><span class="sxs-lookup"><span data-stu-id="0ce10-156">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="0ce10-157">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="0ce10-157">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="0ce10-158">İade edildiğinde sabit sürücüleri alacak olan alıcının adı.</span><span class="sxs-lookup"><span data-stu-id="0ce10-158">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="0ce10-159">-Returnaddressstateorili</span><span class="sxs-lookup"><span data-stu-id="0ce10-159">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="0ce10-160">Sürücüleri döndürürken kullanılacak eyalet veya bölge.</span><span class="sxs-lookup"><span data-stu-id="0ce10-160">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="0ce10-161">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="0ce10-161">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="0ce10-162">Sürücülerin döndürülmesi sırasında kullanılacak sokak adresinin ilk satırı.</span><span class="sxs-lookup"><span data-stu-id="0ce10-162">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="0ce10-163">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="0ce10-163">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="0ce10-164">Sürücülerin döndürülmesi sırasında kullanılacak sokak adresinin ikinci satırı.</span><span class="sxs-lookup"><span data-stu-id="0ce10-164">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="0ce10-165">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="0ce10-165">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="0ce10-166">Taşıyıcıda müşterinin hesap numarası.</span><span class="sxs-lookup"><span data-stu-id="0ce10-166">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="0ce10-167">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="0ce10-167">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="0ce10-168">Taşıyıcı adı.</span><span class="sxs-lookup"><span data-stu-id="0ce10-168">The carrier's name.</span></span>

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

### <span data-ttu-id="0ce10-169">Durumlu</span><span class="sxs-lookup"><span data-stu-id="0ce10-169">-State</span></span>
<span data-ttu-id="0ce10-170">Belirtilmişse, Içeri/dışarı aktarma hizmetine iş paketinin sevk edilmiş olduğunu bildiren değer sevkıyat olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0ce10-170">If specified, the value must be Shipping, which tells the Import/Export service that the package for the job has been shipped.</span></span>
<span data-ttu-id="0ce10-171">Bu istekte veya önceki bir istekte ReturnAddress ve, bir önceki istekte ayarlanmış olmalıdır, aksi takdirde istek başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="0ce10-171">The ReturnAddress and DeliveryPackage properties must have been set either in this request or in a previous request, otherwise the request will fail.</span></span>

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

### <span data-ttu-id="0ce10-172">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0ce10-172">-SubscriptionId</span></span>
<span data-ttu-id="0ce10-173">Azure kullanıcısına ait abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0ce10-173">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ce10-174">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0ce10-174">-Tag</span></span>
<span data-ttu-id="0ce10-175">İşe atanacak etiketleri belirtir</span><span class="sxs-lookup"><span data-stu-id="0ce10-175">Specifies the tags that will be assigned to the job</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IUpdateJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ce10-176">-Onay</span><span class="sxs-lookup"><span data-stu-id="0ce10-176">-Confirm</span></span>
<span data-ttu-id="0ce10-177">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0ce10-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ce10-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ce10-178">-WhatIf</span></span>
<span data-ttu-id="0ce10-179">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0ce10-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ce10-180">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0ce10-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ce10-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce10-181">CommonParameters</span></span>
<span data-ttu-id="0ce10-182">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0ce10-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce10-183">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0ce10-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce10-184">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ce10-184">INPUTS</span></span>

### <span data-ttu-id="0ce10-185">Microsoft. Azure. PowerShell. cmdlet. ımportexport. modeller. ıımportexportidentity</span><span class="sxs-lookup"><span data-stu-id="0ce10-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="0ce10-186">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ce10-186">OUTPUTS</span></span>

### <span data-ttu-id="0ce10-187">Microsoft. Azure. PowerShell. cmdlet. ımportexport. modeller. Api20161101. ıjobresponse</span><span class="sxs-lookup"><span data-stu-id="0ce10-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="0ce10-188">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ce10-188">NOTES</span></span>

<span data-ttu-id="0ce10-189">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="0ce10-189">ALIASES</span></span>

<span data-ttu-id="0ce10-190">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="0ce10-190">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0ce10-191">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0ce10-191">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0ce10-192">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0ce10-192">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0ce10-193">DRIVELIST <IDriveStatus [] >: işi oluşturan sürücülerin listesi.</span><span class="sxs-lookup"><span data-stu-id="0ce10-193">DRIVELIST <IDriveStatus[]>: List of drives that comprise the job.</span></span>
  - <span data-ttu-id="0ce10-194">`[BitLockerKey <String>]`: Sürücüyü şifrelemek için kullanılan BitLocker anahtarı.</span><span class="sxs-lookup"><span data-stu-id="0ce10-194">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="0ce10-195">`[BytesSucceeded <Int64?>]`: Sürücü için bayt başarıyla aktarıldı.</span><span class="sxs-lookup"><span data-stu-id="0ce10-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="0ce10-196">`[CopyStatus <String>]`: Veri aktarım süreci hakkında ayrıntılı durum.</span><span class="sxs-lookup"><span data-stu-id="0ce10-196">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="0ce10-197">Bu alan, sürücü aktarma durumunda olana kadar yanıtta döndürülmez.</span><span class="sxs-lookup"><span data-stu-id="0ce10-197">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="0ce10-198">`[DriveHeaderHash <String>]`: Sürücü üstbilgisi karma değeri.</span><span class="sxs-lookup"><span data-stu-id="0ce10-198">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="0ce10-199">`[DriveId <String>]`: Sürücünün boşluksuz donanım seri numarası.</span><span class="sxs-lookup"><span data-stu-id="0ce10-199">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="0ce10-200">`[ErrorLogUri <String>]`: Veri aktarma işlemi için hata günlüğünü içeren blob 'a işaret eden bir URI.</span><span class="sxs-lookup"><span data-stu-id="0ce10-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="0ce10-201">`[ManifestFile <String>]`: Sürücüdeki bildirim dosyasının göreli yolu.</span><span class="sxs-lookup"><span data-stu-id="0ce10-201">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="0ce10-202">`[ManifestHash <String>]`: Sürücüdeki bildirim dosyasının Base16 ile kodlanmış MD5 karması.</span><span class="sxs-lookup"><span data-stu-id="0ce10-202">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="0ce10-203">`[ManifestUri <String>]`: Sürücü bildirim dosyasını içeren blob 'a işaret eden bir URI.</span><span class="sxs-lookup"><span data-stu-id="0ce10-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="0ce10-204">`[PercentComplete <Int32?>]`: Sürücü için yüzde tamamlandı.</span><span class="sxs-lookup"><span data-stu-id="0ce10-204">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="0ce10-205">`[State <DriveState?>]`: Sürücünün geçerli durumu.</span><span class="sxs-lookup"><span data-stu-id="0ce10-205">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="0ce10-206">`[VerboseLogUri <String>]`: Veri aktarma işlemi için ayrıntılı günlüğü içeren blob 'a işaret eden bir URI.</span><span class="sxs-lookup"><span data-stu-id="0ce10-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

<span data-ttu-id="0ce10-207">INPUTOBJECT <IImportExportIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="0ce10-207">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0ce10-208">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="0ce10-208">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0ce10-209">`[JobName <String>]`: İçeri/dışarı aktarma işinin adı.</span><span class="sxs-lookup"><span data-stu-id="0ce10-209">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="0ce10-210">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="0ce10-210">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="0ce10-211">Örneğin, Batı ABD veya westus.</span><span class="sxs-lookup"><span data-stu-id="0ce10-211">For example, West US or westus.</span></span>
  - <span data-ttu-id="0ce10-212">`[ResourceGroupName <String>]`: Kaynak grubu adı, kaynak grubunu Kullanıcı aboneliğindeki benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="0ce10-212">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="0ce10-213">`[SubscriptionId <String>]`: Azure kullanıcısının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0ce10-213">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="0ce10-214">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ce10-214">RELATED LINKS</span></span>

