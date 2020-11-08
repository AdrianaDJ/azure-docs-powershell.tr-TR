---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 0da8ce1e7da509c140e5893240fadb37d7852ad8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280214"
---
# <span data-ttu-id="1ee90-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="1ee90-101">New-AzKeyVault</span></span>

## <span data-ttu-id="1ee90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ee90-102">SYNOPSIS</span></span>
<span data-ttu-id="1ee90-103">Bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ee90-103">Creates a key vault.</span></span>

## <span data-ttu-id="1ee90-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ee90-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ee90-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ee90-105">DESCRIPTION</span></span>
<span data-ttu-id="1ee90-106">**Yeni-Aztuş Kasası** cmdlet 'i, belirtilen kaynak grubunda bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ee90-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="1ee90-107">Bu cmdlet, şu anda oturum açmış olan kullanıcıya, anahtar kasasındaki anahtarları ve gizlilikleri eklemek, kaldırmak veya listelemek amacıyla izinler verir.</span><span class="sxs-lookup"><span data-stu-id="1ee90-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="1ee90-108">Not: yeni anahtar kasayı oluşturmaya çalıştığınızda, **abonelik ' Microsoft. Keykasa ' ad alanını kullanmak için kaydedilmemiş olduğunu** görürseniz, **register-azresourceprovider-Providernamespace "Microsoft. keykasa"** öğesini çalıştırın ve ardından **New-azkeykasa** komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="1ee90-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="1ee90-109">Daha fazla bilgi için Register-AzResourceProvider konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="1ee90-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="1ee90-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ee90-110">EXAMPLES</span></span>

### <span data-ttu-id="1ee90-111">Örnek 1: standart bir Anahtar Kasası oluşturma</span><span class="sxs-lookup"><span data-stu-id="1ee90-111">Example 1: Create a Standard key vault</span></span>
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

<span data-ttu-id="1ee90-112">Bu komut, Azure bölgesinde Contoso03Vault adlı bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ee90-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="1ee90-113">Komut, anahtar kasayı Group14 adlı kaynak grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="1ee90-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="1ee90-114">Komut, *SKU* parametresi için bir değer belirtmediğinden, standart bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ee90-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="1ee90-115">Örnek 2: Premium Anahtar Kasası oluşturma</span><span class="sxs-lookup"><span data-stu-id="1ee90-115">Example 2: Create a Premium key vault</span></span>
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

<span data-ttu-id="1ee90-116">Bu komut, önceki örnekte olduğu gibi bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ee90-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="1ee90-117">Bununla birlikte, Özel Anahtar Kasası oluşturmak için *SKU* parametresi için Premium değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ee90-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="1ee90-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="1ee90-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="1ee90-119">Anahtar Kasası oluşturma ve $myNetworkResId tarafından belirtilen sanal ağdan belirtilen IP adresine erişim izni vermek için ağ kurallarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ee90-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="1ee90-120">`New-AzKeyVaultNetworkRuleSetObject`Daha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="1ee90-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="1ee90-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ee90-121">PARAMETERS</span></span>

### <span data-ttu-id="1ee90-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ee90-122">-DefaultProfile</span></span>
<span data-ttu-id="1ee90-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1ee90-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ee90-124">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="1ee90-124">-EnabledForDeployment</span></span>
<span data-ttu-id="1ee90-125">Kaynak oluşturmada bu Anahtar Kasası, örneğin sanal makine oluştururken bu anahtar kasasına başvurulduğunda, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1ee90-125">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="1ee90-126">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="1ee90-126">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="1ee90-127">Azure disk şifreleme hizmeti 'nin, bu anahtar kasasından parolaları almasını ve anahtarları kaydırılmasını sağlayın.</span><span class="sxs-lookup"><span data-stu-id="1ee90-127">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="1ee90-128">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="1ee90-128">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="1ee90-129">Bu anahtar kasası bir şablon dağıtımında başvuruluyorsa, Azure Resource Manager 'ın bu anahtar kasasından gizli kod almasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="1ee90-129">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="1ee90-130">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="1ee90-130">-EnablePurgeProtection</span></span>
<span data-ttu-id="1ee90-131">Belirtilmişse, bu kasa için anında silinmeye karşı koruma etkinleştirilir; yumuşak silmenin da etkinleştirilmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="1ee90-131">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="1ee90-132">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="1ee90-132">-EnableRbacAuthorization</span></span>
<span data-ttu-id="1ee90-133">Belirtilmişse, veri eylemlerine rol tabanlı erişim denetimi (RBAC) tarafından yetki verme izni verir ve ardından kasa özelliklerinde belirtilen erişim ilkeleri yok sayılır.</span><span class="sxs-lookup"><span data-stu-id="1ee90-133">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="1ee90-134">Yönetim eylemlerine her zaman RBAC ile yetki verildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="1ee90-134">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="1ee90-135">-Konum</span><span class="sxs-lookup"><span data-stu-id="1ee90-135">-Location</span></span>
<span data-ttu-id="1ee90-136">Anahtar Kasası oluşturacağınız Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ee90-136">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="1ee90-137">Seçimlerinizi görmek için [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="1ee90-137">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

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

