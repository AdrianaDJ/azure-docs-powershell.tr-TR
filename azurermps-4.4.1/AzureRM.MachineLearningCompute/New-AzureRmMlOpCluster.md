---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: 222813dc78b4dd7c0118b8146a75ca4d225ce83c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592614"
---
# <span data-ttu-id="d8ede-101">New-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d8ede-101">New-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="d8ede-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8ede-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ede-103">Yeni bir operationalization kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8ede-103">Creates a new operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8ede-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8ede-104">SYNTAX</span></span>

### <span data-ttu-id="d8ede-105">Bir OperationalizationCluster örneği tanımından yeni bir operationalization kümesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d8ede-105">Create a new operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d8ede-106">Cmdlet Giriş parametrelerinden yeni bir operationalization kümesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d8ede-106">Create a new operationalization cluster from cmdlet input parameters.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <String>]
 [-Description <String>] [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-GlobalServiceConfigurationAdditionalProperties <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="d8ede-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8ede-107">DESCRIPTION</span></span>
<span data-ttu-id="d8ede-108">Yeni bir operationalization kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8ede-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="d8ede-109">Bu, bir küme nesnesi, gerekirse bir kapsayıcı hizmeti, Application Insights ve bir Azure kapsayıcısı kayıt defteri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8ede-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="d8ede-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8ede-110">EXAMPLES</span></span>

### <span data-ttu-id="d8ede-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d8ede-111">Example 1</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="d8ede-112">Azure Kapsayıcı Hizmeti ve Orchestrator olarak Kuberıtes içeren yeni bir operationalization kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8ede-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="d8ede-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d8ede-113">Example 2</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="d8ede-114">Yerel olarak yeni bir operationalization kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8ede-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="d8ede-115">Bu, bir Azure Kapsayıcı kayıt defteri, Application Insights ve depolama hesabı oluşturur, ancak kapsayıcı hizmeti oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="d8ede-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="d8ede-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8ede-116">PARAMETERS</span></span>

### <span data-ttu-id="d8ede-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="d8ede-117">-AgentCount</span></span>
<span data-ttu-id="d8ede-118">ACS kümesindeki aracı düğümlerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="d8ede-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="d8ede-119">-AgentVmSize</span></span>
<span data-ttu-id="d8ede-120">ACS kümesindeki aracı düğümlerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="d8ede-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d8ede-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="d8ede-122">Azure Kapsayıcı kayıt defterinin, oluşturmak yerine kullanması için URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="d8ede-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8ede-123">-InputObject</span></span>
<span data-ttu-id="d8ede-124">Operationalization kümesi özellikleri.</span><span class="sxs-lookup"><span data-stu-id="d8ede-124">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Create a new operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-125">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="d8ede-125">-ClusterType</span></span>
<span data-ttu-id="d8ede-126">Operationalization kümesi türü.</span><span class="sxs-lookup"><span data-stu-id="d8ede-126">The operationalization cluster type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="d8ede-127">-Confirm</span></span>
<span data-ttu-id="d8ede-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d8ede-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-129">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="d8ede-129">-Description</span></span>
<span data-ttu-id="d8ede-130">ACS kümesindeki ana düğümlerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="d8ede-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="d8ede-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="d8ede-132">Genel hizmet yapılandırması için ek özellikler.</span><span class="sxs-lookup"><span data-stu-id="d8ede-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="d8ede-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="d8ede-134">Güncelleştirmelerin yapılandırma ETag öğesi.</span><span class="sxs-lookup"><span data-stu-id="d8ede-134">The configuration ETag for updates.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-135">-Konum</span><span class="sxs-lookup"><span data-stu-id="d8ede-135">-Location</span></span>
<span data-ttu-id="d8ede-136">Operationalization kümesinin konumu.</span><span class="sxs-lookup"><span data-stu-id="d8ede-136">The operationalization cluster's location.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-137">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="d8ede-137">-MasterCount</span></span>
<span data-ttu-id="d8ede-138">ACS kümesindeki ana düğümlerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="d8ede-138">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8ede-139">-Name</span></span>
<span data-ttu-id="d8ede-140">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="d8ede-140">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-141">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="d8ede-141">-OrchestratorType</span></span>
<span data-ttu-id="d8ede-142">ACS kümesinin Orchestrator türü.</span><span class="sxs-lookup"><span data-stu-id="d8ede-142">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8ede-143">-ResourceGroupName</span></span>
<span data-ttu-id="d8ede-144">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d8ede-144">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-145">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="d8ede-145">-ClientId</span></span>
<span data-ttu-id="d8ede-146">ACS kümesinin Orchestrator Service Principal ID 'si.</span><span class="sxs-lookup"><span data-stu-id="d8ede-146">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-147">-Parola</span><span class="sxs-lookup"><span data-stu-id="d8ede-147">-Secret</span></span>
<span data-ttu-id="d8ede-148">ACS kümesinin Orchestrator hizmeti sorumlu parolası.</span><span class="sxs-lookup"><span data-stu-id="d8ede-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-149">-SslCName</span><span class="sxs-lookup"><span data-stu-id="d8ede-149">-SslCName</span></span>
<span data-ttu-id="d8ede-150">SSL sertifikası için CName.</span><span class="sxs-lookup"><span data-stu-id="d8ede-150">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-151">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="d8ede-151">-SslCertificate</span></span>
<span data-ttu-id="d8ede-152">Base64 dizesi olarak kodlanan PEM biçimindeki SSL sertifikası verileri.</span><span class="sxs-lookup"><span data-stu-id="d8ede-152">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="d8ede-153">-SslKey</span></span>
<span data-ttu-id="d8ede-154">Base64 dizesi olarak kodlanan PEM biçimindeki SSL anahtar verileri.</span><span class="sxs-lookup"><span data-stu-id="d8ede-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="d8ede-155">-SslStatus</span></span>
<span data-ttu-id="d8ede-156">SSL durumu.</span><span class="sxs-lookup"><span data-stu-id="d8ede-156">SSL status.</span></span>
<span data-ttu-id="d8ede-157">Olası değerler ' Enabled ' ve ' Disabled ' değerleridir.</span><span class="sxs-lookup"><span data-stu-id="d8ede-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d8ede-158">-StorageAccount</span></span>
<span data-ttu-id="d8ede-159">Bir tane oluşturmak yerine kullanılacak depolama hesabının URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="d8ede-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ede-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8ede-160">-WhatIf</span></span>
<span data-ttu-id="d8ede-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8ede-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8ede-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d8ede-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="d8ede-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8ede-163">INPUTS</span></span>

### <span data-ttu-id="d8ede-164">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d8ede-164">None</span></span>


## <span data-ttu-id="d8ede-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8ede-165">OUTPUTS</span></span>

### <span data-ttu-id="d8ede-166">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="d8ede-166">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>


## <span data-ttu-id="d8ede-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8ede-167">NOTES</span></span>

## <span data-ttu-id="d8ede-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8ede-168">RELATED LINKS</span></span>

