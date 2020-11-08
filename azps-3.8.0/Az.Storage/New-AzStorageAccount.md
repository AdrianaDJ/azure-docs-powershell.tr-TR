---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: c88e56a485f9e42daf229667ab4c07d7a7464578
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098624"
---
# <span data-ttu-id="6d47c-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d47c-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="6d47c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d47c-102">SYNOPSIS</span></span>
<span data-ttu-id="6d47c-103">Depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d47c-103">Creates a Storage account.</span></span>

## <span data-ttu-id="6d47c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d47c-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d47c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d47c-105">DESCRIPTION</span></span>
<span data-ttu-id="6d47c-106">**New-AzStorageAccount** cmdlet 'ı bir Azure depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d47c-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="6d47c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d47c-107">EXAMPLES</span></span>

### <span data-ttu-id="6d47c-108">Örnek 1: depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="6d47c-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="6d47c-109">Bu komut MyResourceGroup kaynak grubu adı için bir depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d47c-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="6d47c-110">Örnek 2: BlobStorage türü ve Hot AccessTier ile BLOB depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="6d47c-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="6d47c-111">Bu komut, BlobStorage türü ve Hot AccessTier içeren bir BLOB depolama hesabı oluşturur</span><span class="sxs-lookup"><span data-stu-id="6d47c-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="6d47c-112">Örnek 3: StorageV2 türünde bir depolama hesabı oluşturun ve Azure Keykasa için bir kimlik oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="6d47c-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="6d47c-113">Bu komut, StorageV2 türünde bir depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d47c-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="6d47c-114">Ayrıca, Azure Keykasası aracılığıyla hesap anahtarlarını yönetmek için kullanılabilecek bir kimlik oluşturur ve bunu atar.</span><span class="sxs-lookup"><span data-stu-id="6d47c-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="6d47c-115">Örnek 4: JSON 'den NetworkRuleSet ile depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="6d47c-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="6d47c-116">Bu komut, JSON 'den NetworkRuleSet özelliğine sahip bir depolama hesabı oluşturur</span><span class="sxs-lookup"><span data-stu-id="6d47c-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="6d47c-117">Örnek 5: hiyerarşik ad alanı etkinleştirilmiş bir depolama hesabı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6d47c-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="6d47c-118">Bu komut hiyerarşik ad alanı etkinleştirilmiş bir depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d47c-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="6d47c-119">Örnek 6: Azure dosyaları için AAD DS kimlik doğrulaması ile depolama hesabı oluşturun ve büyük dosya paylaşımını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="6d47c-119">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="6d47c-120">Bu komut, Azure dosyaları AAD DS kimlik doğrulaması içeren bir depolama hesabı oluşturur ve büyük dosya paylaşımını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-120">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share..</span></span>

