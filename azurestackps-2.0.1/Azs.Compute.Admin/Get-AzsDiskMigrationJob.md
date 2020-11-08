---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: 96c14cd8d8d48b6212ed0e4c7b0d5934754912a5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105275"
---
# <span data-ttu-id="447e0-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="447e0-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="447e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="447e0-102">SYNOPSIS</span></span>
<span data-ttu-id="447e0-103">İstenen disk geçiş işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="447e0-103">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="447e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="447e0-104">SYNTAX</span></span>

### <span data-ttu-id="447e0-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="447e0-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] [-SubscriptionId <String[]>] [-Status <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="447e0-106">Al</span><span class="sxs-lookup"><span data-stu-id="447e0-106">Get</span></span>
```
Get-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="447e0-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="447e0-107">GetViaIdentity</span></span>
```
Get-AzsDiskMigrationJob -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="447e0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="447e0-108">DESCRIPTION</span></span>
<span data-ttu-id="447e0-109">İstenen disk geçiş işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="447e0-109">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="447e0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="447e0-110">EXAMPLES</span></span>

### <span data-ttu-id="447e0-111">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="447e0-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob
```

<span data-ttu-id="447e0-112">Yerel konumda yönetilen disk geçiş işlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="447e0-112">Returns a list of managed disk migration jobs at the location local.</span></span>

### <span data-ttu-id="447e0-113">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="447e0-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob -Name TestNewDiskMigrationJob

CreationTime : 2/26/2020 10:45:41 AM
EndTime      : 2/26/2020 10:46:32 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrationjobs/TestNewDiskMigrationJob
Location     : redmond
MigrationId  : TestNewDiskMigrationJob
Name         : redmond/TestNewDiskMigrationJob
StartTime    : 2/26/2020 10:45:41 AM
Status       : Succeeded
Subtask      : {edacd0f6-760a-43f9-a188-8833751f89ce, f1ee38a4-5c27-4728-a12b-36976c565042}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_1
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="447e0-114">Belirli bir yönetilen disk geçiş işi edinin.</span><span class="sxs-lookup"><span data-stu-id="447e0-114">Get a specific managed disk migration job.</span></span>

## <span data-ttu-id="447e0-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="447e0-115">PARAMETERS</span></span>

### <span data-ttu-id="447e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="447e0-116">-DefaultProfile</span></span>
<span data-ttu-id="447e0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="447e0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="447e0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="447e0-118">-InputObject</span></span>
<span data-ttu-id="447e0-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="447e0-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="447e0-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="447e0-120">-Location</span></span>
<span data-ttu-id="447e0-121">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="447e0-121">Location of the resource.</span></span>

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

### <span data-ttu-id="447e0-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="447e0-122">-Name</span></span>
<span data-ttu-id="447e0-123">Geçiş işi GUID adı.</span><span class="sxs-lookup"><span data-stu-id="447e0-123">The migration job guid name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="447e0-124">-Durum</span><span class="sxs-lookup"><span data-stu-id="447e0-124">-Status</span></span>
<span data-ttu-id="447e0-125">Disk geçiş işinin parametreleri.</span><span class="sxs-lookup"><span data-stu-id="447e0-125">The parameters of disk migration job status.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="447e0-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="447e0-126">-SubscriptionId</span></span>
<span data-ttu-id="447e0-127">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="447e0-127">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="447e0-128">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="447e0-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="447e0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="447e0-129">CommonParameters</span></span>
<span data-ttu-id="447e0-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="447e0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="447e0-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="447e0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="447e0-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="447e0-132">INPUTS</span></span>

### <span data-ttu-id="447e0-133">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. ıuteadminıdentity</span><span class="sxs-lookup"><span data-stu-id="447e0-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="447e0-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="447e0-134">OUTPUTS</span></span>

### <span data-ttu-id="447e0-135">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. Api20180730Preview. ıdiskmigrationjob</span><span class="sxs-lookup"><span data-stu-id="447e0-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="447e0-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="447e0-136">NOTES</span></span>

<span data-ttu-id="447e0-137">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="447e0-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="447e0-138">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="447e0-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="447e0-139">INPUTOBJECT <IComputeAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="447e0-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="447e0-140">`[DiskId <String>]`: Kimlik olarak disk Guid 'si.</span><span class="sxs-lookup"><span data-stu-id="447e0-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="447e0-141">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="447e0-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="447e0-142">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="447e0-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="447e0-143">`[MigrationId <String>]`: Geçiş işi GUID adı.</span><span class="sxs-lookup"><span data-stu-id="447e0-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="447e0-144">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="447e0-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="447e0-145">`[Publisher <String>]`: Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="447e0-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="447e0-146">`[QuotaName <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="447e0-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="447e0-147">`[Sku <String>]`: SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="447e0-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="447e0-148">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="447e0-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="447e0-149">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="447e0-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="447e0-150">`[Type <String>]`: Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="447e0-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="447e0-151">`[Version <String>]`: Kaynağın sürümü.</span><span class="sxs-lookup"><span data-stu-id="447e0-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="447e0-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="447e0-152">RELATED LINKS</span></span>

