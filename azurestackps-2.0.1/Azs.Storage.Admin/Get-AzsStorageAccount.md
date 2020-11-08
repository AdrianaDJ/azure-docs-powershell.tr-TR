---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 0ddf99277834e69a55b009abcb4b683eebb7a4ec
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105327"
---
# <span data-ttu-id="ee642-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ee642-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="ee642-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee642-102">SYNOPSIS</span></span>
<span data-ttu-id="ee642-103">İstenen depolama hesabını döndürür.</span><span class="sxs-lookup"><span data-stu-id="ee642-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="ee642-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee642-104">SYNTAX</span></span>

### <span data-ttu-id="ee642-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ee642-105">List (Default)</span></span>
```
Get-AzsStorageAccount [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Summary]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ee642-106">Al</span><span class="sxs-lookup"><span data-stu-id="ee642-106">Get</span></span>
```
Get-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ee642-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="ee642-107">GetViaIdentity</span></span>
```
Get-AzsStorageAccount -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ee642-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee642-108">DESCRIPTION</span></span>
<span data-ttu-id="ee642-109">İstenen depolama hesabını döndürür.</span><span class="sxs-lookup"><span data-stu-id="ee642-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="ee642-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee642-110">EXAMPLES</span></span>

### <span data-ttu-id="ee642-111">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="ee642-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Summary
```

<span data-ttu-id="ee642-112">Depolama hesaplarının (Özet) listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="ee642-112">Get a list of storage accounts (summary).</span></span>

### <span data-ttu-id="ee642-113">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="ee642-113">Example 2:</span></span>
```powershell
PS C:\> $storageAccount = Get-AzsStorageAccount
PS C:\> $storageAccount | Select Location,Name,AccountStatus,HealthState,Kind | ft
```

<span data-ttu-id="ee642-114">Ayrıntılar içeren depolama hesabının bir listesini alın ve durumu yazdırın.</span><span class="sxs-lookup"><span data-stu-id="ee642-114">Get a list of storage account with details and print the status.</span></span>

### <span data-ttu-id="ee642-115">Örnek 3:</span><span class="sxs-lookup"><span data-stu-id="ee642-115">Example 3:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 | fl *
```

<span data-ttu-id="ee642-116">Belirtilen depolama hesabının ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="ee642-116">Get details of the specified storage account.</span></span>

## <span data-ttu-id="ee642-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee642-117">PARAMETERS</span></span>

### <span data-ttu-id="ee642-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee642-118">-DefaultProfile</span></span>
<span data-ttu-id="ee642-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ee642-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee642-120">-Filtre</span><span class="sxs-lookup"><span data-stu-id="ee642-120">-Filter</span></span>
<span data-ttu-id="ee642-121">Filtre dizesi</span><span class="sxs-lookup"><span data-stu-id="ee642-121">Filter string</span></span>

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

### <span data-ttu-id="ee642-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee642-122">-InputObject</span></span>
<span data-ttu-id="ee642-123">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ee642-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="ee642-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="ee642-124">-Location</span></span>
<span data-ttu-id="ee642-125">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="ee642-125">Resource location.</span></span>

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

### <span data-ttu-id="ee642-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="ee642-126">-Name</span></span>
<span data-ttu-id="ee642-127">Kiracıya görünmeyen iç depolama hesap KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ee642-127">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ee642-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ee642-128">-SubscriptionId</span></span>
<span data-ttu-id="ee642-129">Abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="ee642-129">Subscription Id.</span></span>

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

### <span data-ttu-id="ee642-130">-Özet</span><span class="sxs-lookup"><span data-stu-id="ee642-130">-Summary</span></span>
<span data-ttu-id="ee642-131">Özet veya ayrıntılı bilgilerin verilip verilmeyeceğini değiştirme.</span><span class="sxs-lookup"><span data-stu-id="ee642-131">Switch for whether summary or detailed information is returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: $false
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ee642-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee642-132">CommonParameters</span></span>
<span data-ttu-id="ee642-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee642-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee642-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ee642-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee642-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee642-135">INPUTS</span></span>

### <span data-ttu-id="ee642-136">Microsoft. Azure. PowerShell. cmdlet. StorageAdmin. modeller. ıstorageadminıdentity</span><span class="sxs-lookup"><span data-stu-id="ee642-136">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="ee642-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee642-137">OUTPUTS</span></span>

### <span data-ttu-id="ee642-138">Microsoft. Azure. PowerShell. cmdlet. StorageAdmin. modeller. Api201908Preview. ıstorageaccount</span><span class="sxs-lookup"><span data-stu-id="ee642-138">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageAccount</span></span>



## <span data-ttu-id="ee642-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee642-139">NOTES</span></span>

<span data-ttu-id="ee642-140">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ee642-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ee642-141">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ee642-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ee642-142">INPUTOBJECT <IStorageAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="ee642-142">INPUTOBJECT <IStorageAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ee642-143">`[AccountId <String>]`: Kiracıya görünmeyen iç depolama hesap KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ee642-143">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="ee642-144">`[AsyncOperationId <String>]`: Zaman uyumsuz Işlem kimliği.</span><span class="sxs-lookup"><span data-stu-id="ee642-144">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="ee642-145">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="ee642-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ee642-146">`[Location <String>]`: Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="ee642-146">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="ee642-147">`[QuotaName <String>]`: Depolama alanı kotasının adı.</span><span class="sxs-lookup"><span data-stu-id="ee642-147">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="ee642-148">`[ResourceGroup <String>]`: Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ee642-148">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="ee642-149">`[ServiceName <String>]`: Depolama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="ee642-149">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="ee642-150">`[SubscriptionId <String>]`: Abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="ee642-150">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="ee642-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee642-151">RELATED LINKS</span></span>

