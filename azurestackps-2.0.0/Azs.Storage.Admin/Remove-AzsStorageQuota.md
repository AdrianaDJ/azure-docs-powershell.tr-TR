---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/remove-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: 258c7057b8f78ea6de1db506d23c60f679e1ca39
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935974"
---
# <span data-ttu-id="dc21e-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="dc21e-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="dc21e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc21e-102">SYNOPSIS</span></span>


## <span data-ttu-id="dc21e-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc21e-103">SYNTAX</span></span>

### <span data-ttu-id="dc21e-104">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dc21e-104">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dc21e-105">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="dc21e-105">DeleteViaIdentity</span></span>
```
Remove-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dc21e-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc21e-106">DESCRIPTION</span></span>


## <span data-ttu-id="dc21e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc21e-107">EXAMPLES</span></span>

### <span data-ttu-id="dc21e-108">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="dc21e-108">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsStorageQuota -Name 'TestQuota'
```

<span data-ttu-id="dc21e-109">Depolama kotasını ada göre kaldırma.</span><span class="sxs-lookup"><span data-stu-id="dc21e-109">Remove a storage quota by name.</span></span>

### <span data-ttu-id="dc21e-110">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="dc21e-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestQuota' | Remove-AzsStorageQuota
```

<span data-ttu-id="dc21e-111">Bir depolama kotasını boru ile kaldırın.</span><span class="sxs-lookup"><span data-stu-id="dc21e-111">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="dc21e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc21e-112">PARAMETERS</span></span>

### <span data-ttu-id="dc21e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc21e-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="dc21e-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc21e-114">-InputObject</span></span>
<span data-ttu-id="dc21e-115">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dc21e-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="dc21e-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="dc21e-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dc21e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="dc21e-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dc21e-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="dc21e-118">-PassThru</span></span>


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

### <span data-ttu-id="dc21e-119">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="dc21e-119">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dc21e-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="dc21e-120">-Confirm</span></span>
<span data-ttu-id="dc21e-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dc21e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc21e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc21e-122">-WhatIf</span></span>
<span data-ttu-id="dc21e-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dc21e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc21e-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dc21e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc21e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc21e-125">CommonParameters</span></span>
<span data-ttu-id="dc21e-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc21e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc21e-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dc21e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc21e-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc21e-128">INPUTS</span></span>

### <span data-ttu-id="dc21e-129">Microsoft. Azure. PowerShell. cmdlet. StorageAdmin. modeller. ıstorageadminıdentity</span><span class="sxs-lookup"><span data-stu-id="dc21e-129">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="dc21e-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc21e-130">OUTPUTS</span></span>

### <span data-ttu-id="dc21e-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc21e-131">System.Boolean</span></span>



## <span data-ttu-id="dc21e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc21e-132">NOTES</span></span>

<span data-ttu-id="dc21e-133">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dc21e-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc21e-134">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dc21e-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="dc21e-135">INPUTOBJECT <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="dc21e-135">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="dc21e-136">`[AccountId <String>]`: Kiracıya görünmeyen iç depolama hesap KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="dc21e-136">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="dc21e-137">`[AsyncOperationId <String>]`: Zaman uyumsuz Işlem kimliği.</span><span class="sxs-lookup"><span data-stu-id="dc21e-137">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="dc21e-138">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="dc21e-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dc21e-139">`[Location <String>]`: Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="dc21e-139">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="dc21e-140">`[QuotaName <String>]`: Depolama alanı kotasının adı.</span><span class="sxs-lookup"><span data-stu-id="dc21e-140">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="dc21e-141">`[ResourceGroup <String>]`: Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="dc21e-141">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="dc21e-142">`[ServiceName <String>]`: Depolama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="dc21e-142">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="dc21e-143">`[SubscriptionId <String>]`: Abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="dc21e-143">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="dc21e-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc21e-144">RELATED LINKS</span></span>

