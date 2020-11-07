---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae22e6923a03864b9371ccdf5379ef9b6bf5189d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936227"
---
# <span data-ttu-id="5fb11-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5fb11-101">New-AzStorageContext</span></span>

## <span data-ttu-id="5fb11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fb11-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb11-103">Azure depolama bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5fb11-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="5fb11-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5fb11-104">SYNTAX</span></span>

### <span data-ttu-id="5fb11-105">AccountNameAndKey (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5fb11-105">AccountNameAndKey (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="5fb11-106">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="5fb11-106">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="5fb11-107">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="5fb11-107">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5fb11-108">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="5fb11-108">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="5fb11-109">SasToken</span><span class="sxs-lookup"><span data-stu-id="5fb11-109">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="5fb11-110">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="5fb11-110">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="5fb11-111">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="5fb11-111">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="5fb11-112">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="5fb11-112">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="5fb11-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="5fb11-113">DESCRIPTION</span></span>
<span data-ttu-id="5fb11-114">**New-AzStorageContext** cmdlet 'ı bir Azure depolama bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5fb11-114">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="5fb11-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5fb11-115">EXAMPLES</span></span>

### <span data-ttu-id="5fb11-116">Örnek 1: depolama hesabı adı ve anahtarı belirterek bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="5fb11-116">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="5fb11-117">Bu komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5fb11-117">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="5fb11-118">Örnek 2: bağlantı dizesi belirterek bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="5fb11-118">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="5fb11-119">Bu komut, ContosoGeneral hesabı için belirtilen bağlantı dizesine dayalı bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5fb11-119">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="5fb11-120">Örnek 3: anonim depolama hesabı için bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="5fb11-120">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="5fb11-121">Bu komut, ContosoGeneral adlı hesap için anonim kullanım bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5fb11-121">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="5fb11-122">Komut HTTP 'yi bağlantı protokolü olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fb11-122">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="5fb11-123">Örnek 4: yerel geliştirme depolama hesabını kullanarak bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="5fb11-123">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzStorageContext -Local
```

<span data-ttu-id="5fb11-124">Bu komut, yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5fb11-124">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="5fb11-125">Komut *Yerel* parametreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fb11-125">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="5fb11-126">Örnek 5: yerel geliştirici depolama hesabı kapsayıcısını alma</span><span class="sxs-lookup"><span data-stu-id="5fb11-126">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="5fb11-127">Bu komut, yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturur ve yeni bağlamı ardışık düzen işlecini kullanarak **Get-AzStorageContainer** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="5fb11-127">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5fb11-128">Komut, yerel geliştirici depolama hesabı için Azure depolama kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="5fb11-128">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="5fb11-129">Örnek 6: birden çok kapsayıcı alma</span><span class="sxs-lookup"><span data-stu-id="5fb11-129">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="5fb11-130">İlk komut yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturur ve bu $Context bağlamı 01 değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="5fb11-130">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="5fb11-131">İkinci komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur ve bu bağlamı $Context 02 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5fb11-131">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="5fb11-132">Son komutu, **Get-AzStorageContainer** kullanarak $Context 01 ve $Context 02 ' de depolanan bağlamların kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="5fb11-132">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="5fb11-133">Örnek 7: uç noktayla bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="5fb11-133">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="5fb11-134">Bu komut, belirtilen depolama uç noktasına sahip bir Azure depolama bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5fb11-134">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="5fb11-135">Komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5fb11-135">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="5fb11-136">Örnek 8: belirtilen ortamla bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="5fb11-136">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="5fb11-137">Bu komut, belirtilen Azure ortamına sahip bir Azure depolama bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5fb11-137">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="5fb11-138">Komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5fb11-138">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="5fb11-139">Örnek 9: SAS belirteci kullanarak bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="5fb11-139">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="5fb11-140">İlk komut, ContosoMain adlı kapsayıcı için **New-AzStorageContainerSASToken** cmdlet 'INI kullanarak SAS belirteci oluşturur ve bu belirteci $SasToken değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5fb11-140">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="5fb11-141">Bu belirteç okuma, ekleme, güncelleştirme ve silme izinleri içindir.</span><span class="sxs-lookup"><span data-stu-id="5fb11-141">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="5fb11-142">İkinci komut, $SasToken depolanan SAS belirtecini kullanan ContosoGeneral adlı hesap için bir bağlam oluşturur ve bu bağlamı $Context değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5fb11-142">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="5fb11-143">Son komutu, $Context 'da depolanan bağlamı kullanarak ContosoMain adlı kapsayıcıyla ilişkili tüm blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="5fb11-143">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

## <span data-ttu-id="5fb11-144">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5fb11-144">PARAMETERS</span></span>

### <span data-ttu-id="5fb11-145">-Anonim</span><span class="sxs-lookup"><span data-stu-id="5fb11-145">-Anonymous</span></span>
<span data-ttu-id="5fb11-146">Bu cmdlet 'in anonim oturum açma için bir Azure depolama bağlamını oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="5fb11-146">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb11-147">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="5fb11-147">-ConnectionString</span></span>
<span data-ttu-id="5fb11-148">Azure depolama bağlamı için bir bağlantı dizesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fb11-148">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb11-149">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="5fb11-149">-Endpoint</span></span>
<span data-ttu-id="5fb11-150">Azure depolama bağlamının uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fb11-150">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb11-151">-Ortam</span><span class="sxs-lookup"><span data-stu-id="5fb11-151">-Environment</span></span>
<span data-ttu-id="5fb11-152">Azure ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fb11-152">Specifies the Azure environment.</span></span>
<span data-ttu-id="5fb11-153">Bu parametre için kabul edilebilir değerler: Azurecyüksek ve AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="5fb11-153">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="5fb11-154">Daha fazla bilgi için yazın `Get-Help Get-AzureEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="5fb11-154">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb11-155">-Yerel</span><span class="sxs-lookup"><span data-stu-id="5fb11-155">-Local</span></span>
<span data-ttu-id="5fb11-156">Bu cmdlet 'in yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="5fb11-156">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb11-157">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="5fb11-157">-Protocol</span></span>
<span data-ttu-id="5fb11-158">Aktarma Protokolü (https/http).</span><span class="sxs-lookup"><span data-stu-id="5fb11-158">Transfer Protocol (https/http).</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb11-159">-SasToken</span><span class="sxs-lookup"><span data-stu-id="5fb11-159">-SasToken</span></span>
<span data-ttu-id="5fb11-160">Bağlam için paylaşılan bir erişim Imzası (SAS) belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fb11-160">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb11-161">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5fb11-161">-StorageAccountKey</span></span>
<span data-ttu-id="5fb11-162">Bir Azure depolama hesabı anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fb11-162">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="5fb11-163">Bu cmdlet, bu parametrenin belirttiği anahtar için bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5fb11-163">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb11-164">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5fb11-164">-StorageAccountName</span></span>
<span data-ttu-id="5fb11-165">Azure depolama hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fb11-165">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="5fb11-166">Bu cmdlet, bu parametrenin belirttiği hesap için bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5fb11-166">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb11-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb11-167">CommonParameters</span></span>
<span data-ttu-id="5fb11-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5fb11-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb11-169">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fb11-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb11-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5fb11-170">INPUTS</span></span>

### <span data-ttu-id="5fb11-171">System. String</span><span class="sxs-lookup"><span data-stu-id="5fb11-171">System.String</span></span>

## <span data-ttu-id="5fb11-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5fb11-172">OUTPUTS</span></span>

### <span data-ttu-id="5fb11-173">Microsoft. Windowsazme. Commands. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5fb11-173">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="5fb11-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5fb11-174">NOTES</span></span>

## <span data-ttu-id="5fb11-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5fb11-175">RELATED LINKS</span></span>

[<span data-ttu-id="5fb11-176">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="5fb11-176">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="5fb11-177">Yeni-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="5fb11-177">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


