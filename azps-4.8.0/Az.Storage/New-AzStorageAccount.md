---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 022c27b3eec589e395e1044f165ee9f8f17d1cad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273806"
---
# <span data-ttu-id="6b8b1-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6b8b1-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="6b8b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b8b1-102">SYNOPSIS</span></span>
<span data-ttu-id="6b8b1-103">Depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-103">Creates a Storage account.</span></span>

## <span data-ttu-id="6b8b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b8b1-104">SYNTAX</span></span>

### <span data-ttu-id="6b8b1-105">AzureActiveDirectoryDomainServicesForFile (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6b8b1-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b8b1-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="6b8b1-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare]
 [-EnableActiveDirectoryDomainServicesForFile <Boolean>] [-ActiveDirectoryDomainName <String>]
 [-ActiveDirectoryNetBiosDomainName <String>] [-ActiveDirectoryForestName <String>]
 [-ActiveDirectoryDomainGuid <String>] [-ActiveDirectoryDomainSid <String>]
 [-ActiveDirectoryAzureStorageSid <String>] [-AsJob] [-EncryptionKeyTypeForTable <String>]
 [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>]
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b8b1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b8b1-107">DESCRIPTION</span></span>
<span data-ttu-id="6b8b1-108">**New-AzStorageAccount** cmdlet 'ı bir Azure depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="6b8b1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b8b1-109">EXAMPLES</span></span>

