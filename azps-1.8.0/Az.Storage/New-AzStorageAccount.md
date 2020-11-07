---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 316bcbd8efa101a53dc36ede5e56e2b9379f02e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758631"
---
# <span data-ttu-id="163a9-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="163a9-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="163a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="163a9-102">SYNOPSIS</span></span>
<span data-ttu-id="163a9-103">Depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="163a9-103">Creates a Storage account.</span></span>

## <span data-ttu-id="163a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="163a9-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="163a9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="163a9-105">DESCRIPTION</span></span>
<span data-ttu-id="163a9-106">**New-AzStorageAccount** cmdlet 'ı bir Azure depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="163a9-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="163a9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="163a9-107">EXAMPLES</span></span>

### <span data-ttu-id="163a9-108">Örnek 1: depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="163a9-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="163a9-109">Bu komut MyResourceGroup kaynak grubu adı için bir depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="163a9-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="163a9-110">Örnek 2: BlobStorage türü ve Hot AccessTier ile BLOB depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="163a9-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="163a9-111">Bu komut, BlobStorage türü ve Hot AccessTier içeren bir BLOB depolama hesabı oluşturur</span><span class="sxs-lookup"><span data-stu-id="163a9-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="163a9-112">Örnek 3: StorageV2 türünde bir depolama hesabı oluşturun ve Azure Keykasa için bir kimlik oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="163a9-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="163a9-113">Bu komut, StorageV2 türünde bir depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="163a9-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="163a9-114">Ayrıca, Azure Keykasası aracılığıyla hesap anahtarlarını yönetmek için kullanılabilecek bir kimlik oluşturur ve bunu atar.</span><span class="sxs-lookup"><span data-stu-id="163a9-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="163a9-115">Örnek 4: JSON 'den NetworkRuleSet ile depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="163a9-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="163a9-116">Bu komut, JSON 'den NetworkRuleSet özelliğine sahip bir depolama hesabı oluşturur</span><span class="sxs-lookup"><span data-stu-id="163a9-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="163a9-117">Örnek 5: hiyerarşik ad alanı etkinleştirilmiş bir depolama hesabı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="163a9-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="163a9-118">Bu komut hiyerarşik ad alanı etkinleştirilmiş bir depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="163a9-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

## <span data-ttu-id="163a9-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="163a9-119">PARAMETERS</span></span>

### <span data-ttu-id="163a9-120">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="163a9-120">-AccessTier</span></span>
<span data-ttu-id="163a9-121">Bu cmdlet 'in oluşturduğu depolama hesabının erişim katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="163a9-121">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="163a9-122">Bu parametre için kabul edilebilir değerler: kolay ve serin.</span><span class="sxs-lookup"><span data-stu-id="163a9-122">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="163a9-123">*Tür* parametresi Için blobstorage değeri belirtirseniz, *accesstier* parametresi için bir değer belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="163a9-123">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="163a9-124">Bu *tür* parametre Için bir depolama alanı değeri belirtirseniz, *accesstier* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="163a9-124">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="163a9-125">-Iş</span><span class="sxs-lookup"><span data-stu-id="163a9-125">-AsJob</span></span>
<span data-ttu-id="163a9-126">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="163a9-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="163a9-127">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="163a9-127">-AssignIdentity</span></span>
<span data-ttu-id="163a9-128">Azure Keykasa gibi temel yönetim hizmetleriyle kullanmak üzere bu depolama hesabı için yeni bir depolama hesabı kimliği oluşturup atayın.</span><span class="sxs-lookup"><span data-stu-id="163a9-128">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="163a9-129">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="163a9-129">-CustomDomainName</span></span>
<span data-ttu-id="163a9-130">Depolama hesabının özel etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="163a9-130">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="163a9-131">Varsayılan değer depolama alanıdır.</span><span class="sxs-lookup"><span data-stu-id="163a9-131">The default value is Storage.</span></span>

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

