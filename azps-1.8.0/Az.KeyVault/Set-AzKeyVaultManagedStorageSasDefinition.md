---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 65aeede664e0817bbc3465721a14580bd897d1f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916232"
---
# <span data-ttu-id="bcaab-101">Set-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="bcaab-101">Set-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="bcaab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcaab-102">SYNOPSIS</span></span>
<span data-ttu-id="bcaab-103">Belirli bir Anahtar Kasası yönetilen Azure depolama hesabı için anahtar kasası ile paylaşılan erişim Imzası (SAS) tanımı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="bcaab-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="bcaab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bcaab-104">SYNTAX</span></span>

### <span data-ttu-id="bcaab-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bcaab-105">Default (Default)</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcaab-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bcaab-106">ByInputObject</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bcaab-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bcaab-107">DESCRIPTION</span></span>
<span data-ttu-id="bcaab-108">Belirli bir Anahtar Kasası yönetilen Azure depolama hesabıyla paylaşılan erişim Imzası (SAS) tanımı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="bcaab-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="bcaab-109">Bu, SAS belirtecini bu SAS tanımına almak için kullanılabilecek bir gizli ayarlar da yapar.</span><span class="sxs-lookup"><span data-stu-id="bcaab-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="bcaab-110">SAS belirteci, bu parametreler ve Anahtar Kasası yönetilen Azure depolama hesabının etkin anahtarı kullanılarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="bcaab-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="bcaab-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bcaab-111">EXAMPLES</span></span>

### <span data-ttu-id="bcaab-112">Örnek 1: hesap türü SAS tanımını ayarlayın ve buna göre geçerli bir SAS belirteci edinin</span><span class="sxs-lookup"><span data-stu-id="bcaab-112">Example 1 : Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
```powershell
PS C:\> $sa = Get-AzStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzKeyVault -VaultName mykv
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod ([System.Timespan]::FromDays(180))
PS C:\> $sctx = New-AzStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

<span data-ttu-id="bcaab-113">' Mykv ' Kasası ' MySa ' Anahtar Kasası yönetilen depolama hesabında hesap SAS tanımı ' accountsas ' ayarlar.</span><span class="sxs-lookup"><span data-stu-id="bcaab-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="bcaab-114">Özellikle, yukarıdaki sıra aşağıdakileri gerçekleştirir:</span><span class="sxs-lookup"><span data-stu-id="bcaab-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="bcaab-115">bir (önceden var olan) depolama hesabını alır</span><span class="sxs-lookup"><span data-stu-id="bcaab-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="bcaab-116">bir (önceden var olan) bir Anahtar Kasası alır</span><span class="sxs-lookup"><span data-stu-id="bcaab-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="bcaab-117">kasaya bir Anahtar Kasası yönetimli bir depolama hesabı ekler, etkin anahtar olarak anahtar ayarlayın ve yeniden oluşturma dönemi 180 gün içinde yapılır</span><span class="sxs-lookup"><span data-stu-id="bcaab-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="bcaab-118">Anahtar ile belirtilen depolama hesabı için bir depolama bağlamı ayarlar</span><span class="sxs-lookup"><span data-stu-id="bcaab-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="bcaab-119">https üzerinden ve belirtilen başlangıç ve bitiş tarihleri ile birlikte tüm izinlerle birlikte, kaynak türleri hizmeti, dosya, tablo ve sıra için bir hesap SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bcaab-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="bcaab-120">kasada bir Anahtar Kasası yönetilen depolama SAS tanımını, SAS türü ' hesap ' olan SAS simgesi olarak yukarıda oluşturulan ve 30 gün için geçerli olan</span><span class="sxs-lookup"><span data-stu-id="bcaab-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="bcaab-121">SAS tanımına karşılık gelen Keykasa gizliliğine gerçek erişim belirtecini getirir</span><span class="sxs-lookup"><span data-stu-id="bcaab-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="bcaab-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bcaab-122">PARAMETERS</span></span>

### <span data-ttu-id="bcaab-123">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bcaab-123">-AccountName</span></span>
<span data-ttu-id="bcaab-124">Anahtar Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="bcaab-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="bcaab-125">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve yönetim depolama hesap adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bcaab-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcaab-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcaab-126">-DefaultProfile</span></span>
<span data-ttu-id="bcaab-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bcaab-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcaab-128">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="bcaab-128">-Disable</span></span>
<span data-ttu-id="bcaab-129">SAS belirtecinin oluşturulması için SAS tanımı kullanımını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="bcaab-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="bcaab-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcaab-130">-InputObject</span></span>
<span data-ttu-id="bcaab-131">ManagedStorageAccount nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bcaab-131">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcaab-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="bcaab-132">-Name</span></span>
<span data-ttu-id="bcaab-133">Depolama SAS tanım adı.</span><span class="sxs-lookup"><span data-stu-id="bcaab-133">Storage sas definition name.</span></span> <span data-ttu-id="bcaab-134">Cmdlet, kasa adından depolama SAS tanımının FQDN 'sini, şu anda seçili olan ortamı, depolama hesabı adını ve SAS tanım adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bcaab-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcaab-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="bcaab-135">-SasType</span></span>
<span data-ttu-id="bcaab-136">Depolama SAS türü.</span><span class="sxs-lookup"><span data-stu-id="bcaab-136">Storage SAS type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcaab-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="bcaab-137">-Tag</span></span>
<span data-ttu-id="bcaab-138">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="bcaab-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bcaab-139">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="bcaab-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcaab-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="bcaab-140">-TemplateUri</span></span>
<span data-ttu-id="bcaab-141">Depolama SAS tanım şablonu URI 'si.</span><span class="sxs-lookup"><span data-stu-id="bcaab-141">Storage SAS definition template uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcaab-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="bcaab-142">-ValidityPeriod</span></span>
<span data-ttu-id="bcaab-143">SAS belirtecinin geçerlilik süresini oluşturulduğu saatten ayarlamak için kullanılacak geçerlilik süresi</span><span class="sxs-lookup"><span data-stu-id="bcaab-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcaab-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bcaab-144">-VaultName</span></span>
<span data-ttu-id="bcaab-145">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="bcaab-145">Vault name.</span></span>
<span data-ttu-id="bcaab-146">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bcaab-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcaab-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="bcaab-147">-Confirm</span></span>
<span data-ttu-id="bcaab-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bcaab-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcaab-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcaab-149">-WhatIf</span></span>
<span data-ttu-id="bcaab-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bcaab-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcaab-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bcaab-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcaab-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcaab-152">CommonParameters</span></span>
<span data-ttu-id="bcaab-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bcaab-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcaab-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcaab-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcaab-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bcaab-155">INPUTS</span></span>

### <span data-ttu-id="bcaab-156">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultmanagedstorageaccountidentityıtem</span><span class="sxs-lookup"><span data-stu-id="bcaab-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="bcaab-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bcaab-157">OUTPUTS</span></span>

### <span data-ttu-id="bcaab-158">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="bcaab-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="bcaab-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bcaab-159">NOTES</span></span>

## <span data-ttu-id="bcaab-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bcaab-160">RELATED LINKS</span></span>

[<span data-ttu-id="bcaab-161">Azureâ € ‹ RM. â € ‹ Keyâ € ‹ kasa</span><span class="sxs-lookup"><span data-stu-id="bcaab-161">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/az.keyvault/)
