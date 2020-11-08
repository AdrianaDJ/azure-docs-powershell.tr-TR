---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 0df5c0d9975acc048ba5842543ec2c4d522567c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277103"
---
# <span data-ttu-id="ec32a-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="ec32a-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="ec32a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec32a-102">SYNOPSIS</span></span>
<span data-ttu-id="ec32a-103">Yönetilen bir Kubernetes kümesi güncelleştirin veya oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ec32a-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="ec32a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec32a-104">SYNTAX</span></span>

### <span data-ttu-id="ec32a-105">defaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ec32a-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec32a-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="ec32a-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec32a-107">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="ec32a-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec32a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec32a-108">DESCRIPTION</span></span>
<span data-ttu-id="ec32a-109">Yönetilen bir Kubernetes kümesi güncelleştirin veya oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ec32a-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="ec32a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec32a-110">EXAMPLES</span></span>

### <span data-ttu-id="ec32a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ec32a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="ec32a-112">Kubernetes kümesindeki düğümlerin sayısını 5 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ec32a-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="ec32a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec32a-113">PARAMETERS</span></span>

### <span data-ttu-id="ec32a-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="ec32a-114">-AsJob</span></span>
<span data-ttu-id="ec32a-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ec32a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec32a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec32a-116">-DefaultProfile</span></span>
<span data-ttu-id="ec32a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec32a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec32a-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="ec32a-118">-DnsNamePrefix</span></span>
<span data-ttu-id="ec32a-119">Kümenin DNS adı öneki.</span><span class="sxs-lookup"><span data-stu-id="ec32a-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="ec32a-120">-Enablenodeautoölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="ec32a-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="ec32a-121">Otomatik gizleme</span><span class="sxs-lookup"><span data-stu-id="ec32a-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="ec32a-122">-ID</span><span class="sxs-lookup"><span data-stu-id="ec32a-122">-Id</span></span>
<span data-ttu-id="ec32a-123">Yönetilen Kubernetes kümesinin kimliği</span><span class="sxs-lookup"><span data-stu-id="ec32a-123">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec32a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec32a-124">-InputObject</span></span>
<span data-ttu-id="ec32a-125">Normalde ardışık düzen aracılığıyla iletilen bir PSKubernetesCluster nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ec32a-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec32a-126">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="ec32a-126">-KubernetesVersion</span></span>
<span data-ttu-id="ec32a-127">Küme oluştururken kullanılacak Kubernetes sürümü.</span><span class="sxs-lookup"><span data-stu-id="ec32a-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="ec32a-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="ec32a-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="ec32a-129">Linux sanal makinelerinin Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="ec32a-129">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AdminUserName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec32a-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="ec32a-130">-Location</span></span>
<span data-ttu-id="ec32a-131">Kümenin Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="ec32a-131">Azure location for the cluster.</span></span>
<span data-ttu-id="ec32a-132">Kaynak grubunun konumunu varsayılan olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="ec32a-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="ec32a-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="ec32a-133">-Name</span></span>
<span data-ttu-id="ec32a-134">Kubernetes yönetilen küme adı.</span><span class="sxs-lookup"><span data-stu-id="ec32a-134">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec32a-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="ec32a-135">-NodeCount</span></span>
<span data-ttu-id="ec32a-136">Düğüm havuzları için varsayılan düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="ec32a-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="ec32a-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="ec32a-137">-NodeMaxCount</span></span>
<span data-ttu-id="ec32a-138">Otomatik ölçeklendirme için en fazla düğüm sayısı</span><span class="sxs-lookup"><span data-stu-id="ec32a-138">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="ec32a-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="ec32a-139">-NodeMinCount</span></span>
<span data-ttu-id="ec32a-140">Otomatik ölçeklendirme için en az düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="ec32a-140">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="ec32a-141">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="ec32a-141">-NodeName</span></span>
<span data-ttu-id="ec32a-142">Abonelik ve kaynak grubu bağlamında aracı havuzu profilinin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="ec32a-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="ec32a-143">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="ec32a-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="ec32a-144">Düğüm havuzları için varsayılan düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="ec32a-144">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="ec32a-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="ec32a-145">-NodePoolMode</span></span>
<span data-ttu-id="ec32a-146">NodePoolMode bir düğüm havuzu için temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ec32a-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="ec32a-147">-Edevmboyut</span><span class="sxs-lookup"><span data-stu-id="ec32a-147">-NodeVmSize</span></span>
<span data-ttu-id="ec32a-148">Sanal makinenin boyutu.</span><span class="sxs-lookup"><span data-stu-id="ec32a-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="ec32a-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec32a-149">-ResourceGroupName</span></span>
<span data-ttu-id="ec32a-150">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ec32a-150">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec32a-151">-Serviceprenalidancısecret</span><span class="sxs-lookup"><span data-stu-id="ec32a-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="ec32a-152">AAD uygulaması/hizmet sorumlusu ile ilişkilendirilmiş istemci kimliği ve istemci parolası.</span><span class="sxs-lookup"><span data-stu-id="ec32a-152">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: defaultParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec32a-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="ec32a-153">-SshKeyValue</span></span>
<span data-ttu-id="ec32a-154">SSH anahtar dosyası veya anahtar dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="ec32a-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="ec32a-155">{HOME}/.ssh/id_rsa. pub varsayılan olur.</span><span class="sxs-lookup"><span data-stu-id="ec32a-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec32a-156">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ec32a-156">-Tag</span></span>
<span data-ttu-id="ec32a-157">Kaynağa uygulanacak Etiketler</span><span class="sxs-lookup"><span data-stu-id="ec32a-157">Tags to be applied to the resource</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec32a-158">-Onay</span><span class="sxs-lookup"><span data-stu-id="ec32a-158">-Confirm</span></span>
<span data-ttu-id="ec32a-159">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ec32a-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec32a-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec32a-160">-WhatIf</span></span>
<span data-ttu-id="ec32a-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec32a-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec32a-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ec32a-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec32a-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec32a-163">CommonParameters</span></span>
<span data-ttu-id="ec32a-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec32a-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec32a-165">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ec32a-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec32a-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec32a-166">INPUTS</span></span>

### <span data-ttu-id="ec32a-167">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ec32a-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="ec32a-168">System. String</span><span class="sxs-lookup"><span data-stu-id="ec32a-168">System.String</span></span>

## <span data-ttu-id="ec32a-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec32a-169">OUTPUTS</span></span>

### <span data-ttu-id="ec32a-170">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ec32a-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="ec32a-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec32a-171">NOTES</span></span>

## <span data-ttu-id="ec32a-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec32a-172">RELATED LINKS</span></span>
