---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: a3e1561feb470708420015bac1e2f0688f182896
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274491"
---
# <span data-ttu-id="4eca1-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="4eca1-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="4eca1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eca1-102">SYNOPSIS</span></span>
<span data-ttu-id="4eca1-103">Kusto kümesini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="4eca1-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="4eca1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4eca1-104">SYNTAX</span></span>

### <span data-ttu-id="4eca1-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4eca1-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4eca1-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="4eca1-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4eca1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4eca1-107">DESCRIPTION</span></span>
<span data-ttu-id="4eca1-108">Kusto kümesini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="4eca1-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="4eca1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4eca1-109">EXAMPLES</span></span>

### <span data-ttu-id="4eca1-110">Örnek 1: var olan kümeyi adıyla güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="4eca1-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="4eca1-111">Yukarıdaki komut, "testnewkustocluster" kaynak grubunda bulunan "" kusto kümesinin SKU adını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4eca1-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="4eca1-112">Örnek 2: var olan kümeyi adıyla güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="4eca1-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="4eca1-113">Yukarıdaki komut, "testrg" kaynak grubunda bulunan "testnewkustocluster" kümesini müşteri yönetimli anahtarla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4eca1-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="4eca1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4eca1-114">PARAMETERS</span></span>

### <span data-ttu-id="4eca1-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="4eca1-115">-AsJob</span></span>
<span data-ttu-id="4eca1-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="4eca1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4eca1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eca1-117">-DefaultProfile</span></span>
<span data-ttu-id="4eca1-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4eca1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eca1-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="4eca1-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="4eca1-120">Kümenin disklerinin şifrelenip şifrelenmediğini belirten bir Boole değeri.</span><span class="sxs-lookup"><span data-stu-id="4eca1-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="4eca1-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="4eca1-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="4eca1-122">Çift şifrelemenin etkinleştirilip etkinleştirilmediğini belirten Boole değeri.</span><span class="sxs-lookup"><span data-stu-id="4eca1-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="4eca1-123">-Enabletemizle</span><span class="sxs-lookup"><span data-stu-id="4eca1-123">-EnablePurge</span></span>
<span data-ttu-id="4eca1-124">Temizleme işlemlerinin etkinleştirilip etkinleştirilmediğini belirten Boole değeri.</span><span class="sxs-lookup"><span data-stu-id="4eca1-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="4eca1-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="4eca1-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="4eca1-126">Akış gerektiren EST 'nin etkinleştirilip etkinleştirilmediğini belirten Boole değeri.</span><span class="sxs-lookup"><span data-stu-id="4eca1-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="4eca1-127">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4eca1-127">-IdentityType</span></span>
<span data-ttu-id="4eca1-128">Kimlik türü.</span><span class="sxs-lookup"><span data-stu-id="4eca1-128">The identity type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eca1-129">-Identityuseratanandentity</span><span class="sxs-lookup"><span data-stu-id="4eca1-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="4eca1-130">Kusto kümesiyle ilişkili kullanıcı kimliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="4eca1-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="4eca1-131">Kullanıcı kimliği sözlüğü anahtar başvuruları şu formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} '.</span><span class="sxs-lookup"><span data-stu-id="4eca1-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="4eca1-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4eca1-132">-InputObject</span></span>
<span data-ttu-id="4eca1-133">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4eca1-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4eca1-134">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="4eca1-134">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="4eca1-135">Anahtar Kasası anahtarının adı.</span><span class="sxs-lookup"><span data-stu-id="4eca1-135">The name of the key vault key.</span></span>

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

### <span data-ttu-id="4eca1-136">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="4eca1-136">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="4eca1-137">Anahtar Kasası URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="4eca1-137">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="4eca1-138">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="4eca1-138">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="4eca1-139">Anahtar Kasası anahtarının sürümü.</span><span class="sxs-lookup"><span data-stu-id="4eca1-139">The version of the key vault key.</span></span>

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

### <span data-ttu-id="4eca1-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="4eca1-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="4eca1-141">Dil uzantılarının listesi.</span><span class="sxs-lookup"><span data-stu-id="4eca1-141">The list of language extensions.</span></span>
<span data-ttu-id="4eca1-142">Oluşturmak için LANGUAGEEXTENSIONVALUE özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4eca1-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eca1-143">-Konum</span><span class="sxs-lookup"><span data-stu-id="4eca1-143">-Location</span></span>
<span data-ttu-id="4eca1-144">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="4eca1-144">Resource location.</span></span>

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

