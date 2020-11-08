---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: 944241dc7434646272c7149d81b380996e71db8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109855"
---
# <span data-ttu-id="07d08-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="07d08-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="07d08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07d08-102">SYNOPSIS</span></span>
<span data-ttu-id="07d08-103">Belirtilen parametrelerle birlikte yapılandırma deposunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="07d08-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="07d08-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07d08-104">SYNTAX</span></span>

### <span data-ttu-id="07d08-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="07d08-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="07d08-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="07d08-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="07d08-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="07d08-107">DESCRIPTION</span></span>
<span data-ttu-id="07d08-108">Belirtilen parametrelerle birlikte yapılandırma deposunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="07d08-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="07d08-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07d08-109">EXAMPLES</span></span>

### <span data-ttu-id="07d08-110">Örnek 1: uygulama conifguration deposunda, sistem tarafından atanan yönetilen kimlikle veri şifrelemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="07d08-110">Example 1: Enable data encryption of the app conifguration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="07d08-111">Bu komut, sistem tarafından atanan yönetilen bir kimlik kullanarak Azure Anahtar Kasası 'nda depolanan bir anahtarla veri şifrelemeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="07d08-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="07d08-112">Kasa, yumuşak silme ve Temizleme korumasını etkinleştirmiş olmalıdır; yönetilen kimliğin şu anahtar izinlerine sahip olması gerekir: get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="07d08-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="07d08-113">Örnek 2: Kullanıcı tarafından atanan yönetilen kimlikle uygulama conifguration deposu 'nun veri şifrelemesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="07d08-113">Example 2: Enable data encryption of the app conifguration store by user-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $assignedIdentity.PrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test11 -EncryptionKeyIdentifier $key.Id -KeyVaultIdentityClientId $assignedIdentity.ClientId

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="07d08-114">Bu komut, Kullanıcı tarafından atanan yönetilen bir kimlik kullanılarak Azure Anahtar Kasası 'nda depolanan bir anahtarla veri şifrelemeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="07d08-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="07d08-115">Kullanıcı tarafından atanan kimliğin işaretli olması gerekir `-UserAssignedIdentity` .</span><span class="sxs-lookup"><span data-stu-id="07d08-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="07d08-116">Kasa, yumuşak silme ve Temizleme korumasını etkinleştirmiş olmalıdır; yönetilen kimliğin şu anahtar izinlerine sahip olması gerekir: get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="07d08-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="07d08-117">Örnek 3: uygulama conifguration deposu şifrelemesini devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="07d08-117">Example 3: Disable encryption of an app conifguration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="07d08-118">Bu komut, bir App conifguration Store şifrelemesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="07d08-118">This command disables encryption of an app conifguration store.</span></span>

### <span data-ttu-id="07d08-119">Örnek 3: bir App conifguration Store 'un SKU ve etiketini bir ardışık düzene göre güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="07d08-119">Example 3: Update sku and tag of an app conifguration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="07d08-120">Bu komut, bir uygulama conifguration mağazanın SKU ve etiketini ardışık düzene göre güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="07d08-120">This command updates sku and tag of an app conifguration store by pipeline.</span></span>

## <span data-ttu-id="07d08-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07d08-121">PARAMETERS</span></span>

### <span data-ttu-id="07d08-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="07d08-122">-AsJob</span></span>
<span data-ttu-id="07d08-123">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="07d08-123">Run the command as a job</span></span>

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

### <span data-ttu-id="07d08-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d08-124">-DefaultProfile</span></span>
<span data-ttu-id="07d08-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07d08-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07d08-126">-Encryptionkeyıdentifier</span><span class="sxs-lookup"><span data-stu-id="07d08-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="07d08-127">Verileri şifrelemek için kullanılan Anahtar Kasası anahtarının URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="07d08-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="07d08-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="07d08-128">-IdentityType</span></span>
<span data-ttu-id="07d08-129">Kullanılan yönetilen kimliğin türü.</span><span class="sxs-lookup"><span data-stu-id="07d08-129">The type of managed identity used.</span></span>
<span data-ttu-id="07d08-130">' Systemassignedancıuseratandı ' türü, örtülü olarak oluşturulmuş bir kimliği ve Kullanıcı tarafından atanan kimlikler kümesini içerir.</span><span class="sxs-lookup"><span data-stu-id="07d08-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="07d08-131">' None ' türü tüm kimlikleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="07d08-131">The type 'None' will remove any identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d08-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07d08-132">-InputObject</span></span>
<span data-ttu-id="07d08-133">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07d08-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07d08-134">-Kama</span><span class="sxs-lookup"><span data-stu-id="07d08-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="07d08-135">Anahtar kasasına erişmek için kullanılacak kimliğin istemci kimliği.</span><span class="sxs-lookup"><span data-stu-id="07d08-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="07d08-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="07d08-136">-Name</span></span>
<span data-ttu-id="07d08-137">Yapılandırma deposu adı.</span><span class="sxs-lookup"><span data-stu-id="07d08-137">The name of the configuration store.</span></span>

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

