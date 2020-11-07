---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlOpCluster.md
ms.openlocfilehash: 51c8beb396bb0795fa77431a256ddc38e4e8df38
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915875"
---
# <span data-ttu-id="decc8-101">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="decc8-101">New-AzMlOpCluster</span></span>

## <span data-ttu-id="decc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="decc8-102">SYNOPSIS</span></span>
<span data-ttu-id="decc8-103">Yeni bir operationalization kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="decc8-103">Creates a new operationalization cluster.</span></span>

## <span data-ttu-id="decc8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="decc8-104">SYNTAX</span></span>

### <span data-ttu-id="decc8-105">CreateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="decc8-105">CreateWithInputObject</span></span>
```
New-AzMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="decc8-106">CreateWithParameters</span><span class="sxs-lookup"><span data-stu-id="decc8-106">CreateWithParameters</span></span>
```
New-AzMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ClientId <String>] [-Secret <String>] [-Description <String>]
 [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-DefaultProfile <IAzureContextContainer>] [-GlobalServiceConfigurationAdditionalProperties <Hashtable>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="decc8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="decc8-107">DESCRIPTION</span></span>
<span data-ttu-id="decc8-108">Yeni bir operationalization kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="decc8-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="decc8-109">Bu, bir küme nesnesi, gerekirse bir kapsayıcı hizmeti, Application Insights ve bir Azure kapsayıcısı kayıt defteri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="decc8-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="decc8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="decc8-110">EXAMPLES</span></span>

### <span data-ttu-id="decc8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="decc8-111">Example 1</span></span>
```
PS C:\> New-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="decc8-112">Azure Kapsayıcı Hizmeti ve Orchestrator olarak Kuberıtes içeren yeni bir operationalization kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="decc8-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="decc8-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="decc8-113">Example 2</span></span>
```
PS C:\> New-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="decc8-114">Yerel olarak yeni bir operationalization kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="decc8-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="decc8-115">Bu, bir Azure Kapsayıcı kayıt defteri, Application Insights ve depolama hesabı oluşturur, ancak kapsayıcı hizmeti oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="decc8-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="decc8-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="decc8-116">PARAMETERS</span></span>

### <span data-ttu-id="decc8-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="decc8-117">-AgentCount</span></span>
<span data-ttu-id="decc8-118">ACS kümesindeki aracı düğümlerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="decc8-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decc8-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="decc8-119">-AgentVmSize</span></span>
<span data-ttu-id="decc8-120">ACS kümesindeki aracı düğümlerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="decc8-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decc8-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="decc8-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="decc8-122">Azure Kapsayıcı kayıt defterinin, oluşturmak yerine kullanması için URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="decc8-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decc8-123">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="decc8-123">-ClientId</span></span>
<span data-ttu-id="decc8-124">ACS kümesinin Orchestrator Service Principal ID 'si.</span><span class="sxs-lookup"><span data-stu-id="decc8-124">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decc8-125">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="decc8-125">-ClusterType</span></span>
<span data-ttu-id="decc8-126">Operationalization kümesi türü.</span><span class="sxs-lookup"><span data-stu-id="decc8-126">The operationalization cluster type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decc8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="decc8-127">-DefaultProfile</span></span>
<span data-ttu-id="decc8-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="decc8-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="decc8-129">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="decc8-129">-Description</span></span>
<span data-ttu-id="decc8-130">ACS kümesindeki ana düğümlerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="decc8-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decc8-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="decc8-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="decc8-132">Genel hizmet yapılandırması için ek özellikler.</span><span class="sxs-lookup"><span data-stu-id="decc8-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decc8-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="decc8-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="decc8-134">Güncelleştirmelerin yapılandırma ETag öğesi.</span><span class="sxs-lookup"><span data-stu-id="decc8-134">The configuration ETag for updates.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decc8-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="decc8-135">-InputObject</span></span>
<span data-ttu-id="decc8-136">Operationalization kümesi özellikleri.</span><span class="sxs-lookup"><span data-stu-id="decc8-136">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: CreateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decc8-137">-Konum</span><span class="sxs-lookup"><span data-stu-id="decc8-137">-Location</span></span>
<span data-ttu-id="decc8-138">Operationalization kümesinin konumu.</span><span class="sxs-lookup"><span data-stu-id="decc8-138">The operationalization cluster's location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decc8-139">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="decc8-139">-MasterCount</span></span>
<span data-ttu-id="decc8-140">ACS kümesindeki ana düğümlerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="decc8-140">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decc8-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="decc8-141">-Name</span></span>
<span data-ttu-id="decc8-142">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="decc8-142">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="decc8-143">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="decc8-143">-OrchestratorType</span></span>
<span data-ttu-id="decc8-144">ACS kümesinin Orchestrator türü.</span><span class="sxs-lookup"><span data-stu-id="decc8-144">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decc8-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="decc8-145">-ResourceGroupName</span></span>
<span data-ttu-id="decc8-146">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="decc8-146">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="decc8-147">-Parola</span><span class="sxs-lookup"><span data-stu-id="decc8-147">-Secret</span></span>
<span data-ttu-id="decc8-148">ACS kümesinin Orchestrator hizmeti sorumlu parolası.</span><span class="sxs-lookup"><span data-stu-id="decc8-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decc8-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="decc8-149">-SslCertificate</span></span>
<span data-ttu-id="decc8-150">Base64 dizesi olarak kodlanan PEM biçimindeki SSL sertifikası verileri.</span><span class="sxs-lookup"><span data-stu-id="decc8-150">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decc8-151">-SslCName</span><span class="sxs-lookup"><span data-stu-id="decc8-151">-SslCName</span></span>
<span data-ttu-id="decc8-152">SSL sertifikası için CName.</span><span class="sxs-lookup"><span data-stu-id="decc8-152">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decc8-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="decc8-153">-SslKey</span></span>
<span data-ttu-id="decc8-154">Base64 dizesi olarak kodlanan PEM biçimindeki SSL anahtar verileri.</span><span class="sxs-lookup"><span data-stu-id="decc8-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decc8-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="decc8-155">-SslStatus</span></span>
<span data-ttu-id="decc8-156">SSL durumu.</span><span class="sxs-lookup"><span data-stu-id="decc8-156">SSL status.</span></span>
<span data-ttu-id="decc8-157">Olası değerler ' Enabled ' ve ' Disabled ' değerleridir.</span><span class="sxs-lookup"><span data-stu-id="decc8-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decc8-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="decc8-158">-StorageAccount</span></span>
<span data-ttu-id="decc8-159">Bir tane oluşturmak yerine kullanılacak depolama hesabının URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="decc8-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decc8-160">-Onay</span><span class="sxs-lookup"><span data-stu-id="decc8-160">-Confirm</span></span>
<span data-ttu-id="decc8-161">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="decc8-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="decc8-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="decc8-162">-WhatIf</span></span>
<span data-ttu-id="decc8-163">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="decc8-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="decc8-164">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="decc8-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="decc8-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="decc8-165">CommonParameters</span></span>
<span data-ttu-id="decc8-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="decc8-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="decc8-167">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="decc8-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="decc8-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="decc8-168">INPUTS</span></span>

### <span data-ttu-id="decc8-169">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="decc8-169">None</span></span>

## <span data-ttu-id="decc8-170">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="decc8-170">OUTPUTS</span></span>

### <span data-ttu-id="decc8-171">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="decc8-171">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="decc8-172">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="decc8-172">NOTES</span></span>

## <span data-ttu-id="decc8-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="decc8-173">RELATED LINKS</span></span>