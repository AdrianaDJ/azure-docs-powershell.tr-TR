---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 0b5e34fe3d7fe4c680ac20da53a32e1e5bad36fa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275779"
---
# <span data-ttu-id="3853d-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3853d-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="3853d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3853d-102">SYNOPSIS</span></span>
<span data-ttu-id="3853d-103">Depolama hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3853d-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="3853d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3853d-104">SYNTAX</span></span>

### <span data-ttu-id="3853d-105">StorageEncryption (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3853d-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3853d-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="3853d-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3853d-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="3853d-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3853d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3853d-108">DESCRIPTION</span></span>
<span data-ttu-id="3853d-109">**Set-AzStorageAccount** cmdlet 'ı bir Azure Depolama hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3853d-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="3853d-110">Bu cmdlet 'i hesap türünü değiştirmek, müşteri etki alanını güncelleştirmek veya depolama hesabında etiketleri ayarlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3853d-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="3853d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3853d-111">EXAMPLES</span></span>

### <span data-ttu-id="3853d-112">Örnek 1: depolama hesabı türünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="3853d-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="3853d-113">Bu komut depolama hesabı türünü Standard_RAGRS olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3853d-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="3853d-114">Örnek 2: depolama hesabı için özel etki alanı ayarlama</span><span class="sxs-lookup"><span data-stu-id="3853d-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="3853d-115">Bu komut, bir depolama hesabı için özel bir etki alanı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3853d-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="3853d-116">Örnek 3: erişim katmanı değerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="3853d-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="3853d-117">Komut, erişim katmanı değerini Cool olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3853d-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="3853d-118">Örnek 4: özel etki alanı ve etiketleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="3853d-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="3853d-119">Komut, bir depolama hesabı için özel etki alanı ve etiketleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3853d-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="3853d-120">Örnek 5: şifreleme anahtar kaynağını Anahtar Kasası olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="3853d-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="3853d-121">Bu komut şifreleme anahtar kaynağını yeni oluşturulmuş bir Keykasa ile ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3853d-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="3853d-122">Örnek 6: ENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="3853d-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="3853d-123">Bu komut, şifreleme KeySource 'ı "Microsoft. Storage" olarak ayarladı</span><span class="sxs-lookup"><span data-stu-id="3853d-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="3853d-124">Örnek 7: JSON ile depolama hesabının NetworkRuleSet özelliğini ayarlama</span><span class="sxs-lookup"><span data-stu-id="3853d-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="3853d-125">Bu komut, JSON içeren bir depolama hesabının NetworkRuleSet özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3853d-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="3853d-126">Örnek 8: depolama hesabından NetworkRuleSet özelliğini alma ve bunu başka bir depolama hesabına ayarlama</span><span class="sxs-lookup"><span data-stu-id="3853d-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="3853d-127">İlk komut, depolama hesabından NetworkRuleSet özelliğini alır ve ikinci komut bunu başka bir depolama hesabına ayarlar</span><span class="sxs-lookup"><span data-stu-id="3853d-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="3853d-128">Örnek 9: tür "depolama" veya "Blobdepolama" olan bir depolama hesabını "StorageV2" türü depolama hesabına yükselt</span><span class="sxs-lookup"><span data-stu-id="3853d-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="3853d-129">Komut, "depolama" veya "Blobdeposu" olan bir depolama hesabını "StorageV2" türü depolama hesabına yükseltir.</span><span class="sxs-lookup"><span data-stu-id="3853d-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="3853d-130">Örnek 10: Azure dosyaları AAD DS kimlik doğrulamasını etkinleştirerek depolama hesabını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="3853d-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="3853d-131">Azure dosyaları AAD DS kimlik doğrulamasını etkinleştirerek depolama hesabını güncelleştirme komutu.</span><span class="sxs-lookup"><span data-stu-id="3853d-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="3853d-132">Örnek 11: dosyaları Active Directory etki alanı hizmeti kimlik doğrulamasını etkinleştirerek depolama hesabını güncelleyin ve dosya kimliği tabanlı kimlik doğrulama ayarını göster</span><span class="sxs-lookup"><span data-stu-id="3853d-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
        
PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AD

PS C:\> $account.AzureFilesIdentityBasedAuth.ActiveDirectoryProperties