### <span data-ttu-id="6d47c-121">Örnek 8: sıra ve tablo hizmetiyle depolama hesabı oluşturma hesap kapsamlı şifreleme anahtarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="6d47c-121">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account
```

<span data-ttu-id="6d47c-122">Bu komut, kuyruk ve tablo hizmeti olan bir depolama hesabı oluşturur; bu nedenle sıra ve tablo, blob ve dosya hizmeti ile aynı şifreleme anahtarını kullanacaktır.</span><span class="sxs-lookup"><span data-stu-id="6d47c-122">This command creates a Storage account with Queue and Table Service use account-scoped encryption key, so Queue and Table will use same encryption key with Blob and File service.</span></span> <span data-ttu-id="6d47c-123">Ardından depolama hesabı özelliklerini alın ve sıra ve tablo hizmetinin şifreleme anahtar öğesini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="6d47c-123">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service.</span></span>

## <span data-ttu-id="6d47c-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d47c-124">PARAMETERS</span></span>

### <span data-ttu-id="6d47c-125">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="6d47c-125">-AccessTier</span></span>
<span data-ttu-id="6d47c-126">Bu cmdlet 'in oluşturduğu depolama hesabının erişim katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-126">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="6d47c-127">Bu parametre için kabul edilebilir değerler: kolay ve serin.</span><span class="sxs-lookup"><span data-stu-id="6d47c-127">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="6d47c-128">*Tür* parametresi Için blobstorage değeri belirtirseniz, *accesstier* parametresi için bir değer belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-128">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="6d47c-129">Bu *tür* parametre Için bir depolama alanı değeri belirtirseniz, *accesstier* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="6d47c-129">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="6d47c-130">-Iş</span><span class="sxs-lookup"><span data-stu-id="6d47c-130">-AsJob</span></span>
<span data-ttu-id="6d47c-131">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6d47c-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d47c-132">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="6d47c-132">-AssignIdentity</span></span>
<span data-ttu-id="6d47c-133">Azure Keykasa gibi temel yönetim hizmetleriyle kullanmak üzere bu depolama hesabı için yeni bir depolama hesabı kimliği oluşturup atayın.</span><span class="sxs-lookup"><span data-stu-id="6d47c-133">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="6d47c-134">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="6d47c-134">-CustomDomainName</span></span>
<span data-ttu-id="6d47c-135">Depolama hesabının özel etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-135">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="6d47c-136">Varsayılan değer depolama alanıdır.</span><span class="sxs-lookup"><span data-stu-id="6d47c-136">The default value is Storage.</span></span>

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

### <span data-ttu-id="6d47c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d47c-137">-DefaultProfile</span></span>
<span data-ttu-id="6d47c-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d47c-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d47c-139">-Enableazureactivedirectorydomainservicesforfıle</span><span class="sxs-lookup"><span data-stu-id="6d47c-139">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="6d47c-140">Depolama hesabı için Azure dosyalarını Azure Active Directory etki alanı hizmeti kimlik doğrulamasını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="6d47c-140">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="6d47c-141">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="6d47c-141">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="6d47c-142">Depolama hesabının hiyerarşik ad alanını etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-142">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="6d47c-143">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="6d47c-143">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="6d47c-144">Depolama hesabının HTTPS trafiğinin yalnızca etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-144">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="6d47c-145">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="6d47c-145">-EnableLargeFileShare</span></span>
<span data-ttu-id="6d47c-146">Depolama hesabının 5 EB kapasitesinden büyük dosya paylaşımlarını destekleyip desteklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-146">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="6d47c-147">Hesap etkinleştirildikten sonra özellik devre dışı bırakılamaz.</span><span class="sxs-lookup"><span data-stu-id="6d47c-147">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="6d47c-148">Şu anda yalnızca LRS ve ZRS çoğaltma türlerinde desteklenir, bu nedenle coğrafi artıklık hesaplarına yönelik hesap dönüşümleri mümkün olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="6d47c-148">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="6d47c-149">Daha fazla bilgi https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="6d47c-149">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="6d47c-150">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="6d47c-150">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="6d47c-151">Sıra için şifreleme anahtar öğesini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6d47c-151">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="6d47c-152">Varsayılan değer hizmettir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-152">The default value is Service.</span></span>
<span data-ttu-id="6d47c-153">-Hesap: sıra, hesap kapsamlı şifreleme anahtarıyla şifrelenir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-153">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="6d47c-154">-Hizmet: sıra Service-Managed anahtarlarıyla her zaman şifrelenir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-154">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="6d47c-155">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="6d47c-155">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="6d47c-156">Tablo için şifreleme anahtar öğesini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6d47c-156">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="6d47c-157">Varsayılan değer hizmettir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-157">The default value is Service.</span></span>
- <span data-ttu-id="6d47c-158">Hesap: tablo, hesap kapsamlı şifreleme anahtarıyla şifrelenir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-158">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="6d47c-159">Hizmet: tablo daima Service-Managed anahtarlarla şifrelenir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-159">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="6d47c-160">-Tür</span><span class="sxs-lookup"><span data-stu-id="6d47c-160">-Kind</span></span>
<span data-ttu-id="6d47c-161">Bu cmdlet 'in oluşturduğu depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-161">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="6d47c-162">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6d47c-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6d47c-163">Alanını.</span><span class="sxs-lookup"><span data-stu-id="6d47c-163">Storage.</span></span> <span data-ttu-id="6d47c-164">Blob, tablo, kuyruk, dosya ve disklerin depolanmasını destekleyen genel amaçlı depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="6d47c-164">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="6d47c-165">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="6d47c-165">StorageV2.</span></span> <span data-ttu-id="6d47c-166">Veri katmanlama gibi gelişmiş özellikleri içeren blob, tablo, kuyruk, dosya ve diskleri destekleyen genel amaçlı sürüm 2 (GPv2) depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="6d47c-166">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="6d47c-167">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="6d47c-167">BlobStorage.</span></span> <span data-ttu-id="6d47c-168">Yalnızca blob depolamasını destekleyen BLOB depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="6d47c-168">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="6d47c-169">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="6d47c-169">BlockBlobStorage.</span></span> <span data-ttu-id="6d47c-170">Yalnızca blok blob 'Ları depolamayı destekleyen BLOB depolama hesabını engelle.</span><span class="sxs-lookup"><span data-stu-id="6d47c-170">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="6d47c-171">Dosya depolama.</span><span class="sxs-lookup"><span data-stu-id="6d47c-171">FileStorage.</span></span> <span data-ttu-id="6d47c-172">Yalnızca dosyaların depolanmasını destekleyen dosya depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="6d47c-172">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="6d47c-173">Varsayılan değer StorageV2 ' dır.</span><span class="sxs-lookup"><span data-stu-id="6d47c-173">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d47c-174">-Konum</span><span class="sxs-lookup"><span data-stu-id="6d47c-174">-Location</span></span>
<span data-ttu-id="6d47c-175">Oluşturulacak depolama hesabının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-175">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="6d47c-176">-Ad</span><span class="sxs-lookup"><span data-stu-id="6d47c-176">-Name</span></span>
<span data-ttu-id="6d47c-177">Oluşturulacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-177">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="6d47c-178">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d47c-178">-NetworkRuleSet</span></span>
<span data-ttu-id="6d47c-179">NetworkRuleSet, güvenlik duvarları ve sanal ağlar için bir dizi yapılandırma kuralı tanımlamak için kullanılır, ayrıca hizmetler gibi ağ özellikleri için değerlerin ayarlanmasını ve tanımlı kuralların hiçbiriyle eşleşmeyen isteklerin nasıl işleneceğini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6d47c-179">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="6d47c-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d47c-180">-ResourceGroupName</span></span>
<span data-ttu-id="6d47c-181">Depolama hesabının ekleneceği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-181">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="6d47c-182">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6d47c-182">-SkuName</span></span>
<span data-ttu-id="6d47c-183">Bu cmdlet 'in oluşturduğu depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-183">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="6d47c-184">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6d47c-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6d47c-185">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="6d47c-185">Standard_LRS.</span></span> <span data-ttu-id="6d47c-186">Yerel olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="6d47c-186">Locally-redundant storage.</span></span>
- <span data-ttu-id="6d47c-187">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="6d47c-187">Standard_ZRS.</span></span> <span data-ttu-id="6d47c-188">Bölge ile yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="6d47c-188">Zone-redundant storage.</span></span>
- <span data-ttu-id="6d47c-189">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="6d47c-189">Standard_GRS.</span></span> <span data-ttu-id="6d47c-190">Coğrafi olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="6d47c-190">Geo-redundant storage.</span></span>
- <span data-ttu-id="6d47c-191">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="6d47c-191">Standard_RAGRS.</span></span> <span data-ttu-id="6d47c-192">Okuma erişimi coğrafi depolama.</span><span class="sxs-lookup"><span data-stu-id="6d47c-192">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="6d47c-193">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="6d47c-193">Premium_LRS.</span></span> <span data-ttu-id="6d47c-194">Premium yerel olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="6d47c-194">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="6d47c-195">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="6d47c-195">Premium_ZRS.</span></span> <span data-ttu-id="6d47c-196">Premium bölge-yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="6d47c-196">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="6d47c-197">Standard_GZRS-Coğrafi-Yedekli bölge-yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="6d47c-197">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="6d47c-198">Standard_RAGZRS-Access coğrafi</span><span class="sxs-lookup"><span data-stu-id="6d47c-198">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="6d47c-199">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6d47c-199">-Tag</span></span>
<span data-ttu-id="6d47c-200">Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="6d47c-200">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="6d47c-201">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="6d47c-201">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6d47c-202">-Usealt etki alanı</span><span class="sxs-lookup"><span data-stu-id="6d47c-202">-UseSubDomain</span></span>
<span data-ttu-id="6d47c-203">Dolaylı CName doğrulamasının etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d47c-203">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="6d47c-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d47c-204">CommonParameters</span></span>
<span data-ttu-id="6d47c-205">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d47c-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d47c-206">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6d47c-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d47c-207">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d47c-207">INPUTS</span></span>

### <span data-ttu-id="6d47c-208">System. String</span><span class="sxs-lookup"><span data-stu-id="6d47c-208">System.String</span></span>

## <span data-ttu-id="6d47c-209">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d47c-209">OUTPUTS</span></span>

### <span data-ttu-id="6d47c-210">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d47c-210">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="6d47c-211">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d47c-211">NOTES</span></span>

## <span data-ttu-id="6d47c-212">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d47c-212">RELATED LINKS</span></span>

[<span data-ttu-id="6d47c-213">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d47c-213">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="6d47c-214">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d47c-214">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="6d47c-215">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d47c-215">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