### <span data-ttu-id="163a9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="163a9-132">-DefaultProfile</span></span>
<span data-ttu-id="163a9-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="163a9-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="163a9-134">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="163a9-134">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="163a9-135">Depolama hesabının hiyerarşik ad alanını etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="163a9-135">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="163a9-136">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="163a9-136">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="163a9-137">Depolama hesabının HTTPS trafiğinin yalnızca etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="163a9-137">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="163a9-138">-Tür</span><span class="sxs-lookup"><span data-stu-id="163a9-138">-Kind</span></span>
<span data-ttu-id="163a9-139">Bu cmdlet 'in oluşturduğu depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="163a9-139">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="163a9-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="163a9-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="163a9-141">Alanını.</span><span class="sxs-lookup"><span data-stu-id="163a9-141">Storage.</span></span> <span data-ttu-id="163a9-142">Blob, tablo, kuyruk, dosya ve disklerin depolanmasını destekleyen genel amaçlı depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="163a9-142">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="163a9-143">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="163a9-143">StorageV2.</span></span> <span data-ttu-id="163a9-144">Veri katmanlama gibi gelişmiş özellikleri içeren blob, tablo, kuyruk, dosya ve diskleri destekleyen genel amaçlı sürüm 2 (GPv2) depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="163a9-144">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="163a9-145">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="163a9-145">BlobStorage.</span></span> <span data-ttu-id="163a9-146">Yalnızca blob depolamasını destekleyen BLOB depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="163a9-146">Blob Storage account which supports storage of Blobs only.</span></span>
<span data-ttu-id="163a9-147">Varsayılan değer depolama alanıdır.</span><span class="sxs-lookup"><span data-stu-id="163a9-147">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163a9-148">-Konum</span><span class="sxs-lookup"><span data-stu-id="163a9-148">-Location</span></span>
<span data-ttu-id="163a9-149">Oluşturulacak depolama hesabının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="163a9-149">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="163a9-150">-Ad</span><span class="sxs-lookup"><span data-stu-id="163a9-150">-Name</span></span>
<span data-ttu-id="163a9-151">Oluşturulacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="163a9-151">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="163a9-152">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="163a9-152">-NetworkRuleSet</span></span>
<span data-ttu-id="163a9-153">NetworkRuleSet, güvenlik duvarları ve sanal ağlar için bir dizi yapılandırma kuralı tanımlamak için kullanılır, ayrıca hizmetler gibi ağ özellikleri için değerlerin ayarlanmasını ve tanımlı kuralların hiçbiriyle eşleşmeyen isteklerin nasıl işleneceğini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="163a9-153">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="163a9-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="163a9-154">-ResourceGroupName</span></span>
<span data-ttu-id="163a9-155">Depolama hesabının ekleneceği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="163a9-155">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="163a9-156">-SkuName</span><span class="sxs-lookup"><span data-stu-id="163a9-156">-SkuName</span></span>
<span data-ttu-id="163a9-157">Bu cmdlet 'in oluşturduğu depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="163a9-157">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="163a9-158">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="163a9-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="163a9-159">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="163a9-159">Standard_LRS.</span></span> <span data-ttu-id="163a9-160">Yerel olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="163a9-160">Locally-redundant storage.</span></span>
- <span data-ttu-id="163a9-161">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="163a9-161">Standard_ZRS.</span></span> <span data-ttu-id="163a9-162">Bölge ile yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="163a9-162">Zone-redundant storage.</span></span>
- <span data-ttu-id="163a9-163">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="163a9-163">Standard_GRS.</span></span> <span data-ttu-id="163a9-164">Coğrafi olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="163a9-164">Geo-redundant storage.</span></span>
- <span data-ttu-id="163a9-165">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="163a9-165">Standard_RAGRS.</span></span> <span data-ttu-id="163a9-166">Okuma erişimi coğrafi depolama.</span><span class="sxs-lookup"><span data-stu-id="163a9-166">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="163a9-167">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="163a9-167">Premium_LRS.</span></span> <span data-ttu-id="163a9-168">Premium yerel olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="163a9-168">Premium locally-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="163a9-169">Etiketli</span><span class="sxs-lookup"><span data-stu-id="163a9-169">-Tag</span></span>
<span data-ttu-id="163a9-170">Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="163a9-170">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="163a9-171">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="163a9-171">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="163a9-172">-Usealt etki alanı</span><span class="sxs-lookup"><span data-stu-id="163a9-172">-UseSubDomain</span></span>
<span data-ttu-id="163a9-173">Dolaylı CName doğrulamasının etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="163a9-173">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="163a9-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="163a9-174">CommonParameters</span></span>
<span data-ttu-id="163a9-175">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="163a9-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="163a9-176">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="163a9-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="163a9-177">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="163a9-177">INPUTS</span></span>

### <span data-ttu-id="163a9-178">System. String</span><span class="sxs-lookup"><span data-stu-id="163a9-178">System.String</span></span>

## <span data-ttu-id="163a9-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="163a9-179">OUTPUTS</span></span>

### <span data-ttu-id="163a9-180">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="163a9-180">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="163a9-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="163a9-181">NOTES</span></span>

## <span data-ttu-id="163a9-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="163a9-182">RELATED LINKS</span></span>

[<span data-ttu-id="163a9-183">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="163a9-183">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="163a9-184">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="163a9-184">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="163a9-185">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="163a9-185">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
