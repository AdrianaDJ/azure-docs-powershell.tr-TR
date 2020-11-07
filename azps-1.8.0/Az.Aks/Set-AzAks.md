---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
ms.openlocfilehash: 9b63ede0bbd24adb98159ca6cfee08238b26aabc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751223"
---
# <span data-ttu-id="5e1b0-101">Set-AzAks</span><span class="sxs-lookup"><span data-stu-id="5e1b0-101">Set-AzAks</span></span>

## <span data-ttu-id="5e1b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e1b0-102">SYNOPSIS</span></span>
<span data-ttu-id="5e1b0-103">Yönetilen bir Kubernetes kümesi güncelleştirin veya oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="5e1b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e1b0-104">SYNTAX</span></span>

### <span data-ttu-id="5e1b0-105">defaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5e1b0-105">defaultParameterSet (Default)</span></span>
```
Set-AzAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e1b0-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="5e1b0-106">InputObjectParameterSet</span></span>
```
Set-AzAks -InputObject <PSKubernetesCluster> [-Location <String>] [-AdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e1b0-107">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="5e1b0-107">IdParameterSet</span></span>
```
Set-AzAks [-Id] <String> [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e1b0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e1b0-108">DESCRIPTION</span></span>
<span data-ttu-id="5e1b0-109">Yönetilen bir Kubernetes kümesi güncelleştirin veya oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="5e1b0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e1b0-110">EXAMPLES</span></span>

### <span data-ttu-id="5e1b0-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5e1b0-111">Example 1</span></span>
```
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="5e1b0-112">Kubernetes kümesindeki düğümlerin sayısını 5 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="5e1b0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e1b0-113">PARAMETERS</span></span>

### <span data-ttu-id="5e1b0-114">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="5e1b0-114">-AdminUserName</span></span>
<span data-ttu-id="5e1b0-115">Linux sanal makinelerinin Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-115">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="5e1b0-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="5e1b0-116">-AsJob</span></span>
<span data-ttu-id="5e1b0-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5e1b0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e1b0-118">-Clientidanvseçsecret</span><span class="sxs-lookup"><span data-stu-id="5e1b0-118">-ClientIdAndSecret</span></span>
<span data-ttu-id="5e1b0-119">AAD uygulaması/hizmet sorumlusu ile ilişkilendirilmiş istemci kimliği ve istemci parolası.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-119">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="5e1b0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e1b0-120">-DefaultProfile</span></span>
<span data-ttu-id="5e1b0-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e1b0-122">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="5e1b0-122">-DnsNamePrefix</span></span>
<span data-ttu-id="5e1b0-123">Kümenin DNS adı öneki.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-123">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="5e1b0-124">-ID</span><span class="sxs-lookup"><span data-stu-id="5e1b0-124">-Id</span></span>
<span data-ttu-id="5e1b0-125">Yönetilen Kubernetes kümesinin kimliği</span><span class="sxs-lookup"><span data-stu-id="5e1b0-125">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="5e1b0-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e1b0-126">-InputObject</span></span>
<span data-ttu-id="5e1b0-127">Normalde ardışık düzen aracılığıyla iletilen bir PSKubernetesCluster nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-127">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="5e1b0-128">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="5e1b0-128">-KubernetesVersion</span></span>
<span data-ttu-id="5e1b0-129">Küme oluştururken kullanılacak Kubernetes sürümü.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-129">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="5e1b0-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="5e1b0-130">-Location</span></span>
<span data-ttu-id="5e1b0-131">Kümenin Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-131">Azure location for the cluster.</span></span>
<span data-ttu-id="5e1b0-132">Kaynak grubunun konumunu varsayılan olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="5e1b0-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="5e1b0-133">-Name</span></span>
<span data-ttu-id="5e1b0-134">Kubernetes yönetilen küme adı.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="5e1b0-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="5e1b0-135">-NodeCount</span></span>
<span data-ttu-id="5e1b0-136">Düğüm havuzları için varsayılan düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="5e1b0-137">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="5e1b0-137">-NodeOsDiskSize</span></span>
<span data-ttu-id="5e1b0-138">Düğüm havuzları için varsayılan düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-138">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="5e1b0-139">-Edevmboyut</span><span class="sxs-lookup"><span data-stu-id="5e1b0-139">-NodeVmSize</span></span>
<span data-ttu-id="5e1b0-140">Sanal makinenin boyutu.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-140">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="5e1b0-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e1b0-141">-ResourceGroupName</span></span>
<span data-ttu-id="5e1b0-142">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-142">Resource Group Name.</span></span>

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

### <span data-ttu-id="5e1b0-143">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="5e1b0-143">-SshKeyValue</span></span>
<span data-ttu-id="5e1b0-144">SSH anahtar dosyası veya anahtar dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-144">SSH key file value or key file path.</span></span>
<span data-ttu-id="5e1b0-145">{HOME}/.ssh/id_rsa. pub varsayılan olur.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-145">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="5e1b0-146">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5e1b0-146">-Tag</span></span>
<span data-ttu-id="5e1b0-147">Kaynağa uygulanacak Etiketler</span><span class="sxs-lookup"><span data-stu-id="5e1b0-147">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="5e1b0-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="5e1b0-148">-Confirm</span></span>
<span data-ttu-id="5e1b0-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e1b0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e1b0-150">-WhatIf</span></span>
<span data-ttu-id="5e1b0-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e1b0-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e1b0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e1b0-153">CommonParameters</span></span>
<span data-ttu-id="5e1b0-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e1b0-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e1b0-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e1b0-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e1b0-156">INPUTS</span></span>

### <span data-ttu-id="5e1b0-157">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="5e1b0-157">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="5e1b0-158">System. String</span><span class="sxs-lookup"><span data-stu-id="5e1b0-158">System.String</span></span>

## <span data-ttu-id="5e1b0-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e1b0-159">OUTPUTS</span></span>

### <span data-ttu-id="5e1b0-160">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="5e1b0-160">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="5e1b0-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e1b0-161">NOTES</span></span>

## <span data-ttu-id="5e1b0-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e1b0-162">RELATED LINKS</span></span>
