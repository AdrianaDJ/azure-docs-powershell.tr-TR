---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 2a6e20137f12ae9317c7eeed330a2433774e1ea9
ms.sourcegitcommit: 7df99dc139e93a8a4e6d5b1a27968857588d75dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2018
ms.locfileid: "40106907"
---
# <a name="release-notes"></a><span data-ttu-id="8d554-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="8d554-103">Release notes</span></span>

<span data-ttu-id="8d554-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="8d554-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="670---august-2018"></a><span data-ttu-id="8d554-105">6.7.0 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="8d554-105">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8d554-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8d554-106">AzureRM.Profile</span></span>
* <span data-ttu-id="8d554-107">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-107">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="8d554-108">Bağlam çakışmasını önlemek için varsayılan bağlam adına kullanıcı kimliği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-108">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="8d554-109">Bağlam #6398 seçerken sorunlara neden olan Clear-AzureRmContext ile ilgili sorunlar giderildi</span><span class="sxs-lookup"><span data-stu-id="8d554-109">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="8d554-110">'Connect-AzureRmAccount' için kiracı etki alanının '-TenantId' parametresine geçirilmesi etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-110">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="8d554-111">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="8d554-111">Azure.Storage</span></span>
* <span data-ttu-id="8d554-112">Azure Dosya Paylaşımı kotasındaki 5 TB'lık sınır kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8d554-112">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="8d554-113">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="8d554-113">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="8d554-114">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8d554-114">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="8d554-115">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-115">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="8d554-116">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8d554-116">Azure.AnalysisServices</span></span>
* <span data-ttu-id="8d554-117">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-117">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="8d554-118">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d554-118">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="8d554-119">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-119">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="8d554-120">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8d554-120">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="8d554-121">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-121">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="8d554-122">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="8d554-122">AzureRM.Automation</span></span>
* <span data-ttu-id="8d554-123">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-123">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="8d554-124">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="8d554-124">AzureRM.Backup</span></span>
* <span data-ttu-id="8d554-125">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-125">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="8d554-126">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="8d554-126">AzureRM.Batch</span></span>
* <span data-ttu-id="8d554-127">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-127">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="8d554-128">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="8d554-128">AzureRM.Billing</span></span>
* <span data-ttu-id="8d554-129">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-129">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="8d554-130">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d554-130">AzureRM.Cdn</span></span>
* <span data-ttu-id="8d554-131">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-131">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="8d554-132">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d554-132">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="8d554-133">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-133">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8d554-134">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8d554-134">AzureRM.Compute</span></span>
* <span data-ttu-id="8d554-135">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-135">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="8d554-136">New-AzureRmVmssConfig’e EvictionPolicy parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-136">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="8d554-137">Hiçbir konum belirtilmediyse New-AzureRmVm’nin DiskFileParameterSet parametresinde varsayılan konum kullanılıyor.</span><span class="sxs-lookup"><span data-stu-id="8d554-137">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="8d554-138">Save-AzureRmVMImage cmdlet'inde parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-138">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="8d554-139">Singlepass ile ilgili bazı senaryolarda Get-AzureRmVMDiskEncryptionStatus cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-139">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="8d554-140">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="8d554-140">AzureRM.Consumption</span></span>
* <span data-ttu-id="8d554-141">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-141">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="8d554-142">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8d554-142">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="8d554-143">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-143">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="8d554-144">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8d554-144">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="8d554-145">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-145">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="8d554-146">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="8d554-146">AzureRM.DataFactories</span></span>
* <span data-ttu-id="8d554-147">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-147">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="8d554-148">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8d554-148">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="8d554-149">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-149">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="8d554-150">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8d554-150">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="8d554-151">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-151">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8d554-152">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d554-152">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8d554-153">DebugPreference Powershell komut satırından ayarlandığında hata ayıklama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-153">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="8d554-154">Set-AzureRmDataLakeStoreItemAcl örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-154">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="8d554-155">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-155">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="8d554-156">Set-AzureRmDataLakeStoreItemAclEntry örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-156">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="8d554-157">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="8d554-157">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="8d554-158">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="8d554-159">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="8d554-159">AzureRM.Dns</span></span>
* <span data-ttu-id="8d554-160">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="8d554-161">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8d554-161">AzureRM.EventGrid</span></span>
* <span data-ttu-id="8d554-162">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="8d554-163">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d554-163">AzureRM.EventHub</span></span>
* <span data-ttu-id="8d554-164">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-164">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="8d554-165">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d554-165">AzureRM.HDInsight</span></span>
* <span data-ttu-id="8d554-166">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-166">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="8d554-167">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="8d554-167">AzureRM.Insights</span></span>
* <span data-ttu-id="8d554-168">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-168">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="8d554-169">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d554-169">AzureRM.IotHub</span></span>
* <span data-ttu-id="8d554-170">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8d554-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d554-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8d554-172">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="8d554-173">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8d554-173">AzureRM.LogicApp</span></span>
* <span data-ttu-id="8d554-174">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="8d554-175">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8d554-175">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="8d554-176">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="8d554-177">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="8d554-177">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="8d554-178">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="8d554-179">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8d554-179">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="8d554-180">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="8d554-181">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="8d554-181">AzureRM.Media</span></span>
* <span data-ttu-id="8d554-182">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-182">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8d554-183">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8d554-183">AzureRM.Network</span></span>
* <span data-ttu-id="8d554-184">Set-AzureRmLocalNetworkGateway örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-184">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="8d554-185">Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey ve New-AzureRmVirtualNetworkGatewayConnection için örnek ve açıklamalar eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-185">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8d554-186">Remove-AzureRmVirtualNetworkGatewayIpConfig ve Reset-AzureRmVirtualNetworkGateway örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-186">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="8d554-187">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-187">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="8d554-188">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-188">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="8d554-189">Set-AzureRmVirtualNetworkGatewayConnection örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-189">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8d554-190">ApplicationSecurityGroup, RouteTable ve Usage için en son kod oluşturucu kullanılarak cmdlet’ler yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="8d554-190">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="8d554-191">Varolmayan bir alt ağ alma girişiminde bulunulduğunda Get-AzureRmVirtualNetworkSubnetConfig cmdlet'inin hata iletisi netleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-191">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="8d554-192">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="8d554-192">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="8d554-193">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="8d554-194">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d554-194">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="8d554-195">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="8d554-196">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8d554-196">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="8d554-197">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="8d554-198">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8d554-198">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="8d554-199">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="8d554-200">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d554-200">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="8d554-201">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="8d554-202">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8d554-202">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8d554-203">Get-AzureRmRecoveryServicesBackItem cmdlet’ine ilke filtresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8d554-203">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="8d554-204">Komut, verilen ilke kimliği tarafından korunan yedekleme öğelerinin listesini döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="8d554-204">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="8d554-205">Microsoft.Azure.Management.RecoveryServices.Backup, sürüm 3.0.0 önizlemesine güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-205">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="8d554-206">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-206">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="8d554-207">Restore-AzureRmRecoveryServicesBackupItem’e TargetResourceGroupName parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8d554-207">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="8d554-208">Yönetilen disklerin geri yüklendiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="8d554-208">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="8d554-209">Yönetilen disklerle yapılan VM yedeklemesi için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="8d554-209">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="8d554-210">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8d554-210">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="8d554-211">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="8d554-212">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8d554-212">AzureRM.RedisCache</span></span>
* <span data-ttu-id="8d554-213">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="8d554-214">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="8d554-214">AzureRM.Relay</span></span>
* <span data-ttu-id="8d554-215">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8d554-216">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8d554-216">AzureRM.Resources</span></span>
* <span data-ttu-id="8d554-217">Abonelik kapsamındaki şablon dağıtımı destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="8d554-217">Support template deployment at subscription scope.</span></span> <span data-ttu-id="8d554-218">Yeni Cmdlet’ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="8d554-218">Add new Cmdlets:</span></span>
    - <span data-ttu-id="8d554-219">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8d554-219">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="8d554-220">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8d554-220">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="8d554-221">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8d554-221">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="8d554-222">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8d554-222">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="8d554-223">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8d554-223">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="8d554-224">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8d554-224">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="8d554-225">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8d554-225">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="8d554-226">Set-AzureRmResource’a bağlam geçirilirken hata oluşmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-226">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="8d554-227">New-AzureRmResourceGroupDeployment cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-227">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="8d554-228">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="8d554-229">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="8d554-229">AzureRM.Scheduler</span></span>
