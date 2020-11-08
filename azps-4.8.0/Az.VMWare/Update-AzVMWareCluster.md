---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
ms.openlocfilehash: b8e1f819c01edac24ff23c629de130036442c9e5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107443"
---
# <span data-ttu-id="0fe03-101">Update-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="0fe03-101">Update-AzVMWareCluster</span></span>

## <span data-ttu-id="0fe03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fe03-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe03-103">Özel bulutta kümeyi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0fe03-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="0fe03-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0fe03-104">SYNTAX</span></span>

### <span data-ttu-id="0fe03-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0fe03-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0fe03-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="0fe03-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWareCluster -InputObject <IVMWareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0fe03-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0fe03-107">DESCRIPTION</span></span>
<span data-ttu-id="0fe03-108">Özel bulutta kümeyi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0fe03-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="0fe03-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0fe03-109">EXAMPLES</span></span>

### <span data-ttu-id="0fe03-110">Örnek 1: küme boyutunu ada göre güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0fe03-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="0fe03-111">Küme boyutunu ada göre güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0fe03-111">Update cluster size by name</span></span>

### <span data-ttu-id="0fe03-112">Örnek 2: küme boyutunu giriş nesnesine göre güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0fe03-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMWareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="0fe03-113">Küme boyutunu giriş nesnesine göre güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0fe03-113">Update cluster size by input object</span></span>

## <span data-ttu-id="0fe03-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0fe03-114">PARAMETERS</span></span>

### <span data-ttu-id="0fe03-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="0fe03-115">-AsJob</span></span>
<span data-ttu-id="0fe03-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="0fe03-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0fe03-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="0fe03-117">-ClusterSize</span></span>
<span data-ttu-id="0fe03-118">Küme boyutu</span><span class="sxs-lookup"><span data-stu-id="0fe03-118">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe03-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe03-119">-DefaultProfile</span></span>
<span data-ttu-id="0fe03-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0fe03-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fe03-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fe03-121">-InputObject</span></span>
<span data-ttu-id="0fe03-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0fe03-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe03-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="0fe03-123">-Name</span></span>
<span data-ttu-id="0fe03-124">Özel buluttaki kümenin adı</span><span class="sxs-lookup"><span data-stu-id="0fe03-124">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe03-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0fe03-125">-NoWait</span></span>
<span data-ttu-id="0fe03-126">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="0fe03-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0fe03-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="0fe03-127">-PrivateCloudName</span></span>
<span data-ttu-id="0fe03-128">Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="0fe03-128">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe03-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fe03-129">-ResourceGroupName</span></span>
<span data-ttu-id="0fe03-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0fe03-130">The name of the resource group.</span></span>
<span data-ttu-id="0fe03-131">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="0fe03-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe03-132">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0fe03-132">-SubscriptionId</span></span>
<span data-ttu-id="0fe03-133">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0fe03-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe03-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="0fe03-134">-Confirm</span></span>
<span data-ttu-id="0fe03-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0fe03-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fe03-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fe03-136">-WhatIf</span></span>
<span data-ttu-id="0fe03-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0fe03-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fe03-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0fe03-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fe03-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe03-139">CommonParameters</span></span>
<span data-ttu-id="0fe03-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0fe03-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe03-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0fe03-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe03-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0fe03-142">INPUTS</span></span>

### <span data-ttu-id="0fe03-143">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. ıvmwareıdentity</span><span class="sxs-lookup"><span data-stu-id="0fe03-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="0fe03-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0fe03-144">OUTPUTS</span></span>

### <span data-ttu-id="0fe03-145">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. Api20200320. ıluster</span><span class="sxs-lookup"><span data-stu-id="0fe03-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="0fe03-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0fe03-146">NOTES</span></span>

<span data-ttu-id="0fe03-147">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="0fe03-147">ALIASES</span></span>

<span data-ttu-id="0fe03-148">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="0fe03-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0fe03-149">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0fe03-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0fe03-150">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0fe03-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0fe03-151">INPUTOBJECT <IVMWareIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="0fe03-151">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0fe03-152">`[AuthorizationName <String>]`: Özel bulutta ExpressRoute devresi yetkilendirmesi adı</span><span class="sxs-lookup"><span data-stu-id="0fe03-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="0fe03-153">`[ClusterName <String>]`: Özel buluttaki kümenin adı</span><span class="sxs-lookup"><span data-stu-id="0fe03-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="0fe03-154">`[HcxEnterpriseSiteName <String>]`: Özel bulutta HCX kurumsal sitesinin adı</span><span class="sxs-lookup"><span data-stu-id="0fe03-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="0fe03-155">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="0fe03-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0fe03-156">`[Location <String>]`: Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="0fe03-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="0fe03-157">`[PrivateCloudName <String>]`: Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="0fe03-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="0fe03-158">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0fe03-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0fe03-159">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="0fe03-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="0fe03-160">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0fe03-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="0fe03-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0fe03-161">RELATED LINKS</span></span>