### <span data-ttu-id="4eca1-145">-Ad</span><span class="sxs-lookup"><span data-stu-id="4eca1-145">-Name</span></span>
<span data-ttu-id="4eca1-146">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="4eca1-146">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eca1-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4eca1-147">-NoWait</span></span>
<span data-ttu-id="4eca1-148">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="4eca1-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4eca1-149">-Optimizedautoscaleısenabled</span><span class="sxs-lookup"><span data-stu-id="4eca1-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="4eca1-150">En iyileştirilmiş otomatik ölçeklendirme özelliğinin etkinleştirilip etkinleştirilmediğini belirten Boole değeri.</span><span class="sxs-lookup"><span data-stu-id="4eca1-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="4eca1-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="4eca1-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="4eca1-152">İzin verilen en fazla örnek sayısı.</span><span class="sxs-lookup"><span data-stu-id="4eca1-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="4eca1-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="4eca1-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="4eca1-154">İzin verilen minimum örnek sayısı.</span><span class="sxs-lookup"><span data-stu-id="4eca1-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="4eca1-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="4eca1-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="4eca1-156">Şablon sürümü, örneğin 1.</span><span class="sxs-lookup"><span data-stu-id="4eca1-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="4eca1-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eca1-157">-ResourceGroupName</span></span>
<span data-ttu-id="4eca1-158">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4eca1-158">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eca1-159">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="4eca1-159">-SkuCapacity</span></span>
<span data-ttu-id="4eca1-160">Kümenin örneklerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="4eca1-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="4eca1-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4eca1-161">-SkuName</span></span>
<span data-ttu-id="4eca1-162">SKU adı.</span><span class="sxs-lookup"><span data-stu-id="4eca1-162">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eca1-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="4eca1-163">-SkuTier</span></span>
<span data-ttu-id="4eca1-164">SKU katmanı.</span><span class="sxs-lookup"><span data-stu-id="4eca1-164">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eca1-165">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="4eca1-165">-SubscriptionId</span></span>
<span data-ttu-id="4eca1-166">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="4eca1-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4eca1-167">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4eca1-167">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eca1-168">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4eca1-168">-Tag</span></span>
<span data-ttu-id="4eca1-169">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="4eca1-169">Resource tags.</span></span>

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

### <span data-ttu-id="4eca1-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="4eca1-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="4eca1-171">Kümenin dış kiracıları.</span><span class="sxs-lookup"><span data-stu-id="4eca1-171">The cluster's external tenants.</span></span>
<span data-ttu-id="4eca1-172">Oluşturmak için, TRUSTEDEXTERNALTENANT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4eca1-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eca1-173">-Virtualnetworkconfigurationdatamanagementpublicıpıd</span><span class="sxs-lookup"><span data-stu-id="4eca1-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="4eca1-174">Veri yönetimi hizmeti genel IP adresi kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="4eca1-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="4eca1-175">-Virtualnetworkconfigurationenginepublicıpıd</span><span class="sxs-lookup"><span data-stu-id="4eca1-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="4eca1-176">Altyapı hizmetinin genel IP adresi kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="4eca1-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="4eca1-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="4eca1-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="4eca1-178">Alt ağ kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="4eca1-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="4eca1-179">-Onay</span><span class="sxs-lookup"><span data-stu-id="4eca1-179">-Confirm</span></span>
<span data-ttu-id="4eca1-180">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4eca1-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eca1-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eca1-181">-WhatIf</span></span>
<span data-ttu-id="4eca1-182">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4eca1-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eca1-183">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4eca1-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eca1-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eca1-184">CommonParameters</span></span>
<span data-ttu-id="4eca1-185">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4eca1-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eca1-186">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4eca1-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eca1-187">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4eca1-187">INPUTS</span></span>

### <span data-ttu-id="4eca1-188">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="4eca1-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="4eca1-189">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4eca1-189">OUTPUTS</span></span>

### <span data-ttu-id="4eca1-190">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. ıluster</span><span class="sxs-lookup"><span data-stu-id="4eca1-190">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="4eca1-191">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4eca1-191">NOTES</span></span>

<span data-ttu-id="4eca1-192">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="4eca1-192">ALIASES</span></span>

<span data-ttu-id="4eca1-193">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="4eca1-193">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4eca1-194">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4eca1-194">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4eca1-195">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4eca1-195">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4eca1-196">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="4eca1-196">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4eca1-197">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="4eca1-197">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="4eca1-198">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="4eca1-198">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="4eca1-199">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="4eca1-199">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="4eca1-200">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="4eca1-200">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="4eca1-201">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="4eca1-201">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4eca1-202">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="4eca1-202">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="4eca1-203">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="4eca1-203">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="4eca1-204">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4eca1-204">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="4eca1-205">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="4eca1-205">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4eca1-206">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4eca1-206">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="4eca1-207">LANGUAGEEXTENSIONVALUE <ılanguageextension [] >: dil uzantılarının listesi.</span><span class="sxs-lookup"><span data-stu-id="4eca1-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="4eca1-208">`[Name <LanguageExtensionName?>]`: Dil uzantısının adı.</span><span class="sxs-lookup"><span data-stu-id="4eca1-208">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="4eca1-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: kümenin dış kiracıları.</span><span class="sxs-lookup"><span data-stu-id="4eca1-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="4eca1-210">`[Value <String>]`: Dış kiracıyı temsil eden GUID.</span><span class="sxs-lookup"><span data-stu-id="4eca1-210">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="4eca1-211">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4eca1-211">RELATED LINKS</span></span>

