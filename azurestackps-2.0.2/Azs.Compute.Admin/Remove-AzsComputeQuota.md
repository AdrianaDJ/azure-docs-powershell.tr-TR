---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 715234586df8383a2983b4f0459ae91ca457d684
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106728"
---
# <span data-ttu-id="d2cf2-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="d2cf2-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="d2cf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="d2cf2-103">Var olan bir Işlem kotasını silme.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-103">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="d2cf2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2cf2-104">SYNTAX</span></span>

### <span data-ttu-id="d2cf2-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d2cf2-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2cf2-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="d2cf2-106">DeleteViaIdentity</span></span>
```
Remove-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d2cf2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2cf2-107">DESCRIPTION</span></span>
<span data-ttu-id="d2cf2-108">Var olan bir Işlem kotasını silme.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-108">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="d2cf2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2cf2-109">EXAMPLES</span></span>

### <span data-ttu-id="d2cf2-110">Örnek 1: Işlem kotasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d2cf2-110">Example 1: Remove a Compute Quota</span></span>
```powershell
PS C:\> Remove-AzsComputeQuota -Name "AComputeQuota"
```

<span data-ttu-id="d2cf2-111">İşlem kotasını kaldırma başarılı bir şekilde çağrı olmaz</span><span class="sxs-lookup"><span data-stu-id="d2cf2-111">A successful call to remove a compute quota will not return any output</span></span>

## <span data-ttu-id="d2cf2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2cf2-112">PARAMETERS</span></span>

### <span data-ttu-id="d2cf2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2cf2-113">-DefaultProfile</span></span>
<span data-ttu-id="d2cf2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2cf2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2cf2-115">-InputObject</span></span>
<span data-ttu-id="d2cf2-116">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d2cf2-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="d2cf2-117">-Location</span></span>
<span data-ttu-id="d2cf2-118">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-118">Location of the resource.</span></span>

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

### <span data-ttu-id="d2cf2-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d2cf2-119">-Name</span></span>
<span data-ttu-id="d2cf2-120">Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-120">Name of the quota.</span></span>

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

### <span data-ttu-id="d2cf2-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d2cf2-121">-PassThru</span></span>
<span data-ttu-id="d2cf2-122">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="d2cf2-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d2cf2-123">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d2cf2-123">-SubscriptionId</span></span>
<span data-ttu-id="d2cf2-124">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-124">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d2cf2-125">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d2cf2-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="d2cf2-126">-Confirm</span></span>
<span data-ttu-id="d2cf2-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2cf2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2cf2-128">-WhatIf</span></span>
<span data-ttu-id="d2cf2-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2cf2-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2cf2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2cf2-131">CommonParameters</span></span>
<span data-ttu-id="d2cf2-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2cf2-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2cf2-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2cf2-134">INPUTS</span></span>

### <span data-ttu-id="d2cf2-135">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. ıuteadminıdentity</span><span class="sxs-lookup"><span data-stu-id="d2cf2-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="d2cf2-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2cf2-136">OUTPUTS</span></span>

### <span data-ttu-id="d2cf2-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2cf2-137">System.Boolean</span></span>



## <span data-ttu-id="d2cf2-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2cf2-138">NOTES</span></span>

<span data-ttu-id="d2cf2-139">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2cf2-140">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d2cf2-141">INPUTOBJECT <IComputeAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="d2cf2-141">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2cf2-142">`[DiskId <String>]`: Kimlik olarak disk Guid 'si.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-142">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="d2cf2-143">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="d2cf2-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2cf2-144">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="d2cf2-145">`[MigrationId <String>]`: Geçiş işi GUID adı.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-145">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="d2cf2-146">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-146">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="d2cf2-147">`[Publisher <String>]`: Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-147">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="d2cf2-148">`[QuotaName <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-148">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="d2cf2-149">`[Sku <String>]`: SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-149">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="d2cf2-150">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-150">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d2cf2-151">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d2cf2-152">`[Type <String>]`: Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-152">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="d2cf2-153">`[Version <String>]`: Kaynağın sürümü.</span><span class="sxs-lookup"><span data-stu-id="d2cf2-153">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="d2cf2-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2cf2-154">RELATED LINKS</span></span>

