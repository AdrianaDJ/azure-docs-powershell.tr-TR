---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277168"
---
# <span data-ttu-id="c9c4b-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c9c4b-101">New-AzStorageContext</span></span>

## <span data-ttu-id="c9c4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c4b-103">Azure depolama bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="c9c4b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9c4b-104">SYNTAX</span></span>

### <span data-ttu-id="c9c4b-105">OAuthAccount (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c9c4b-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="c9c4b-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="c9c4b-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="c9c4b-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="c9c4b-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="c9c4b-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="c9c4b-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9c4b-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="c9c4b-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="c9c4b-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="c9c4b-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="c9c4b-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c9c4b-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="c9c4b-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="c9c4b-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="c9c4b-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="c9c4b-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="c9c4b-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="c9c4b-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="c9c4b-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9c4b-115">DESCRIPTION</span></span>
<span data-ttu-id="c9c4b-116">**New-AzStorageContext** cmdlet 'ı bir Azure depolama bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="c9c4b-117">Depolama bağlamının varsayılan kimlik doğrulaması, yalnızca giriş depolama hesap adı olduğunda OAuth (Azure AD) olur.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="c9c4b-118">Depolama hizmeti 'nin kimlik doğrulamasının ayrıntılarını görün https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services .</span><span class="sxs-lookup"><span data-stu-id="c9c4b-118">See details of authentication of the Storage Service in https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="c9c4b-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9c4b-119">EXAMPLES</span></span>

### <span data-ttu-id="c9c4b-120">Örnek 1: depolama hesabı adı ve anahtarı belirterek bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="c9c4b-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="c9c4b-121">Bu komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="c9c4b-122">Örnek 2: bağlantı dizesi belirterek bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="c9c4b-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="c9c4b-123">Bu komut, ContosoGeneral hesabı için belirtilen bağlantı dizesine dayalı bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="c9c4b-124">Örnek 3: anonim depolama hesabı için bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="c9c4b-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="c9c4b-125">Bu komut, ContosoGeneral adlı hesap için anonim kullanım bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="c9c4b-126">Komut HTTP 'yi bağlantı protokolü olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="c9c4b-127">Örnek 4: yerel geliştirme depolama hesabını kullanarak bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="c9c4b-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="c9c4b-128">Bu komut, yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="c9c4b-129">Komut *Yerel* parametreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="c9c4b-130">Örnek 5: yerel geliştirici depolama hesabı kapsayıcısını alma</span><span class="sxs-lookup"><span data-stu-id="c9c4b-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="c9c4b-131">Bu komut, yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturur ve yeni bağlamı ardışık düzen işlecini kullanarak **Get-AzStorageContainer** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c9c4b-132">Komut, yerel geliştirici depolama hesabı için Azure depolama kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="c9c4b-133">Örnek 6: birden çok kapsayıcı alma</span><span class="sxs-lookup"><span data-stu-id="c9c4b-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="c9c4b-134">İlk komut yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturur ve bu $Context bağlamı 01 değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="c9c4b-135">İkinci komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur ve bu bağlamı $Context 02 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="c9c4b-136">Son komutu, **Get-AzStorageContainer** kullanarak $Context 01 ve $Context 02 ' de depolanan bağlamların kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="c9c4b-137">Örnek 7: uç noktayla bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="c9c4b-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="c9c4b-138">Bu komut, belirtilen depolama uç noktasına sahip bir Azure depolama bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="c9c4b-139">Komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="c9c4b-140">Örnek 8: belirtilen ortamla bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="c9c4b-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="c9c4b-141">Bu komut, belirtilen Azure ortamına sahip bir Azure depolama bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="c9c4b-142">Komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="c9c4b-143">Örnek 9: SAS belirteci kullanarak bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="c9c4b-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="c9c4b-144">İlk komut, ContosoMain adlı kapsayıcı için **New-AzStorageContainerSASToken** cmdlet 'INI kullanarak SAS belirteci oluşturur ve bu belirteci $SasToken değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="c9c4b-145">Bu belirteç okuma, ekleme, güncelleştirme ve silme izinleri içindir.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="c9c4b-146">İkinci komut, $SasToken depolanan SAS belirtecini kullanan ContosoGeneral adlı hesap için bir bağlam oluşturur ve bu bağlamı $Context değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="c9c4b-147">Son komutu, $Context 'da depolanan bağlamı kullanarak ContosoMain adlı kapsayıcıyla ilişkili tüm blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="c9c4b-148">Örnek 10: OAuth kimlik doğrulamasını kullanarak bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="c9c4b-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="c9c4b-149">Bu komut, OAuth (Azure AD) kimlik doğrulamasını kullanarak bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-149">This command creates a context by using the OAuth (Azure AD) Authentication.</span></span>

