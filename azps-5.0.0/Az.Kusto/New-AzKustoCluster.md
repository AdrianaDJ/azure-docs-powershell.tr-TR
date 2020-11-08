---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b8b6c11da622b7fa0ee67dc418f2055dd72c1d13
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278996"
---
# <span data-ttu-id="dc64a-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="dc64a-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="dc64a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc64a-102">SYNOPSIS</span></span>
<span data-ttu-id="dc64a-103">Kusto kümesi oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="dc64a-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="dc64a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc64a-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dc64a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc64a-105">DESCRIPTION</span></span>
<span data-ttu-id="dc64a-106">Kusto kümesi oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="dc64a-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="dc64a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc64a-107">EXAMPLES</span></span>

### <span data-ttu-id="dc64a-108">Örnek 1: yeni bir kusto kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="dc64a-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="dc64a-109">Yukarıdaki komut, "testrg" kaynak grubunda "testnewkustocluster" adlı yeni bir kusto kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc64a-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="dc64a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc64a-110">PARAMETERS</span></span>

### <span data-ttu-id="dc64a-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="dc64a-111">-AsJob</span></span>
<span data-ttu-id="dc64a-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="dc64a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="dc64a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc64a-113">-DefaultProfile</span></span>
<span data-ttu-id="dc64a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dc64a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc64a-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="dc64a-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="dc64a-116">Kümenin disklerinin şifrelenip şifrelenmediğini belirten bir Boole değeri.</span><span class="sxs-lookup"><span data-stu-id="dc64a-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="dc64a-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="dc64a-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="dc64a-118">Çift şifrelemenin etkinleştirilip etkinleştirilmediğini belirten Boole değeri.</span><span class="sxs-lookup"><span data-stu-id="dc64a-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="dc64a-119">-Enabletemizle</span><span class="sxs-lookup"><span data-stu-id="dc64a-119">-EnablePurge</span></span>
<span data-ttu-id="dc64a-120">Temizleme işlemlerinin etkinleştirilip etkinleştirilmediğini belirten Boole değeri.</span><span class="sxs-lookup"><span data-stu-id="dc64a-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="dc64a-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="dc64a-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="dc64a-122">Akış gerektiren EST 'nin etkinleştirilip etkinleştirilmediğini belirten Boole değeri.</span><span class="sxs-lookup"><span data-stu-id="dc64a-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="dc64a-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="dc64a-123">-IdentityType</span></span>
<span data-ttu-id="dc64a-124">Kimlik türü.</span><span class="sxs-lookup"><span data-stu-id="dc64a-124">The identity type.</span></span>

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

### <span data-ttu-id="dc64a-125">-Identityuseratanandentity</span><span class="sxs-lookup"><span data-stu-id="dc64a-125">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="dc64a-126">Kusto kümesiyle ilişkili kullanıcı kimliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="dc64a-126">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="dc64a-127">Kullanıcı kimliği sözlüğü anahtar başvuruları şu formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} '.</span><span class="sxs-lookup"><span data-stu-id="dc64a-127">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="dc64a-128">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="dc64a-128">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="dc64a-129">Anahtar Kasası anahtarının adı.</span><span class="sxs-lookup"><span data-stu-id="dc64a-129">The name of the key vault key.</span></span>

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

### <span data-ttu-id="dc64a-130">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="dc64a-130">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="dc64a-131">Anahtar Kasası URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="dc64a-131">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="dc64a-132">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="dc64a-132">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="dc64a-133">Anahtar Kasası anahtarının sürümü.</span><span class="sxs-lookup"><span data-stu-id="dc64a-133">The version of the key vault key.</span></span>

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

