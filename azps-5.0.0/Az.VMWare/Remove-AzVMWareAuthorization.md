---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
ms.openlocfilehash: 13f5e76a7fbb101e9fa6b1247f233c0f85aba8bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277901"
---
# <span data-ttu-id="617b4-101">Remove-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="617b4-101">Remove-AzVMWareAuthorization</span></span>

## <span data-ttu-id="617b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="617b4-102">SYNOPSIS</span></span>
<span data-ttu-id="617b4-103">Özel bulutta ExpressRoute devresini silme</span><span class="sxs-lookup"><span data-stu-id="617b4-103">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="617b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="617b4-104">SYNTAX</span></span>

### <span data-ttu-id="617b4-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="617b4-105">Delete (Default)</span></span>
```
Remove-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="617b4-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="617b4-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="617b4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="617b4-107">DESCRIPTION</span></span>
<span data-ttu-id="617b4-108">Özel bulutta ExpressRoute devresini silme</span><span class="sxs-lookup"><span data-stu-id="617b4-108">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="617b4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="617b4-109">EXAMPLES</span></span>

### <span data-ttu-id="617b4-110">Örnek 1: özel bulut için Yetkilendirmeyi silme</span><span class="sxs-lookup"><span data-stu-id="617b4-110">Example 1: Delete authorization for private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="617b4-111">Özel bulutun yetkilendirmesini silme</span><span class="sxs-lookup"><span data-stu-id="617b4-111">Delete authorization for private cloud</span></span>

## <span data-ttu-id="617b4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="617b4-112">PARAMETERS</span></span>

### <span data-ttu-id="617b4-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="617b4-113">-AsJob</span></span>
<span data-ttu-id="617b4-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="617b4-114">Run the command as a job</span></span>

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

### <span data-ttu-id="617b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="617b4-115">-DefaultProfile</span></span>
<span data-ttu-id="617b4-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="617b4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="617b4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="617b4-117">-InputObject</span></span>
<span data-ttu-id="617b4-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="617b4-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="617b4-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="617b4-119">-Name</span></span>
<span data-ttu-id="617b4-120">Özel bulutta ExpressRoute devresi yetkilendirmesi adı</span><span class="sxs-lookup"><span data-stu-id="617b4-120">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="617b4-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="617b4-121">-NoWait</span></span>
<span data-ttu-id="617b4-122">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="617b4-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="617b4-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="617b4-123">-PassThru</span></span>
<span data-ttu-id="617b4-124">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="617b4-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="617b4-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="617b4-125">-PrivateCloudName</span></span>
<span data-ttu-id="617b4-126">Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="617b4-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="617b4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="617b4-127">-ResourceGroupName</span></span>
<span data-ttu-id="617b4-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="617b4-128">The name of the resource group.</span></span>
<span data-ttu-id="617b4-129">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="617b4-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="617b4-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="617b4-130">-SubscriptionId</span></span>
<span data-ttu-id="617b4-131">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="617b4-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="617b4-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="617b4-132">-Confirm</span></span>
<span data-ttu-id="617b4-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="617b4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="617b4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="617b4-134">-WhatIf</span></span>
<span data-ttu-id="617b4-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="617b4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="617b4-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="617b4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="617b4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="617b4-137">CommonParameters</span></span>
<span data-ttu-id="617b4-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="617b4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="617b4-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="617b4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="617b4-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="617b4-140">INPUTS</span></span>

### <span data-ttu-id="617b4-141">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. ıvmwareıdentity</span><span class="sxs-lookup"><span data-stu-id="617b4-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="617b4-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="617b4-142">OUTPUTS</span></span>

### <span data-ttu-id="617b4-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="617b4-143">System.Boolean</span></span>

## <span data-ttu-id="617b4-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="617b4-144">NOTES</span></span>

<span data-ttu-id="617b4-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="617b4-145">ALIASES</span></span>

<span data-ttu-id="617b4-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="617b4-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="617b4-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="617b4-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="617b4-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="617b4-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="617b4-149">INPUTOBJECT <IVMWareIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="617b4-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="617b4-150">`[AuthorizationName <String>]`: Özel bulutta ExpressRoute devresi yetkilendirmesi adı</span><span class="sxs-lookup"><span data-stu-id="617b4-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="617b4-151">`[ClusterName <String>]`: Özel buluttaki kümenin adı</span><span class="sxs-lookup"><span data-stu-id="617b4-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="617b4-152">`[HcxEnterpriseSiteName <String>]`: Özel bulutta HCX kurumsal sitesinin adı</span><span class="sxs-lookup"><span data-stu-id="617b4-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="617b4-153">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="617b4-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="617b4-154">`[Location <String>]`: Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="617b4-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="617b4-155">`[PrivateCloudName <String>]`: Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="617b4-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="617b4-156">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="617b4-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="617b4-157">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="617b4-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="617b4-158">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="617b4-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="617b4-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="617b4-159">RELATED LINKS</span></span>

