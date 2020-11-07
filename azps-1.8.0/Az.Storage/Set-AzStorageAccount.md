---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 2850499ddfee121c5e51325eae5f9fab475ec944
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758548"
---
# <span data-ttu-id="843f3-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="843f3-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="843f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="843f3-102">SYNOPSIS</span></span>
<span data-ttu-id="843f3-103">Depolama hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="843f3-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="843f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="843f3-104">SYNTAX</span></span>

### <span data-ttu-id="843f3-105">StorageEncryption (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="843f3-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="843f3-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="843f3-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="843f3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="843f3-107">DESCRIPTION</span></span>
<span data-ttu-id="843f3-108">**Set-AzStorageAccount** cmdlet 'ı bir Azure Depolama hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="843f3-108">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="843f3-109">Bu cmdlet 'i hesap türünü değiştirmek, müşteri etki alanını güncelleştirmek veya depolama hesabında etiketleri ayarlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="843f3-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="843f3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="843f3-110">EXAMPLES</span></span>

### <span data-ttu-id="843f3-111">Örnek 1: depolama hesabı türünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="843f3-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="843f3-112">Bu komut depolama hesabı türünü Standard_RAGRS olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="843f3-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="843f3-113">Örnek 2: depolama hesabı için özel etki alanı ayarlama</span><span class="sxs-lookup"><span data-stu-id="843f3-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="843f3-114">Bu komut, bir depolama hesabı için özel bir etki alanı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="843f3-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="843f3-115">Örnek 3: erişim katmanı değerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="843f3-115">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="843f3-116">Komut, erişim katmanı değerini Cool olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="843f3-116">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="843f3-117">Örnek 4: özel etki alanı ve etiketleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="843f3-117">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="843f3-118">Komut, bir depolama hesabı için özel etki alanı ve etiketleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="843f3-118">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="843f3-119">Örnek 5: şifreleme anahtar kaynağını Anahtar Kasası olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="843f3-119">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="843f3-120">Bu komut şifreleme anahtar kaynağını yeni oluşturulmuş bir Keykasa ile ayarlar.</span><span class="sxs-lookup"><span data-stu-id="843f3-120">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="843f3-121">Örnek 6: ENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="843f3-121">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="843f3-122">Bu komut, şifreleme KeySource 'ı "Microsoft. Storage" olarak ayarladı</span><span class="sxs-lookup"><span data-stu-id="843f3-122">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="843f3-123">Örnek 7: JSON ile depolama hesabının NetworkRuleSet özelliğini ayarlama</span><span class="sxs-lookup"><span data-stu-id="843f3-123">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="843f3-124">Bu komut, JSON içeren bir depolama hesabının NetworkRuleSet özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="843f3-124">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="843f3-125">Örnek 8: depolama hesabından NetworkRuleSet özelliğini alma ve bunu başka bir depolama hesabına ayarlama</span><span class="sxs-lookup"><span data-stu-id="843f3-125">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="843f3-126">İlk komut, depolama hesabından NetworkRuleSet özelliğini alır ve ikinci komut bunu başka bir depolama hesabına ayarlar</span><span class="sxs-lookup"><span data-stu-id="843f3-126">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="843f3-127">Örnek 9: tür "depolama" veya "Blobdepolama" olan bir depolama hesabını "StorageV2" türü depolama hesabına yükselt</span><span class="sxs-lookup"><span data-stu-id="843f3-127">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="843f3-128">Komut, "depolama" veya "Blobdeposu" olan bir depolama hesabını "StorageV2" türü depolama hesabına yükseltir.</span><span class="sxs-lookup"><span data-stu-id="843f3-128">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

## <span data-ttu-id="843f3-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="843f3-129">PARAMETERS</span></span>

