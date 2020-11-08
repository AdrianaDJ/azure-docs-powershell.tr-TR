---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: a11e962e2af6beaa3f3004cec104530f7603bb3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267214"
---
# <span data-ttu-id="8b842-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8b842-101">New-AzKeyVault</span></span>

## <span data-ttu-id="8b842-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b842-102">SYNOPSIS</span></span>
<span data-ttu-id="8b842-103">Bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b842-103">Creates a key vault.</span></span>

## <span data-ttu-id="8b842-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b842-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-DisableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b842-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b842-105">DESCRIPTION</span></span>
<span data-ttu-id="8b842-106">**Yeni-Aztuş Kasası** cmdlet 'i, belirtilen kaynak grubunda bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b842-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="8b842-107">Bu cmdlet, şu anda oturum açmış olan kullanıcıya, anahtar kasasındaki anahtarları ve gizlilikleri eklemek, kaldırmak veya listelemek amacıyla izinler verir.</span><span class="sxs-lookup"><span data-stu-id="8b842-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="8b842-108">Not: yeni anahtar kasayı oluşturmaya çalıştığınızda, **abonelik ' Microsoft. Keykasa ' ad alanını kullanmak için kaydedilmemiş olduğunu** görürseniz, **register-azresourceprovider-Providernamespace "Microsoft. keykasa"** öğesini çalıştırın ve ardından **New-azkeykasa** komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="8b842-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="8b842-109">Daha fazla bilgi için Register-AzResourceProvider konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="8b842-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="8b842-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b842-110">EXAMPLES</span></span>

### <span data-ttu-id="8b842-111">Örnek 1: standart bir Anahtar Kasası oluşturma</span><span class="sxs-lookup"><span data-stu-id="8b842-111">Example 1: Create a Standard key vault</span></span>
```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="8b842-112">Bu komut, Azure bölgesinde Contoso03Vault adlı bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b842-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="8b842-113">Komut, anahtar kasayı Group14 adlı kaynak grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="8b842-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="8b842-114">Komut, *SKU* parametresi için bir değer belirtmediğinden, standart bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b842-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="8b842-115">Örnek 2: Premium Anahtar Kasası oluşturma</span><span class="sxs-lookup"><span data-stu-id="8b842-115">Example 2: Create a Premium key vault</span></span>
```powershell
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Premium
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="8b842-116">Bu komut, önceki örnekte olduğu gibi bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b842-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="8b842-117">Bununla birlikte, Özel Anahtar Kasası oluşturmak için *SKU* parametresi için Premium değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b842-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="8b842-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="8b842-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="8b842-119">Anahtar Kasası oluşturma ve $myNetworkResId tarafından belirtilen sanal ağdan belirtilen IP adresine erişim izni vermek için ağ kurallarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b842-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="8b842-120">`New-AzKeyVaultNetworkRuleSetObject`Daha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="8b842-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="8b842-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b842-121">PARAMETERS</span></span>

### <span data-ttu-id="8b842-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b842-122">-DefaultProfile</span></span>
<span data-ttu-id="8b842-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8b842-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b842-124">-DisableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="8b842-124">-DisableSoftDelete</span></span>
<span data-ttu-id="8b842-125">Belirtilmişse, bu Anahtar Kasası için ' yumuşak silme ' işlevi devre dışı bırakılmıştır.</span><span class="sxs-lookup"><span data-stu-id="8b842-125">If specified, 'soft delete' functionality is disabled for this key vault.</span></span>

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