### <span data-ttu-id="07d08-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="07d08-138">-NoWait</span></span>
<span data-ttu-id="07d08-139">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="07d08-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="07d08-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07d08-140">-ResourceGroupName</span></span>
<span data-ttu-id="07d08-141">Kapsayıcı kayıt defterinin ait olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="07d08-141">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="07d08-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="07d08-142">-Sku</span></span>
<span data-ttu-id="07d08-143">Yapılandırma deposu SKU adı.</span><span class="sxs-lookup"><span data-stu-id="07d08-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="07d08-144">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="07d08-144">-SubscriptionId</span></span>
<span data-ttu-id="07d08-145">Microsoft Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="07d08-145">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="07d08-146">Etiketli</span><span class="sxs-lookup"><span data-stu-id="07d08-146">-Tag</span></span>
<span data-ttu-id="07d08-147">ARM kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="07d08-147">The ARM resource tags.</span></span>

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

### <span data-ttu-id="07d08-148">-Useratandidentity</span><span class="sxs-lookup"><span data-stu-id="07d08-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="07d08-149">Kaynakla ilişkili kullanıcı tarafından atanan kimliklerin listesi.</span><span class="sxs-lookup"><span data-stu-id="07d08-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="07d08-150">Kullanıcı tarafından atanan kimlik sözlüğü anahtarları şu formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} '.</span><span class="sxs-lookup"><span data-stu-id="07d08-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="07d08-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="07d08-151">-Confirm</span></span>
<span data-ttu-id="07d08-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="07d08-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07d08-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07d08-153">-WhatIf</span></span>
<span data-ttu-id="07d08-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="07d08-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07d08-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="07d08-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07d08-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d08-156">CommonParameters</span></span>
<span data-ttu-id="07d08-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07d08-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d08-158">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="07d08-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d08-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07d08-159">INPUTS</span></span>

### <span data-ttu-id="07d08-160">Microsoft. Azure. PowerShell. cmdlet. AppConfiguration. modeller. ıappconfigurationıdentity</span><span class="sxs-lookup"><span data-stu-id="07d08-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="07d08-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07d08-161">OUTPUTS</span></span>

### <span data-ttu-id="07d08-162">Microsoft. Azure. PowerShell. cmdlet. AppConfiguration. modeller. Api20200601. Iconationstore</span><span class="sxs-lookup"><span data-stu-id="07d08-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="07d08-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07d08-163">NOTES</span></span>

<span data-ttu-id="07d08-164">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="07d08-164">ALIASES</span></span>

<span data-ttu-id="07d08-165">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="07d08-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="07d08-166">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="07d08-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="07d08-167">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="07d08-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="07d08-168">INPUTOBJECT <IAppConfigurationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="07d08-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="07d08-169">`[ConfigStoreName <String>]`: Yapılandırma deposu adı.</span><span class="sxs-lookup"><span data-stu-id="07d08-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="07d08-170">`[GroupName <String>]`: Özel bağlantı kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="07d08-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="07d08-171">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="07d08-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="07d08-172">`[PrivateEndpointConnectionName <String>]`: Özel uç noktası bağlantı adı</span><span class="sxs-lookup"><span data-stu-id="07d08-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="07d08-173">`[ResourceGroupName <String>]`: Kapsayıcı kayıt defterinin ait olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="07d08-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="07d08-174">`[SubscriptionId <String>]`: Microsoft Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="07d08-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="07d08-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07d08-175">RELATED LINKS</span></span>



<span data-ttu-id="07d08-176">[Set-Azanahtarvaultaccesspolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [New-Azuseratanandentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="07d08-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>

