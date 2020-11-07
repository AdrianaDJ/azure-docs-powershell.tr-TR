---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsvmextension
schema: 2.0.0
ms.openlocfilehash: c2214f01b35e68ba22f9dbfc6fe9e602badb9ba9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937162"
---
# <span data-ttu-id="1029c-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="1029c-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="1029c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1029c-102">SYNOPSIS</span></span>
<span data-ttu-id="1029c-103">İstenen sanal makine uzantısı görüntüsünü (yayımcı, tür, sürüm) döndürür.</span><span class="sxs-lookup"><span data-stu-id="1029c-103">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="1029c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1029c-104">SYNTAX</span></span>

### <span data-ttu-id="1029c-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1029c-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1029c-106">Al</span><span class="sxs-lookup"><span data-stu-id="1029c-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1029c-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="1029c-107">GetViaIdentity</span></span>
```
Get-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1029c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1029c-108">DESCRIPTION</span></span>
<span data-ttu-id="1029c-109">İstenen sanal makine uzantısı görüntüsünü (yayımcı, tür, sürüm) döndürür.</span><span class="sxs-lookup"><span data-stu-id="1029c-109">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="1029c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1029c-110">EXAMPLES</span></span>

### <span data-ttu-id="1029c-111">Örnek 1: tüm VM uzantılarını alma</span><span class="sxs-lookup"><span data-stu-id="1029c-111">Example 1:  Get All VM Extensions</span></span>
```powershell
PS C:\> Get-AzsVMExtension

ExtensionType            : IaaSDiagnostics
TypeHandlerVersion       : 1.11.3.12
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/northwest/artifactTypes/VMExtension/publishers/Microsoft.Azure.Diagnostics/types/IaaSDia
                           gnostics/versions/1.11.3.12
IsSystemExtension        : False
Location                 : northwest
Name                     :
ProvisioningState        : Succeeded
Publisher                : Microsoft.Azure.Diagnostics
SourceBlobUri            :
SupportMultipleExtension : False
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Windows

...
```

<span data-ttu-id="1029c-112">Tüm parametreleri boş bırakarak tüm VMExtensions listesini alın.</span><span class="sxs-lookup"><span data-stu-id="1029c-112">Get a list of all VMExtensions by leaving all parameters blank.</span></span>

## <span data-ttu-id="1029c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1029c-113">PARAMETERS</span></span>

### <span data-ttu-id="1029c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1029c-114">-DefaultProfile</span></span>
<span data-ttu-id="1029c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1029c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1029c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1029c-116">-InputObject</span></span>
<span data-ttu-id="1029c-117">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1029c-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1029c-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="1029c-118">-Location</span></span>
<span data-ttu-id="1029c-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="1029c-119">Location of the resource.</span></span>

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

### <span data-ttu-id="1029c-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="1029c-120">-Publisher</span></span>
<span data-ttu-id="1029c-121">Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="1029c-121">Name of the publisher.</span></span>

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

### <span data-ttu-id="1029c-122">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="1029c-122">-SubscriptionId</span></span>
<span data-ttu-id="1029c-123">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="1029c-123">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1029c-124">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1029c-124">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1029c-125">-Tür</span><span class="sxs-lookup"><span data-stu-id="1029c-125">-Type</span></span>
<span data-ttu-id="1029c-126">Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="1029c-126">Type of extension.</span></span>

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

### <span data-ttu-id="1029c-127">-Version</span><span class="sxs-lookup"><span data-stu-id="1029c-127">-Version</span></span>
<span data-ttu-id="1029c-128">Kaynağın sürümü.</span><span class="sxs-lookup"><span data-stu-id="1029c-128">The version of the resource.</span></span>

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

### <span data-ttu-id="1029c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1029c-129">CommonParameters</span></span>
<span data-ttu-id="1029c-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1029c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1029c-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1029c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1029c-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1029c-132">INPUTS</span></span>

### <span data-ttu-id="1029c-133">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. ıuteadminıdentity</span><span class="sxs-lookup"><span data-stu-id="1029c-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="1029c-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1029c-134">OUTPUTS</span></span>

### <span data-ttu-id="1029c-135">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. Api20151201Preview.</span><span class="sxs-lookup"><span data-stu-id="1029c-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="1029c-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1029c-136">NOTES</span></span>

<span data-ttu-id="1029c-137">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1029c-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1029c-138">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1029c-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1029c-139">INPUTOBJECT <IComputeAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="1029c-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1029c-140">`[DiskId <String>]`: Kimlik olarak disk Guid 'si.</span><span class="sxs-lookup"><span data-stu-id="1029c-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="1029c-141">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="1029c-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1029c-142">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="1029c-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="1029c-143">`[MigrationId <String>]`: Geçiş işi GUID adı.</span><span class="sxs-lookup"><span data-stu-id="1029c-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="1029c-144">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="1029c-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="1029c-145">`[Publisher <String>]`: Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="1029c-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="1029c-146">`[QuotaName <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="1029c-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="1029c-147">`[Sku <String>]`: SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="1029c-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="1029c-148">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="1029c-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1029c-149">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1029c-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="1029c-150">`[Type <String>]`: Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="1029c-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="1029c-151">`[Version <String>]`: Kaynağın sürümü.</span><span class="sxs-lookup"><span data-stu-id="1029c-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="1029c-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1029c-152">RELATED LINKS</span></span>