### <span data-ttu-id="1ee90-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="1ee90-138">-Name</span></span>
<span data-ttu-id="1ee90-139">Oluşturulacak Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ee90-139">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="1ee90-140">Ad, harf, sayı veya kısa çizgi bileşimleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="1ee90-140">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="1ee90-141">Ad bir harfle veya rakamla başlamalıdır ve bitmelidir.</span><span class="sxs-lookup"><span data-stu-id="1ee90-141">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="1ee90-142">Ad, evrensel olarak benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1ee90-142">The name must be universally unique.</span></span>

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

### <span data-ttu-id="1ee90-143">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1ee90-143">-NetworkRuleSet</span></span>
<span data-ttu-id="1ee90-144">Kasanın ağ kuralı kümesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ee90-144">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="1ee90-145">Belirli ağ konumlarından Anahtar Kasası erişilebilirliğini yönetir.</span><span class="sxs-lookup"><span data-stu-id="1ee90-145">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="1ee90-146">Oluşturan `New-AzKeyVaultNetworkRuleSetObject` .</span><span class="sxs-lookup"><span data-stu-id="1ee90-146">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

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

### <span data-ttu-id="1ee90-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ee90-147">-ResourceGroupName</span></span>
<span data-ttu-id="1ee90-148">Anahtar Kasası oluşturulacak varolan bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ee90-148">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="1ee90-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="1ee90-149">-Sku</span></span>
<span data-ttu-id="1ee90-150">Anahtar Kasası örneğinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ee90-150">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="1ee90-151">Her SKU için hangi özelliklerin kullanılabildiği hakkında bilgi için, Azure Anahtar Kasası fiyatlandırma web sitesine ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="1ee90-151">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee90-152">-Softdeleteretentionındays</span><span class="sxs-lookup"><span data-stu-id="1ee90-152">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="1ee90-153">Silinmiş kaynakların ne kadar süreyle korunacağını ve silinmiş durumda bir kasaya veya nesnenin temizlenmesinin ne kadar süreceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ee90-153">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="1ee90-154">Varsayılan değer 90 gündür.</span><span class="sxs-lookup"><span data-stu-id="1ee90-154">The default is 90 days.</span></span>

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

### <span data-ttu-id="1ee90-155">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1ee90-155">-Tag</span></span>
<span data-ttu-id="1ee90-156">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="1ee90-156">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1ee90-157">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="1ee90-157">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1ee90-158">-Onay</span><span class="sxs-lookup"><span data-stu-id="1ee90-158">-Confirm</span></span>
<span data-ttu-id="1ee90-159">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1ee90-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ee90-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ee90-160">-WhatIf</span></span>
<span data-ttu-id="1ee90-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ee90-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ee90-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1ee90-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ee90-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ee90-163">CommonParameters</span></span>
<span data-ttu-id="1ee90-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ee90-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ee90-165">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1ee90-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ee90-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ee90-166">INPUTS</span></span>

### <span data-ttu-id="1ee90-167">System. String</span><span class="sxs-lookup"><span data-stu-id="1ee90-167">System.String</span></span>

### <span data-ttu-id="1ee90-168">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1ee90-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1ee90-169">Microsoft. Azure. Management. Keykasa. modeller. SkuName</span><span class="sxs-lookup"><span data-stu-id="1ee90-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="1ee90-170">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1ee90-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1ee90-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ee90-171">OUTPUTS</span></span>

### <span data-ttu-id="1ee90-172">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="1ee90-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="1ee90-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ee90-173">NOTES</span></span>

## <span data-ttu-id="1ee90-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ee90-174">RELATED LINKS</span></span>

[<span data-ttu-id="1ee90-175">Get-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="1ee90-175">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="1ee90-176">Remove-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="1ee90-176">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
