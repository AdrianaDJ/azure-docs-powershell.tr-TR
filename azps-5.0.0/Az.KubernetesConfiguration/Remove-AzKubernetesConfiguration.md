---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: 2a9547b88129a199f97bbcff9281348f9d2c4659
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279034"
---
# <span data-ttu-id="e45e7-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="e45e7-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="e45e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e45e7-102">SYNOPSIS</span></span>
<span data-ttu-id="e45e7-103">Bu işlem, kaynak denetimi yapılandırmasını ayarlamak için kullanılan YAML dosyasını silecek ve gelecekte kaynak depo 'tan gelecek eşitlemeyi durduracaktır.</span><span class="sxs-lookup"><span data-stu-id="e45e7-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="e45e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e45e7-104">SYNTAX</span></span>

### <span data-ttu-id="e45e7-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e45e7-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e45e7-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="e45e7-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e45e7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e45e7-107">DESCRIPTION</span></span>
<span data-ttu-id="e45e7-108">Bu işlem, kaynak denetimi yapılandırmasını ayarlamak için kullanılan YAML dosyasını silecek ve gelecekte kaynak depo 'tan gelecek eşitlemeyi durduracaktır.</span><span class="sxs-lookup"><span data-stu-id="e45e7-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="e45e7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e45e7-109">EXAMPLES</span></span>

### <span data-ttu-id="e45e7-110">Örnek 1: Kubernetes kümesini adıyla yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e45e7-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ClusterName connaks-d983yc -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test01

```

<span data-ttu-id="e45e7-111">Bu komut, Kubernetes kümesinin adını adıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e45e7-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="e45e7-112">Örnek 2: Kubernetes kümesini nesneye göre yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e45e7-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="e45e7-113">Bu komut, Kubernetes kümesini nesneye göre yapılandırma öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e45e7-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="e45e7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e45e7-114">PARAMETERS</span></span>

### <span data-ttu-id="e45e7-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="e45e7-115">-AsJob</span></span>
<span data-ttu-id="e45e7-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="e45e7-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e45e7-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e45e7-117">-ClusterName</span></span>
<span data-ttu-id="e45e7-118">Kubernetes kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="e45e7-118">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="e45e7-119">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="e45e7-119">-ClusterType</span></span>
<span data-ttu-id="e45e7-120">Kubernetes küme kaynak adı (AKS kümeleri için) veya Connectedkümeler (OnPrem K8S kümeleri için).</span><span class="sxs-lookup"><span data-stu-id="e45e7-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="e45e7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e45e7-121">-DefaultProfile</span></span>
<span data-ttu-id="e45e7-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e45e7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e45e7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e45e7-123">-InputObject</span></span>
<span data-ttu-id="e45e7-124">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e45e7-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e45e7-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="e45e7-125">-Name</span></span>
<span data-ttu-id="e45e7-126">Kaynak denetimi yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="e45e7-126">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e45e7-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e45e7-127">-NoWait</span></span>
<span data-ttu-id="e45e7-128">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="e45e7-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e45e7-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e45e7-129">-PassThru</span></span>
<span data-ttu-id="e45e7-130">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="e45e7-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e45e7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e45e7-131">-ResourceGroupName</span></span>
<span data-ttu-id="e45e7-132">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e45e7-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="e45e7-133">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="e45e7-133">-SubscriptionId</span></span>
<span data-ttu-id="e45e7-134">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e45e7-134">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="e45e7-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="e45e7-135">-Confirm</span></span>
<span data-ttu-id="e45e7-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e45e7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e45e7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e45e7-137">-WhatIf</span></span>
<span data-ttu-id="e45e7-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e45e7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e45e7-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e45e7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e45e7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e45e7-140">CommonParameters</span></span>
<span data-ttu-id="e45e7-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e45e7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e45e7-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e45e7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e45e7-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e45e7-143">INPUTS</span></span>

### <span data-ttu-id="e45e7-144">Microsoft. Azure. PowerShell. cmdlet. KubernetesConfiguration. modeller. ıkubernetesconfigurationıdentity</span><span class="sxs-lookup"><span data-stu-id="e45e7-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="e45e7-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e45e7-145">OUTPUTS</span></span>

### <span data-ttu-id="e45e7-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e45e7-146">System.Boolean</span></span>

## <span data-ttu-id="e45e7-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e45e7-147">NOTES</span></span>

<span data-ttu-id="e45e7-148">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="e45e7-148">ALIASES</span></span>

<span data-ttu-id="e45e7-149">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="e45e7-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e45e7-150">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e45e7-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e45e7-151">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e45e7-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e45e7-152">INPUTOBJECT <IKubernetesConfigurationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="e45e7-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e45e7-153">`[ClusterName <String>]`: Kubernetes kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="e45e7-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="e45e7-154">`[ClusterResourceName <String>]`: Kubernetes küme kaynak adı (AKS kümeleri için) veya Connectedkümeler (OnPrem K8S kümeleri için).</span><span class="sxs-lookup"><span data-stu-id="e45e7-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="e45e7-155">`[ClusterRp <String>]`: Kubernetes küme RP-Microsoft. ContainerService (AKS kümeleri için) veya Microsoft. Kubernetes (OnPrem K8S kümeleri için).</span><span class="sxs-lookup"><span data-stu-id="e45e7-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="e45e7-156">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="e45e7-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e45e7-157">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e45e7-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="e45e7-158">`[SourceControlConfigurationName <String>]`: Kaynak denetimi yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="e45e7-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="e45e7-159">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e45e7-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="e45e7-160">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="e45e7-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="e45e7-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e45e7-161">RELATED LINKS</span></span>

