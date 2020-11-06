---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
ms.openlocfilehash: 9de6b2b52205bdf80de9c57e3e338f4b7216c5ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591515"
---
# <span data-ttu-id="0b2dd-101">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="0b2dd-101">New-AzureStorageContext</span></span>

## <span data-ttu-id="0b2dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b2dd-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2dd-103">Azure depolama bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-103">Creates an Azure Storage context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b2dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b2dd-104">SYNTAX</span></span>

### <span data-ttu-id="0b2dd-105">OAuthAccount (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0b2dd-105">OAuthAccount (Default)</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="0b2dd-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="0b2dd-106">AccountNameAndKey</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="0b2dd-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="0b2dd-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="0b2dd-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="0b2dd-108">AnonymousAccount</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b2dd-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="0b2dd-109">AnonymousAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="0b2dd-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="0b2dd-110">SasToken</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="0b2dd-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="0b2dd-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="0b2dd-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="0b2dd-112">OAuthAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="0b2dd-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="0b2dd-113">ConnectionString</span></span>
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="0b2dd-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="0b2dd-114">LocalDevelopment</span></span>
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="0b2dd-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b2dd-115">DESCRIPTION</span></span>
<span data-ttu-id="0b2dd-116">**New-AzureStorageContext** cmdlet 'ı Azure depolama bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-116">The **New-AzureStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="0b2dd-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b2dd-117">EXAMPLES</span></span>

### <span data-ttu-id="0b2dd-118">Örnek 1: depolama hesabı adı ve anahtarı belirterek bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="0b2dd-118">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="0b2dd-119">Bu komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-119">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="0b2dd-120">Örnek 2: bağlantı dizesi belirterek bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="0b2dd-120">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="0b2dd-121">Bu komut, ContosoGeneral hesabı için belirtilen bağlantı dizesine dayalı bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-121">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="0b2dd-122">Örnek 3: anonim depolama hesabı için bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="0b2dd-122">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="0b2dd-123">Bu komut, ContosoGeneral adlı hesap için anonim kullanım bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-123">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="0b2dd-124">Komut HTTP 'yi bağlantı protokolü olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-124">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="0b2dd-125">Örnek 4: yerel geliştirme depolama hesabını kullanarak bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="0b2dd-125">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local
```

<span data-ttu-id="0b2dd-126">Bu komut, yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-126">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="0b2dd-127">Komut *Yerel* parametreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-127">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="0b2dd-128">Örnek 5: yerel geliştirici depolama hesabı kapsayıcısını alma</span><span class="sxs-lookup"><span data-stu-id="0b2dd-128">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

<span data-ttu-id="0b2dd-129">Bu komut, yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturur ve ardından ardışık düzen işlecini kullanarak yeni bağlamı **Get-AzureStorageContainer** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-129">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzureStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0b2dd-130">Komut, yerel geliştirici depolama hesabı için Azure depolama kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-130">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="0b2dd-131">Örnek 6: birden çok kapsayıcı alma</span><span class="sxs-lookup"><span data-stu-id="0b2dd-131">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

<span data-ttu-id="0b2dd-132">İlk komut yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturur ve bu $Context bağlamı 01 değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-132">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="0b2dd-133">İkinci komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur ve bu bağlamı $Context 02 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-133">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="0b2dd-134">Son komutu, **Get-AzureStorageContainer** kullanarak $Context 01 ve $Context 02 ' da depolanan bağlamların kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-134">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="0b2dd-135">Örnek 7: uç noktayla bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="0b2dd-135">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="0b2dd-136">Bu komut, belirtilen depolama uç noktasına sahip bir Azure depolama bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-136">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="0b2dd-137">Komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-137">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="0b2dd-138">Örnek 8: belirtilen ortamla bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="0b2dd-138">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="0b2dd-139">Bu komut, belirtilen Azure ortamına sahip bir Azure depolama bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-139">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="0b2dd-140">Komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-140">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="0b2dd-141">Örnek 9: SAS belirteci kullanarak bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="0b2dd-141">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="0b2dd-142">İlk komut, ContosoMain adlı kapsayıcı için **New-AzureStorageContainerSASToken** cmdlet 'INI kullanarak SAS belirteci oluşturur ve bu belirteci $SasToken değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-142">The first command generates an SAS token by using the **New-AzureStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="0b2dd-143">Bu belirteç okuma, ekleme, güncelleştirme ve silme izinleri içindir.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-143">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="0b2dd-144">İkinci komut, $SasToken depolanan SAS belirtecini kullanan ContosoGeneral adlı hesap için bir bağlam oluşturur ve bu bağlamı $Context değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-144">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="0b2dd-145">Son komutu, $Context 'da depolanan bağlamı kullanarak ContosoMain adlı kapsayıcıyla ilişkili tüm blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-145">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="0b2dd-146">Örnek 10: OAuth kimlik doğrulamasını kullanarak bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="0b2dd-146">Example 10: Create a context by using the OAuth Authentication</span></span>
```
C:\PS>Connect-AzureRmAccount
C:\PS> $Context = New-AzureStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="0b2dd-147">Bu komut, OAuth kimlik doğrulamasını kullanarak bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-147">This command creates a context by using the OAuth Authentication.</span></span>

