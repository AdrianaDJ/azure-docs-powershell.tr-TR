---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4db0b752e8bf887e899a4de6a8e4175eaa2d9855
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572025"
---
# <span data-ttu-id="f91ef-101">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f91ef-101">New-AzureStorageContext</span></span>

## <span data-ttu-id="f91ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f91ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f91ef-103">Azure depolama bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f91ef-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="f91ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f91ef-104">SYNTAX</span></span>

### <span data-ttu-id="f91ef-105">AccountNameAndKey (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f91ef-105">AccountNameAndKey (Default)</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="f91ef-106">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="f91ef-106">AccountNameAndKeyEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="f91ef-107">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="f91ef-107">AnonymousAccount</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f91ef-108">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="f91ef-108">AnonymousAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="f91ef-109">SasToken</span><span class="sxs-lookup"><span data-stu-id="f91ef-109">SasToken</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="f91ef-110">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f91ef-110">SasTokenWithAzureEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="f91ef-111">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="f91ef-111">ConnectionString</span></span>
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="f91ef-112">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="f91ef-112">LocalDevelopment</span></span>
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="f91ef-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="f91ef-113">DESCRIPTION</span></span>
<span data-ttu-id="f91ef-114">**New-AzureStorageContext** cmdlet 'ı Azure depolama bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f91ef-114">The **New-AzureStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="f91ef-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f91ef-115">EXAMPLES</span></span>

### <span data-ttu-id="f91ef-116">Örnek 1: depolama hesabı adı ve anahtarı belirterek bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="f91ef-116">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="f91ef-117">Bu komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f91ef-117">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="f91ef-118">Örnek 2: bağlantı dizesi belirterek bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="f91ef-118">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="f91ef-119">Bu komut, ContosoGeneral hesabı için belirtilen bağlantı dizesine dayalı bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f91ef-119">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="f91ef-120">Örnek 3: anonim depolama hesabı için bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="f91ef-120">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="f91ef-121">Bu komut, ContosoGeneral adlı hesap için anonim kullanım bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f91ef-121">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="f91ef-122">Komut HTTP 'yi bağlantı protokolü olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="f91ef-122">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="f91ef-123">Örnek 4: yerel geliştirme depolama hesabını kullanarak bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="f91ef-123">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local
```

<span data-ttu-id="f91ef-124">Bu komut, yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f91ef-124">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="f91ef-125">Komut *Yerel* parametreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f91ef-125">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="f91ef-126">Örnek 5: yerel geliştirici depolama hesabı kapsayıcısını alma</span><span class="sxs-lookup"><span data-stu-id="f91ef-126">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

<span data-ttu-id="f91ef-127">Bu komut, yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturur ve ardından ardışık düzen işlecini kullanarak yeni bağlamı **Get-AzureStorageContainer** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="f91ef-127">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzureStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f91ef-128">Komut, yerel geliştirici depolama hesabı için Azure depolama kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="f91ef-128">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="f91ef-129">Örnek 6: birden çok kapsayıcı alma</span><span class="sxs-lookup"><span data-stu-id="f91ef-129">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

<span data-ttu-id="f91ef-130">İlk komut yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturur ve bu $Context bağlamı 01 değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="f91ef-130">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>

<span data-ttu-id="f91ef-131">İkinci komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur ve bu bağlamı $Context 02 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f91ef-131">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>

<span data-ttu-id="f91ef-132">Son komutu, **Get-AzureStorageContainer** kullanarak $Context 01 ve $Context 02 ' da depolanan bağlamların kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="f91ef-132">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="f91ef-133">Örnek 7: uç noktayla bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="f91ef-133">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="f91ef-134">Bu komut, belirtilen depolama uç noktasına sahip bir Azure depolama bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f91ef-134">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="f91ef-135">Komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f91ef-135">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="f91ef-136">Örnek 8: belirtilen ortamla bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="f91ef-136">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="f91ef-137">Bu komut, belirtilen Azure ortamına sahip bir Azure depolama bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f91ef-137">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="f91ef-138">Komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f91ef-138">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="f91ef-139">Örnek 9: SAS belirteci kullanarak bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="f91ef-139">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "raud"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="f91ef-140">İlk komut, ContosoMain adlı kapsayıcı için **New-AzureStorageContainerSASToken** cmdlet 'INI kullanarak SAS belirteci oluşturur ve bu belirteci $SasToken değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f91ef-140">The first command generates an SAS token by using the **New-AzureStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="f91ef-141">Bu belirteç okuma, ekleme, güncelleştirme ve silme izinleri içindir.</span><span class="sxs-lookup"><span data-stu-id="f91ef-141">That token is for read, add, update, and delete permissions.</span></span>

<span data-ttu-id="f91ef-142">İkinci komut, $SasToken depolanan SAS belirtecini kullanan ContosoGeneral adlı hesap için bir bağlam oluşturur ve bu bağlamı $Context değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f91ef-142">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>

<span data-ttu-id="f91ef-143">Son komutu, $Context 'da depolanan bağlamı kullanarak ContosoMain adlı kapsayıcıyla ilişkili tüm blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="f91ef-143">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

## <span data-ttu-id="f91ef-144">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f91ef-144">PARAMETERS</span></span>

### <span data-ttu-id="f91ef-145">-Anonim</span><span class="sxs-lookup"><span data-stu-id="f91ef-145">-Anonymous</span></span>
<span data-ttu-id="f91ef-146">Bu cmdlet 'in anonim oturum açma için bir Azure depolama bağlamını oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="f91ef-146">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f91ef-147">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="f91ef-147">-ConnectionString</span></span>
<span data-ttu-id="f91ef-148">Azure depolama bağlamı için bir bağlantı dizesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f91ef-148">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: String
Parameter Sets: ConnectionString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f91ef-149">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="f91ef-149">-Endpoint</span></span>
<span data-ttu-id="f91ef-150">Azure depolama bağlamının uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f91ef-150">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f91ef-151">-Ortam</span><span class="sxs-lookup"><span data-stu-id="f91ef-151">-Environment</span></span>
<span data-ttu-id="f91ef-152">Azure ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f91ef-152">Specifies the Azure environment.</span></span>
<span data-ttu-id="f91ef-153">Bu parametre için kabul edilebilir değerler: Azurecyüksek ve AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="f91ef-153">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="f91ef-154">Daha fazla bilgi için yazın `Get-Help Get-AzureEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="f91ef-154">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SasTokenWithAzureEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f91ef-155">-Yerel</span><span class="sxs-lookup"><span data-stu-id="f91ef-155">-Local</span></span>
<span data-ttu-id="f91ef-156">Bu cmdlet 'in yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="f91ef-156">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LocalDevelopment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f91ef-157">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="f91ef-157">-Protocol</span></span>
<span data-ttu-id="f91ef-158">Hesap SA 'larının verildiği bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f91ef-158">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="f91ef-159">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f91ef-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f91ef-160">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="f91ef-160">HttpsOnly</span></span>
- <span data-ttu-id="f91ef-161">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="f91ef-161">HttpsOrHttp</span></span>

