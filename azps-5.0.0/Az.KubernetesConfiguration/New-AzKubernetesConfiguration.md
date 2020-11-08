---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 70ff3c636f6c88ac89e53a5c2b1acb209aad274a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280185"
---
# <span data-ttu-id="d8b36-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8b36-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="d8b36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8b36-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b36-103">Yeni bir Kubernetes kaynak denetimi yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d8b36-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="d8b36-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8b36-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d8b36-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8b36-105">DESCRIPTION</span></span>
<span data-ttu-id="d8b36-106">Yeni bir Kubernetes kaynak denetimi yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d8b36-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="d8b36-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8b36-107">EXAMPLES</span></span>

### <span data-ttu-id="d8b36-108">Örnek 1: Kubernetes kümesi için yapılandırma oluşturma</span><span class="sxs-lookup"><span data-stu-id="d8b36-108">Example 1: Create a configuation for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -Name conf-test01 -ClusterName connaks-d983yc -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="d8b36-109">Bu komut, Kubernetes kümesi için bir yapılandırma oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8b36-109">This command creates a configuation for kubernetes cluster.</span></span>

## <span data-ttu-id="d8b36-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8b36-110">PARAMETERS</span></span>

### <span data-ttu-id="d8b36-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d8b36-111">-ClusterName</span></span>
<span data-ttu-id="d8b36-112">Kubernetes kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="d8b36-112">The name of the kubernetes cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b36-113">-Clusterkapsamlıdır</span><span class="sxs-lookup"><span data-stu-id="d8b36-113">-ClusterScoped</span></span>
<span data-ttu-id="d8b36-114">Geçirilen yapılandırmanın kapsamını kümeye ayarla (varsayılan olarak ad alanıdır).</span><span class="sxs-lookup"><span data-stu-id="d8b36-114">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="d8b36-115">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="d8b36-115">-ClusterType</span></span>
<span data-ttu-id="d8b36-116">Kubernetes küme kaynak adı (AKS kümeleri için) veya Connectedkümeler (OnPrem K8S kümeleri için).</span><span class="sxs-lookup"><span data-stu-id="d8b36-116">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b36-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b36-117">-DefaultProfile</span></span>
<span data-ttu-id="d8b36-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8b36-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8b36-119">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="d8b36-119">-EnableHelmOperator</span></span>
<span data-ttu-id="d8b36-120">Bu git yapılandırması için Helm Işlecini etkinleştirme seçeneği.</span><span class="sxs-lookup"><span data-stu-id="d8b36-120">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="d8b36-121">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="d8b36-121">-HelmOperatorChartValues</span></span>
<span data-ttu-id="d8b36-122">İşleç grafiği için değerler geçersiz kılınır.</span><span class="sxs-lookup"><span data-stu-id="d8b36-122">Values override for the operator Helm chart.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b36-123">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="d8b36-123">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="d8b36-124">Operatör Helm grafiğinin sürümü.</span><span class="sxs-lookup"><span data-stu-id="d8b36-124">Version of the operator Helm chart.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b36-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8b36-125">-Name</span></span>
<span data-ttu-id="d8b36-126">Kaynak denetimi yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="d8b36-126">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b36-127">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="d8b36-127">-OperatorInstanceName</span></span>
<span data-ttu-id="d8b36-128">Belirli bir yapılandırmayı tanımlayan işlecin örnek adı.</span><span class="sxs-lookup"><span data-stu-id="d8b36-128">Instance name of the operator - identifying the specific configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b36-129">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="d8b36-129">-OperatorNamespace</span></span>
<span data-ttu-id="d8b36-130">Bu işlecin yüklendiği ad alanı.</span><span class="sxs-lookup"><span data-stu-id="d8b36-130">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="d8b36-131">En fazla 253 küçük harf alfasayısal karakter, kısa çizgi ve yalnızca nokta.</span><span class="sxs-lookup"><span data-stu-id="d8b36-131">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b36-132">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="d8b36-132">-OperatorParameters</span></span>
<span data-ttu-id="d8b36-133">Dize biçiminde Işleç örneği için tüm parametreler.</span><span class="sxs-lookup"><span data-stu-id="d8b36-133">Any Parameters for the Operator instance in string format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b36-134">-Depotorurl</span><span class="sxs-lookup"><span data-stu-id="d8b36-134">-RepositoryUrl</span></span>
<span data-ttu-id="d8b36-135">SourceControl deposunun URL 'si.</span><span class="sxs-lookup"><span data-stu-id="d8b36-135">Url of the SourceControl Repository.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b36-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8b36-136">-ResourceGroupName</span></span>
<span data-ttu-id="d8b36-137">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d8b36-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b36-138">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d8b36-138">-SubscriptionId</span></span>
<span data-ttu-id="d8b36-139">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d8b36-139">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b36-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="d8b36-140">-Confirm</span></span>
<span data-ttu-id="d8b36-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d8b36-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8b36-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8b36-142">-WhatIf</span></span>
<span data-ttu-id="d8b36-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8b36-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8b36-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d8b36-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8b36-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b36-145">CommonParameters</span></span>
<span data-ttu-id="d8b36-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8b36-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b36-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d8b36-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b36-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8b36-148">INPUTS</span></span>

## <span data-ttu-id="d8b36-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8b36-149">OUTPUTS</span></span>

### <span data-ttu-id="d8b36-150">Microsoft. Azure. PowerShell. cmdlet. KubernetesConfiguration. modeller. Api20191101Preview. ısourcecontrolconfiguration</span><span class="sxs-lookup"><span data-stu-id="d8b36-150">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="d8b36-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8b36-151">NOTES</span></span>

<span data-ttu-id="d8b36-152">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="d8b36-152">ALIASES</span></span>

## <span data-ttu-id="d8b36-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8b36-153">RELATED LINKS</span></span>

