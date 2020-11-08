---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsvmextension
schema: 2.0.0
ms.openlocfilehash: 0b2bca9555b14a391df69acc4abdb2fc8c95017c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106725"
---
# <span data-ttu-id="43846-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="43846-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="43846-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43846-102">SYNOPSIS</span></span>
<span data-ttu-id="43846-103">Belirtilen sanal makine uzantısı görüntüsünü siler.</span><span class="sxs-lookup"><span data-stu-id="43846-103">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="43846-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43846-104">SYNTAX</span></span>

### <span data-ttu-id="43846-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="43846-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="43846-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="43846-106">DeleteViaIdentity</span></span>
```
Remove-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="43846-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="43846-107">DESCRIPTION</span></span>
<span data-ttu-id="43846-108">Belirtilen sanal makine uzantısı görüntüsünü siler.</span><span class="sxs-lookup"><span data-stu-id="43846-108">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="43846-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43846-109">EXAMPLES</span></span>

### <span data-ttu-id="43846-110">Örnek 1: var olan bir VM uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="43846-110">Example 1: Remove a VM Extension that Exists</span></span> 
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type MicroExtension -Version 0.1.0
```

<span data-ttu-id="43846-111">İşlem kotasını kaldırma başarılı bir şekilde çağrı olmaz</span><span class="sxs-lookup"><span data-stu-id="43846-111">A successful call to remove a compute quota will not return any output</span></span>

### <span data-ttu-id="43846-112">Örnek 2: varolmayan bir VM uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="43846-112">Example 2: Remove a VM Extension that Does Not Exist</span></span>
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type DoesntExist -Version 9.8.7
```

<span data-ttu-id="43846-113">Var olmayan bir platform görüntüsünü kaldırmak için başarılı bir çağrı çıkışı döndürmez</span><span class="sxs-lookup"><span data-stu-id="43846-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="43846-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43846-114">PARAMETERS</span></span>

### <span data-ttu-id="43846-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43846-115">-DefaultProfile</span></span>
<span data-ttu-id="43846-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="43846-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43846-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43846-117">-InputObject</span></span>
<span data-ttu-id="43846-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="43846-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="43846-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="43846-119">-Location</span></span>
<span data-ttu-id="43846-120">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="43846-120">Location of the resource.</span></span>

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

### <span data-ttu-id="43846-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="43846-121">-PassThru</span></span>
<span data-ttu-id="43846-122">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="43846-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="43846-123">-Publisher</span><span class="sxs-lookup"><span data-stu-id="43846-123">-Publisher</span></span>
<span data-ttu-id="43846-124">Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="43846-124">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="43846-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="43846-125">-SubscriptionId</span></span>
<span data-ttu-id="43846-126">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="43846-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="43846-127">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="43846-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="43846-128">-Tür</span><span class="sxs-lookup"><span data-stu-id="43846-128">-Type</span></span>
<span data-ttu-id="43846-129">Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="43846-129">Type of extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="43846-130">-Version</span><span class="sxs-lookup"><span data-stu-id="43846-130">-Version</span></span>
<span data-ttu-id="43846-131">Kaynağın sürümü.</span><span class="sxs-lookup"><span data-stu-id="43846-131">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="43846-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="43846-132">-Confirm</span></span>
<span data-ttu-id="43846-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="43846-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43846-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43846-134">-WhatIf</span></span>
<span data-ttu-id="43846-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="43846-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43846-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="43846-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43846-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43846-137">CommonParameters</span></span>
<span data-ttu-id="43846-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43846-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43846-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="43846-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43846-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43846-140">INPUTS</span></span>

### <span data-ttu-id="43846-141">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. ıuteadminıdentity</span><span class="sxs-lookup"><span data-stu-id="43846-141">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="43846-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43846-142">OUTPUTS</span></span>

### <span data-ttu-id="43846-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43846-143">System.Boolean</span></span>



## <span data-ttu-id="43846-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43846-144">NOTES</span></span>

<span data-ttu-id="43846-145">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="43846-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43846-146">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="43846-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="43846-147">INPUTOBJECT <IComputeAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="43846-147">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43846-148">`[DiskId <String>]`: Kimlik olarak disk Guid 'si.</span><span class="sxs-lookup"><span data-stu-id="43846-148">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="43846-149">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="43846-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43846-150">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="43846-150">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="43846-151">`[MigrationId <String>]`: Geçiş işi GUID adı.</span><span class="sxs-lookup"><span data-stu-id="43846-151">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="43846-152">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="43846-152">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="43846-153">`[Publisher <String>]`: Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="43846-153">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="43846-154">`[QuotaName <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="43846-154">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="43846-155">`[Sku <String>]`: SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="43846-155">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="43846-156">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="43846-156">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="43846-157">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="43846-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="43846-158">`[Type <String>]`: Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="43846-158">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="43846-159">`[Version <String>]`: Kaynağın sürümü.</span><span class="sxs-lookup"><span data-stu-id="43846-159">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="43846-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43846-160">RELATED LINKS</span></span>

