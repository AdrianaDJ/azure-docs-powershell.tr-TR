---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: ae4fc80c54aedf7f35ebfc6c0c5f16bb2e5028ee
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106727"
---
# <span data-ttu-id="e935b-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="e935b-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="e935b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e935b-102">SYNOPSIS</span></span>
<span data-ttu-id="e935b-103">Platform görüntüsünü silme</span><span class="sxs-lookup"><span data-stu-id="e935b-103">Delete a platform image</span></span>

## <span data-ttu-id="e935b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e935b-104">SYNTAX</span></span>

### <span data-ttu-id="e935b-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e935b-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e935b-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="e935b-106">DeleteViaIdentity</span></span>
```
Remove-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e935b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e935b-107">DESCRIPTION</span></span>
<span data-ttu-id="e935b-108">Platform görüntüsünü silme</span><span class="sxs-lookup"><span data-stu-id="e935b-108">Delete a platform image</span></span>

## <span data-ttu-id="e935b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e935b-109">EXAMPLES</span></span>

### <span data-ttu-id="e935b-110">Örnek 1: platform görüntüsünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="e935b-110">Example 1: Remove a Platform Image</span></span>
```powershell
PS C:\>Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.0.0
```

<span data-ttu-id="e935b-111">Bir platform görüntüsünü kaldırma işleminin başarılı olması hiçbir çıkış döndürmez</span><span class="sxs-lookup"><span data-stu-id="e935b-111">A successful call to remove a platform image will not return any output</span></span>

### <span data-ttu-id="e935b-112">Örnek 2: bir platform görüntüsünü kaldırma yok</span><span class="sxs-lookup"><span data-stu-id="e935b-112">Example 2: Remove a Platform Image the Does Not Exist</span></span>
```powershell
PS C:\>  Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.1.6

```

<span data-ttu-id="e935b-113">Var olmayan bir platform görüntüsünü kaldırmak için başarılı bir çağrı çıkışı döndürmez</span><span class="sxs-lookup"><span data-stu-id="e935b-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="e935b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e935b-114">PARAMETERS</span></span>

### <span data-ttu-id="e935b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e935b-115">-DefaultProfile</span></span>
<span data-ttu-id="e935b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e935b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e935b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e935b-117">-InputObject</span></span>
<span data-ttu-id="e935b-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e935b-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e935b-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="e935b-119">-Location</span></span>
<span data-ttu-id="e935b-120">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="e935b-120">Location of the resource.</span></span>

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

### <span data-ttu-id="e935b-121">-Teklif</span><span class="sxs-lookup"><span data-stu-id="e935b-121">-Offer</span></span>
<span data-ttu-id="e935b-122">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="e935b-122">Name of the offer.</span></span>

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

### <span data-ttu-id="e935b-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e935b-123">-PassThru</span></span>
<span data-ttu-id="e935b-124">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="e935b-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e935b-125">-Publisher</span><span class="sxs-lookup"><span data-stu-id="e935b-125">-Publisher</span></span>
<span data-ttu-id="e935b-126">Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="e935b-126">Name of the publisher.</span></span>

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

### <span data-ttu-id="e935b-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="e935b-127">-Sku</span></span>
<span data-ttu-id="e935b-128">SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="e935b-128">Name of the SKU.</span></span>

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

### <span data-ttu-id="e935b-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="e935b-129">-SubscriptionId</span></span>
<span data-ttu-id="e935b-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="e935b-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e935b-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e935b-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e935b-132">-Version</span><span class="sxs-lookup"><span data-stu-id="e935b-132">-Version</span></span>
<span data-ttu-id="e935b-133">Kaynağın sürümü.</span><span class="sxs-lookup"><span data-stu-id="e935b-133">The version of the resource.</span></span>

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

### <span data-ttu-id="e935b-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="e935b-134">-Confirm</span></span>
<span data-ttu-id="e935b-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e935b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e935b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e935b-136">-WhatIf</span></span>
<span data-ttu-id="e935b-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e935b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e935b-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e935b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e935b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e935b-139">CommonParameters</span></span>
<span data-ttu-id="e935b-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e935b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e935b-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e935b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e935b-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e935b-142">INPUTS</span></span>

### <span data-ttu-id="e935b-143">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. ıuteadminıdentity</span><span class="sxs-lookup"><span data-stu-id="e935b-143">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="e935b-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e935b-144">OUTPUTS</span></span>

### <span data-ttu-id="e935b-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e935b-145">System.Boolean</span></span>



## <span data-ttu-id="e935b-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e935b-146">NOTES</span></span>

<span data-ttu-id="e935b-147">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e935b-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e935b-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e935b-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e935b-149">INPUTOBJECT <IComputeAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="e935b-149">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e935b-150">`[DiskId <String>]`: Kimlik olarak disk Guid 'si.</span><span class="sxs-lookup"><span data-stu-id="e935b-150">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="e935b-151">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="e935b-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e935b-152">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="e935b-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="e935b-153">`[MigrationId <String>]`: Geçiş işi GUID adı.</span><span class="sxs-lookup"><span data-stu-id="e935b-153">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="e935b-154">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="e935b-154">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="e935b-155">`[Publisher <String>]`: Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="e935b-155">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="e935b-156">`[QuotaName <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="e935b-156">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="e935b-157">`[Sku <String>]`: SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="e935b-157">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="e935b-158">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="e935b-158">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e935b-159">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e935b-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e935b-160">`[Type <String>]`: Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="e935b-160">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="e935b-161">`[Version <String>]`: Kaynağın sürümü.</span><span class="sxs-lookup"><span data-stu-id="e935b-161">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="e935b-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e935b-162">RELATED LINKS</span></span>

