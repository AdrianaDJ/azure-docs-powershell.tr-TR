---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
ms.openlocfilehash: 04778d2aef4bbafe1638e8ab1971f626303c7be5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096784"
---
# <span data-ttu-id="f5f3e-101">Set-AzAks</span><span class="sxs-lookup"><span data-stu-id="f5f3e-101">Set-AzAks</span></span>

## <span data-ttu-id="f5f3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5f3e-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f3e-103">Yönetilen bir Kubernetes kümesi güncelleştirin veya oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="f5f3e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5f3e-104">SYNTAX</span></span>

### <span data-ttu-id="f5f3e-105">defaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f5f3e-105">defaultParameterSet (Default)</span></span>
```
Set-AzAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5f3e-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="f5f3e-106">InputObjectParameterSet</span></span>
```
Set-AzAks -InputObject <PSKubernetesCluster> [-Location <String>] [-AdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5f3e-107">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="f5f3e-107">IdParameterSet</span></span>
```
Set-AzAks [-Id] <String> [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5f3e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5f3e-108">DESCRIPTION</span></span>
<span data-ttu-id="f5f3e-109">Yönetilen bir Kubernetes kümesi güncelleştirin veya oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="f5f3e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5f3e-110">EXAMPLES</span></span>

### <span data-ttu-id="f5f3e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f5f3e-111">Example 1</span></span>
```
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="f5f3e-112">Kubernetes kümesindeki düğümlerin sayısını 5 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="f5f3e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5f3e-113">PARAMETERS</span></span>

### <span data-ttu-id="f5f3e-114">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="f5f3e-114">-AdminUserName</span></span>
<span data-ttu-id="f5f3e-115">Linux sanal makinelerinin Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-115">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="f5f3e-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="f5f3e-116">-AsJob</span></span>
<span data-ttu-id="f5f3e-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f5f3e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5f3e-118">-Clientidanvseçsecret</span><span class="sxs-lookup"><span data-stu-id="f5f3e-118">-ClientIdAndSecret</span></span>
<span data-ttu-id="f5f3e-119">AAD uygulaması/hizmet sorumlusu ile ilişkilendirilmiş istemci kimliği ve istemci parolası.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-119">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="f5f3e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f3e-120">-DefaultProfile</span></span>
<span data-ttu-id="f5f3e-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5f3e-122">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="f5f3e-122">-DnsNamePrefix</span></span>
<span data-ttu-id="f5f3e-123">Kümenin DNS adı öneki.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-123">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="f5f3e-124">-ID</span><span class="sxs-lookup"><span data-stu-id="f5f3e-124">-Id</span></span>
<span data-ttu-id="f5f3e-125">Yönetilen Kubernetes kümesinin kimliği</span><span class="sxs-lookup"><span data-stu-id="f5f3e-125">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="f5f3e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5f3e-126">-InputObject</span></span>
<span data-ttu-id="f5f3e-127">Normalde ardışık düzen aracılığıyla iletilen bir PSKubernetesCluster nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-127">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="f5f3e-128">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="f5f3e-128">-KubernetesVersion</span></span>
<span data-ttu-id="f5f3e-129">Küme oluştururken kullanılacak Kubernetes sürümü.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-129">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="f5f3e-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="f5f3e-130">-Location</span></span>
<span data-ttu-id="f5f3e-131">Kümenin Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-131">Azure location for the cluster.</span></span>
<span data-ttu-id="f5f3e-132">Kaynak grubunun konumunu varsayılan olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="f5f3e-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="f5f3e-133">-Name</span></span>
<span data-ttu-id="f5f3e-134">Kubernetes yönetilen küme adı.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="f5f3e-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="f5f3e-135">-NodeCount</span></span>
<span data-ttu-id="f5f3e-136">Düğüm havuzları için varsayılan düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="f5f3e-137">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="f5f3e-137">-NodeOsDiskSize</span></span>
<span data-ttu-id="f5f3e-138">Düğüm havuzları için varsayılan düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-138">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="f5f3e-139">-Edevmboyut</span><span class="sxs-lookup"><span data-stu-id="f5f3e-139">-NodeVmSize</span></span>
<span data-ttu-id="f5f3e-140">Sanal makinenin boyutu.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-140">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="f5f3e-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5f3e-141">-ResourceGroupName</span></span>
<span data-ttu-id="f5f3e-142">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-142">Resource Group Name.</span></span>

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

### <span data-ttu-id="f5f3e-143">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="f5f3e-143">-SshKeyValue</span></span>
<span data-ttu-id="f5f3e-144">SSH anahtar dosyası veya anahtar dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-144">SSH key file value or key file path.</span></span>
<span data-ttu-id="f5f3e-145">{HOME}/.ssh/id_rsa. pub varsayılan olur.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-145">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="f5f3e-146">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f5f3e-146">-Tag</span></span>
<span data-ttu-id="f5f3e-147">Kaynağa uygulanacak Etiketler</span><span class="sxs-lookup"><span data-stu-id="f5f3e-147">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="f5f3e-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="f5f3e-148">-Confirm</span></span>
<span data-ttu-id="f5f3e-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5f3e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5f3e-150">-WhatIf</span></span>
<span data-ttu-id="f5f3e-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5f3e-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5f3e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f3e-153">CommonParameters</span></span>
<span data-ttu-id="f5f3e-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f3e-155">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5f3e-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f3e-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5f3e-156">INPUTS</span></span>

### <span data-ttu-id="f5f3e-157">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="f5f3e-157">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="f5f3e-158">System. String</span><span class="sxs-lookup"><span data-stu-id="f5f3e-158">System.String</span></span>

## <span data-ttu-id="f5f3e-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5f3e-159">OUTPUTS</span></span>

### <span data-ttu-id="f5f3e-160">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="f5f3e-160">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="f5f3e-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5f3e-161">NOTES</span></span>

## <span data-ttu-id="f5f3e-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5f3e-162">RELATED LINKS</span></span>
