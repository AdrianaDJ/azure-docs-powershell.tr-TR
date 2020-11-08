---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 715b6a52bc2f2a19dbfec3641d54752fe4321011
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107468"
---
# <span data-ttu-id="33ab2-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="33ab2-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="33ab2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33ab2-102">SYNOPSIS</span></span>
<span data-ttu-id="33ab2-103">Tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="33ab2-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="33ab2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="33ab2-104">SYNTAX</span></span>

### <span data-ttu-id="33ab2-105">Setbyıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="33ab2-105">SetByIntegrationRuntimeName (Default)</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33ab2-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="33ab2-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33ab2-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="33ab2-107">SetByParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33ab2-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="33ab2-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33ab2-109">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="33ab2-109">SetByResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33ab2-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="33ab2-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33ab2-111">Setbyıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="33ab2-111">SetByIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33ab2-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="33ab2-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33ab2-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="33ab2-113">DESCRIPTION</span></span>
<span data-ttu-id="33ab2-114">**Set-AzSynapseIntegrationRuntime** cmdlet 'i belirli parametrelerle tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="33ab2-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="33ab2-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="33ab2-115">EXAMPLES</span></span>

### <span data-ttu-id="33ab2-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="33ab2-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="33ab2-117">Cmdlet, ' test-Selfhost-IR ' adlı tümleştirme çalışma zamanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="33ab2-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="33ab2-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="33ab2-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="33ab2-119">Cmdlet, paylaşılan tümleştirme çalışma zamanını kullanmak için çalışma alanını ekler.</span><span class="sxs-lookup"><span data-stu-id="33ab2-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="33ab2-120">Parametre kullanılırken `-SharedIntegrationRuntimeResourceId` de eklenmelidir `-Type` .</span><span class="sxs-lookup"><span data-stu-id="33ab2-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="33ab2-121">Çalışma alanına cmdlet 'i çalıştırmadan önce tümleştirme çalışma zamanını kullanma izni verilmesi gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="33ab2-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="33ab2-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="33ab2-122">PARAMETERS</span></span>

### <span data-ttu-id="33ab2-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="33ab2-123">-AuthKey</span></span>
<span data-ttu-id="33ab2-124">Self-hosted Integration Runtime 'ın kimlik doğrulama anahtarı.</span><span class="sxs-lookup"><span data-stu-id="33ab2-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="33ab2-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="33ab2-126">Tümleştirme çalışma zamanının Katalog veritabanı yöneticisi kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="33ab2-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="33ab2-127">-CatalogPricingTier</span></span>
<span data-ttu-id="33ab2-128">Tümleştirme çalışma zamanının Katalog veritabanı fiyatlandırma katmanı.</span><span class="sxs-lookup"><span data-stu-id="33ab2-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="33ab2-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="33ab2-130">Tümleştirme çalışma zamanının Katalog veritabanı sunucusu uç noktası.</span><span class="sxs-lookup"><span data-stu-id="33ab2-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="33ab2-131">-DataFlowComputeType</span></span>
<span data-ttu-id="33ab2-132">Veri akışı işini yürütecek veri akışı kümesinin işlem türü.</span><span class="sxs-lookup"><span data-stu-id="33ab2-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="33ab2-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="33ab2-134">Veri akışı işini yürütecek veri akışı kümesinin çekirdek sayısı.</span><span class="sxs-lookup"><span data-stu-id="33ab2-134">Core count of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="33ab2-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="33ab2-136">Veri akışı işi yürütecek veri akışı kümesinin (dakika olarak) yaşam süresi.</span><span class="sxs-lookup"><span data-stu-id="33ab2-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-137">-Dataproxyıntegrationruntimename</span><span class="sxs-lookup"><span data-stu-id="33ab2-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="33ab2-138">Proxy olarak kullanılan Self-Hosted Integration Runtime adı.</span><span class="sxs-lookup"><span data-stu-id="33ab2-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="33ab2-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="33ab2-140">Self-Hosted ile Azure-SSIS tümleştirmesi çalışma zamanı arasında veri taşırken kullanılacak hazırlama veri deposuna başvuruda bulunan Azure Blob depolama bağlantılı hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="33ab2-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="33ab2-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="33ab2-142">Verileri Self-Hosted ile Azure-SSIS tümleştirmesi arasında taşırken kullanılacak hazırlama verileri deposundaki yol, belirtilmemişse varsayılan bir kapsayıcı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="33ab2-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33ab2-143">-DefaultProfile</span></span>
<span data-ttu-id="33ab2-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="33ab2-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33ab2-145">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="33ab2-145">-Description</span></span>
<span data-ttu-id="33ab2-146">Tümleştirme çalışma zamanı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="33ab2-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="33ab2-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="33ab2-147">-Edition</span></span>
<span data-ttu-id="33ab2-148">Standart veya kurumsal olabilecek SSIS tümleştirmesi çalışma zamanı modülü, belirtilmemişse varsayılan standart olur.</span><span class="sxs-lookup"><span data-stu-id="33ab2-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="33ab2-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="33ab2-150">Özel kurulum komut dosyası olmadan yapılandırmaları ve üçüncü taraf bileşenlerini ayarlamak için kullanılan SIS Integration Runtime için hızlı özel kurulum.</span><span class="sxs-lookup"><span data-stu-id="33ab2-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