<span data-ttu-id="f91ef-162">Varsayılan değer HttpsOrHttp değeridir.</span><span class="sxs-lookup"><span data-stu-id="f91ef-162">The default value is HttpsOrHttp.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
Aliases: 
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f91ef-163">-SasToken</span><span class="sxs-lookup"><span data-stu-id="f91ef-163">-SasToken</span></span>
<span data-ttu-id="f91ef-164">Bağlam için paylaşılan bir erişim Imzası (SAS) belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="f91ef-164">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f91ef-165">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f91ef-165">-StorageAccountKey</span></span>
<span data-ttu-id="f91ef-166">Bir Azure depolama hesabı anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f91ef-166">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="f91ef-167">Bu cmdlet, bu parametrenin belirttiği anahtar için bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f91ef-167">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f91ef-168">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f91ef-168">-StorageAccountName</span></span>
<span data-ttu-id="f91ef-169">Azure depolama hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f91ef-169">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="f91ef-170">Bu cmdlet, bu parametrenin belirttiği hesap için bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f91ef-170">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f91ef-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f91ef-171">CommonParameters</span></span>
<span data-ttu-id="f91ef-172">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f91ef-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f91ef-173">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f91ef-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f91ef-174">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f91ef-174">INPUTS</span></span>

## <span data-ttu-id="f91ef-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f91ef-175">OUTPUTS</span></span>

### <span data-ttu-id="f91ef-176">AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f91ef-176">AzureStorageContext</span></span>

## <span data-ttu-id="f91ef-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f91ef-177">NOTES</span></span>

## <span data-ttu-id="f91ef-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f91ef-178">RELATED LINKS</span></span>

[<span data-ttu-id="f91ef-179">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="f91ef-179">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="f91ef-180">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="f91ef-180">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)