* <span data-ttu-id="8d554-230">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8d554-231">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d554-231">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8d554-232">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="8d554-233">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d554-233">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="8d554-234">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8d554-235">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8d554-235">AzureRM.Sql</span></span>
* <span data-ttu-id="8d554-236">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="8d554-237">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="8d554-237">AzureRM.Storage</span></span>
* <span data-ttu-id="8d554-238">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="8d554-239">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="8d554-239">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="8d554-240">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="8d554-241">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="8d554-241">AzureRM.Tags</span></span>
* <span data-ttu-id="8d554-242">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8d554-243">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8d554-243">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8d554-244">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="8d554-245">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="8d554-245">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="8d554-246">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8d554-247">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8d554-247">AzureRM.Websites</span></span>
* <span data-ttu-id="8d554-248">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="8d554-249">6.6.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="8d554-249">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8d554-250">Genel</span><span class="sxs-lookup"><span data-stu-id="8d554-250">General</span></span>
* <span data-ttu-id="8d554-251">Tüm yardım dosyaları tam parametre türleriyle doğru giriş/çıkış türlerini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-251">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="8d554-252">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8d554-252">AzureRM.Profile</span></span>
* <span data-ttu-id="8d554-253">Kaynağın geçerli yapılandırmasının hedef kaynakla uyumlu olduğunu doğrulayabilmek için Common.Strategy kitaplığı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-253">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="8d554-254">Common.Storage'a ps1xml türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-254">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="8d554-255">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="8d554-255">Azure.Storage</span></span>
* <span data-ttu-id="8d554-256">DefaultProfile’dan Depolama Bağlamı almak için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-256">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="8d554-257">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi.</span><span class="sxs-lookup"><span data-stu-id="8d554-257">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="8d554-258">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d554-258">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="8d554-259">https://github.com/Azure/azure-powershell/issues/6370 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-259">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="8d554-260">PsApiManagementApi'yi ApiContract'e çevirmek için Automapper hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-260">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="8d554-261">https://github.com/Azure/azure-powershell/issues/6515 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-261">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="8d554-262">Kodlama Türü ile aşırı yüklemeyi önlemek için File.Save hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-262">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="8d554-263">https://github.com/Azure/azure-powershell/issues/6560 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-263">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="8d554-264">apiId üzerindeki desen özel durumunu düzelten 4.0.3 Nuget sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-264">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8d554-265">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8d554-265">AzureRM.Compute</span></span>
* <span data-ttu-id="8d554-266">PremiumLRS depolama hesap türü yeniden adlandırması nedeniyle New-AzureRmVm'de DiskFileParameterSet kullanılarak sanal makine oluşturmanın başarısız olmasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-266">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="8d554-267">Invoke-AzureRmVMRunCommand cmdlet'i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-267">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="8d554-268">Abonelikteki tüm kullanılabilir kümelerin listelenebilmesi için Get-AzureRmAvailabilitySet güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-268">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="8d554-269">(ResouceGroupName parametresi artık isteğe bağlı.)</span><span class="sxs-lookup"><span data-stu-id="8d554-269">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="8d554-270">Uygun sanal makinelerde Hızlandırılmış Ağı etkinleştirmek için 'New-AzureRmVm' cmdlet'inin SimpleParameterSet öğesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-270">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="8d554-271">Kullanıcının belirttiği LB zaten mevcut olduğunda vmss oluşturmanın başarısız olması için New-AzureRmVmss basit parametre kümesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-271">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="8d554-272">New-AzureRmDisk örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-272">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="8d554-273">'New-AzureRmVM' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-273">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="8d554-274">Set-AzureRmVMOSDisk açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-274">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="8d554-275">Yazımı ve ön eki düzeltmek amacıyla Set-AzureRmVMBginfoExtension için Örnek 1 güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-275">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="8d554-276">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8d554-276">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="8d554-277">ADF .Net SDK sürümü 1.1.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-277">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="8d554-278">Veri fabrikaları arasında paylaşılan şirket içinde barındırılan tümleştirme çalışma zamanı desteği.</span><span class="sxs-lookup"><span data-stu-id="8d554-278">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="8d554-279">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine yeni -SharedIntegrationRuntimeResourceId parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8d554-279">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="8d554-280">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine isteğe bağlı yeni -LinkedDataFactoryName parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8d554-280">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8d554-281">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d554-281">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8d554-282">DataPlane SDK'sı (Microsoft.Azure.DataLake.Store) sürümü 1.1.9'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-282">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="8d554-283">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d554-283">AzureRM.EventHub</span></span>
* <span data-ttu-id="8d554-284">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-284">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="8d554-285">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="8d554-285">AzureRM.Insights</span></span>
* <span data-ttu-id="8d554-286">Yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-286">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="8d554-287">Microsoft.Azure.Management.Monitor SDK 0.19.1-preview kullanımı</span><span class="sxs-lookup"><span data-stu-id="8d554-287">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8d554-288">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d554-288">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8d554-289">Set-AzureRmKeyVaultAccessPolicy'de yönlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-289">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8d554-290">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8d554-290">AzureRM.Network</span></span>
* <span data-ttu-id="8d554-291">LoadBalancerInboundNatPoolConfig cmdlet'leri için örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="8d554-291">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8d554-292">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8d554-292">AzureRM.Resources</span></span>
* <span data-ttu-id="8d554-293">'Get-AzureRmResource' için hem etiket adı hem de değer sağlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-293">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="8d554-294">'Set-AzureRmResource' için yönlendirme senaryosu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-294">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8d554-295">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d554-295">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8d554-296">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-296">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="8d554-297">birkaç sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-297">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="8d554-298">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8d554-298">AzureRM.Sql</span></span>
* <span data-ttu-id="8d554-299">Aşağıdaki cmdlet'lere Sunucu Gelişmiş Tehdit Koruması desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="8d554-299">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="8d554-300">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d554-300">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="8d554-301">Aşağıdaki cmdlet'lere Güvenlik Açığı Değerlendirme desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="8d554-301">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="8d554-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="8d554-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="8d554-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="8d554-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="8d554-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="8d554-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="8d554-305">Remove-AzureRmSqlServerFirewallRulecmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-305">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="8d554-306">Get-AzureSqlSyncGroupLog içinde ABD temelli olmayan kültürde yanlış tarih saat işlemesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-306">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="8d554-307">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="8d554-307">AzureRM.Storage</span></span>
* <span data-ttu-id="8d554-308">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-308">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="8d554-309">Tablo görünümünde StorageAccount cmdlet'i çıkışı gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="8d554-309">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="8d554-310">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d554-310">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="8d554-311">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d554-311">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="8d554-312">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d554-312">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="8d554-313">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="8d554-313">AzureRM.Tags</span></span>
* <span data-ttu-id="8d554-314">Tag cmdlet'inin yardımında hatayı deyim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8d554-314">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="8d554-315">6.5.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="8d554-315">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8d554-316">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8d554-316">AzureRM.Profile</span></span>
* <span data-ttu-id="8d554-317">'Get-AzureRmContextAutosaveSetting' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-317">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="8d554-318">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="8d554-318">Azure.Storage</span></span>
* <span data-ttu-id="8d554-319">Salt yazılır Sas belirteciyle Karşıya Yükleme Blobu veya Dosyası desteği</span><span class="sxs-lookup"><span data-stu-id="8d554-319">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="8d554-320">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8d554-320">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="8d554-321">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8d554-321">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="8d554-322">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8d554-322">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="8d554-323">AS'ye gerekli ResourceGroupName özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="8d554-323">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="8d554-324">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="8d554-324">AzureRM.Automation</span></span>
* <span data-ttu-id="8d554-325">'New-AzureRMAutomationSchedule' için yardım güncelleştirildi ve örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-325">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8d554-326">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8d554-326">AzureRM.Compute</span></span>
* <span data-ttu-id="8d554-327">Update/New-AzureRmAvailabilitySet komutlarına -Tag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-327">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="8d554-328">'Add-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-328">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="8d554-329">'Remove-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-329">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="8d554-330">'Set-AzureRmVMAccessExtension' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-330">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="8d554-331">New-AzureRmVmss için SimpleParameterSet güncelleştirilerek SinglePlacementGroup varsayılan olarak false değerine ayarlandı ve kullanıcının tek yerleşim grubunda VMSS oluşturmasına olanak tanıyan 'SinglePlacementGroup' geçiş parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8d554-331">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="8d554-332">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d554-332">AzureRM.EventHub</span></span>
* <span data-ttu-id="8d554-333">PSEventHubDRConfigurationAttributes sınıfına, çoğaltma işlemi devam ederken bekleyen çoğaltma işlemlerinin sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-333">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8d554-334">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d554-334">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8d554-335">Set-AzureRmKeyVaultAccessPolicy için hata iletisi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-335">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="8d554-336">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8d554-336">AzureRM.LogicApp</span></span>
* <span data-ttu-id="8d554-337">New-AzureRmLogicApp’te "parametre kümesi çözümlenemedi" hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-337">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8d554-338">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8d554-338">AzureRM.Network</span></span>
* <span data-ttu-id="8d554-339">Set/Add-AzureRmVirtualNetworkPeering için birden çok Kiracıdaki Sanal Makineler arasında eşleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-339">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="8d554-340">Aşağıdaki cmdlet’ler Application Gateway için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-340">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="8d554-341">New-AzureRmApplicationGateway : EnableFIPS bayrağı ve Zones desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-341">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="8d554-342">New-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-342">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="8d554-343">Set-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-343">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="8d554-344">RouteTable cmdlet’leri en son oluşturucu sürümüyle yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="8d554-344">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="8d554-345">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="8d554-345">AzureRM.Relay</span></span>
* <span data-ttu-id="8d554-346">Markdown dosyaları güncelleştirildi, örnekteki parametre adı sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="8d554-346">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8d554-347">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8d554-347">AzureRM.Resources</span></span>
* <span data-ttu-id="8d554-348">Roleassignment ve roledefinition cmdlet’leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="8d554-348">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="8d554-349">Disk belleğinin parçası olarak yapılan ek roledefinition çağrıları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8d554-349">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="8d554-350">Get-AzureRmRoleAssignment cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-350">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="8d554-351">-ExpandPrincipalGroups komut parametresi işlevselliği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-351">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="8d554-352">'-ResourceType' parametresinin büyük/küçük harfe duyarlı olduğu 'Get-AzureRmResource' sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-352">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8d554-353">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d554-353">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8d554-354">Liste cmdlet’lerine top ve skip parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-354">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="8d554-355">Standard'dan Premium NameSpace'e geçiş cmdlet’leri eklendi :</span><span class="sxs-lookup"><span data-stu-id="8d554-355">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="8d554-356">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8d554-356">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8d554-357">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8d554-357">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8d554-358">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8d554-358">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8d554-359">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8d554-359">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8d554-360">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8d554-360">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="8d554-361">PSServiceBusDRConfigurationAttributes sınıfına, çoğaltma işlemi sürerken beklemede olan çoğaltma işlemi sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-361">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="8d554-362">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d554-362">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="8d554-363">'New-AzureRmServiceFabricCluster' için örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-363">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8d554-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8d554-364">AzureRM.Sql</span></span>
* <span data-ttu-id="8d554-365">Müşterilerin Sql Server örneğine veya Yönetilen Örneğe TDE Sertifikası ekleyebilmeleri için yeni Management.Sql Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-365">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="8d554-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="8d554-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="8d554-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="8d554-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8d554-368">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8d554-368">AzureRM.Websites</span></span>
* <span data-ttu-id="8d554-369">Artık `Set-AzureRmWebApp -AssignIdentity` ve `Set-AzureRmWebAppSlot -AssignIdentity` false olarak ayarlandığında site object.Removing önizleme etiketinden Identity özelliğini kaldırıyor.</span><span class="sxs-lookup"><span data-stu-id="8d554-369">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="8d554-370">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-370">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="8d554-371">`Set-AzureRmWebApp -PhpVersion` geçerli bir php sürümü off değerini destekliyor</span><span class="sxs-lookup"><span data-stu-id="8d554-371">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="8d554-372">6.4.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="8d554-372">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8d554-373">Genel</span><span class="sxs-lookup"><span data-stu-id="8d554-373">General</span></span>
* <span data-ttu-id="8d554-374">Modüllerin çoğu için yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-374">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="8d554-375">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8d554-375">AzureRM.Profile</span></span>
* <span data-ttu-id="8d554-376">Temel çıkış türlerine Ps1Xml özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-376">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8d554-377">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8d554-377">AzureRM.Compute</span></span>
* <span data-ttu-id="8d554-378">VMSS için IP Etiketi özelliği</span><span class="sxs-lookup"><span data-stu-id="8d554-378">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="8d554-379">'New-AzureRmVmssIpTagConfig' cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-379">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="8d554-380">New-AzureRmVmssIpConfig cmdlet'ine IpTag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-380">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="8d554-381">VMSS için Otomatik İşletim Sistemi Geri Alma özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-381">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="8d554-382">New-AzureRmVmssConfig ve Update-AzureRmVmss cmdlet'lerine DisableAutoRollback parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-382">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="8d554-383">VMSS için İşletim Sistemi Yükseltme Geçmişi özelliği</span><span class="sxs-lookup"><span data-stu-id="8d554-383">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="8d554-384">Get-AzureRmVmss cmdlet'ine OSUpgradeHistory anahtarı parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-384">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="8d554-385">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8d554-385">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="8d554-386">Aşağıdaki komutlarla Katalog ACL'si için destek eklendi:</span><span class="sxs-lookup"><span data-stu-id="8d554-386">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="8d554-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8d554-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="8d554-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8d554-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="8d554-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8d554-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8d554-390">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d554-390">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8d554-391">Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry ve Set-AzureRmDataLakeStoreItemAcl için iptal desteği ve ilerleme izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-391">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="8d554-392">Export-AzureRmDataLakeStoreChildItemProperties için iptal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-392">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="8d554-393">Özyinelemeli işlemler gerçekleştiren cmdlet'ler için hata ayıklama iletilerinin boşaltılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-393">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="8d554-394">DataLake cmdlet'lerinin test konumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-394">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="8d554-395">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d554-395">AzureRM.EventHub</span></span>
* <span data-ttu-id="8d554-396">Get-AzureRmEventHub ve Get-AzureRmEventHubConsumerGroup Listeleme İşlemleri cmdlet'lerine İsteğe Bağlı MaxCount parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-396">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="8d554-397">New-AzureRmEventHub cmdlet'inde yeni Olay Hub'ı oluşturma sırasında en az bir parametreye ihtiyaç duyma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-397">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="8d554-398">Varsayılan Parametre kümesi sağlandı.</span><span class="sxs-lookup"><span data-stu-id="8d554-398">Provided Default Parameter set.</span></span>
* <span data-ttu-id="8d554-399">Kullanıcının New-AzureRmEventHubKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8d554-399">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8d554-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d554-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8d554-401">Get-AzureRmKeyVault -Tag ile tüm kaynakların döndürülmesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-401">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8d554-402">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8d554-402">AzureRM.Network</span></span>
* <span data-ttu-id="8d554-403">Zone-Redundant VirtualNetworkGateways için yeni SKU'lar kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="8d554-403">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="8d554-404">ARM aracılığıyla ExpressRoute Partner API'leri özelliği için yeni komutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-404">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="8d554-405">Get-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-405">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="8d554-406">Set-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-406">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="8d554-407">Add-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-407">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="8d554-408">Get-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-408">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="8d554-409">Remove-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-409">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="8d554-410">Get-AzureRMExpressRouteCrossConnectionArpTable eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-410">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="8d554-411">Get-AzureRMExpressRouteCrossConnectionRouteTable eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-411">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="8d554-412">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-412">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="8d554-413">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8d554-413">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8d554-414">Get-AzureRmRecoveryServicesBackupStatus cmdlet'i eklendi.</span><span class="sxs-lookup"><span data-stu-id="8d554-414">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="8d554-415">Bu cmdlet bir sanal makinenin kimliğini alır ve sanal makinenin abonelik içindeki kasaların koruması altında olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="8d554-415">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="8d554-416">Böyle bir kasa varsa cmdlet, bu kasanın ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d554-416">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8d554-417">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8d554-417">AzureRM.Resources</span></span>
* <span data-ttu-id="8d554-418">Get-AzureRmPolicyAssignment cmdlet'leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="8d554-418">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="8d554-419">Yönetim grubu düzeyinde -Scope değerlerini listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-419">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="8d554-420">Yönetim grubu düzeyinde -Scope değerlerine sahip olan tek atamaları alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-420">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="8d554-421">control parametresine -Effective ve -All anahtarları eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-421">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="8d554-422">Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-422">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="8d554-423">Belirli bir yönetim grubuna işlem uygulamayı sağlayan için -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-423">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="8d554-424">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-424">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="8d554-425">Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-425">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="8d554-426">Belirli bir yönetim grubuna işlem uygulamayı sağlayan -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-426">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="8d554-427">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-427">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="8d554-428">'New-AzureRmResourceGroupDeployment' içinde 'TemplateParameterObject' kullanırken parametrelerde KeyVault gizli dizi başvurusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-428">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="8d554-429">'New-AzureRmADAppCredential' için '-EndDate' parametresinin yoksayılmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-429">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="8d554-430">'Add-AzureRmADGroupMember' cmdlet'inin istekte bulunmak için yanlış URL'yi kullandığı sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-430">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="8d554-431">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d554-431">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8d554-432">Kullanıcının New-AzureRmServiceBusKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8d554-432">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8d554-433">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8d554-433">AzureRM.Sql</span></span>
* <span data-ttu-id="8d554-434">New-AzureRmSqlDatabaseRestorePoint yardımında Kullanıcı Tanımlı Geri Yükleme Noktaları netleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-434">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="8d554-435">Birden fazla cmdlet'te -ComputeGeneration parametresinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-435">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="8d554-436">6.3.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="8d554-436">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8d554-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8d554-437">AzureRM.Profile</span></span>
* <span data-ttu-id="8d554-438">Enable-AzureRmContextAutoSave için hata iletileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-438">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="8d554-439">'Connect-AzureRmAccount' cmdlet'i eski bir bağlam olmadan çalıştırıldığında her abonelik için bir bağlam oluşturur</span><span class="sxs-lookup"><span data-stu-id="8d554-439">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="8d554-440">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="8d554-440">Azure.Storage</span></span>
* <span data-ttu-id="8d554-441">Yardım dosyalarına -Permissions parametresi hakkında daha fazla bilgi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8d554-441">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8d554-442">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8d554-442">AzureRM.Compute</span></span>
* <span data-ttu-id="8d554-443">'Get-AzureRmVmDiskEncryptionStatus' için veri diski bulunmayan VM'lerde karşılaşılan bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-443">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="8d554-444">Aşağıdaki cmdlet'leri düzeltmek için bilgisayar istemci kitaplığı sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-444">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="8d554-445">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8d554-445">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="8d554-446">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="8d554-446">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="8d554-447">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8d554-447">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="8d554-448">Aşağıdaki cmdlet'ler 'operation ID' ve 'operation status' bilgilerini doğru gösterecek şekilde düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="8d554-448">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="8d554-449">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8d554-449">Start-AzureRmVM</span></span>
    - <span data-ttu-id="8d554-450">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8d554-450">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="8d554-451">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8d554-451">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="8d554-452">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8d554-452">Set-AzureRmVM</span></span>
    - <span data-ttu-id="8d554-453">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8d554-453">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="8d554-454">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8d554-454">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="8d554-455">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="8d554-455">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="8d554-456">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="8d554-456">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="8d554-457">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8d554-457">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="8d554-458">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8d554-458">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="8d554-459">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8d554-459">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="8d554-460">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8d554-460">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="8d554-461">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="8d554-461">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="8d554-462">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="8d554-462">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="8d554-463">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="8d554-463">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="8d554-464">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8d554-464">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="8d554-465">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="8d554-465">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="8d554-466">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="8d554-466">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="8d554-467">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8d554-467">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="8d554-468">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8d554-468">AzureRM.EventGrid</span></span>