### <span data-ttu-id="dc64a-134">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="dc64a-134">-LanguageExtensionValue</span></span>
<span data-ttu-id="dc64a-135">Dil uzantılarının listesi.</span><span class="sxs-lookup"><span data-stu-id="dc64a-135">The list of language extensions.</span></span>
<span data-ttu-id="dc64a-136">Oluşturmak için LANGUAGEEXTENSIONVALUE özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dc64a-136">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="dc64a-137">-Konum</span><span class="sxs-lookup"><span data-stu-id="dc64a-137">-Location</span></span>
<span data-ttu-id="dc64a-138">Kaynağın yaşadığı coğrafi konum</span><span class="sxs-lookup"><span data-stu-id="dc64a-138">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="dc64a-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="dc64a-139">-Name</span></span>
<span data-ttu-id="dc64a-140">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="dc64a-140">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc64a-141">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dc64a-141">-NoWait</span></span>
<span data-ttu-id="dc64a-142">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="dc64a-142">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dc64a-143">-Optimizedautoscaleısenabled</span><span class="sxs-lookup"><span data-stu-id="dc64a-143">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="dc64a-144">En iyileştirilmiş otomatik ölçeklendirme özelliğinin etkinleştirilip etkinleştirilmediğini belirten Boole değeri.</span><span class="sxs-lookup"><span data-stu-id="dc64a-144">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="dc64a-145">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="dc64a-145">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="dc64a-146">İzin verilen en fazla örnek sayısı.</span><span class="sxs-lookup"><span data-stu-id="dc64a-146">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="dc64a-147">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="dc64a-147">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="dc64a-148">İzin verilen minimum örnek sayısı.</span><span class="sxs-lookup"><span data-stu-id="dc64a-148">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="dc64a-149">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="dc64a-149">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="dc64a-150">Şablon sürümü, örneğin 1.</span><span class="sxs-lookup"><span data-stu-id="dc64a-150">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="dc64a-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc64a-151">-ResourceGroupName</span></span>
<span data-ttu-id="dc64a-152">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="dc64a-152">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="dc64a-153">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="dc64a-153">-SkuCapacity</span></span>
<span data-ttu-id="dc64a-154">Kümenin örneklerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="dc64a-154">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="dc64a-155">-SkuName</span><span class="sxs-lookup"><span data-stu-id="dc64a-155">-SkuName</span></span>
<span data-ttu-id="dc64a-156">SKU adı.</span><span class="sxs-lookup"><span data-stu-id="dc64a-156">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc64a-157">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="dc64a-157">-SkuTier</span></span>
<span data-ttu-id="dc64a-158">SKU katmanı.</span><span class="sxs-lookup"><span data-stu-id="dc64a-158">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc64a-159">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="dc64a-159">-SubscriptionId</span></span>
<span data-ttu-id="dc64a-160">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="dc64a-160">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dc64a-161">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="dc64a-161">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dc64a-162">Etiketli</span><span class="sxs-lookup"><span data-stu-id="dc64a-162">-Tag</span></span>
<span data-ttu-id="dc64a-163">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="dc64a-163">Resource tags.</span></span>

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

### <span data-ttu-id="dc64a-164">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="dc64a-164">-TrustedExternalTenant</span></span>
<span data-ttu-id="dc64a-165">Kümenin dış kiracıları.</span><span class="sxs-lookup"><span data-stu-id="dc64a-165">The cluster's external tenants.</span></span>
<span data-ttu-id="dc64a-166">Oluşturmak için, TRUSTEDEXTERNALTENANT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dc64a-166">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dc64a-167">-Virtualnetworkconfigurationdatamanagementpublicıpıd</span><span class="sxs-lookup"><span data-stu-id="dc64a-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="dc64a-168">Veri yönetimi hizmeti genel IP adresi kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="dc64a-168">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="dc64a-169">-Virtualnetworkconfigurationenginepublicıpıd</span><span class="sxs-lookup"><span data-stu-id="dc64a-169">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="dc64a-170">Altyapı hizmetinin genel IP adresi kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="dc64a-170">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="dc64a-171">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="dc64a-171">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="dc64a-172">Alt ağ kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="dc64a-172">The subnet resource id.</span></span>

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

### <span data-ttu-id="dc64a-173">-Bölge</span><span class="sxs-lookup"><span data-stu-id="dc64a-173">-Zone</span></span>
<span data-ttu-id="dc64a-174">Kümenin kullanılabilirlik bölgeleri.</span><span class="sxs-lookup"><span data-stu-id="dc64a-174">The availability zones of the cluster.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc64a-175">-Onay</span><span class="sxs-lookup"><span data-stu-id="dc64a-175">-Confirm</span></span>
<span data-ttu-id="dc64a-176">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dc64a-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc64a-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc64a-177">-WhatIf</span></span>
<span data-ttu-id="dc64a-178">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dc64a-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc64a-179">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dc64a-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc64a-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc64a-180">CommonParameters</span></span>
<span data-ttu-id="dc64a-181">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc64a-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc64a-182">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dc64a-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc64a-183">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc64a-183">INPUTS</span></span>

## <span data-ttu-id="dc64a-184">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc64a-184">OUTPUTS</span></span>

### <span data-ttu-id="dc64a-185">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. ıluster</span><span class="sxs-lookup"><span data-stu-id="dc64a-185">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="dc64a-186">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc64a-186">NOTES</span></span>

<span data-ttu-id="dc64a-187">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="dc64a-187">ALIASES</span></span>

<span data-ttu-id="dc64a-188">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="dc64a-188">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dc64a-189">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dc64a-189">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc64a-190">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dc64a-190">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dc64a-191">LANGUAGEEXTENSIONVALUE <ılanguageextension [] >: dil uzantılarının listesi.</span><span class="sxs-lookup"><span data-stu-id="dc64a-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="dc64a-192">`[Name <LanguageExtensionName?>]`: Dil uzantısının adı.</span><span class="sxs-lookup"><span data-stu-id="dc64a-192">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="dc64a-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: kümenin dış kiracıları.</span><span class="sxs-lookup"><span data-stu-id="dc64a-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="dc64a-194">`[Value <String>]`: Dış kiracıyı temsil eden GUID.</span><span class="sxs-lookup"><span data-stu-id="dc64a-194">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="dc64a-195">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc64a-195">RELATED LINKS</span></span>