### <span data-ttu-id="843f3-130">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="843f3-130">-AccessTier</span></span>
<span data-ttu-id="843f3-131">Bu cmdlet 'in değiştirdiği depolama hesabının erişim katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="843f3-131">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="843f3-132">Bu parametre için kabul edilebilir değerler: kolay ve serin.</span><span class="sxs-lookup"><span data-stu-id="843f3-132">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="843f3-133">Erişim katmanını değiştirirseniz, ek ücretler ortaya çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="843f3-133">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="843f3-134">Daha fazla bilgi [için bkz.](https://go.microsoft.com/fwlink/?LinkId=786482)</span><span class="sxs-lookup"><span data-stu-id="843f3-134">For more information, see [Azure Blob Storage: Hot and cool storage tiers](https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="843f3-135">Depolama hesabında tür StorageV2 veya Blobdepolama alanı varsa, *Accesstier* parametresini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="843f3-135">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="843f3-136">Depolama hesabının depolama alanı türü varsa, *Accesstier* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="843f3-136">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="843f3-137">-Iş</span><span class="sxs-lookup"><span data-stu-id="843f3-137">-AsJob</span></span>
<span data-ttu-id="843f3-138">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="843f3-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="843f3-139">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="843f3-139">-AssignIdentity</span></span>
<span data-ttu-id="843f3-140">Azure Keykasa gibi temel yönetim hizmetleriyle kullanmak üzere bu depolama hesabı için yeni bir depolama hesabı kimliği oluşturup atayın.</span><span class="sxs-lookup"><span data-stu-id="843f3-140">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="843f3-141">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="843f3-141">-CustomDomainName</span></span>
<span data-ttu-id="843f3-142">Özel etki alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="843f3-142">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="843f3-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="843f3-143">-DefaultProfile</span></span>
<span data-ttu-id="843f3-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="843f3-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="843f3-145">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="843f3-145">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="843f3-146">Depolama hesabının HTTPS trafiğinin yalnızca etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="843f3-146">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="843f3-147">-Force</span><span class="sxs-lookup"><span data-stu-id="843f3-147">-Force</span></span>
<span data-ttu-id="843f3-148">Değişikliğin depolama hesabına yazılmasını zorlar.</span><span class="sxs-lookup"><span data-stu-id="843f3-148">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="843f3-149">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="843f3-149">-KeyName</span></span>
<span data-ttu-id="843f3-150">Anahtar Kasası ile şifrelemeyi etkinleştirmek için-KeyvaultEncryption kullanıyorsanız, bu seçenekle KeyName özelliğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="843f3-150">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="843f3-151">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="843f3-151">-KeyvaultEncryption</span></span>
<span data-ttu-id="843f3-152">Depolama hizmeti şifrelemesi kullanırken şifreleme anahtarları için Microsoft Keykasası kullanılıp kullanılmayacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="843f3-152">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="843f3-153">KeyName, KeyVersion ve KeyVaultUri hepsi ayarlanmışsa, KeySource bu parametrenin ayarlanmış olup olmadığını Microsoft. Keykasa olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="843f3-153">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="843f3-154">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="843f3-154">-KeyVaultUri</span></span>
<span data-ttu-id="843f3-155">-KeyvaultEncryption parametresini belirterek Anahtar Kasası şifrelemesini kullanırken, anahtar kasaya URI 'yi belirtmek için bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="843f3-155">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="843f3-156">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="843f3-156">-KeyVersion</span></span>
<span data-ttu-id="843f3-157">-KeyvaultEncryption parametresini belirterek Anahtar Kasası şifrelemesini kullanırken, anahtar sürümüne URI 'yi belirtmek için bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="843f3-157">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="843f3-158">-Ad</span><span class="sxs-lookup"><span data-stu-id="843f3-158">-Name</span></span>
<span data-ttu-id="843f3-159">Değiştirilecek depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="843f3-159">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="843f3-160">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="843f3-160">-NetworkRuleSet</span></span>
<span data-ttu-id="843f3-161">NetworkRuleSet, güvenlik duvarları ve sanal ağlar için bir dizi yapılandırma kuralı tanımlamak için kullanılır, ayrıca hizmetler gibi ağ özellikleri için değerlerin ayarlanmasını ve tanımlı kuralların hiçbiriyle eşleşmeyen isteklerin nasıl işleneceğini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="843f3-161">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="843f3-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="843f3-162">-ResourceGroupName</span></span>
<span data-ttu-id="843f3-163">Depolama hesabının değiştirileceği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="843f3-163">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="843f3-164">-SkuName</span><span class="sxs-lookup"><span data-stu-id="843f3-164">-SkuName</span></span>
<span data-ttu-id="843f3-165">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="843f3-165">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="843f3-166">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="843f3-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="843f3-167">Standard_LRS-yerel olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="843f3-167">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="843f3-168">Standard_ZRS bölge-yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="843f3-168">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="843f3-169">Standard_GRS-coğrafi olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="843f3-169">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="843f3-170">Standard_RAGRS-Access coğrafi yedekli depolama alanı.</span><span class="sxs-lookup"><span data-stu-id="843f3-170">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="843f3-171">Premium_LRS-Premium yerel olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="843f3-171">Premium_LRS - Premium locally-redundant storage.</span></span>
<span data-ttu-id="843f3-172">Standard_ZRS ve Premium_LRS türlerini diğer hesap türleriyle değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="843f3-172">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="843f3-173">Diğer hesap türlerini Standard_ZRS veya Premium_LRS olarak değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="843f3-173">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="843f3-174">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="843f3-174">-StorageEncryption</span></span>
<span data-ttu-id="843f3-175">Depolama hesabı şifrelemesinin Microsoft tarafından yönetilen anahtarları kullanacak şekilde belirlenmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="843f3-175">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="843f3-176">Etiketli</span><span class="sxs-lookup"><span data-stu-id="843f3-176">-Tag</span></span>
<span data-ttu-id="843f3-177">Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="843f3-177">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="843f3-178">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="843f3-178">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="843f3-179">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="843f3-179">-UpgradeToStorageV2</span></span>
<span data-ttu-id="843f3-180">Depolama hesabı türünü depolama alanından veya BlobStorage StorageV2 uygulamasına yükseltme.</span><span class="sxs-lookup"><span data-stu-id="843f3-180">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="843f3-181">-Usealt etki alanı</span><span class="sxs-lookup"><span data-stu-id="843f3-181">-UseSubDomain</span></span>
<span data-ttu-id="843f3-182">Dolaylı CName doğrulamasının etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="843f3-182">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="843f3-183">-Onay</span><span class="sxs-lookup"><span data-stu-id="843f3-183">-Confirm</span></span>
<span data-ttu-id="843f3-184">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="843f3-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="843f3-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="843f3-185">-WhatIf</span></span>
<span data-ttu-id="843f3-186">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="843f3-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="843f3-187">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="843f3-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="843f3-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="843f3-188">CommonParameters</span></span>
<span data-ttu-id="843f3-189">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="843f3-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="843f3-190">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="843f3-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="843f3-191">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="843f3-191">INPUTS</span></span>

### <span data-ttu-id="843f3-192">System. String</span><span class="sxs-lookup"><span data-stu-id="843f3-192">System.String</span></span>

### <span data-ttu-id="843f3-193">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="843f3-193">System.Collections.Hashtable</span></span>

## <span data-ttu-id="843f3-194">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="843f3-194">OUTPUTS</span></span>

### <span data-ttu-id="843f3-195">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="843f3-195">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="843f3-196">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="843f3-196">NOTES</span></span>

## <span data-ttu-id="843f3-197">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="843f3-197">RELATED LINKS</span></span>

[<span data-ttu-id="843f3-198">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="843f3-198">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="843f3-199">Yeni-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="843f3-199">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="843f3-200">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="843f3-200">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
