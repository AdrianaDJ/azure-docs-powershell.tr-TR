---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: d91e930c486fea5c7a17e5a8f7d8f8d30a88b351
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937161"
---
# <span data-ttu-id="2e05d-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="2e05d-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="2e05d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e05d-102">SYNOPSIS</span></span>
<span data-ttu-id="2e05d-103">Yayımcı, teklif, STB 'ler ve sürüm ile eşleşen özel platform görüntüsünü döndürür.</span><span class="sxs-lookup"><span data-stu-id="2e05d-103">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="2e05d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e05d-104">SYNTAX</span></span>

### <span data-ttu-id="2e05d-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2e05d-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e05d-106">Al</span><span class="sxs-lookup"><span data-stu-id="2e05d-106">Get</span></span>
```
Get-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2e05d-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="2e05d-107">GetViaIdentity</span></span>
```
Get-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2e05d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e05d-108">DESCRIPTION</span></span>
<span data-ttu-id="2e05d-109">Yayımcı, teklif, STB 'ler ve sürüm ile eşleşen özel platform görüntüsünü döndürür.</span><span class="sxs-lookup"><span data-stu-id="2e05d-109">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="2e05d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e05d-110">EXAMPLES</span></span>

### <span data-ttu-id="2e05d-111">Örnek 1: tüm platform görüntülerini alma</span><span class="sxs-lookup"><span data-stu-id="2e05d-111">Example 1: Get All Platform Images</span></span>
```powershell
PS C:\> Get-AzsPlatformImage

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/loc
                    al/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=r
                    wdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="2e05d-112">Tüm parametreleri boş bırakarak tüm platform görüntülerinin bir listesini alın.</span><span class="sxs-lookup"><span data-stu-id="2e05d-112">Get a list of all Platform Images by leaving all parameters blank.</span></span>

### <span data-ttu-id="2e05d-113">Örnek 2: belirli bir platform görüntüsü edinin</span><span class="sxs-lookup"><span data-stu-id="2e05d-113">Example 2: Get Specific Platform Image</span></span>
```powershell
PS C:\> Get-AzsPlatformImage -Offer ExampleOffer -Publisher ExamplePublisher -Location local -Sku ExampleSku -Version 1.0.0

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifa
                    ctTypes/platformImage/publishers/ExamplePublisher/offers/ExampleOffer/skus/ExampleSku/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&s
                    e=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="2e05d-114">Platform görüntüsünü almak için teklifi, yayımcıyı, konumu, SKU 'yu ve sürümü belirtin.</span><span class="sxs-lookup"><span data-stu-id="2e05d-114">Specify the Offer, Publisher, Location, Sku, and Version to retrieve a Platform Image.</span></span>

## <span data-ttu-id="2e05d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e05d-115">PARAMETERS</span></span>

### <span data-ttu-id="2e05d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e05d-116">-DefaultProfile</span></span>
<span data-ttu-id="2e05d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e05d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e05d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e05d-118">-InputObject</span></span>
<span data-ttu-id="2e05d-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2e05d-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2e05d-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="2e05d-120">-Location</span></span>
<span data-ttu-id="2e05d-121">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="2e05d-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2e05d-122">-Teklif</span><span class="sxs-lookup"><span data-stu-id="2e05d-122">-Offer</span></span>
<span data-ttu-id="2e05d-123">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="2e05d-123">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2e05d-124">-Publisher</span><span class="sxs-lookup"><span data-stu-id="2e05d-124">-Publisher</span></span>
<span data-ttu-id="2e05d-125">Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="2e05d-125">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2e05d-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="2e05d-126">-Sku</span></span>
<span data-ttu-id="2e05d-127">SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="2e05d-127">Name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2e05d-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="2e05d-128">-SubscriptionId</span></span>
<span data-ttu-id="2e05d-129">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="2e05d-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2e05d-130">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2e05d-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2e05d-131">-Version</span><span class="sxs-lookup"><span data-stu-id="2e05d-131">-Version</span></span>
<span data-ttu-id="2e05d-132">Kaynağın sürümü.</span><span class="sxs-lookup"><span data-stu-id="2e05d-132">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2e05d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e05d-133">CommonParameters</span></span>
<span data-ttu-id="2e05d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e05d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e05d-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2e05d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e05d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e05d-136">INPUTS</span></span>

### <span data-ttu-id="2e05d-137">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. ıuteadminıdentity</span><span class="sxs-lookup"><span data-stu-id="2e05d-137">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="2e05d-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e05d-138">OUTPUTS</span></span>

### <span data-ttu-id="2e05d-139">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. Api20151201Preview. ıplatformimage</span><span class="sxs-lookup"><span data-stu-id="2e05d-139">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="2e05d-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e05d-140">NOTES</span></span>

<span data-ttu-id="2e05d-141">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2e05d-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2e05d-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2e05d-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2e05d-143">INPUTOBJECT <IComputeAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="2e05d-143">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2e05d-144">`[DiskId <String>]`: Kimlik olarak disk Guid 'si.</span><span class="sxs-lookup"><span data-stu-id="2e05d-144">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="2e05d-145">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="2e05d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2e05d-146">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="2e05d-146">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="2e05d-147">`[MigrationId <String>]`: Geçiş işi GUID adı.</span><span class="sxs-lookup"><span data-stu-id="2e05d-147">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="2e05d-148">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="2e05d-148">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="2e05d-149">`[Publisher <String>]`: Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="2e05d-149">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="2e05d-150">`[QuotaName <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="2e05d-150">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="2e05d-151">`[Sku <String>]`: SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="2e05d-151">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="2e05d-152">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="2e05d-152">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2e05d-153">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2e05d-153">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2e05d-154">`[Type <String>]`: Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="2e05d-154">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="2e05d-155">`[Version <String>]`: Kaynağın sürümü.</span><span class="sxs-lookup"><span data-stu-id="2e05d-155">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="2e05d-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e05d-156">RELATED LINKS</span></span>

