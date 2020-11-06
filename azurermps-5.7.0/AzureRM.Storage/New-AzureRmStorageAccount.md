---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 1b00930332d9f3f5a78e4cfe8ab7478a5dc5fa19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593360"
---
# <span data-ttu-id="1d94b-101">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d94b-101">New-AzureRmStorageAccount</span></span>

## <span data-ttu-id="1d94b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d94b-102">SYNOPSIS</span></span>
<span data-ttu-id="1d94b-103">Depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d94b-103">Creates a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d94b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d94b-104">SYNTAX</span></span>

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1d94b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d94b-105">DESCRIPTION</span></span>
<span data-ttu-id="1d94b-106">**New-AzureRmStorageAccount** cmdlet 'ı bir Azure depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d94b-106">The **New-AzureRmStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="1d94b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d94b-107">EXAMPLES</span></span>

### <span data-ttu-id="1d94b-108">Örnek 1: depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d94b-108">Example 1: Create a Storage Account</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS"
```

<span data-ttu-id="1d94b-109">Bu komut MyResourceGroup kaynak grubu adı için bir depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d94b-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="1d94b-110">Örnek 2: depolama hizmeti şifrelemesi kullanan bir BLOB depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d94b-110">Example 2: Create a Blob Storage account that uses Storage Service Encryption</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

<span data-ttu-id="1d94b-111">Bu komut, etkin erişim türünü kullanan bir BLOB depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d94b-111">This command creates a Blob Storage account that uses the hot access type.</span></span>
<span data-ttu-id="1d94b-112">Hesap, blob hizmetinde depolama hizmeti şifrelemesini etkinleştirdi.</span><span class="sxs-lookup"><span data-stu-id="1d94b-112">The account has enabled Storage Service encryption on Blob Service.</span></span>

### <span data-ttu-id="1d94b-113">Örnek 3: blob ve dosya hizmetlerinde depolama hizmeti şifrelemesini sağlayan bir depolama hesabı oluşturun ve Azure Keykasa için bir kimlik oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="1d94b-113">Example 3: Create a Storage Account that Enables Storage Service Encryption on Blob and File Services, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

<span data-ttu-id="1d94b-114">Bu komut, blob ve dosya hizmetlerinde depolama hizmeti şifrelemesini destekleyen bir depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d94b-114">This command creates a Storage account that enabled Storage Service encryption on Blob and File Services.</span></span>  <span data-ttu-id="1d94b-115">Ayrıca, Azure Keykasası aracılığıyla hesap anahtarlarını yönetmek için kullanılabilecek bir kimlik oluşturur ve bunu atar.</span><span class="sxs-lookup"><span data-stu-id="1d94b-115">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

## <span data-ttu-id="1d94b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d94b-116">PARAMETERS</span></span>

### <span data-ttu-id="1d94b-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="1d94b-117">-AccessTier</span></span>
<span data-ttu-id="1d94b-118">Bu cmdlet 'in oluşturduğu depolama hesabının erişim katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d94b-118">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="1d94b-119">Bu parametre için kabul edilebilir değerler: kolay ve serin.</span><span class="sxs-lookup"><span data-stu-id="1d94b-119">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="1d94b-120">*Tür* parametresi Için blobstorage değeri belirtirseniz, *accesstier* parametresi için bir değer belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d94b-120">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="1d94b-121">Bu *tür* parametre Için bir depolama alanı değeri belirtirseniz, *accesstier* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="1d94b-121">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94b-122">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="1d94b-122">-AssignIdentity</span></span>
<span data-ttu-id="1d94b-123">Azure Keykasa gibi temel yönetim hizmetleriyle kullanmak üzere bu depolama hesabı için yeni bir depolama hesabı kimliği oluşturup atayın.</span><span class="sxs-lookup"><span data-stu-id="1d94b-123">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94b-124">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="1d94b-124">-CustomDomainName</span></span>
<span data-ttu-id="1d94b-125">Depolama hesabının özel etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d94b-125">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="1d94b-126">Varsayılan değer depolama alanıdır.</span><span class="sxs-lookup"><span data-stu-id="1d94b-126">The default value is Storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94b-127">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="1d94b-127">-EnableEncryptionService</span></span>
<span data-ttu-id="1d94b-128">Bu cmdlet 'in depolama hizmeti için depolama hizmeti şifrelemesini etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d94b-128">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="1d94b-129">Azure Blob ve Azure dosya hizmetleri destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="1d94b-129">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94b-130">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="1d94b-130">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="1d94b-131">Depolama hesabının https trafiğinin yalnızca etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d94b-131">Indicates whether or not the Storage Account only enable https traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d94b-132">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="1d94b-132">-InformationAction</span></span>
<span data-ttu-id="1d94b-133">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d94b-133">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1d94b-134">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1d94b-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1d94b-135">'A</span><span class="sxs-lookup"><span data-stu-id="1d94b-135">Continue</span></span>
- <span data-ttu-id="1d94b-136">Manıza</span><span class="sxs-lookup"><span data-stu-id="1d94b-136">Ignore</span></span>
- <span data-ttu-id="1d94b-137">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="1d94b-137">Inquire</span></span>
- <span data-ttu-id="1d94b-138">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="1d94b-138">SilentlyContinue</span></span>
- <span data-ttu-id="1d94b-139">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="1d94b-139">Stop</span></span>
- <span data-ttu-id="1d94b-140">Biliriz</span><span class="sxs-lookup"><span data-stu-id="1d94b-140">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94b-141">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="1d94b-141">-InformationVariable</span></span>
<span data-ttu-id="1d94b-142">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d94b-142">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94b-143">-Tür</span><span class="sxs-lookup"><span data-stu-id="1d94b-143">-Kind</span></span>
<span data-ttu-id="1d94b-144">Bu cmdlet 'in oluşturduğu depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d94b-144">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="1d94b-145">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1d94b-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1d94b-146">Alanını.</span><span class="sxs-lookup"><span data-stu-id="1d94b-146">Storage.</span></span>
<span data-ttu-id="1d94b-147">Blob, tablo, kuyruk, dosya ve disklerin depolanmasını destekleyen genel amaçlı depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="1d94b-147">General purpose storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>

- <span data-ttu-id="1d94b-148">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="1d94b-148">BlobStorage.</span></span>
<span data-ttu-id="1d94b-149">Yalnızca blob depolamasını destekleyen BLOB depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="1d94b-149">Blob storage account which supports storage of Blobs only.</span></span>


<span data-ttu-id="1d94b-150">Varsayılan değer depolama alanıdır.</span><span class="sxs-lookup"><span data-stu-id="1d94b-150">The default value is Storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94b-151">-Konum</span><span class="sxs-lookup"><span data-stu-id="1d94b-151">-Location</span></span>
<span data-ttu-id="1d94b-152">Oluşturulacak depolama hesabının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d94b-152">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d94b-153">-Ad</span><span class="sxs-lookup"><span data-stu-id="1d94b-153">-Name</span></span>
<span data-ttu-id="1d94b-154">Oluşturulacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d94b-154">Specifies the name of the Storage account to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d94b-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d94b-155">-ResourceGroupName</span></span>
<span data-ttu-id="1d94b-156">Depolama hesabının ekleneceği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d94b-156">Specifies the name of the resource group in which to add the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d94b-157">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1d94b-157">-SkuName</span></span>
<span data-ttu-id="1d94b-158">Bu cmdlet 'in oluşturduğu depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d94b-158">Specifies the SKU name of the storage account that this cmdlet creates.</span></span>
<span data-ttu-id="1d94b-159">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1d94b-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1d94b-160">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="1d94b-160">Standard_LRS.</span></span>
<span data-ttu-id="1d94b-161">Yerel olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="1d94b-161">Locally-redundant storage.</span></span>
- <span data-ttu-id="1d94b-162">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="1d94b-162">Standard_ZRS.</span></span>
<span data-ttu-id="1d94b-163">Bölge ile yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="1d94b-163">Zone-redundant storage.</span></span>
- <span data-ttu-id="1d94b-164">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="1d94b-164">Standard_GRS.</span></span>
<span data-ttu-id="1d94b-165">Coğrafi olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="1d94b-165">Geo-redundant storage.</span></span>
- <span data-ttu-id="1d94b-166">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="1d94b-166">Standard_RAGRS.</span></span>
<span data-ttu-id="1d94b-167">Okuma erişimi coğrafi depolama.</span><span class="sxs-lookup"><span data-stu-id="1d94b-167">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="1d94b-168">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="1d94b-168">Premium_LRS.</span></span>
<span data-ttu-id="1d94b-169">Premium yerel olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="1d94b-169">Premium locally-redundant storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d94b-170">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1d94b-170">-Tag</span></span>
<span data-ttu-id="1d94b-171">*Tür* parametresi Için blobstorage değeri belirtirseniz, *accesstier* parametresi için bir değer belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d94b-171">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="1d94b-172">Bu *tür* parametre Için bir depolama alanı değeri belirtirseniz, *accesstier* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="1d94b-172">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94b-173">-Usealt etki alanı</span><span class="sxs-lookup"><span data-stu-id="1d94b-173">-UseSubDomain</span></span>
<span data-ttu-id="1d94b-174">Dolaylı CName doğrulamasının etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d94b-174">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94b-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d94b-175">CommonParameters</span></span>
<span data-ttu-id="1d94b-176">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d94b-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d94b-177">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d94b-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d94b-178">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d94b-178">INPUTS</span></span>

### <span data-ttu-id="1d94b-179">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1d94b-179">None</span></span>
<span data-ttu-id="1d94b-180">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1d94b-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1d94b-181">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d94b-181">OUTPUTS</span></span>

## <span data-ttu-id="1d94b-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d94b-182">NOTES</span></span>

## <span data-ttu-id="1d94b-183">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d94b-183">RELATED LINKS</span></span>

[<span data-ttu-id="1d94b-184">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d94b-184">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="1d94b-185">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d94b-185">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="1d94b-186">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d94b-186">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
