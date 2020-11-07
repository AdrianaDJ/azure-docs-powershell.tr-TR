---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 50384630658f7626ee02ca1dee223e82bf122ef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765024"
---
# <span data-ttu-id="8180d-101">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8180d-101">New-AzureRmStorageAccount</span></span>

## <span data-ttu-id="8180d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8180d-102">SYNOPSIS</span></span>
<span data-ttu-id="8180d-103">Depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8180d-103">Creates a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8180d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8180d-104">SYNTAX</span></span>

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8180d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8180d-105">DESCRIPTION</span></span>
<span data-ttu-id="8180d-106">**New-AzureRmStorageAccount** cmdlet 'ı bir Azure depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8180d-106">The **New-AzureRmStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="8180d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8180d-107">EXAMPLES</span></span>

### <span data-ttu-id="8180d-108">Örnek 1: depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="8180d-108">Example 1: Create a Storage Account</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS"
```

<span data-ttu-id="8180d-109">Bu komut MyResourceGroup kaynak grubu adı için bir depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8180d-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="8180d-110">Örnek 2: depolama hizmeti şifrelemesi kullanan bir BLOB depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="8180d-110">Example 2: Create a Blob Storage account that uses Storage Service Encryption</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

<span data-ttu-id="8180d-111">Bu komut, etkin erişim türünü kullanan bir BLOB depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8180d-111">This command creates a Blob Storage account that uses the hot access type.</span></span>
<span data-ttu-id="8180d-112">Hesap, blob hizmetinde depolama hizmeti şifrelemesini etkinleştirdi.</span><span class="sxs-lookup"><span data-stu-id="8180d-112">The account has enabled Storage Service encryption on Blob Service.</span></span>

### <span data-ttu-id="8180d-113">Örnek 3: blob ve dosya hizmetlerinde depolama hizmeti şifrelemesini sağlayan bir depolama hesabı oluşturun ve Azure Keykasa için bir kimlik oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="8180d-113">Example 3: Create a Storage Account that Enables Storage Service Encryption on Blob and File Services, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

<span data-ttu-id="8180d-114">Bu komut, blob ve dosya hizmetlerinde depolama hizmeti şifrelemesini destekleyen bir depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8180d-114">This command creates a Storage account that enabled Storage Service encryption on Blob and File Services.</span></span>  <span data-ttu-id="8180d-115">Ayrıca, Azure Keykasası aracılığıyla hesap anahtarlarını yönetmek için kullanılabilecek bir kimlik oluşturur ve bunu atar.</span><span class="sxs-lookup"><span data-stu-id="8180d-115">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

## <span data-ttu-id="8180d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8180d-116">PARAMETERS</span></span>

### <span data-ttu-id="8180d-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="8180d-117">-AccessTier</span></span>
<span data-ttu-id="8180d-118">Bu cmdlet 'in oluşturduğu depolama hesabının erişim katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8180d-118">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="8180d-119">Bu parametre için kabul edilebilir değerler: kolay ve serin.</span><span class="sxs-lookup"><span data-stu-id="8180d-119">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="8180d-120">*Tür* parametresi Için blobstorage değeri belirtirseniz, *accesstier* parametresi için bir değer belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8180d-120">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="8180d-121">Bu *tür* parametre Için bir depolama alanı değeri belirtirseniz, *accesstier* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="8180d-121">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8180d-122">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="8180d-122">-AssignIdentity</span></span>
<span data-ttu-id="8180d-123">Azure Keykasa gibi temel yönetim hizmetleriyle kullanmak üzere bu depolama hesabı için yeni bir depolama hesabı kimliği oluşturup atayın.</span><span class="sxs-lookup"><span data-stu-id="8180d-123">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="8180d-124">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="8180d-124">-CustomDomainName</span></span>
<span data-ttu-id="8180d-125">Depolama hesabının özel etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8180d-125">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="8180d-126">Varsayılan değer depolama alanıdır.</span><span class="sxs-lookup"><span data-stu-id="8180d-126">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8180d-127">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="8180d-127">-EnableEncryptionService</span></span>
<span data-ttu-id="8180d-128">Bu cmdlet 'in depolama hizmeti için depolama hizmeti şifrelemesini etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8180d-128">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="8180d-129">Azure Blob ve Azure dosya hizmetleri destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="8180d-129">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8180d-130">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="8180d-130">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="8180d-131">Depolama hesabının https trafiğinin yalnızca etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8180d-131">Indicates whether or not the Storage Account only enable https traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8180d-132">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="8180d-132">-InformationAction</span></span>
<span data-ttu-id="8180d-133">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8180d-133">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8180d-134">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8180d-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8180d-135">'A</span><span class="sxs-lookup"><span data-stu-id="8180d-135">Continue</span></span>
- <span data-ttu-id="8180d-136">Manıza</span><span class="sxs-lookup"><span data-stu-id="8180d-136">Ignore</span></span>
- <span data-ttu-id="8180d-137">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="8180d-137">Inquire</span></span>
- <span data-ttu-id="8180d-138">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="8180d-138">SilentlyContinue</span></span>
- <span data-ttu-id="8180d-139">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="8180d-139">Stop</span></span>
- <span data-ttu-id="8180d-140">Biliriz</span><span class="sxs-lookup"><span data-stu-id="8180d-140">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8180d-141">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="8180d-141">-InformationVariable</span></span>
<span data-ttu-id="8180d-142">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="8180d-142">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8180d-143">-Tür</span><span class="sxs-lookup"><span data-stu-id="8180d-143">-Kind</span></span>
<span data-ttu-id="8180d-144">Bu cmdlet 'in oluşturduğu depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8180d-144">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="8180d-145">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8180d-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8180d-146">Alanını.</span><span class="sxs-lookup"><span data-stu-id="8180d-146">Storage.</span></span>
<span data-ttu-id="8180d-147">Blob, tablo, kuyruk, dosya ve disklerin depolanmasını destekleyen genel amaçlı depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="8180d-147">General purpose storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
 
- <span data-ttu-id="8180d-148">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="8180d-148">BlobStorage.</span></span>
<span data-ttu-id="8180d-149">Yalnızca blob depolamasını destekleyen BLOB depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="8180d-149">Blob storage account which supports storage of Blobs only.</span></span>
 

<span data-ttu-id="8180d-150">Varsayılan değer depolama alanıdır.</span><span class="sxs-lookup"><span data-stu-id="8180d-150">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8180d-151">-Konum</span><span class="sxs-lookup"><span data-stu-id="8180d-151">-Location</span></span>
<span data-ttu-id="8180d-152">Oluşturulacak depolama hesabının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8180d-152">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8180d-153">-Ad</span><span class="sxs-lookup"><span data-stu-id="8180d-153">-Name</span></span>
<span data-ttu-id="8180d-154">Oluşturulacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8180d-154">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="8180d-155">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8180d-155">-NetworkRuleSet</span></span>
<span data-ttu-id="8180d-156">Depolama hesabı ağ kuralı kümesi</span><span class="sxs-lookup"><span data-stu-id="8180d-156">Storage Account NetworkRuleSet</span></span>

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

### <span data-ttu-id="8180d-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8180d-157">-ResourceGroupName</span></span>
<span data-ttu-id="8180d-158">Depolama hesabının ekleneceği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8180d-158">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="8180d-159">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8180d-159">-SkuName</span></span>
<span data-ttu-id="8180d-160">Bu cmdlet 'in oluşturduğu depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8180d-160">Specifies the SKU name of the storage account that this cmdlet creates.</span></span>
<span data-ttu-id="8180d-161">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8180d-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8180d-162">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="8180d-162">Standard_LRS.</span></span>
<span data-ttu-id="8180d-163">Yerel olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="8180d-163">Locally-redundant storage.</span></span> 
- <span data-ttu-id="8180d-164">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="8180d-164">Standard_ZRS.</span></span>
<span data-ttu-id="8180d-165">Bölge ile yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="8180d-165">Zone-redundant storage.</span></span>
- <span data-ttu-id="8180d-166">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="8180d-166">Standard_GRS.</span></span>
<span data-ttu-id="8180d-167">Coğrafi olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="8180d-167">Geo-redundant storage.</span></span> 
- <span data-ttu-id="8180d-168">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="8180d-168">Standard_RAGRS.</span></span>
<span data-ttu-id="8180d-169">Okuma erişimi coğrafi depolama.</span><span class="sxs-lookup"><span data-stu-id="8180d-169">Read access geo-redundant storage.</span></span> 
- <span data-ttu-id="8180d-170">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="8180d-170">Premium_LRS.</span></span>
<span data-ttu-id="8180d-171">Premium yerel olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="8180d-171">Premium locally-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8180d-172">Etiketli</span><span class="sxs-lookup"><span data-stu-id="8180d-172">-Tag</span></span>
<span data-ttu-id="8180d-173">*Tür* parametresi Için blobstorage değeri belirtirseniz, *accesstier* parametresi için bir değer belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8180d-173">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="8180d-174">Bu *tür* parametre Için bir depolama alanı değeri belirtirseniz, *accesstier* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="8180d-174">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8180d-175">-Usealt etki alanı</span><span class="sxs-lookup"><span data-stu-id="8180d-175">-UseSubDomain</span></span>
<span data-ttu-id="8180d-176">Dolaylı CName doğrulamasının etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8180d-176">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8180d-177">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8180d-177">-DefaultProfile</span></span>
<span data-ttu-id="8180d-178">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8180d-178">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8180d-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8180d-179">CommonParameters</span></span>
<span data-ttu-id="8180d-180">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8180d-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8180d-181">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8180d-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8180d-182">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8180d-182">INPUTS</span></span>

## <span data-ttu-id="8180d-183">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8180d-183">OUTPUTS</span></span>

## <span data-ttu-id="8180d-184">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8180d-184">NOTES</span></span>

## <span data-ttu-id="8180d-185">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8180d-185">RELATED LINKS</span></span>

[<span data-ttu-id="8180d-186">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8180d-186">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="8180d-187">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8180d-187">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="8180d-188">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8180d-188">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


