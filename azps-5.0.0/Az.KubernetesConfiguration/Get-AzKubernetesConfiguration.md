---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 3fd93e42b8f38659f61fcbeb0f49040409f635a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279036"
---
# <span data-ttu-id="d4d7c-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4d7c-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="d4d7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4d7c-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d7c-103">Kaynak denetimi yapılandırmasının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="d4d7c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4d7c-104">SYNTAX</span></span>

### <span data-ttu-id="d4d7c-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d4d7c-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d4d7c-106">Al</span><span class="sxs-lookup"><span data-stu-id="d4d7c-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d4d7c-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="d4d7c-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4d7c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4d7c-108">DESCRIPTION</span></span>
<span data-ttu-id="d4d7c-109">Kaynak denetimi yapılandırmasının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="d4d7c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4d7c-110">EXAMPLES</span></span>

### <span data-ttu-id="d4d7c-111">Örnek 1: Kubernetes kümesinin tüm yapılandırmalarını alma</span><span class="sxs-lookup"><span data-stu-id="d4d7c-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="d4d7c-112">Bu komut, tüm Kubernetes kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="d4d7c-113">Örnek 2: bir Kubernetes kümesini adıyla yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d4d7c-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name conf-t02

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="d4d7c-114">Bu komut, Kubernetes kümesinin adını adıyla alır.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="d4d7c-115">Örnek 3: bir Kubernetes kümesini nesneye göre yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d4d7c-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name conf-test02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="d4d7c-116">Bu komut, bir Kubernetes kümesini nesneye göre yapılandırmanızı alır.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="d4d7c-117">Örnek 4: bir Kubernetes kümesini ardışık düzene göre yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d4d7c-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/conf-test01'} | Get-AzKubernetesConfiguration

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="d4d7c-118">Bu komut, bir Kubernetes kümesini ardışık düzene göre yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="d4d7c-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4d7c-119">PARAMETERS</span></span>

### <span data-ttu-id="d4d7c-120">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d4d7c-120">-ClusterName</span></span>
<span data-ttu-id="d4d7c-121">Kubernetes kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-121">The name of the kubernetes cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d7c-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="d4d7c-122">-ClusterRp</span></span>
<span data-ttu-id="d4d7c-123">Kubernetes küme RP-Microsoft. ContainerService (örneğin kümeler için) veya Microsoft. Kubernetes (OnPrem K8S kümeleri için).</span><span class="sxs-lookup"><span data-stu-id="d4d7c-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d7c-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="d4d7c-124">-ClusterType</span></span>
<span data-ttu-id="d4d7c-125">Kubernetes küme kaynak adı (AKS kümeleri için) veya Connectedkümeler (OnPrem K8S kümeleri için).</span><span class="sxs-lookup"><span data-stu-id="d4d7c-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d7c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4d7c-126">-DefaultProfile</span></span>
<span data-ttu-id="d4d7c-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4d7c-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4d7c-128">-InputObject</span></span>
<span data-ttu-id="d4d7c-129">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4d7c-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="d4d7c-130">-Name</span></span>
<span data-ttu-id="d4d7c-131">Kaynak denetimi yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-131">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d7c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4d7c-132">-ResourceGroupName</span></span>
<span data-ttu-id="d4d7c-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d7c-134">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d4d7c-134">-SubscriptionId</span></span>
<span data-ttu-id="d4d7c-135">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-135">The Azure subscription ID.</span></span>
<span data-ttu-id="d4d7c-136">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="d4d7c-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="d4d7c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d7c-137">CommonParameters</span></span>
<span data-ttu-id="d4d7c-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d7c-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d7c-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4d7c-140">INPUTS</span></span>

### <span data-ttu-id="d4d7c-141">Microsoft. Azure. PowerShell. cmdlet. KubernetesConfiguration. modeller. ıkubernetesconfigurationıdentity</span><span class="sxs-lookup"><span data-stu-id="d4d7c-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="d4d7c-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4d7c-142">OUTPUTS</span></span>

### <span data-ttu-id="d4d7c-143">Microsoft. Azure. PowerShell. cmdlet. KubernetesConfiguration. modeller. Api20191101Preview. ısourcecontrolconfiguration</span><span class="sxs-lookup"><span data-stu-id="d4d7c-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="d4d7c-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4d7c-144">NOTES</span></span>

<span data-ttu-id="d4d7c-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="d4d7c-145">ALIASES</span></span>

<span data-ttu-id="d4d7c-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="d4d7c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d4d7c-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d4d7c-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d4d7c-149">INPUTOBJECT <IKubernetesConfigurationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="d4d7c-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d4d7c-150">`[ClusterName <String>]`: Kubernetes kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="d4d7c-151">`[ClusterResourceName <String>]`: Kubernetes küme kaynak adı (AKS kümeleri için) veya Connectedkümeler (OnPrem K8S kümeleri için).</span><span class="sxs-lookup"><span data-stu-id="d4d7c-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="d4d7c-152">`[ClusterRp <String>]`: Kubernetes küme RP-Microsoft. ContainerService (AKS kümeleri için) veya Microsoft. Kubernetes (OnPrem K8S kümeleri için).</span><span class="sxs-lookup"><span data-stu-id="d4d7c-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="d4d7c-153">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="d4d7c-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d4d7c-154">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d4d7c-155">`[SourceControlConfigurationName <String>]`: Kaynak denetimi yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="d4d7c-156">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d4d7c-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="d4d7c-157">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="d4d7c-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="d4d7c-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4d7c-158">RELATED LINKS</span></span>