## <span data-ttu-id="0b2dd-148">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b2dd-148">PARAMETERS</span></span>

### <span data-ttu-id="0b2dd-149">-Anonim</span><span class="sxs-lookup"><span data-stu-id="0b2dd-149">-Anonymous</span></span>
<span data-ttu-id="0b2dd-150">Bu cmdlet 'in anonim oturum açma için bir Azure depolama bağlamını oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-150">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="0b2dd-151">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="0b2dd-151">-ConnectionString</span></span>
<span data-ttu-id="0b2dd-152">Azure depolama bağlamı için bir bağlantı dizesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-152">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="0b2dd-153">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="0b2dd-153">-Endpoint</span></span>
<span data-ttu-id="0b2dd-154">Azure depolama bağlamının uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-154">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2dd-155">-Ortam</span><span class="sxs-lookup"><span data-stu-id="0b2dd-155">-Environment</span></span>
<span data-ttu-id="0b2dd-156">Azure ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-156">Specifies the Azure environment.</span></span>
<span data-ttu-id="0b2dd-157">Bu parametre için kabul edilebilir değerler: Azurecyüksek ve AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-157">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="0b2dd-158">Daha fazla bilgi için yazın `Get-Help Get-AzureEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="0b2dd-158">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

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
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2dd-159">-Yerel</span><span class="sxs-lookup"><span data-stu-id="0b2dd-159">-Local</span></span>
<span data-ttu-id="0b2dd-160">Bu cmdlet 'in yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-160">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="0b2dd-161">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="0b2dd-161">-Protocol</span></span>
<span data-ttu-id="0b2dd-162">Aktarma Protokolü (https/http).</span><span class="sxs-lookup"><span data-stu-id="0b2dd-162">Transfer Protocol (https/http).</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2dd-163">-SasToken</span><span class="sxs-lookup"><span data-stu-id="0b2dd-163">-SasToken</span></span>
<span data-ttu-id="0b2dd-164">Bağlam için paylaşılan bir erişim Imzası (SAS) belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-164">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="0b2dd-165">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0b2dd-165">-StorageAccountKey</span></span>
<span data-ttu-id="0b2dd-166">Bir Azure depolama hesabı anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-166">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="0b2dd-167">Bu cmdlet, bu parametrenin belirttiği anahtar için bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-167">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="0b2dd-168">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0b2dd-168">-StorageAccountName</span></span>
<span data-ttu-id="0b2dd-169">Azure depolama hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-169">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="0b2dd-170">Bu cmdlet, bu parametrenin belirttiği hesap için bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-170">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2dd-171">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="0b2dd-171">-UseConnectedAccount</span></span>
<span data-ttu-id="0b2dd-172">Bu cmdlet 'in OAuth kimlik doğrulaması içeren bir Azure depolama bağlamını oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-172">Indicates that this cmdlet creates an Azure Storage context with OAuth Authentication.</span></span>
<span data-ttu-id="0b2dd-173">Başka bir anththcation belirtilmediğinde cmdlet, OAuth kimlik doğrulamasını varsayılan olarak kullanır.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-173">The cmdlet will use OAuth Authentication by default, when other anthentication not specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2dd-174">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="0b2dd-174">-UseConnectedAccount</span></span>
<span data-ttu-id="0b2dd-175">Bu cmdlet 'in OAuth kimlik doğrulaması içeren bir Azure depolama bağlamını oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-175">Indicates that this cmdlet creates an Azure Storage context with OAuth Authentication.</span></span>
<span data-ttu-id="0b2dd-176">Başka bir anththcation belirtilmediğinde cmdlet, OAuth kimlik doğrulamasını varsayılan olarak kullanır.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-176">The cmdlet will use OAuth Authentication by default, when other anthentication not specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2dd-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2dd-177">CommonParameters</span></span>
<span data-ttu-id="0b2dd-178">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b2dd-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2dd-179">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b2dd-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2dd-180">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b2dd-180">INPUTS</span></span>

### <span data-ttu-id="0b2dd-181">System. String</span><span class="sxs-lookup"><span data-stu-id="0b2dd-181">System.String</span></span>

## <span data-ttu-id="0b2dd-182">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b2dd-182">OUTPUTS</span></span>

### <span data-ttu-id="0b2dd-183">Microsoft. Windowsazme. Commands. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="0b2dd-183">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="0b2dd-184">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b2dd-184">NOTES</span></span>

## <span data-ttu-id="0b2dd-185">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b2dd-185">RELATED LINKS</span></span>

[<span data-ttu-id="0b2dd-186">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="0b2dd-186">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="0b2dd-187">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="0b2dd-187">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)