## <span data-ttu-id="c9c4b-150">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9c4b-150">PARAMETERS</span></span>

### <span data-ttu-id="c9c4b-151">-Anonim</span><span class="sxs-lookup"><span data-stu-id="c9c4b-151">-Anonymous</span></span>
<span data-ttu-id="c9c4b-152">Bu cmdlet 'in anonim oturum açma için bir Azure depolama bağlamını oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="c9c4b-153">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="c9c4b-153">-ConnectionString</span></span>
<span data-ttu-id="c9c4b-154">Azure depolama bağlamı için bir bağlantı dizesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-154">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="c9c4b-155">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="c9c4b-155">-Endpoint</span></span>
<span data-ttu-id="c9c4b-156">Azure depolama bağlamının uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-156">Specifies the endpoint for the Azure Storage context.</span></span>

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

### <span data-ttu-id="c9c4b-157">-Ortam</span><span class="sxs-lookup"><span data-stu-id="c9c4b-157">-Environment</span></span>
<span data-ttu-id="c9c4b-158">Azure ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="c9c4b-159">Bu parametre için kabul edilebilir değerler: Azurecyüksek ve AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="c9c4b-160">Daha fazla bilgi için yazın `Get-Help Get-AzEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="c9c4b-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

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

### <span data-ttu-id="c9c4b-161">-Yerel</span><span class="sxs-lookup"><span data-stu-id="c9c4b-161">-Local</span></span>
<span data-ttu-id="c9c4b-162">Bu cmdlet 'in yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="c9c4b-163">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="c9c4b-163">-Protocol</span></span>
<span data-ttu-id="c9c4b-164">Aktarma Protokolü (https/http).</span><span class="sxs-lookup"><span data-stu-id="c9c4b-164">Transfer Protocol (https/http).</span></span>

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

### <span data-ttu-id="c9c4b-165">-SasToken</span><span class="sxs-lookup"><span data-stu-id="c9c4b-165">-SasToken</span></span>
<span data-ttu-id="c9c4b-166">Bağlam için paylaşılan bir erişim Imzası (SAS) belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="c9c4b-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c9c4b-167">-StorageAccountKey</span></span>
<span data-ttu-id="c9c4b-168">Bir Azure depolama hesabı anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="c9c4b-169">Bu cmdlet, bu parametrenin belirttiği anahtar için bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="c9c4b-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c9c4b-170">-StorageAccountName</span></span>
<span data-ttu-id="c9c4b-171">Azure depolama hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="c9c4b-172">Bu cmdlet, bu parametrenin belirttiği hesap için bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="c9c4b-173">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="c9c4b-173">-UseConnectedAccount</span></span>
<span data-ttu-id="c9c4b-174">Bu cmdlet 'in OAuth (Azure AD) kimlik doğrulamasıyla bir Azure depolama bağlamını oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="c9c4b-175">Diğer kimlik doğrulama belirtilmezse cmdlet, OAuth kimlik doğrulamasını varsayılan olarak kullanır.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c4b-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c4b-176">CommonParameters</span></span>
<span data-ttu-id="c9c4b-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c4b-178">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9c4b-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c4b-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9c4b-179">INPUTS</span></span>

### <span data-ttu-id="c9c4b-180">System. String</span><span class="sxs-lookup"><span data-stu-id="c9c4b-180">System.String</span></span>

## <span data-ttu-id="c9c4b-181">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9c4b-181">OUTPUTS</span></span>

### <span data-ttu-id="c9c4b-182">Microsoft. Windowsazme. Commands. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c9c4b-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="c9c4b-183">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9c4b-183">NOTES</span></span>

## <span data-ttu-id="c9c4b-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9c4b-184">RELATED LINKS</span></span>

[<span data-ttu-id="c9c4b-185">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c9c4b-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="c9c4b-186">Yeni-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="c9c4b-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


