---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: 127cbe1efb710fff04420590985e97ee72a196a9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936043"
---
# <span data-ttu-id="1b786-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="1b786-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="1b786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b786-102">SYNOPSIS</span></span>
<span data-ttu-id="1b786-103">Yayımcı, teklif, STB 'ler ve sürüm ile yeni bir platform görüntüsü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b786-103">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="1b786-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b786-104">SYNTAX</span></span>

### <span data-ttu-id="1b786-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1b786-105">CreateExpanded (Default)</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-BillingPartNumber <String>] [-DataDisks <IDataDisk[]>] [-OsType <OSType>]
 [-OsUri <String>] [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1b786-106">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="1b786-106">Create</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 -NewImage <IPlatformImageParameters> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1b786-107">Createviaıdentity</span><span class="sxs-lookup"><span data-stu-id="1b786-107">CreateViaIdentity</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> -NewImage <IPlatformImageParameters>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1b786-108">Createviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="1b786-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-BillingPartNumber <String>]
 [-DataDisks <IDataDisk[]>] [-OsType <OSType>] [-OsUri <String>] [-ProvisioningState <ProvisioningState>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1b786-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b786-109">DESCRIPTION</span></span>
<span data-ttu-id="1b786-110">Yayımcı, teklif, STB 'ler ve sürüm ile yeni bir platform görüntüsü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b786-110">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="1b786-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b786-111">EXAMPLES</span></span>

### <span data-ttu-id="1b786-112">Örnek 1: Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="1b786-112">Example 1: Add-AzsPlatformImage</span></span>
```powershell
PS C:\> Add-AzsPlatformImage -Offer "asdf" -Publisher "asdf" -Sku "asdf" -Version "1.0.0" -OsType Windows -OsUri "https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https&sig=CKkE2r9MJc%2FK40PjRB5Tfz6DArxNd0akD90IvKJX95g%3D"

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
#Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="1b786-113">BLOB depolama 'dan bir platform görüntüsü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="1b786-113">Add a Platform Image from Blob Storage.</span></span> <span data-ttu-id="1b786-114">Plaformımage 'ın konumunu belirtmek veya genel olarak erişilebilir bir URL kullanmak için bir Sasurı kullanın.</span><span class="sxs-lookup"><span data-stu-id="1b786-114">Use the a SasUri to specify the location of the PlatformImage, or use a publicly accessible URL.</span></span>

## <span data-ttu-id="1b786-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b786-115">PARAMETERS</span></span>

### <span data-ttu-id="1b786-116">Exception. Message</span><span class="sxs-lookup"><span data-stu-id="1b786-116">Exception.Message</span></span>
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

### <span data-ttu-id="1b786-117">-Billingpartnumarası</span><span class="sxs-lookup"><span data-stu-id="1b786-117">-BillingPartNumber</span></span>
<span data-ttu-id="1b786-118">Bölüm numarası, Yazılım maliyetlerini faturalamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1b786-118">The part number is used to bill for software costs.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1b786-119">-DataDisks</span><span class="sxs-lookup"><span data-stu-id="1b786-119">-DataDisks</span></span>
<span data-ttu-id="1b786-120">Platform görüntüsü tarafından kullanılan veri diskleri.</span><span class="sxs-lookup"><span data-stu-id="1b786-120">Data disks used by the platform image.</span></span>
<span data-ttu-id="1b786-121">Oluşturmak için, DATADISKS özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1b786-121">To construct, see NOTES section for DATADISKS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IDataDisk[]
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1b786-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b786-122">-DefaultProfile</span></span>
<span data-ttu-id="1b786-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b786-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b786-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b786-124">-InputObject</span></span>
<span data-ttu-id="1b786-125">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b786-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="1b786-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="1b786-126">-Location</span></span>
<span data-ttu-id="1b786-127">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="1b786-127">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1b786-128">-NewImage</span><span class="sxs-lookup"><span data-stu-id="1b786-128">-NewImage</span></span>
<span data-ttu-id="1b786-129">Yeni bir platform görüntüsü oluşturmak için kullanılan parametreler.</span><span class="sxs-lookup"><span data-stu-id="1b786-129">Parameters used to create a new platform image.</span></span>
<span data-ttu-id="1b786-130">Oluşturmak için, NEWIMAGE özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1b786-130">To construct, see NOTES section for NEWIMAGE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="1b786-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1b786-131">-NoWait</span></span>
<span data-ttu-id="1b786-132">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="1b786-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1b786-133">-Teklif</span><span class="sxs-lookup"><span data-stu-id="1b786-133">-Offer</span></span>
<span data-ttu-id="1b786-134">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="1b786-134">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1b786-135">-OsType</span><span class="sxs-lookup"><span data-stu-id="1b786-135">-OsType</span></span>
<span data-ttu-id="1b786-136">İşletim sistemi türü.</span><span class="sxs-lookup"><span data-stu-id="1b786-136">Operating system type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.OSType
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1b786-137">-OsUri</span><span class="sxs-lookup"><span data-stu-id="1b786-137">-OsUri</span></span>
<span data-ttu-id="1b786-138">Diskin konumu.</span><span class="sxs-lookup"><span data-stu-id="1b786-138">Location of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1b786-139">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="1b786-139">-ProvisioningState</span></span>
<span data-ttu-id="1b786-140">Platform görüntüsünün sağlama durumu.</span><span class="sxs-lookup"><span data-stu-id="1b786-140">Provisioning status of the platform image.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1b786-141">-Publisher</span><span class="sxs-lookup"><span data-stu-id="1b786-141">-Publisher</span></span>
<span data-ttu-id="1b786-142">Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="1b786-142">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1b786-143">-SKU</span><span class="sxs-lookup"><span data-stu-id="1b786-143">-Sku</span></span>
<span data-ttu-id="1b786-144">SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="1b786-144">Name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1b786-145">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="1b786-145">-SubscriptionId</span></span>
<span data-ttu-id="1b786-146">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="1b786-146">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1b786-147">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1b786-147">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1b786-148">-Version</span><span class="sxs-lookup"><span data-stu-id="1b786-148">-Version</span></span>
<span data-ttu-id="1b786-149">Kaynağın sürümü.</span><span class="sxs-lookup"><span data-stu-id="1b786-149">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1b786-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b786-150">-Confirm</span></span>
<span data-ttu-id="1b786-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b786-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b786-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b786-152">-WhatIf</span></span>
<span data-ttu-id="1b786-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b786-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b786-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b786-154">The cmdlet is not run.</span></span>

### <span data-ttu-id="1b786-155">Exception. Message</span><span class="sxs-lookup"><span data-stu-id="1b786-155">Exception.Message</span></span>

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

### <span data-ttu-id="1b786-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b786-156">CommonParameters</span></span>
<span data-ttu-id="1b786-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b786-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b786-158">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1b786-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b786-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b786-159">INPUTS</span></span>

### <span data-ttu-id="1b786-160">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. Api20151201Preview. ıplatformımageparameters</span><span class="sxs-lookup"><span data-stu-id="1b786-160">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters</span></span>

### <span data-ttu-id="1b786-161">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. ıuteadminıdentity</span><span class="sxs-lookup"><span data-stu-id="1b786-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="1b786-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b786-162">OUTPUTS</span></span>

### <span data-ttu-id="1b786-163">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. Api20151201Preview. ıplatformimage</span><span class="sxs-lookup"><span data-stu-id="1b786-163">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="1b786-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b786-164">NOTES</span></span>

<span data-ttu-id="1b786-165">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1b786-165">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1b786-166">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1b786-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1b786-167">DATADISKS <ıdatadisk [] >: platform görüntüsü tarafından kullanılan veri diskleri.</span><span class="sxs-lookup"><span data-stu-id="1b786-167">DATADISKS <IDataDisk[]>: Data disks used by the platform image.</span></span>
  - <span data-ttu-id="1b786-168">`[Lun <Int32?>]`: Mantıksal birim numarası.</span><span class="sxs-lookup"><span data-stu-id="1b786-168">`[Lun <Int32?>]`: Logical unit number.</span></span>
  - <span data-ttu-id="1b786-169">`[Uri <String>]`: Disk şablonunun konumu.</span><span class="sxs-lookup"><span data-stu-id="1b786-169">`[Uri <String>]`: Location of the disk template.</span></span>

<span data-ttu-id="1b786-170">INPUTOBJECT <IComputeAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="1b786-170">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1b786-171">`[DiskId <String>]`: Kimlik olarak disk Guid 'si.</span><span class="sxs-lookup"><span data-stu-id="1b786-171">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="1b786-172">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="1b786-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1b786-173">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="1b786-173">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="1b786-174">`[MigrationId <String>]`: Geçiş işi GUID adı.</span><span class="sxs-lookup"><span data-stu-id="1b786-174">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="1b786-175">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="1b786-175">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="1b786-176">`[Publisher <String>]`: Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="1b786-176">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="1b786-177">`[QuotaName <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="1b786-177">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="1b786-178">`[Sku <String>]`: SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="1b786-178">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="1b786-179">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="1b786-179">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1b786-180">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1b786-180">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="1b786-181">`[Type <String>]`: Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="1b786-181">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="1b786-182">`[Version <String>]`: Kaynağın sürümü.</span><span class="sxs-lookup"><span data-stu-id="1b786-182">`[Version <String>]`: The version of the resource.</span></span>

<span data-ttu-id="1b786-183">NEWIMAGE <IPlatformImageParameters> : yeni bir platform görüntüsü oluşturmak için kullanılan parametreler.</span><span class="sxs-lookup"><span data-stu-id="1b786-183">NEWIMAGE <IPlatformImageParameters>: Parameters used to create a new platform image.</span></span>
  - <span data-ttu-id="1b786-184">`[DataDisk <IDataDisk[]>]`: Platform görüntüsü tarafından kullanılan veri diskleri.</span><span class="sxs-lookup"><span data-stu-id="1b786-184">`[DataDisk <IDataDisk[]>]`: Data disks used by the platform image.</span></span>
    - <span data-ttu-id="1b786-185">`[Lun <Int32?>]`: Mantıksal birim numarası.</span><span class="sxs-lookup"><span data-stu-id="1b786-185">`[Lun <Int32?>]`: Logical unit number.</span></span>
    - <span data-ttu-id="1b786-186">`[Uri <String>]`: Disk şablonunun konumu.</span><span class="sxs-lookup"><span data-stu-id="1b786-186">`[Uri <String>]`: Location of the disk template.</span></span>
  - <span data-ttu-id="1b786-187">`[DetailBillingPartNumber <String>]`: Bölüm numarası Yazılım maliyetlerini faturalamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1b786-187">`[DetailBillingPartNumber <String>]`: The part number is used to bill for software costs.</span></span>
  - <span data-ttu-id="1b786-188">`[OSDiskOstype <OSType?>]`: İşletim sistemi türü.</span><span class="sxs-lookup"><span data-stu-id="1b786-188">`[OSDiskOstype <OSType?>]`: Operating system type.</span></span>
  - <span data-ttu-id="1b786-189">`[OSDiskUri <String>]`: Diskin konumu.</span><span class="sxs-lookup"><span data-stu-id="1b786-189">`[OSDiskUri <String>]`: Location of the disk.</span></span>
  - <span data-ttu-id="1b786-190">`[ProvisioningState <ProvisioningState?>]`: Platform görüntüsünün sağlama durumu.</span><span class="sxs-lookup"><span data-stu-id="1b786-190">`[ProvisioningState <ProvisioningState?>]`: Provisioning status of the platform image.</span></span>

## <span data-ttu-id="1b786-191">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b786-191">RELATED LINKS</span></span>