### <span data-ttu-id="8b842-126">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="8b842-126">-EnabledForDeployment</span></span>
<span data-ttu-id="8b842-127">Kaynak oluşturmada bu Anahtar Kasası, örneğin sanal makine oluştururken bu anahtar kasasına başvurulduğunda, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8b842-127">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b842-128">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="8b842-128">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="8b842-129">Azure disk şifreleme hizmeti 'nin, bu anahtar kasasından parolaları almasını ve anahtarları kaydırılmasını sağlayın.</span><span class="sxs-lookup"><span data-stu-id="8b842-129">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b842-130">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="8b842-130">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="8b842-131">Bu anahtar kasası bir şablon dağıtımında başvuruluyorsa, Azure Resource Manager 'ın bu anahtar kasasından gizli kod almasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="8b842-131">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b842-132">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="8b842-132">-EnablePurgeProtection</span></span>
<span data-ttu-id="8b842-133">Belirtilmişse, bu kasa için anında silinmeye karşı koruma etkinleştirilir; yumuşak silmenin da etkinleştirilmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="8b842-133">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="8b842-134">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="8b842-134">-EnableRbacAuthorization</span></span>
<span data-ttu-id="8b842-135">Belirtilmişse, veri eylemlerine rol tabanlı erişim denetimi (RBAC) tarafından yetki verme izni verir ve ardından kasa özelliklerinde belirtilen erişim ilkeleri yok sayılır.</span><span class="sxs-lookup"><span data-stu-id="8b842-135">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="8b842-136">Yönetim eylemlerine her zaman RBAC ile yetki verildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="8b842-136">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="8b842-137">-Konum</span><span class="sxs-lookup"><span data-stu-id="8b842-137">-Location</span></span>
<span data-ttu-id="8b842-138">Anahtar Kasası oluşturacağınız Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b842-138">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="8b842-139">Seçimlerinizi görmek için [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="8b842-139">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b842-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="8b842-140">-Name</span></span>
<span data-ttu-id="8b842-141">Oluşturulacak Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b842-141">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="8b842-142">Ad, harf, sayı veya kısa çizgi bileşimleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="8b842-142">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="8b842-143">Ad bir harfle veya rakamla başlamalıdır ve bitmelidir.</span><span class="sxs-lookup"><span data-stu-id="8b842-143">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="8b842-144">Ad, evrensel olarak benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8b842-144">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b842-145">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8b842-145">-NetworkRuleSet</span></span>
<span data-ttu-id="8b842-146">Kasanın ağ kuralı kümesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b842-146">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="8b842-147">Belirli ağ konumlarından Anahtar Kasası erişilebilirliğini yönetir.</span><span class="sxs-lookup"><span data-stu-id="8b842-147">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="8b842-148">Oluşturan `New-AzKeyVaultNetworkRuleSetObject` .</span><span class="sxs-lookup"><span data-stu-id="8b842-148">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b842-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b842-149">-ResourceGroupName</span></span>
<span data-ttu-id="8b842-150">Anahtar Kasası oluşturulacak varolan bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b842-150">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b842-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="8b842-151">-Sku</span></span>
<span data-ttu-id="8b842-152">Anahtar Kasası örneğinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b842-152">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="8b842-153">Her SKU için hangi özelliklerin kullanılabildiği hakkında bilgi için, Azure Anahtar Kasası fiyatlandırma web sitesine ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="8b842-153">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: Microsoft.Azure.Management.KeyVault.Models.SkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b842-154">-Softdeleteretentionındays</span><span class="sxs-lookup"><span data-stu-id="8b842-154">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="8b842-155">Silinmiş kaynakların ne kadar süreyle korunacağını ve silinmiş durumda bir kasaya veya nesnenin temizlenmesinin ne kadar süreceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b842-155">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="8b842-156">Varsayılan değer 90 gündür.</span><span class="sxs-lookup"><span data-stu-id="8b842-156">The default is 90 days.</span></span>

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

### <span data-ttu-id="8b842-157">Etiketli</span><span class="sxs-lookup"><span data-stu-id="8b842-157">-Tag</span></span>
<span data-ttu-id="8b842-158">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="8b842-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8b842-159">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="8b842-159">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b842-160">-Onay</span><span class="sxs-lookup"><span data-stu-id="8b842-160">-Confirm</span></span>
<span data-ttu-id="8b842-161">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8b842-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b842-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b842-162">-WhatIf</span></span>
<span data-ttu-id="8b842-163">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b842-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b842-164">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8b842-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b842-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b842-165">CommonParameters</span></span>
<span data-ttu-id="8b842-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b842-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b842-167">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8b842-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b842-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b842-168">INPUTS</span></span>

### <span data-ttu-id="8b842-169">System. String</span><span class="sxs-lookup"><span data-stu-id="8b842-169">System.String</span></span>

### <span data-ttu-id="8b842-170">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8b842-170">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8b842-171">Microsoft. Azure. Management. Keykasa. modeller. SkuName</span><span class="sxs-lookup"><span data-stu-id="8b842-171">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="8b842-172">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8b842-172">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8b842-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b842-173">OUTPUTS</span></span>

### <span data-ttu-id="8b842-174">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="8b842-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="8b842-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b842-175">NOTES</span></span>

## <span data-ttu-id="8b842-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b842-176">RELATED LINKS</span></span>

[<span data-ttu-id="8b842-177">Get-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="8b842-177">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="8b842-178">Remove-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="8b842-178">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