### <span data-ttu-id="6b8b1-110">Örnek 1: depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="6b8b1-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="6b8b1-111">Bu komut MyResourceGroup kaynak grubu adı için bir depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="6b8b1-112">Örnek 2: BlobStorage türü ve Hot AccessTier ile BLOB depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="6b8b1-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="6b8b1-113">Bu komut, BlobStorage türü ve Hot AccessTier içeren bir BLOB depolama hesabı oluşturur</span><span class="sxs-lookup"><span data-stu-id="6b8b1-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="6b8b1-114">Örnek 3: StorageV2 türünde bir depolama hesabı oluşturun ve Azure Keykasa için bir kimlik oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="6b8b1-115">Bu komut, StorageV2 türünde bir depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="6b8b1-116">Ayrıca, Azure Keykasası aracılığıyla hesap anahtarlarını yönetmek için kullanılabilecek bir kimlik oluşturur ve bunu atar.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="6b8b1-117">Örnek 4: JSON 'den NetworkRuleSet ile depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="6b8b1-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="6b8b1-118">Bu komut, JSON 'den NetworkRuleSet özelliğine sahip bir depolama hesabı oluşturur</span><span class="sxs-lookup"><span data-stu-id="6b8b1-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="6b8b1-119">Örnek 5: hiyerarşik ad alanı etkinleştirilmiş bir depolama hesabı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="6b8b1-120">Bu komut hiyerarşik ad alanı etkinleştirilmiş bir depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="6b8b1-121">Örnek 6: Azure dosyaları için AAD DS kimlik doğrulaması ile depolama hesabı oluşturun ve büyük dosya paylaşımını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="6b8b1-122">Bu komut, Azure dosyaları AAD DS kimlik doğrulaması içeren bir depolama hesabı oluşturur ve büyük dosya paylaşımını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="6b8b1-123">Örnek 7: dosyaları etkinleştir Active Directory etki alanı hizmeti kimlik doğrulaması ile depolama hesabı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="6b8b1-124">Bu komut dosyaları Active Directory etki alanı hizmeti kimlik doğrulamasını etkinleştirmek için bir depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="6b8b1-125">Örnek 8: sıra ve tablo hizmetiyle depolama hesabı oluşturma hesap kapsamlı şifreleme anahtarını kullanın ve altyapı şifrelemesi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account -RequireInfrastructureEncryption

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\> $account.Encryption.RequireInfrastructureEncryption
True
```

<span data-ttu-id="6b8b1-126">Bu komut, kuyruk ve tablo hizmeti olan bir depolama hesabı oluşturur hesap kapsamlı şifreleme anahtarını kullanır ve altyapı şifrelemesi gerektirir, bu nedenle sıra ve tablo, blob ve dosya hizmeti ile aynı şifreleme anahtarını kullanır</span><span class="sxs-lookup"><span data-stu-id="6b8b1-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="6b8b1-127">Ardından depolama hesabı özelliklerini alın ve sıra ve tablo hizmetinin şifreleme anahtar öğesini ve RequireInfrastructureEncryption değerini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="6b8b1-128">Örnek 9: hesap oluşturma MinimumTlsVersion ve AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="6b8b1-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="6b8b1-129">Command, MinimumTlsVersion ve AllowBlobPublicAccess içeren bir hesap oluşturur ve ardından oluşturulan hesabın 2 özelliklerini gösterir</span><span class="sxs-lookup"><span data-stu-id="6b8b1-129">The command create account with MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the created account</span></span> 

## <span data-ttu-id="6b8b1-130">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b8b1-130">PARAMETERS</span></span>

### <span data-ttu-id="6b8b1-131">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="6b8b1-131">-AccessTier</span></span>
<span data-ttu-id="6b8b1-132">Bu cmdlet 'in oluşturduğu depolama hesabının erişim katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-132">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="6b8b1-133">Bu parametre için kabul edilebilir değerler: kolay ve serin.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-133">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="6b8b1-134">*Tür* parametresi Için blobstorage değeri belirtirseniz, *accesstier* parametresi için bir değer belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-134">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="6b8b1-135">Bu *tür* parametre Için bir depolama alanı değeri belirtirseniz, *accesstier* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-135">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="6b8b1-136">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="6b8b1-136">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="6b8b1-137">Azure depolama için güvenlik tanımlayıcısını (SID) belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-137">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="6b8b1-138">Bu parametre,-EnableActiveDirectoryDomainServicesForFile true olarak ayarlandığında ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-138">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="6b8b1-139">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="6b8b1-139">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="6b8b1-140">Etki alanı GUID 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-140">Specifies the domain GUID.</span></span> <span data-ttu-id="6b8b1-141">Bu parametre,-EnableActiveDirectoryDomainServicesForFile true olarak ayarlandığında ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-141">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="6b8b1-142">-Activedirectoryetkialanıadı</span><span class="sxs-lookup"><span data-stu-id="6b8b1-142">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="6b8b1-143">AD DNS sunucusunun yetkili olduğu birincil etki alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-143">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="6b8b1-144">Bu parametre,-EnableActiveDirectoryDomainServicesForFile true olarak ayarlandığında ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-144">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="6b8b1-145">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="6b8b1-145">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="6b8b1-146">Güvenlik tanımlayıcısını (SID) belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-146">Specifies the security identifier (SID).</span></span> <span data-ttu-id="6b8b1-147">Bu parametre,-EnableActiveDirectoryDomainServicesForFile true olarak ayarlandığında ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-147">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="6b8b1-148">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="6b8b1-148">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="6b8b1-149">Alınacak Active Directory ormanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-149">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="6b8b1-150">Bu parametre,-EnableActiveDirectoryDomainServicesForFile true olarak ayarlandığında ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-150">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="6b8b1-151">-Activedirectorynetbiosetkialanıadı</span><span class="sxs-lookup"><span data-stu-id="6b8b1-151">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="6b8b1-152">NetBIOS etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-152">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="6b8b1-153">Bu parametre,-EnableActiveDirectoryDomainServicesForFile true olarak ayarlandığında ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-153">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="6b8b1-154">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="6b8b1-154">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="6b8b1-155">Depolama hesabındaki tüm blob veya kapsayıcılara genel erişime izin verin.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-155">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="6b8b1-156">Bu özellik için varsayılan yorumda doğrudur.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-156">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="6b8b1-157">-Iş</span><span class="sxs-lookup"><span data-stu-id="6b8b1-157">-AsJob</span></span>
<span data-ttu-id="6b8b1-158">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6b8b1-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b8b1-159">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="6b8b1-159">-AssignIdentity</span></span>
<span data-ttu-id="6b8b1-160">Azure Keykasa gibi temel yönetim hizmetleriyle kullanmak üzere bu depolama hesabı için yeni bir depolama hesabı kimliği oluşturup atayın.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-160">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="6b8b1-161">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="6b8b1-161">-CustomDomainName</span></span>
<span data-ttu-id="6b8b1-162">Depolama hesabının özel etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-162">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="6b8b1-163">Varsayılan değer depolama alanıdır.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-163">The default value is Storage.</span></span>

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

### <span data-ttu-id="6b8b1-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b8b1-164">-DefaultProfile</span></span>
<span data-ttu-id="6b8b1-165">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b8b1-166">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="6b8b1-166">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="6b8b1-167">Depolama hesabı için Azure dosyalarını etkinleştirme Active Directory etki alanı hizmeti kimlik doğrulaması.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-167">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8b1-168">-Enableazureactivedirectorydomainservicesforfıle</span><span class="sxs-lookup"><span data-stu-id="6b8b1-168">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="6b8b1-169">Depolama hesabı için Azure dosyalarını Azure Active Directory etki alanı hizmeti kimlik doğrulamasını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-169">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AzureActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8b1-170">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="6b8b1-170">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="6b8b1-171">Depolama hesabının hiyerarşik ad alanını etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-171">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="6b8b1-172">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="6b8b1-172">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="6b8b1-173">Depolama hesabının HTTPS trafiğinin yalnızca etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-173">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="6b8b1-174">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="6b8b1-174">-EnableLargeFileShare</span></span>
<span data-ttu-id="6b8b1-175">Depolama hesabının 5 EB kapasitesinden büyük dosya paylaşımlarını destekleyip desteklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-175">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="6b8b1-176">Hesap etkinleştirildikten sonra özellik devre dışı bırakılamaz.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-176">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="6b8b1-177">Şu anda yalnızca LRS ve ZRS çoğaltma türlerinde desteklenir, bu nedenle coğrafi artıklık hesaplarına yönelik hesap dönüşümleri mümkün olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-177">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="6b8b1-178">Daha fazla bilgi https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="6b8b1-178">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="6b8b1-179">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="6b8b1-179">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="6b8b1-180">Sıra için şifreleme anahtar öğesini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-180">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="6b8b1-181">Varsayılan değer hizmettir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-181">The default value is Service.</span></span>
<span data-ttu-id="6b8b1-182">-Hesap: sıra, hesap kapsamlı şifreleme anahtarıyla şifrelenir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-182">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="6b8b1-183">-Hizmet: sıra Service-Managed anahtarlarıyla her zaman şifrelenir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-183">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8b1-184">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="6b8b1-184">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="6b8b1-185">Tablo için şifreleme anahtar öğesini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-185">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="6b8b1-186">Varsayılan değer hizmettir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-186">The default value is Service.</span></span>
- <span data-ttu-id="6b8b1-187">Hesap: tablo, hesap kapsamlı şifreleme anahtarıyla şifrelenir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-187">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="6b8b1-188">Hizmet: tablo daima Service-Managed anahtarlarla şifrelenir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-188">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8b1-189">-Tür</span><span class="sxs-lookup"><span data-stu-id="6b8b1-189">-Kind</span></span>
<span data-ttu-id="6b8b1-190">Bu cmdlet 'in oluşturduğu depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-190">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="6b8b1-191">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6b8b1-191">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6b8b1-192">Alanını.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-192">Storage.</span></span> <span data-ttu-id="6b8b1-193">Blob, tablo, kuyruk, dosya ve disklerin depolanmasını destekleyen genel amaçlı depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-193">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="6b8b1-194">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-194">StorageV2.</span></span> <span data-ttu-id="6b8b1-195">Veri katmanlama gibi gelişmiş özellikleri içeren blob, tablo, kuyruk, dosya ve diskleri destekleyen genel amaçlı sürüm 2 (GPv2) depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-195">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="6b8b1-196">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-196">BlobStorage.</span></span> <span data-ttu-id="6b8b1-197">Yalnızca blob depolamasını destekleyen BLOB depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-197">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="6b8b1-198">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-198">BlockBlobStorage.</span></span> <span data-ttu-id="6b8b1-199">Yalnızca blok blob 'Ları depolamayı destekleyen BLOB depolama hesabını engelle.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-199">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="6b8b1-200">Dosya depolama.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-200">FileStorage.</span></span> <span data-ttu-id="6b8b1-201">Yalnızca dosyaların depolanmasını destekleyen dosya depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-201">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="6b8b1-202">Varsayılan değer StorageV2 ' dır.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-202">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: StorageV2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8b1-203">-Konum</span><span class="sxs-lookup"><span data-stu-id="6b8b1-203">-Location</span></span>
<span data-ttu-id="6b8b1-204">Oluşturulacak depolama hesabının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-204">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b8b1-205">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="6b8b1-205">-MinimumTlsVersion</span></span>
<span data-ttu-id="6b8b1-206">Depolama için isteklere izin verilecek en düşük TLS sürümü.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-206">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="6b8b1-207">Bu özellik için varsayılan yorumlamayı TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-207">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="6b8b1-208">-Ad</span><span class="sxs-lookup"><span data-stu-id="6b8b1-208">-Name</span></span>
<span data-ttu-id="6b8b1-209">Oluşturulacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-209">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="6b8b1-210">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b8b1-210">-NetworkRuleSet</span></span>
<span data-ttu-id="6b8b1-211">NetworkRuleSet, güvenlik duvarları ve sanal ağlar için bir dizi yapılandırma kuralı tanımlamak için kullanılır, ayrıca hizmetler gibi ağ özellikleri için değerlerin ayarlanmasını ve tanımlı kuralların hiçbiriyle eşleşmeyen isteklerin nasıl işleneceğini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-211">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="6b8b1-212">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="6b8b1-212">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="6b8b1-213">Hizmet, geri kalan veriler için platform yönetilen anahtarlarıyla ikincil bir şifreleme katmanı uygular.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-213">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="6b8b1-214">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b8b1-214">-ResourceGroupName</span></span>
<span data-ttu-id="6b8b1-215">Depolama hesabının ekleneceği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-215">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="6b8b1-216">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6b8b1-216">-SkuName</span></span>
<span data-ttu-id="6b8b1-217">Bu cmdlet 'in oluşturduğu depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-217">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="6b8b1-218">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6b8b1-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6b8b1-219">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-219">Standard_LRS.</span></span> <span data-ttu-id="6b8b1-220">Yerel olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-220">Locally-redundant storage.</span></span>
- <span data-ttu-id="6b8b1-221">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-221">Standard_ZRS.</span></span> <span data-ttu-id="6b8b1-222">Bölge ile yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-222">Zone-redundant storage.</span></span>
- <span data-ttu-id="6b8b1-223">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-223">Standard_GRS.</span></span> <span data-ttu-id="6b8b1-224">Coğrafi olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-224">Geo-redundant storage.</span></span>
- <span data-ttu-id="6b8b1-225">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-225">Standard_RAGRS.</span></span> <span data-ttu-id="6b8b1-226">Okuma erişimi coğrafi depolama.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-226">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="6b8b1-227">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-227">Premium_LRS.</span></span> <span data-ttu-id="6b8b1-228">Premium yerel olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-228">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="6b8b1-229">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-229">Premium_ZRS.</span></span> <span data-ttu-id="6b8b1-230">Premium bölge-yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-230">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="6b8b1-231">Standard_GZRS-Coğrafi-Yedekli bölge-yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-231">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="6b8b1-232">Standard_RAGZRS-Access coğrafi</span><span class="sxs-lookup"><span data-stu-id="6b8b1-232">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS, Standard_GZRS, Standard_RAGZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b8b1-233">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6b8b1-233">-Tag</span></span>
<span data-ttu-id="6b8b1-234">Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-234">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="6b8b1-235">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="6b8b1-235">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6b8b1-236">-Usealt etki alanı</span><span class="sxs-lookup"><span data-stu-id="6b8b1-236">-UseSubDomain</span></span>
<span data-ttu-id="6b8b1-237">Dolaylı CName doğrulamasının etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-237">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="6b8b1-238">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b8b1-238">CommonParameters</span></span>
<span data-ttu-id="6b8b1-239">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b8b1-239">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b8b1-240">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b8b1-240">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b8b1-241">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b8b1-241">INPUTS</span></span>

### <span data-ttu-id="6b8b1-242">System. String</span><span class="sxs-lookup"><span data-stu-id="6b8b1-242">System.String</span></span>

## <span data-ttu-id="6b8b1-243">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b8b1-243">OUTPUTS</span></span>

### <span data-ttu-id="6b8b1-244">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6b8b1-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="6b8b1-245">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b8b1-245">NOTES</span></span>

## <span data-ttu-id="6b8b1-246">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b8b1-246">RELATED LINKS</span></span>

[<span data-ttu-id="6b8b1-247">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6b8b1-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="6b8b1-248">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6b8b1-248">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="6b8b1-249">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6b8b1-249">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