DomainName        : mydomain.com
NetBiosDomainName : mydomain.com
ForestName        : mydomain.com
DomainGuid        : 12345678-1234-1234-1234-123456789012
DomainSid         : S-1-5-21-1234567890-1234567890-1234567890
AzureStorageSid   : S-1-5-21-1234567890-1234567890-1234567890-1234
```

<span data-ttu-id="3853d-133">Komut, Azure Files Active Directory etki alanı hizmeti kimlik doğrulamasını etkinleştirerek bir depolama hesabını güncelleştirir ve dosya kimliği tabanlı kimlik doğrulama ayarını gösterir</span><span class="sxs-lookup"><span data-stu-id="3853d-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="3853d-134">Örnek 12: MinimumTlsVersion ve AllowBlobPublicAccess 'i ayarlama</span><span class="sxs-lookup"><span data-stu-id="3853d-134">Example 12: Set MinimumTlsVersion and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="3853d-135">Komut MinimumTlsVersion ve AllowBlobPublicAccess değerini ayarlar ve sonra hesabın 2 özelliklerini gösterir</span><span class="sxs-lookup"><span data-stu-id="3853d-135">The command sets MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the account</span></span> 

## <span data-ttu-id="3853d-136">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3853d-136">PARAMETERS</span></span>

### <span data-ttu-id="3853d-137">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="3853d-137">-AccessTier</span></span>
<span data-ttu-id="3853d-138">Bu cmdlet 'in değiştirdiği depolama hesabının erişim katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3853d-138">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="3853d-139">Bu parametre için kabul edilebilir değerler: kolay ve serin.</span><span class="sxs-lookup"><span data-stu-id="3853d-139">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="3853d-140">Erişim katmanını değiştirirseniz, ek ücretler ortaya çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="3853d-140">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="3853d-141">Daha fazla bilgi [için bkz.](http://go.microsoft.com/fwlink/?LinkId=786482)</span><span class="sxs-lookup"><span data-stu-id="3853d-141">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="3853d-142">Depolama hesabında tür StorageV2 veya Blobdepolama alanı varsa, *Accesstier* parametresini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3853d-142">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="3853d-143">Depolama hesabının depolama alanı türü varsa, *Accesstier* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="3853d-143">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-144">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="3853d-144">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="3853d-145">Azure depolama için güvenlik tanımlayıcısını (SID) belirtir.</span><span class="sxs-lookup"><span data-stu-id="3853d-145">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="3853d-146">Bu parametre,-EnableActiveDirectoryDomainServicesForFile true olarak ayarlandığında ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3853d-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-147">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="3853d-147">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="3853d-148">Etki alanı GUID 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3853d-148">Specifies the domain GUID.</span></span> <span data-ttu-id="3853d-149">Bu parametre,-EnableActiveDirectoryDomainServicesForFile true olarak ayarlandığında ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3853d-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-150">-Activedirectoryetkialanıadı</span><span class="sxs-lookup"><span data-stu-id="3853d-150">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="3853d-151">AD DNS sunucusunun yetkili olduğu birincil etki alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3853d-151">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="3853d-152">Bu parametre,-EnableActiveDirectoryDomainServicesForFile true olarak ayarlandığında ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3853d-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-153">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="3853d-153">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="3853d-154">Güvenlik tanımlayıcısını (SID) belirtir.</span><span class="sxs-lookup"><span data-stu-id="3853d-154">Specifies the security identifier (SID).</span></span> <span data-ttu-id="3853d-155">Bu parametre,-EnableActiveDirectoryDomainServicesForFile true olarak ayarlandığında ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3853d-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-156">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="3853d-156">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="3853d-157">Alınacak Active Directory ormanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3853d-157">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="3853d-158">Bu parametre,-EnableActiveDirectoryDomainServicesForFile true olarak ayarlandığında ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3853d-158">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-159">-Activedirectorynetbiosetkialanıadı</span><span class="sxs-lookup"><span data-stu-id="3853d-159">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="3853d-160">NetBIOS etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3853d-160">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="3853d-161">Bu parametre,-EnableActiveDirectoryDomainServicesForFile true olarak ayarlandığında ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3853d-161">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-162">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="3853d-162">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="3853d-163">Depolama hesabındaki tüm blob veya kapsayıcılara genel erişime izin verin veya vermeyin.</span><span class="sxs-lookup"><span data-stu-id="3853d-163">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-164">-Iş</span><span class="sxs-lookup"><span data-stu-id="3853d-164">-AsJob</span></span>
<span data-ttu-id="3853d-165">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3853d-165">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3853d-166">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="3853d-166">-AssignIdentity</span></span>
<span data-ttu-id="3853d-167">Azure Keykasa gibi temel yönetim hizmetleriyle kullanmak üzere bu depolama hesabı için yeni bir depolama hesabı kimliği oluşturup atayın.</span><span class="sxs-lookup"><span data-stu-id="3853d-167">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="3853d-168">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="3853d-168">-CustomDomainName</span></span>
<span data-ttu-id="3853d-169">Özel etki alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3853d-169">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="3853d-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3853d-170">-DefaultProfile</span></span>
<span data-ttu-id="3853d-171">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3853d-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3853d-172">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="3853d-172">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="3853d-173">Depolama hesabı için Azure dosyalarını etkinleştirme Active Directory etki alanı hizmeti kimlik doğrulaması.</span><span class="sxs-lookup"><span data-stu-id="3853d-173">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-174">-Enableazureactivedirectorydomainservicesforfıle</span><span class="sxs-lookup"><span data-stu-id="3853d-174">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="3853d-175">Depolama hesabı için Azure dosyalarını etkinleştirme Active Directory etki alanı hizmeti kimlik doğrulaması.</span><span class="sxs-lookup"><span data-stu-id="3853d-175">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StorageEncryption, KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-176">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="3853d-176">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="3853d-177">Depolama hesabının HTTPS trafiğinin yalnızca etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3853d-177">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-178">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="3853d-178">-EnableLargeFileShare</span></span>
<span data-ttu-id="3853d-179">Depolama hesabının 5 EB kapasitesinden büyük dosya paylaşımlarını destekleyip desteklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3853d-179">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="3853d-180">Hesap etkinleştirildikten sonra özellik devre dışı bırakılamaz.</span><span class="sxs-lookup"><span data-stu-id="3853d-180">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="3853d-181">Şu anda yalnızca LRS ve ZRS çoğaltma türlerinde desteklenir, bu nedenle coğrafi artıklık hesaplarına yönelik hesap dönüşümleri mümkün olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="3853d-181">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="3853d-182">Daha fazla bilgi https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="3853d-182">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="3853d-183">-Force</span><span class="sxs-lookup"><span data-stu-id="3853d-183">-Force</span></span>
<span data-ttu-id="3853d-184">Değişikliğin depolama hesabına yazılmasını zorlar.</span><span class="sxs-lookup"><span data-stu-id="3853d-184">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="3853d-185">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="3853d-185">-KeyName</span></span>
<span data-ttu-id="3853d-186">Anahtar Kasası ile şifrelemeyi etkinleştirmek için-KeyvaultEncryption kullanıyorsanız, bu seçenekle KeyName özelliğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="3853d-186">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-187">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="3853d-187">-KeyvaultEncryption</span></span>
<span data-ttu-id="3853d-188">Depolama hizmeti şifrelemesi kullanırken şifreleme anahtarları için Microsoft Keykasası kullanılıp kullanılmayacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3853d-188">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="3853d-189">KeyName, KeyVersion ve KeyVaultUri hepsi ayarlanmışsa, KeySource bu parametrenin ayarlanmış olup olmadığını Microsoft. Keykasa olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="3853d-189">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-190">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="3853d-190">-KeyVaultUri</span></span>
<span data-ttu-id="3853d-191">-KeyvaultEncryption parametresini belirterek Anahtar Kasası şifrelemesini kullanırken, anahtar kasaya URI 'yi belirtmek için bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="3853d-191">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-192">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="3853d-192">-KeyVersion</span></span>
<span data-ttu-id="3853d-193">-KeyvaultEncryption parametresini belirterek Anahtar Kasası şifrelemesini kullanırken, anahtar sürümüne URI 'yi belirtmek için bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="3853d-193">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-194">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="3853d-194">-MinimumTlsVersion</span></span>
<span data-ttu-id="3853d-195">Depolama için isteklere izin verilecek en düşük TLS sürümü.</span><span class="sxs-lookup"><span data-stu-id="3853d-195">The minimum TLS version to be permitted on requests to storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLS1_0, TLS1_1, TLS1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-196">-Ad</span><span class="sxs-lookup"><span data-stu-id="3853d-196">-Name</span></span>
<span data-ttu-id="3853d-197">Değiştirilecek depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3853d-197">Specifies the name of the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-198">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="3853d-198">-NetworkRuleSet</span></span>
<span data-ttu-id="3853d-199">NetworkRuleSet, güvenlik duvarları ve sanal ağlar için bir dizi yapılandırma kuralı tanımlamak için kullanılır, ayrıca hizmetler gibi ağ özellikleri için değerlerin ayarlanmasını ve tanımlı kuralların hiçbiriyle eşleşmeyen isteklerin nasıl işleneceğini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3853d-199">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3853d-200">-ResourceGroupName</span></span>
<span data-ttu-id="3853d-201">Depolama hesabının değiştirileceği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3853d-201">Specifies the name of the resource group in which to modify the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-202">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3853d-202">-SkuName</span></span>
<span data-ttu-id="3853d-203">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3853d-203">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="3853d-204">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3853d-204">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3853d-205">Standard_LRS-yerel olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="3853d-205">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="3853d-206">Standard_ZRS bölge-yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="3853d-206">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="3853d-207">Standard_GRS-coğrafi olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="3853d-207">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="3853d-208">Standard_RAGRS-Access coğrafi yedekli depolama alanı.</span><span class="sxs-lookup"><span data-stu-id="3853d-208">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="3853d-209">Premium_LRS-Premium yerel olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="3853d-209">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="3853d-210">Standard_GZRS-Coğrafi-Yedekli bölge-yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="3853d-210">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="3853d-211">Standard_RAGZRS-Access coğrafi</span><span class="sxs-lookup"><span data-stu-id="3853d-211">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="3853d-212">Standard_ZRS ve Premium_LRS türlerini diğer hesap türleriyle değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="3853d-212">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="3853d-213">Diğer hesap türlerini Standard_ZRS veya Premium_LRS olarak değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="3853d-213">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Standard_GZRS, Standard_RAGZRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-214">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="3853d-214">-StorageEncryption</span></span>
<span data-ttu-id="3853d-215">Depolama hesabı şifrelemesinin Microsoft tarafından yönetilen anahtarları kullanacak şekilde belirlenmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3853d-215">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-216">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3853d-216">-Tag</span></span>
<span data-ttu-id="3853d-217">Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="3853d-217">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="3853d-218">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="3853d-218">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3853d-219">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="3853d-219">-UpgradeToStorageV2</span></span>
<span data-ttu-id="3853d-220">Depolama hesabı türünü depolama alanından veya BlobStorage StorageV2 uygulamasına yükseltme.</span><span class="sxs-lookup"><span data-stu-id="3853d-220">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="3853d-221">-Usealt etki alanı</span><span class="sxs-lookup"><span data-stu-id="3853d-221">-UseSubDomain</span></span>
<span data-ttu-id="3853d-222">Dolaylı CName doğrulamasının etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3853d-222">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-223">-Onay</span><span class="sxs-lookup"><span data-stu-id="3853d-223">-Confirm</span></span>
<span data-ttu-id="3853d-224">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3853d-224">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3853d-225">-WhatIf</span></span>
<span data-ttu-id="3853d-226">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3853d-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3853d-227">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3853d-227">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853d-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3853d-228">CommonParameters</span></span>
<span data-ttu-id="3853d-229">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3853d-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3853d-230">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3853d-230">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3853d-231">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3853d-231">INPUTS</span></span>

### <span data-ttu-id="3853d-232">System. String</span><span class="sxs-lookup"><span data-stu-id="3853d-232">System.String</span></span>

### <span data-ttu-id="3853d-233">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3853d-233">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3853d-234">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3853d-234">OUTPUTS</span></span>

### <span data-ttu-id="3853d-235">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3853d-235">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="3853d-236">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3853d-236">NOTES</span></span>

## <span data-ttu-id="3853d-237">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3853d-237">RELATED LINKS</span></span>

[<span data-ttu-id="3853d-238">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3853d-238">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="3853d-239">Yeni-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3853d-239">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="3853d-240">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3853d-240">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
