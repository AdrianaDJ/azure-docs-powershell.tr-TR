---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
ms.openlocfilehash: 936ed70f7040f9558db891b4e75299759c647bf9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107440"
---
# <span data-ttu-id="29caa-101">Remove-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="29caa-101">Remove-AzVMWareCluster</span></span>

## <span data-ttu-id="29caa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29caa-102">SYNOPSIS</span></span>
<span data-ttu-id="29caa-103">Özel buluttaki kümeyi silme</span><span class="sxs-lookup"><span data-stu-id="29caa-103">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="29caa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29caa-104">SYNTAX</span></span>

### <span data-ttu-id="29caa-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="29caa-105">Delete (Default)</span></span>
```
Remove-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="29caa-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="29caa-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="29caa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="29caa-107">DESCRIPTION</span></span>
<span data-ttu-id="29caa-108">Özel buluttaki kümeyi silme</span><span class="sxs-lookup"><span data-stu-id="29caa-108">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="29caa-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29caa-109">EXAMPLES</span></span>

### <span data-ttu-id="29caa-110">Örnek 1: özel bulutta kümeyi silme</span><span class="sxs-lookup"><span data-stu-id="29caa-110">Example 1: Delete cluster in private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="29caa-111">Özel bulutta kümeyi silme</span><span class="sxs-lookup"><span data-stu-id="29caa-111">Delete cluster in private cloud</span></span>

## <span data-ttu-id="29caa-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29caa-112">PARAMETERS</span></span>

### <span data-ttu-id="29caa-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="29caa-113">-AsJob</span></span>
<span data-ttu-id="29caa-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="29caa-114">Run the command as a job</span></span>

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

### <span data-ttu-id="29caa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29caa-115">-DefaultProfile</span></span>
<span data-ttu-id="29caa-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="29caa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29caa-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29caa-117">-InputObject</span></span>
<span data-ttu-id="29caa-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29caa-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="29caa-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="29caa-119">-Name</span></span>
<span data-ttu-id="29caa-120">Özel buluttaki kümenin adı</span><span class="sxs-lookup"><span data-stu-id="29caa-120">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29caa-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="29caa-121">-NoWait</span></span>
<span data-ttu-id="29caa-122">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="29caa-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="29caa-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="29caa-123">-PassThru</span></span>
<span data-ttu-id="29caa-124">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="29caa-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="29caa-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="29caa-125">-PrivateCloudName</span></span>
<span data-ttu-id="29caa-126">Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="29caa-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="29caa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29caa-127">-ResourceGroupName</span></span>
<span data-ttu-id="29caa-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="29caa-128">The name of the resource group.</span></span>
<span data-ttu-id="29caa-129">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="29caa-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="29caa-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="29caa-130">-SubscriptionId</span></span>
<span data-ttu-id="29caa-131">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="29caa-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="29caa-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="29caa-132">-Confirm</span></span>
<span data-ttu-id="29caa-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="29caa-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29caa-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29caa-134">-WhatIf</span></span>
<span data-ttu-id="29caa-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="29caa-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29caa-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="29caa-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29caa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29caa-137">CommonParameters</span></span>
<span data-ttu-id="29caa-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29caa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29caa-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="29caa-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29caa-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29caa-140">INPUTS</span></span>

### <span data-ttu-id="29caa-141">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. ıvmwareıdentity</span><span class="sxs-lookup"><span data-stu-id="29caa-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="29caa-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29caa-142">OUTPUTS</span></span>

### <span data-ttu-id="29caa-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29caa-143">System.Boolean</span></span>

## <span data-ttu-id="29caa-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29caa-144">NOTES</span></span>

<span data-ttu-id="29caa-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="29caa-145">ALIASES</span></span>

<span data-ttu-id="29caa-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="29caa-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="29caa-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="29caa-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="29caa-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="29caa-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="29caa-149">INPUTOBJECT <IVMWareIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="29caa-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="29caa-150">`[AuthorizationName <String>]`: Özel bulutta ExpressRoute devresi yetkilendirmesi adı</span><span class="sxs-lookup"><span data-stu-id="29caa-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="29caa-151">`[ClusterName <String>]`: Özel buluttaki kümenin adı</span><span class="sxs-lookup"><span data-stu-id="29caa-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="29caa-152">`[HcxEnterpriseSiteName <String>]`: Özel bulutta HCX kurumsal sitesinin adı</span><span class="sxs-lookup"><span data-stu-id="29caa-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="29caa-153">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="29caa-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="29caa-154">`[Location <String>]`: Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="29caa-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="29caa-155">`[PrivateCloudName <String>]`: Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="29caa-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="29caa-156">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="29caa-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="29caa-157">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="29caa-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="29caa-158">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="29caa-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="29caa-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29caa-159">RELATED LINKS</span></span>

