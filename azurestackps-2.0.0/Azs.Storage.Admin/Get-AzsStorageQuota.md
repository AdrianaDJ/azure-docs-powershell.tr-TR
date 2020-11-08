---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: ed5261a9b6d65918fce0fd90c8f2db0ff42baa3a
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94105085"
---
# <span data-ttu-id="4a7dc-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="4a7dc-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="4a7dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a7dc-102">SYNOPSIS</span></span>


## <span data-ttu-id="4a7dc-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a7dc-103">SYNTAX</span></span>

### <span data-ttu-id="4a7dc-104">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4a7dc-104">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a7dc-105">Al</span><span class="sxs-lookup"><span data-stu-id="4a7dc-105">Get</span></span>
```
Get-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4a7dc-106">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="4a7dc-106">GetViaIdentity</span></span>
```
Get-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4a7dc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a7dc-107">DESCRIPTION</span></span>


## <span data-ttu-id="4a7dc-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a7dc-108">EXAMPLES</span></span>

### <span data-ttu-id="4a7dc-109">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="4a7dc-109">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota
```

<span data-ttu-id="4a7dc-110">Depolama kotaları listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="4a7dc-110">Get the list of storage quotas.</span></span>

### <span data-ttu-id="4a7dc-111">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="4a7dc-111">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'Default Quota'
```

<span data-ttu-id="4a7dc-112">Belirtilen depolama kotasının ayrıntılarını ada göre edinin.</span><span class="sxs-lookup"><span data-stu-id="4a7dc-112">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="4a7dc-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a7dc-113">PARAMETERS</span></span>

### <span data-ttu-id="4a7dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a7dc-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="4a7dc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a7dc-115">-InputObject</span></span>
<span data-ttu-id="4a7dc-116">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4a7dc-116">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: System.String
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4a7dc-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="4a7dc-117">-Location</span></span>


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

### <span data-ttu-id="4a7dc-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="4a7dc-118">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a7dc-119">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="4a7dc-119">-SubscriptionId</span></span>


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

### <span data-ttu-id="4a7dc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a7dc-120">CommonParameters</span></span>
<span data-ttu-id="4a7dc-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a7dc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a7dc-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4a7dc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a7dc-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a7dc-123">INPUTS</span></span>

### <span data-ttu-id="4a7dc-124">Microsoft. Azure. PowerShell. cmdlet. StorageAdmin. modeller. ıstorageadminıdentity</span><span class="sxs-lookup"><span data-stu-id="4a7dc-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="4a7dc-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a7dc-125">OUTPUTS</span></span>

### <span data-ttu-id="4a7dc-126">Microsoft. Azure. PowerShell. cmdlet. StorageAdmin. modeller. Api201908Preview. ıstoragequota</span><span class="sxs-lookup"><span data-stu-id="4a7dc-126">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="4a7dc-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a7dc-127">NOTES</span></span>

<span data-ttu-id="4a7dc-128">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4a7dc-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a7dc-129">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4a7dc-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4a7dc-130">INPUTOBJECT <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="4a7dc-130">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="4a7dc-131">`[AccountId <String>]`: Kiracıya görünmeyen iç depolama hesap KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4a7dc-131">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="4a7dc-132">`[AsyncOperationId <String>]`: Zaman uyumsuz Işlem kimliği.</span><span class="sxs-lookup"><span data-stu-id="4a7dc-132">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="4a7dc-133">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="4a7dc-133">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4a7dc-134">`[Location <String>]`: Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="4a7dc-134">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="4a7dc-135">`[QuotaName <String>]`: Depolama alanı kotasının adı.</span><span class="sxs-lookup"><span data-stu-id="4a7dc-135">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="4a7dc-136">`[ResourceGroup <String>]`: Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4a7dc-136">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="4a7dc-137">`[ServiceName <String>]`: Depolama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="4a7dc-137">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="4a7dc-138">`[SubscriptionId <String>]`: Abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="4a7dc-138">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="4a7dc-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a7dc-139">RELATED LINKS</span></span>

