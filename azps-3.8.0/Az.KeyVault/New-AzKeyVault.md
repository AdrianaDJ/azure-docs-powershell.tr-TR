---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 067928930474d6210d96491a870d85226d2fd732
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096161"
---
# <span data-ttu-id="6c5e4-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="6c5e4-101">New-AzKeyVault</span></span>

## <span data-ttu-id="6c5e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c5e4-102">SYNOPSIS</span></span>
<span data-ttu-id="6c5e4-103">Bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-103">Creates a key vault.</span></span>

## <span data-ttu-id="6c5e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c5e4-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete] [-EnablePurgeProtection]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c5e4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c5e4-105">DESCRIPTION</span></span>
<span data-ttu-id="6c5e4-106">**Yeni-Aztuş Kasası** cmdlet 'i, belirtilen kaynak grubunda bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="6c5e4-107">Bu cmdlet, şu anda oturum açmış olan kullanıcıya, anahtar kasasındaki anahtarları ve gizlilikleri eklemek, kaldırmak veya listelemek amacıyla izinler verir.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="6c5e4-108">Not: yeni anahtar kasayı oluşturmaya çalıştığınızda, **abonelik ' Microsoft. Keykasa ' ad alanını kullanmak için kaydedilmemiş olduğunu** görürseniz, **register-azresourceprovider-Providernamespace "Microsoft. keykasa"** öğesini çalıştırın ve ardından **New-azkeykasa** komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="6c5e4-109">Daha fazla bilgi için Register-AzResourceProvider konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="6c5e4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c5e4-110">EXAMPLES</span></span>

### <span data-ttu-id="6c5e4-111">Örnek 1: standart bir Anahtar Kasası oluşturma</span><span class="sxs-lookup"><span data-stu-id="6c5e4-111">Example 1: Create a Standard key vault</span></span>
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

<span data-ttu-id="6c5e4-112">Bu komut, Azure bölgesinde Contoso03Vault adlı bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="6c5e4-113">Komut, anahtar kasayı Group14 adlı kaynak grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="6c5e4-114">Komut, *SKU* parametresi için bir değer belirtmediğinden, standart bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="6c5e4-115">Örnek 2: Premium Anahtar Kasası oluşturma</span><span class="sxs-lookup"><span data-stu-id="6c5e4-115">Example 2: Create a Premium key vault</span></span>
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

<span data-ttu-id="6c5e4-116">Bu komut, önceki örnekte olduğu gibi bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="6c5e4-117">Bununla birlikte, Özel Anahtar Kasası oluşturmak için *SKU* parametresi için Premium değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="6c5e4-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c5e4-118">PARAMETERS</span></span>

### <span data-ttu-id="6c5e4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c5e4-119">-DefaultProfile</span></span>
<span data-ttu-id="6c5e4-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6c5e4-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c5e4-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="6c5e4-121">-EnabledForDeployment</span></span>
<span data-ttu-id="6c5e4-122">Kaynak oluşturmada bu Anahtar Kasası, örneğin sanal makine oluştururken bu anahtar kasasına başvurulduğunda, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="6c5e4-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="6c5e4-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="6c5e4-124">Azure disk şifreleme hizmeti 'nin, bu anahtar kasasından parolaları almasını ve anahtarları kaydırılmasını sağlayın.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="6c5e4-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="6c5e4-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="6c5e4-126">Bu anahtar kasası bir şablon dağıtımında başvuruluyorsa, Azure Resource Manager 'ın bu anahtar kasasından gizli kod almasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="6c5e4-127">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="6c5e4-127">-EnablePurgeProtection</span></span>
<span data-ttu-id="6c5e4-128">Belirtilmişse, bu kasa için anında silinmeye karşı koruma etkinleştirilir; yumuşak silmenin da etkinleştirilmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-128">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="6c5e4-129">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="6c5e4-129">-EnableSoftDelete</span></span>
<span data-ttu-id="6c5e4-130">Bu anahtar kasası için yazılımla silme işlevinin etkinleştirildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-130">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="6c5e4-131">Yazılımdan silme etkinleştirildiğinde, bir yetkisiz kullanım süresi için bu anahtar kasası ve içeriğini silindikten sonra kurtarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-131">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>
<span data-ttu-id="6c5e4-132">Bu işlev hakkında daha fazla bilgi [için bkz.](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)</span><span class="sxs-lookup"><span data-stu-id="6c5e4-132">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="6c5e4-133">Nasıl yapılır yönergeleri için [PowerShell Ile Anahtar Kasası kolay silme 'yi kullanma](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell)konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-133">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

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

### <span data-ttu-id="6c5e4-134">-Konum</span><span class="sxs-lookup"><span data-stu-id="6c5e4-134">-Location</span></span>
<span data-ttu-id="6c5e4-135">Anahtar Kasası oluşturacağınız Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-135">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="6c5e4-136">Seçimlerinizi görmek için [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-136">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

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

### <span data-ttu-id="6c5e4-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="6c5e4-137">-Name</span></span>
<span data-ttu-id="6c5e4-138">Oluşturulacak Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-138">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="6c5e4-139">Ad, harf, sayı veya kısa çizgi bileşimleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-139">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="6c5e4-140">Ad bir harfle veya rakamla başlamalıdır ve bitmelidir.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-140">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="6c5e4-141">Ad, evrensel olarak benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-141">The name must be universally unique.</span></span>

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

### <span data-ttu-id="6c5e4-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c5e4-142">-ResourceGroupName</span></span>
<span data-ttu-id="6c5e4-143">Anahtar Kasası oluşturulacak varolan bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-143">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="6c5e4-144">-SKU</span><span class="sxs-lookup"><span data-stu-id="6c5e4-144">-Sku</span></span>
<span data-ttu-id="6c5e4-145">Anahtar Kasası örneğinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-145">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="6c5e4-146">Her SKU için hangi özelliklerin kullanılabildiği hakkında bilgi için, Azure Anahtar Kasası fiyatlandırma web sitesine ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="6c5e4-146">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

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

### <span data-ttu-id="6c5e4-147">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6c5e4-147">-Tag</span></span>
<span data-ttu-id="6c5e4-148">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6c5e4-149">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="6c5e4-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6c5e4-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="6c5e4-150">-Confirm</span></span>
<span data-ttu-id="6c5e4-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c5e4-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c5e4-152">-WhatIf</span></span>
<span data-ttu-id="6c5e4-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c5e4-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c5e4-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c5e4-155">CommonParameters</span></span>
<span data-ttu-id="6c5e4-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c5e4-157">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c5e4-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c5e4-158">INPUTS</span></span>

### <span data-ttu-id="6c5e4-159">System. String</span><span class="sxs-lookup"><span data-stu-id="6c5e4-159">System.String</span></span>

### <span data-ttu-id="6c5e4-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6c5e4-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6c5e4-161">Microsoft. Azure. Management. Keykasa. modeller. SkuName</span><span class="sxs-lookup"><span data-stu-id="6c5e4-161">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="6c5e4-162">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6c5e4-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6c5e4-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c5e4-163">OUTPUTS</span></span>

### <span data-ttu-id="6c5e4-164">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="6c5e4-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="6c5e4-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c5e4-165">NOTES</span></span>

## <span data-ttu-id="6c5e4-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c5e4-166">RELATED LINKS</span></span>

[<span data-ttu-id="6c5e4-167">Get-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="6c5e4-167">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="6c5e4-168">Remove-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="6c5e4-168">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