```yaml
Type: System.Collections.ArrayList
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-151">-Force</span><span class="sxs-lookup"><span data-stu-id="33ab2-151">-Force</span></span>
<span data-ttu-id="33ab2-152">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="33ab2-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="33ab2-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33ab2-153">-InputObject</span></span>
<span data-ttu-id="33ab2-154">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="33ab2-154">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: SetByIntegrationRuntimeObject, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="33ab2-155">-LicenseType</span></span>
<span data-ttu-id="33ab2-156">SıR için seçmek istediğiniz lisans türü.</span><span class="sxs-lookup"><span data-stu-id="33ab2-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="33ab2-157">İki tür vardır: Licenseeklenmiş veya temel fiyat.</span><span class="sxs-lookup"><span data-stu-id="33ab2-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="33ab2-158">Azure Karma Kullanım Avantajı (AHUB) fiyatlandırması yeterliği Kazanmıyorsanız, lütfen temel fiyat seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="33ab2-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="33ab2-159">Yoksa, lütfen License'i seçin.</span><span class="sxs-lookup"><span data-stu-id="33ab2-159">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-160">-Konum</span><span class="sxs-lookup"><span data-stu-id="33ab2-160">-Location</span></span>
<span data-ttu-id="33ab2-161">Tümleştirme çalışma zamanı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="33ab2-161">The integration runtime description.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-162">-Maxparalellexecutionspernode</span><span class="sxs-lookup"><span data-stu-id="33ab2-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="33ab2-163">Yönetilen adanmış tümleştirme çalışma zamanının düğüm başına en yüksek paralel yürütme sayısı.</span><span class="sxs-lookup"><span data-stu-id="33ab2-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-164">-Ad</span><span class="sxs-lookup"><span data-stu-id="33ab2-164">-Name</span></span>
<span data-ttu-id="33ab2-165">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="33ab2-165">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName, SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="33ab2-166">-NodeCount</span></span>
<span data-ttu-id="33ab2-167">Tümleştirme çalışma zamanının hedef düğümler sayısı.</span><span class="sxs-lookup"><span data-stu-id="33ab2-167">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="33ab2-168">-NodeSize</span></span>
<span data-ttu-id="33ab2-169">Tümleştirme çalışma zamanı düğümü boyutu.</span><span class="sxs-lookup"><span data-stu-id="33ab2-169">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-170">-Publicıp</span><span class="sxs-lookup"><span data-stu-id="33ab2-170">-PublicIP</span></span>
<span data-ttu-id="33ab2-171">Tümleştirme çalışma zamanının kullanacağı statik genel IP adresleri.</span><span class="sxs-lookup"><span data-stu-id="33ab2-171">The static public IP addresses which the integration runtime will use.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: PublicIPs

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33ab2-172">-ResourceGroupName</span></span>
<span data-ttu-id="33ab2-173">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="33ab2-173">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-174">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="33ab2-174">-ResourceId</span></span>
<span data-ttu-id="33ab2-175">SYNAPSE tümleştirme çalışma zamanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="33ab2-175">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByLinkedIntegrationRuntimeResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="33ab2-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="33ab2-177">Özel kurulum betiğini içeren Azure Blob kapsayıcısının SAS URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="33ab2-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-178">-Sharedıntegrationruntimeresourceıd</span><span class="sxs-lookup"><span data-stu-id="33ab2-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="33ab2-179">Paylaşılan Self-hosted Integration Runtime 'ın kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="33ab2-179">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLinkedIntegrationRuntimeName, SetByLinkedIntegrationRuntimeParentObject, SetByLinkedIntegrationRuntimeResourceId, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-180">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="33ab2-180">-Subnet</span></span>
<span data-ttu-id="33ab2-181">VNet içindeki alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="33ab2-181">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-182">-Tür</span><span class="sxs-lookup"><span data-stu-id="33ab2-182">-Type</span></span>
<span data-ttu-id="33ab2-183">Tümleştirme çalışma zamanı türü.</span><span class="sxs-lookup"><span data-stu-id="33ab2-183">The integration runtime type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="33ab2-184">-VNetId</span></span>
<span data-ttu-id="33ab2-185">Tümleştirme çalışma zamanının katılacağı VNet KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="33ab2-185">The ID of the VNet which the integration runtime will join.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-186">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="33ab2-186">-WorkspaceName</span></span>
<span data-ttu-id="33ab2-187">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="33ab2-187">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-188">-</span><span class="sxs-lookup"><span data-stu-id="33ab2-188">-WorkspaceObject</span></span>
<span data-ttu-id="33ab2-189">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="33ab2-189">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33ab2-190">-Onay</span><span class="sxs-lookup"><span data-stu-id="33ab2-190">-Confirm</span></span>
<span data-ttu-id="33ab2-191">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="33ab2-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33ab2-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33ab2-192">-WhatIf</span></span>
<span data-ttu-id="33ab2-193">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="33ab2-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33ab2-194">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="33ab2-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33ab2-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33ab2-195">CommonParameters</span></span>
<span data-ttu-id="33ab2-196">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="33ab2-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33ab2-197">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="33ab2-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33ab2-198">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="33ab2-198">INPUTS</span></span>

### <span data-ttu-id="33ab2-199">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="33ab2-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="33ab2-200">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="33ab2-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="33ab2-201">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="33ab2-201">OUTPUTS</span></span>

### <span data-ttu-id="33ab2-202">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="33ab2-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="33ab2-203">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="33ab2-203">NOTES</span></span>

## <span data-ttu-id="33ab2-204">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="33ab2-204">RELATED LINKS</span></span>