* <span data-ttu-id="8d554-469">Gerekli olması halinde parametrelerin boş dizeyle değiştirilmesine izin vermek için Update-AzureRmEventGridSubscription cmdlet'i içindeki SubjectBeginsWith/SubjectEndsWith için ValidateNotNullOrEmpty doğrulama koşulları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8d554-469">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8d554-470">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d554-470">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8d554-471">Get-AzureRmKeyVault -Tag çalıştırıldığında etiket döndürülmeme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-471">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="8d554-472">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8d554-472">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="8d554-473">Policy Insights cmdlet'leri genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="8d554-473">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="8d554-474">API 2018-04-04 sürümünü kullanın</span><span class="sxs-lookup"><span data-stu-id="8d554-474">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="8d554-475">PolicyDefinitionReferenceId, Get-AzureRmPolicyStateSummary sonuçlarına eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-475">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="8d554-476">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8d554-476">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8d554-477">RecoveryServices.Backup cmdlet'lerine -Vault parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8d554-477">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="8d554-478">Bu parametre iletildiğinde Set-AzureRmRecoveryServicesContext cmdlet'ini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="8d554-478">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8d554-479">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8d554-479">AzureRM.Sql</span></span>
* <span data-ttu-id="8d554-480">Yardım dosyasındaki Get-AzureRmSqlDatabaseExpanded örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-480">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8d554-481">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8d554-481">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8d554-482">Yardım dosyasındaki Add-AzureRmTrafficManagerEndpointConfig bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-482">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8d554-483">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8d554-483">AzureRM.Websites</span></span>
* <span data-ttu-id="8d554-484">'Set-AzureRmWebApp', -AssignIdentity kullanıldığında AppSettings verilerini geçersiz kılmayacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-484">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="8d554-485">'New-AzureRmWebAppSlot', isteğe bağlı parametre olarak AppServicePlan girişini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-485">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="8d554-486">6.2.1 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="8d554-486">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="8d554-487">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d554-487">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="8d554-488">PSWorkspace modeli Network için tür parametresini kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-488">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="8d554-489">6.2.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="8d554-489">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8d554-490">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8d554-490">AzureRM.Profile</span></span>
* <span data-ttu-id="8d554-491">Modülün içeri aktarılması sırasında Newtonsoft.Json 10.0.3 sürümünün yüklenmemesine ilişkin sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-491">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8d554-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8d554-492">AzureRM.Compute</span></span>
* <span data-ttu-id="8d554-493">VMSS VM Güncelleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="8d554-493">VMSS VM Update feature</span></span>
    - <span data-ttu-id="8d554-494">'Update-AzureRmVmssVM' ve 'New-AzureRmVMDataDisk' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-494">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="8d554-495">VMSS VM’sine veri diski eklemeyi desteklemek için 'Add-AzureRmVMDataDisk' cmdlet’ine VirtualMachineScaleSetVM parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8d554-495">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="8d554-496">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8d554-496">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="8d554-497">ADF .Net SDK sürümü, aşağıdaki değişiklikleri içeren 0.8.0-preview sürümüne güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="8d554-497">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="8d554-498">Fabrika deposunu yapılandırma işlemi eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-498">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="8d554-499">QuickBooks LinkedService, consumerKey ve consumerSecret özelliklerini kullanıma sunmak üzere güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-499">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="8d554-500">SecretBase’ten Object’e birkaç model türü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-500">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="8d554-501">Blob Etkinliklerini tetikleme eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-501">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="8d554-502">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d554-502">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8d554-503">Belgeler örnek çıktı ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-503">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="8d554-504">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8d554-504">AzureRM.Network</span></span>
