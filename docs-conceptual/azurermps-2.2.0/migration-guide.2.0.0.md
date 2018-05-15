# <a name="table-of-contents"></a><span data-ttu-id="a792e-101">İçindekiler</span><span class="sxs-lookup"><span data-stu-id="a792e-101">Table of Contents</span></span>
1. [<span data-ttu-id="a792e-102">Force parametrelerinin kaldırılması</span><span class="sxs-lookup"><span data-stu-id="a792e-102">Removal of Force parameters</span></span>](#removal-of-force-parameters)
2. [<span data-ttu-id="a792e-103">Tag parametrelerinin değiştirilmesi</span><span class="sxs-lookup"><span data-stu-id="a792e-103">Change of Tag parameters</span></span>](#change-of-tag-parameters)
3. [<span data-ttu-id="a792e-104">Depolama cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="a792e-104">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
4. [<span data-ttu-id="a792e-105">AD cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="a792e-105">Breaking changes to AD cmdlets</span></span>](#breaking-changes-to-ad-cmdlets)

## <a name="removal-of-force-parameters"></a><span data-ttu-id="a792e-106">Force parametrelerinin kaldırılması</span><span class="sxs-lookup"><span data-stu-id="a792e-106">Removal of Force parameters</span></span>

<span data-ttu-id="a792e-107">Bu sürümde, cmdlet’lerden tüm Eski `Force` parametrelerini ve parametrelerin gelecekteki bir sürümde kaldırılacağına ilişkin uyarıları kaldırdık.</span><span class="sxs-lookup"><span data-stu-id="a792e-107">This release, we removed all Obsolete `Force` parameters from cmdlets and the corresponding warnings that the parameter would be removed in a future release.</span></span>

<span data-ttu-id="a792e-108">Bu değişiklikten aşağıdaki cmdlet’ler etkilenir:</span><span class="sxs-lookup"><span data-stu-id="a792e-108">The following cmdlets are affected by this change:</span></span>

<span data-ttu-id="a792e-109">**ApiManagement**</span><span class="sxs-lookup"><span data-stu-id="a792e-109">**ApiManagement**</span></span>
- <span data-ttu-id="a792e-110">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="a792e-110">Remove-AzureRmApiManagement</span></span>
- <span data-ttu-id="a792e-111">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a792e-111">Remove-AzureRmApiManagementApi</span></span>
- <span data-ttu-id="a792e-112">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a792e-112">Remove-AzureRmApiManagementGroup</span></span>
- <span data-ttu-id="a792e-113">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a792e-113">Remove-AzureRmApiManagementLogger</span></span>
- <span data-ttu-id="a792e-114">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a792e-114">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>
- <span data-ttu-id="a792e-115">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a792e-115">Remove-AzureRmApiManagementOperation</span></span>
- <span data-ttu-id="a792e-116">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a792e-116">Remove-AzureRmApiManagementPolicy</span></span>
- <span data-ttu-id="a792e-117">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a792e-117">Remove-AzureRmApiManagementProduct</span></span>
- <span data-ttu-id="a792e-118">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="a792e-118">Remove-AzureRmApiManagementProperty</span></span>
- <span data-ttu-id="a792e-119">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a792e-119">Remove-AzureRmApiManagementSubscription</span></span>
- <span data-ttu-id="a792e-120">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a792e-120">Remove-AzureRmApiManagementUser</span></span>

<span data-ttu-id="a792e-121">**Otomasyon**</span><span class="sxs-lookup"><span data-stu-id="a792e-121">**Automation**</span></span>
- <span data-ttu-id="a792e-122">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a792e-122">Remove-AzureRmAutomationCertificate</span></span>
- <span data-ttu-id="a792e-123">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a792e-123">Remove-AzureRmAutomationCredential</span></span>
- <span data-ttu-id="a792e-124">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a792e-124">Remove-AzureRmAutomationVariable</span></span>
- <span data-ttu-id="a792e-125">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a792e-125">Remove-AzureRmAutomationWebhook</span></span>

<span data-ttu-id="a792e-126">**Batch**</span><span class="sxs-lookup"><span data-stu-id="a792e-126">**Batch**</span></span>
- <span data-ttu-id="a792e-127">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="a792e-127">Remove-AzureBatchCertificate</span></span>
- <span data-ttu-id="a792e-128">Remove-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a792e-128">Remove-AzureBatchComputeNode</span></span>
- <span data-ttu-id="a792e-129">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="a792e-129">Remove-AzureBatchComputeNodeUser</span></span>

<span data-ttu-id="a792e-130">**DataFactories**</span><span class="sxs-lookup"><span data-stu-id="a792e-130">**DataFactories**</span></span>
- <span data-ttu-id="a792e-131">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a792e-131">Resume-AzureRmDataFactoryPipeline</span></span>
- <span data-ttu-id="a792e-132">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="a792e-132">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>
- <span data-ttu-id="a792e-133">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a792e-133">Suspend-AzureRmDataFactoryPipeline</span></span>

<span data-ttu-id="a792e-134">**DataLakeStore**</span><span class="sxs-lookup"><span data-stu-id="a792e-134">**DataLakeStore**</span></span>
- <span data-ttu-id="a792e-135">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a792e-135">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>
- <span data-ttu-id="a792e-136">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="a792e-136">Set-AzureRmDataLakeStoreItemAcl</span></span>
- <span data-ttu-id="a792e-137">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a792e-137">Set-AzureRmDataLakeStoreItemAclEntry</span></span>
- <span data-ttu-id="a792e-138">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="a792e-138">Set-AzureRmDataLakeStoreItemOwner</span></span>

<span data-ttu-id="a792e-139">**OperationalInsights**</span><span class="sxs-lookup"><span data-stu-id="a792e-139">**OperationalInsights**</span></span>
- <span data-ttu-id="a792e-140">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="a792e-140">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

<span data-ttu-id="a792e-141">**Profil**</span><span class="sxs-lookup"><span data-stu-id="a792e-141">**Profile**</span></span>
- <span data-ttu-id="a792e-142">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="a792e-142">Remove-AzureRmEnvironment</span></span>

<span data-ttu-id="a792e-143">**RedisCache**</span><span class="sxs-lookup"><span data-stu-id="a792e-143">**RedisCache**</span></span>
- <span data-ttu-id="a792e-144">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a792e-144">Remove-AzureRmRedisCacheDiagnostics</span></span>

<span data-ttu-id="a792e-145">**Kaynaklar**</span><span class="sxs-lookup"><span data-stu-id="a792e-145">**Resources**</span></span>
- <span data-ttu-id="a792e-146">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="a792e-146">Register-AzureRmProviderFeature</span></span>
- <span data-ttu-id="a792e-147">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a792e-147">Register-AzureRmResourceProvider</span></span>
- <span data-ttu-id="a792e-148">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a792e-148">Remove-AzureRmADServicePrincipal</span></span>
- <span data-ttu-id="a792e-149">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a792e-149">Remove-AzureRmPolicyAssignment</span></span>
- <span data-ttu-id="a792e-150">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a792e-150">Remove-AzureRmResourceGroupDeployment</span></span>
- <span data-ttu-id="a792e-151">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a792e-151">Remove-AzureRmRoleAssignment</span></span>
- <span data-ttu-id="a792e-152">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a792e-152">Stop-AzureRmResourceGroupDeployment</span></span>
- <span data-ttu-id="a792e-153">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a792e-153">Unregister-AzureRmResourceProvider</span></span>

<span data-ttu-id="a792e-154">**Depolama**</span><span class="sxs-lookup"><span data-stu-id="a792e-154">**Storage**</span></span>
- <span data-ttu-id="a792e-155">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a792e-155">Remove-AzureStorageContainerStoredAccessPolicy</span></span>
- <span data-ttu-id="a792e-156">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a792e-156">Remove-AzureStorageQueueStoredAccessPolicy</span></span>
- <span data-ttu-id="a792e-157">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a792e-157">Remove-AzureStorageShareStoredAccessPolicy</span></span>
- <span data-ttu-id="a792e-158">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a792e-158">Remove-AzureStorageTableStoredAccessPolicy</span></span>

<span data-ttu-id="a792e-159">**StreamAnalytics**</span><span class="sxs-lookup"><span data-stu-id="a792e-159">**StreamAnalytics**</span></span>
- <span data-ttu-id="a792e-160">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a792e-160">Remove-AzureRmStreamAnalyticsFunction</span></span>
- <span data-ttu-id="a792e-161">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a792e-161">Remove-AzureRmStreamAnalyticsInput</span></span>
- <span data-ttu-id="a792e-162">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a792e-162">Remove-AzureRmStreamAnalyticsJob</span></span>
- <span data-ttu-id="a792e-163">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="a792e-163">Remove-AzureRmStreamAnalyticsOutput</span></span>

<span data-ttu-id="a792e-164">**Tag**</span><span class="sxs-lookup"><span data-stu-id="a792e-164">**Tag**</span></span>
- <span data-ttu-id="a792e-165">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="a792e-165">Remove-AzureRmTag</span></span>

<br>

<span data-ttu-id="a792e-166">Yukarıdaki cmdlet'lerinden herhangi birini kullanan bir betiğiniz varsa `Force` parametresinin kaldırılması, bozucu değişikliğin düzeltilmesi için yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="a792e-166">If you have a script that uses any of the above cmdlets, the breaking change can be fixed by simply removing the `Force` parameter.</span></span>

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location -Force

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location
```

<br>

## <a name="change-of-tag-parameters"></a><span data-ttu-id="a792e-167">Tag parametrelerinin değiştirilmesi</span><span class="sxs-lookup"><span data-stu-id="a792e-167">Change of Tag parameters</span></span>

<span data-ttu-id="a792e-168">Bu sürümde `Tags` parametresinin adı `Tag` olarak, `Hashtable[]` olan tür ise `Hashtable` olarak değiştirildiğinden, anahtar-değer eşleştirmelerinin biçimi değişmiştir.</span><span class="sxs-lookup"><span data-stu-id="a792e-168">This release, the `Tags` parameter name was changed to `Tag`, and the type was changed from `Hashtable[]` to `Hashtable`, changing the format of the key-value pairings.</span></span>

<span data-ttu-id="a792e-169">Önceden her bir `Hashtable[]` girdisi tek bir anahtar-değer eşleştirmesini temsil ediyordu:</span><span class="sxs-lookup"><span data-stu-id="a792e-169">Previously, each entry in the `Hashtable[]` represented a single key-value pairing:</span></span>

```powershell
$tags = @{ Name = "test1"; Value = "testval1" }, @{ Name = "test2", Value = "testval2" }
$tags[0].Name  # Key for the first entry, "test1"
$tags[0].Value # Value for the first entry, "testval1"
$tags[1].Name  # Key for the second entry, "test2"
$tags[1].Value # Value for the second entry, "testval2"
```

<span data-ttu-id="a792e-170">Şimdiyse `Name` ve `Value` artık gerekli olmadığından, `Hashtable`’da `Key = "Value"` atanarak anahtar-değer eşleştirmeleri oluşturulabilir:</span><span class="sxs-lookup"><span data-stu-id="a792e-170">Now, `Name` and `Value` are no longer necessary, allowing for key-value pairings to be created by assigning `Key = "Value"` in the `Hashtable`:</span></span>

```powershell
$tag = @{ test1 = "testval1"; test2 = "testval2" }
$tag["test1"] # Gets the value associated with the key "test1"
$tag["test2"] # Gets the value associated with the key "test2"
```

<span data-ttu-id="a792e-171">Bu değişiklikten aşağıdaki cmdlet’ler etkilenir:</span><span class="sxs-lookup"><span data-stu-id="a792e-171">The following cmdlets are affected by this change:</span></span>

<span data-ttu-id="a792e-172">**Batch**</span><span class="sxs-lookup"><span data-stu-id="a792e-172">**Batch**</span></span>
- <span data-ttu-id="a792e-173">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a792e-173">Get-AzureRmBatchAccount</span></span>
- <span data-ttu-id="a792e-174">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a792e-174">New-AzureRmBatchAccount</span></span>
- <span data-ttu-id="a792e-175">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a792e-175">Set-AzureRmBatchAccount</span></span>

<span data-ttu-id="a792e-176">**İşlem**</span><span class="sxs-lookup"><span data-stu-id="a792e-176">**Compute**</span></span>
- <span data-ttu-id="a792e-177">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a792e-177">New-AzureRmVM</span></span>
- <span data-ttu-id="a792e-178">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a792e-178">Update-AzureRmVM</span></span>

<span data-ttu-id="a792e-179">**DataLakeAnalytics**</span><span class="sxs-lookup"><span data-stu-id="a792e-179">**DataLakeAnalytics**</span></span>
- <span data-ttu-id="a792e-180">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a792e-180">New-AzureRmDataLakeAnalyticsAccount</span></span>
- <span data-ttu-id="a792e-181">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a792e-181">Set-AzureRmDataLakeAnalyticsAccount</span></span>

<span data-ttu-id="a792e-182">**DataLakeStore**</span><span class="sxs-lookup"><span data-stu-id="a792e-182">**DataLakeStore**</span></span>
- <span data-ttu-id="a792e-183">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a792e-183">New-AzureRmDataLakeStoreAccount</span></span>
- <span data-ttu-id="a792e-184">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a792e-184">Set-AzureRmDataLakeStoreAccount</span></span>

<span data-ttu-id="a792e-185">**Dns**</span><span class="sxs-lookup"><span data-stu-id="a792e-185">**Dns**</span></span>
- <span data-ttu-id="a792e-186">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="a792e-186">New-AzureRmDnsZone</span></span>
- <span data-ttu-id="a792e-187">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="a792e-187">Set-AzureRmDnsZone</span></span>

<span data-ttu-id="a792e-188">**KeyVault**</span><span class="sxs-lookup"><span data-stu-id="a792e-188">**KeyVault**</span></span>
- <span data-ttu-id="a792e-189">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="a792e-189">Get-AzureRmKeyVault</span></span>
- <span data-ttu-id="a792e-190">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="a792e-190">New-AzureRmKeyVault</span></span>

<span data-ttu-id="a792e-191">**Ağ**</span><span class="sxs-lookup"><span data-stu-id="a792e-191">**Network**</span></span>
- <span data-ttu-id="a792e-192">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a792e-192">New-AzureRmApplicationGateway</span></span>
- <span data-ttu-id="a792e-193">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a792e-193">New-AzureRmExpressRouteCircuit</span></span>
- <span data-ttu-id="a792e-194">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a792e-194">New-AzureRmLoadBalancer</span></span>
- <span data-ttu-id="a792e-195">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a792e-195">New-AzureRmLocalNetworkGateway</span></span>
- <span data-ttu-id="a792e-196">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a792e-196">New-AzureRmNetworkInterface</span></span>
- <span data-ttu-id="a792e-197">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a792e-197">New-AzureRmNetworkSecurityGroup</span></span>
- <span data-ttu-id="a792e-198">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a792e-198">New-AzureRmPublicIpAddress</span></span>
- <span data-ttu-id="a792e-199">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="a792e-199">New-AzureRmRouteTable</span></span>
- <span data-ttu-id="a792e-200">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a792e-200">New-AzureRmVirtualNetwork</span></span>
- <span data-ttu-id="a792e-201">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a792e-201">New-AzureRmVirtualNetworkGateway</span></span>
- <span data-ttu-id="a792e-202">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a792e-202">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="a792e-203">New-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a792e-203">New-AzureRmVirtualNetworkPeering</span></span>

<span data-ttu-id="a792e-204">**Kaynaklar**</span><span class="sxs-lookup"><span data-stu-id="a792e-204">**Resources**</span></span>
- <span data-ttu-id="a792e-205">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a792e-205">Find-AzureRmResource</span></span>
- <span data-ttu-id="a792e-206">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a792e-206">Find-AzureRmResourceGroup</span></span>
- <span data-ttu-id="a792e-207">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a792e-207">New-AzureRmResource</span></span>
- <span data-ttu-id="a792e-208">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a792e-208">New-AzureRmResourceGroup</span></span>
- <span data-ttu-id="a792e-209">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a792e-209">Set-AzureRmResource</span></span>
- <span data-ttu-id="a792e-210">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a792e-210">Set-AzureRmResourceGroup</span></span>

<span data-ttu-id="a792e-211">**SQL**</span><span class="sxs-lookup"><span data-stu-id="a792e-211">**SQL**</span></span>
- <span data-ttu-id="a792e-212">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a792e-212">New-AzureRmSqlDatabase</span></span>
- <span data-ttu-id="a792e-213">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a792e-213">New-AzureRmSqlDatabaseCopy</span></span>
- <span data-ttu-id="a792e-214">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a792e-214">New-AzureRmSqlDatabaseSecondary</span></span>
- <span data-ttu-id="a792e-215">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a792e-215">New-AzureRmSqlElasticPool</span></span>
- <span data-ttu-id="a792e-216">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="a792e-216">New-AzureRmSqlServer</span></span>
- <span data-ttu-id="a792e-217">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a792e-217">Set-AzureRmSqlDatabase</span></span>
- <span data-ttu-id="a792e-218">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a792e-218">Set-AzureRmSqlElasticPool</span></span>
- <span data-ttu-id="a792e-219">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="a792e-219">Set-AzureRmSqlServer</span></span>

<span data-ttu-id="a792e-220">**Depolama**</span><span class="sxs-lookup"><span data-stu-id="a792e-220">**Storage**</span></span>
- <span data-ttu-id="a792e-221">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a792e-221">New-AzureRmStorageAccount</span></span>
- <span data-ttu-id="a792e-222">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a792e-222">Set-AzureRmStorageAccount</span></span>

<span data-ttu-id="a792e-223">**TrafficManager**</span><span class="sxs-lookup"><span data-stu-id="a792e-223">**TrafficManager**</span></span>
- <span data-ttu-id="a792e-224">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a792e-224">New-AzureRmTrafficManagerProfile</span></span>

<br>

<span data-ttu-id="a792e-225">Yukarıdaki cmdlet'lerinden herhangi birini kullanan bir betiğiniz varsa, bozucu değişiklik `Tags` parametresinin `Tag` olarak değiştirilmesinin yanı sıra `Tag` öğesinin yeni biçime değiştirilmesi ile düzeltilebilir.</span><span class="sxs-lookup"><span data-stu-id="a792e-225">If you have a script that uses any of the above cmdlets, the breaking change can be fixed by changing the `Tags` parameter to `Tag`, as well as changing the `Tag` to the new format.</span></span>

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tags @{ Name = "testtag"; Value = "testval" }

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tag @{ testtag = "testval" }
```

<br>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="a792e-226">Depolama cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="a792e-226">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="a792e-227">Bu sürümden aşağıdaki cmdlet’ler etkilenir:</span><span class="sxs-lookup"><span data-stu-id="a792e-227">The following cmdlets were affected this release:</span></span>

<span data-ttu-id="a792e-228">**Get-AzureRmStorageAccountKey**</span><span class="sxs-lookup"><span data-stu-id="a792e-228">**Get-AzureRmStorageAccountKey**</span></span>
- <span data-ttu-id="a792e-229">Bu cmdlet artık her anahtarın özelliklerini içeren bir nesne yerine anahtarların listesini döndürür</span><span class="sxs-lookup"><span data-stu-id="a792e-229">The cmdlet now returns a list of keys, rather than an object with properties for each key</span></span>

```powershell
# Old
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Key1

# New
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName)[0].Value
```

<span data-ttu-id="a792e-230">**New-AzureRmStorageAccountKey**</span><span class="sxs-lookup"><span data-stu-id="a792e-230">**New-AzureRmStorageAccountKey**</span></span>
- <span data-ttu-id="a792e-231">Bu cmdlet’in çıktısındaki `StorageAccountRegenerateKeyResponse` alanı, artık her anahtarın özelliklerini içeren bir nesne yerine anahtarların listesi olan `StorageAccountListKeysResults` olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="a792e-231">`StorageAccountRegenerateKeyResponse` field in output of this cmdlet is renamed to `StorageAccountListKeysResults`, which is now a list of keys rather than an object with properties for each key</span></span>

```powershell
# Old
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).StorageAccountKeys.Key1

# New
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Keys[0].Value
```

<span data-ttu-id="a792e-232">**New/Get/Set-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="a792e-232">**New/Get/Set-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="a792e-233">Bu cmdlet’in çıktısındaki `AccountType` alanı, `Sku.Name` olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="a792e-233">`AccountType` field in output of this cmdlet is renamed to `Sku.Name`</span></span>
- <span data-ttu-id="a792e-234">Birincil uç noktalar/İkincil uç noktalar blob/tablo/kuyruk/dosya için `Uri` olan çıktı türü `String` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="a792e-234">Output type for PrimaryEndpoints/Secondary endpoints blob/table/queue/file changed from `Uri` to `String`</span></span>

```powershell
# Old
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).AccountType

# New
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).Sku.Name
```

```powershell
# Old 
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.AbsolutePath

# New
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob
```

<br>

## <a name="breaking-changes-to-ad-cmdlets"></a><span data-ttu-id="a792e-235">AD cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="a792e-235">Breaking changes to AD cmdlets</span></span>

<span data-ttu-id="a792e-236">Bu sürümden aşağıdaki cmdlet’ler etkilenmiştir:</span><span class="sxs-lookup"><span data-stu-id="a792e-236">The following cmdlets were affected this release:</span></span>

<span data-ttu-id="a792e-237">**Get-AzureRMADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="a792e-237">**Get-AzureRMADServicePrincipal**</span></span>
- <span data-ttu-id="a792e-238">Bu cmdlet’in çıktısındaki `ServicePrincipalName` alanı, `ServicePrincipalNames` olarak yeniden adlandırıldı ve bir koleksiyona dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="a792e-238">`ServicePrincipalName` field in output of this cmdlet is renamed to `ServicePrincipalNames` and is now a collection.</span></span> <span data-ttu-id="a792e-239">Artık identifierUri’nin yanı sıra bir SPN olarak `ApplicationId`’yi de görüntülüyor.</span><span class="sxs-lookup"><span data-stu-id="a792e-239">It now displays `ApplicationId` also as one of the SPN, along with the identifierUri.</span></span>

```powershell
# Old
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalName

# New
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalNames[0]
```

<span data-ttu-id="a792e-240">**Get-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="a792e-240">**Get-AzureRmADApplication**</span></span>
- <span data-ttu-id="a792e-241">`ApplicationObjectId` parametresi `ObjectId` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="a792e-241">Parameter `ApplicationObjectId` is renamed to `ObjectId`.</span></span>
- <span data-ttu-id="a792e-242">Bu cmdlet’in çıktısındaki `ApplicationObjectId`, `ObjectId` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="a792e-242">In output of this cmdlet, `ApplicationObjectId` is renamed to `ObjectId`.</span></span>

```powershell
# Old
$app = Get-AzureRmADApplication -ApplicationObjectId $applicationObjectId
$objectId = $app.ApplicationObjectId

# New
$app = Get-AzureRmADApplication -ObjectId $objectId
$objectId = $app.ObjectId
```

<span data-ttu-id="a792e-243">**Remove-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="a792e-243">**Remove-AzureRmADApplication**</span></span>
- <span data-ttu-id="a792e-244">`ApplicationObjectId` parametresi `ObjectId` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="a792e-244">Parameter `ApplicationObjectId` is renamed to `ObjectId`.</span></span>

```powershell
# Old
$app = Remove-AzureRmADApplication -ApplicationObjectId $applicationObjectId -Force

# New
$app = Remove-AzureRmADApplication -ObjectId $objectId -Force
```

<span data-ttu-id="a792e-245">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="a792e-245">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="a792e-246">Bu cmdlet’in çıktısındaki `ApplicationObjectId`, `ObjectId` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="a792e-246">In output of this cmdlet, `ApplicationObjectId` is renamed to `ObjectId`.</span></span>
- <span data-ttu-id="a792e-247">`KeyValue`, `KeyUsage`, `KeyType` parametreleri kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="a792e-247">`KeyValue`, `KeyUsage`, `KeyType` parameters are removed.</span></span>

```powershell
# Old
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris -KeyValue $kv -KeyType $kt -KeyUsage $ku
$id = $app.ApplicationObjectId

# New
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris
$id = $app.ObjectId
New-AzureRmADAppCredential -ObjectId $id -Password $kv
```

<span data-ttu-id="a792e-248">**Get-AzureRmADGroup**</span><span class="sxs-lookup"><span data-stu-id="a792e-248">**Get-AzureRmADGroup**</span></span>
- <span data-ttu-id="a792e-249">`Mail` alanı çıktıdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="a792e-249">`Mail` field is removed from the output.</span></span>

<span data-ttu-id="a792e-250">**Get-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="a792e-250">**Get-AzureRmADUser**</span></span>
- <span data-ttu-id="a792e-251">`Mail` alanı çıktıdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="a792e-251">`Mail` field is removed from the output.</span></span>

<span data-ttu-id="a792e-252">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="a792e-252">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="a792e-253">`DisableAccount` parametresi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="a792e-253">Removed `DisableAccount` parameter.</span></span>

```powershell
# Old
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password -DisableAccount true

# New
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password
Remove-AzureRmADServicePrincipal -ObjectId $servicePrincipal.ObjectId
```