* <span data-ttu-id="8d554-505">Ağ İzleyicisi cmdlet’leri üzerindeki Trafik Analizi parametreleri etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-505">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8d554-506">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8d554-506">AzureRM.Resources</span></span>
* <span data-ttu-id="8d554-507">'Get-AzureRmResource' cmdlet’inden döndürülen 'PSResource' nesnesinin 'Properties' özelliğiyle ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-507">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="8d554-508">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="8d554-508">AzureRM.Scheduler</span></span>
* <span data-ttu-id="8d554-509">Güncelleştirilen ServiceBusQueueJob’ın yeni Kimlik Doğrulaması değerlerini ayarlamamasıyla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-509">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="8d554-510">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8d554-510">AzureRM.Sql</span></span>
* <span data-ttu-id="8d554-511">Şu cmdlet’ler isteğe bağlı LicenseType parametresiyle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="8d554-511">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="8d554-512">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8d554-512">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="8d554-513">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8d554-513">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="8d554-514">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8d554-514">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="8d554-515">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8d554-515">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="8d554-516">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8d554-516">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8d554-517">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8d554-517">AzureRM.Websites</span></span>
* <span data-ttu-id="8d554-518">'New-AzureRMWebApp' Strategy kütüphanesindeki ortak algoritmaları kullanmak üzere güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-518">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="8d554-519">6.1.0 - Mayıs 2018</span><span class="sxs-lookup"><span data-stu-id="8d554-519">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8d554-520">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8d554-520">AzureRM.Profile</span></span>
* <span data-ttu-id="8d554-521">'Clear-AzureRmContext' komutunun çalıştırılmasının boş bir bağlamı önceki varsayılan bağlamın adıyla tutmasına ve böylece kullanıcının eski ad ile yeni bir bağlam oluşturamadığı bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8d554-521">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="8d554-522">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8d554-522">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="8d554-523">AS’de Ağ geçidi ilişkilendirme/ilişkilendirme kaldırma işlemlerini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="8d554-523">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="8d554-524">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d554-524">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="8d554-525">ApiVersions, ApiReleases ve ApiRevisions desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-525">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="8d554-526">ServiceFabric Arka Ucu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-526">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="8d554-527">Application Insights Günlükçüsü desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-527">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="8d554-528">‘Temel’ sku’yu Api Yönetim hizmetinin geçerli sku’su olarak algılama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-528">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="8d554-529">Özel CA tarafından Kök veya CA olarak yayınlanan Sertifikaları yükleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-529">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="8d554-530">Özel SSL sertifikalarını KeyVault ve Çoklu ara sunucu ana bilgisayar adlarıyla kabul etme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-530">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="8d554-531">MSI kimliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-531">Added support for MSI identity</span></span>
* <span data-ttu-id="8d554-532">İlkeleri Url ile kabul etme desteği eklendi NOT: Aşağıdaki cmdlet’ler gelecekteki sürümlerde kullanım dışı kalacaktır</span><span class="sxs-lookup"><span data-stu-id="8d554-532">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="8d554-533">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="8d554-533">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="8d554-534">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d554-534">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="8d554-535">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="8d554-535">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="8d554-536">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="8d554-536">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="8d554-537">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="8d554-537">AzureRM.Batch</span></span>
* <span data-ttu-id="8d554-538">Yeni Get-AzureBatchPoolNodeCounts cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="8d554-538">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="8d554-539">Yeni AzureBatchComputeNodeServiceLogUpload cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="8d554-539">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="8d554-540">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="8d554-540">AzureRM.Consumption</span></span>
* <span data-ttu-id="8d554-541">Get-AzureRmConsumptionUsageDetail cmdlet’inde yeni Expand, ResourceGroup, InstanceName, InstanceId, Tags ve Top parametrelerini ekleme</span><span class="sxs-lookup"><span data-stu-id="8d554-541">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8d554-542">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d554-542">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8d554-543">Export-AzureRmDataLakeStoreChildItemProperties için düzeltme örneği</span><span class="sxs-lookup"><span data-stu-id="8d554-543">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="8d554-544">Set-AzureRmDataLakeStoreItemAclEntry komutunda Özyineleme durumu için null parametresi özel durumunu düzeltme</span><span class="sxs-lookup"><span data-stu-id="8d554-544">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="8d554-545">Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry’ye yönelik yardım dosyalarını düzeltme</span><span class="sxs-lookup"><span data-stu-id="8d554-545">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="8d554-546">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8d554-546">AzureRM.Network</span></span>
* <span data-ttu-id="8d554-547">Ağ SDK sürümünü 18.0.0-önizleme’den 19.0.0-önizlemeye yükseltme</span><span class="sxs-lookup"><span data-stu-id="8d554-547">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="8d554-548">Protokol yapılandırması oluşturma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-548">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="8d554-549">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d554-549">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="8d554-550">Varolan express route bağlantı hattına yeni bir bağlantı hattı ekleme cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="8d554-550">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="8d554-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8d554-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="8d554-552">Varolan express route bağlantı hattındaki bir bağlantı hattı bağlantısını kaldırma cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="8d554-552">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="8d554-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8d554-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="8d554-554">Bağlantı hattı bağlantısı alma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="8d554-554">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="8d554-555">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8d554-555">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="8d554-556">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d554-556">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="8d554-557">Oluşturulan sertifikalarla sunucu kimlik doğrulaması kullanımı düzeltildi (Sorun No. 5998)</span><span class="sxs-lookup"><span data-stu-id="8d554-557">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8d554-558">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8d554-558">AzureRM.Sql</span></span>
* <span data-ttu-id="8d554-559">AuditActions veya AuditActionGroups’un kaldırılmasını sağlamak üzere Denetim cmdlet’leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8d554-559">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="8d554-560">Yeni bir esnek saklama ilkesi ayarlarken komutun ‘Azure kurtarma hizmeti kasası ve ilkesiyle uzun süreli saklama ilkesini yapılandırma artık desteklenmiyor. Lütfen yeni esnek saklama ilkesi ile istek gönderin’ hatasını verdiği Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d554-560">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="8d554-561">komutuna ilişkin sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8d554-561">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="8d554-562">Ölçek ve katman ilişkili özelliklere yönelik Sku özelliğini destekleyen yeni Veritabanı API’sini kullanmak için tüm Azure Sql Database/ElasticPool Creation/Update cmdlet’lerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="8d554-562">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="8d554-563">Güncelleştirilen cmlet’ler arasında şunlar yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="8d554-563">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="8d554-564">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8d554-564">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="8d554-565">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8d554-565">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="8d554-566">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8d554-566">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="8d554-567">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8d554-567">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="8d554-568">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8d554-568">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8d554-569">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8d554-569">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8d554-570">-Name parametresini kullanırken -ResourceGroupName parametresinin gerekli olması için 'Get-AzureRmTrafficManagerProfile'a yönelik parametreleri güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="8d554-570">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
