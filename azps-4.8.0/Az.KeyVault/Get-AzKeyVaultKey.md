---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: 0de3582d9a5cbdaba8555cf53bd9038d3eaf15b2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267217"
---
# <span data-ttu-id="23131-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="23131-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="23131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23131-102">SYNOPSIS</span></span>
<span data-ttu-id="23131-103">Önemli kasa anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="23131-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="23131-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23131-104">SYNTAX</span></span>

### <span data-ttu-id="23131-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="23131-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23131-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="23131-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23131-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="23131-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23131-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="23131-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23131-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="23131-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23131-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="23131-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23131-111">Byresourceıdvaultname</span><span class="sxs-lookup"><span data-stu-id="23131-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23131-112">Byresourceıdkeyname</span><span class="sxs-lookup"><span data-stu-id="23131-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23131-113">Byresourceıdkeyversions</span><span class="sxs-lookup"><span data-stu-id="23131-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23131-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="23131-114">DESCRIPTION</span></span>
<span data-ttu-id="23131-115">**Get-Azanahtarvaultkey** cmdlet 'ı Azure Anahtar Kasası anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="23131-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="23131-116">Bu cmdlet, belirli bir **Microsoft. Azure. Commands. Keykasa. model. Keydemeti** veya Anahtar Kasası veya sürüme göre tüm **anahtar paketi** nesnelerinin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="23131-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="23131-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23131-117">EXAMPLES</span></span>

### <span data-ttu-id="23131-118">Örnek 1: anahtar kasasındaki tüm anahtarları alma</span><span class="sxs-lookup"><span data-stu-id="23131-118">Example 1: Get all the keys in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso'

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="23131-119">Bu komut, contoso adlı anahtar kasasındaki tüm anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="23131-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="23131-120">Örnek 2: anahtarın geçerli sürümünü alma</span><span class="sxs-lookup"><span data-stu-id="23131-120">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1'

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="23131-121">Bu komut, contoso adlı anahtar kasasına test1 adlı anahtarın geçerli sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="23131-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="23131-122">Örnek 3: anahtarın tüm sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="23131-122">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -IncludeVersions

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="23131-123">Bu komut, contoso adındaki anahtar vaultile ıpfx adındaki anahtarın tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="23131-123">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="23131-124">Örnek 4: anahtarın belirli bir sürümünü alma</span><span class="sxs-lookup"><span data-stu-id="23131-124">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -Version 'e4e95940e669407fbdb4298bc21a3e1d'

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="23131-125">Bu komut, contoso adlı anahtar kasasına test1 adlı anahtarın belirli bir sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="23131-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="23131-126">Bu komutu çalıştırdıktan sonra, $Key nesnesinde gezinerek anahtarın çeşitli özelliklerini inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23131-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="23131-127">Örnek 5: silinmiş ancak bu Anahtar Kasası için temizlenmiş tüm anahtarları edinin.</span><span class="sxs-lookup"><span data-stu-id="23131-127">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="23131-128">Bu komut, contoso adlı tuş kasasına önceden silinen ancak temizlenmemayan tüm anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="23131-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="23131-129">Örnek 6: silinen, ancak bu Anahtar Kasası için temizlenmiş olan anahtar ıpfx 'i alır.</span><span class="sxs-lookup"><span data-stu-id="23131-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test3' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3/1af807cc331a49d0b52b7c75e1b2366e
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="23131-130">Bu komut, contoso adlı Anahtar Kasası 'nda daha önce silinen ancak temizlenmediğim anahtar test3.</span><span class="sxs-lookup"><span data-stu-id="23131-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="23131-131">Bu komut, silme tarihi gibi meta verileri ve bu silinmiş anahtarın zamanlanan Temizleme tarihini döndürür.</span><span class="sxs-lookup"><span data-stu-id="23131-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="23131-132">Örnek 7: filtreleme kullanarak anahtar kasasındaki tüm anahtarları alma</span><span class="sxs-lookup"><span data-stu-id="23131-132">Example 7: Get all the keys in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName "test*"

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="23131-133">Bu komut, "test" ile başlayan contoso adlı tuş kasasındaki tüm anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="23131-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="23131-134">Örnek 8: ortak anahtarı. pem dosyası olarak Indirme</span><span class="sxs-lookup"><span data-stu-id="23131-134">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="23131-135">Parametre belirterek RSA anahtarının ortak anahtarını indirebilirsiniz `-OutFile` .</span><span class="sxs-lookup"><span data-stu-id="23131-135">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="23131-136">Bu, HSM korumalı anahtarları Azure Anahtar Kasası 'na almanın bir adımıdır.</span><span class="sxs-lookup"><span data-stu-id="23131-136">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="23131-137">Öğrenmek https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="23131-137">See https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="23131-138">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23131-138">PARAMETERS</span></span>

### <span data-ttu-id="23131-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23131-139">-DefaultProfile</span></span>
<span data-ttu-id="23131-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="23131-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23131-141">-Includeversions</span><span class="sxs-lookup"><span data-stu-id="23131-141">-IncludeVersions</span></span>
<span data-ttu-id="23131-142">Bu cmdlet 'in bir anahtarın tüm sürümlerini aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="23131-142">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="23131-143">Anahtarın geçerli sürümü listedeki ilk sürümdür.</span><span class="sxs-lookup"><span data-stu-id="23131-143">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="23131-144">Bu parametreyi belirtirseniz, *Name* ve *vaultname* parametrelerini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="23131-144">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="23131-145">*Includeversions* parametresini belirtmezseniz, bu cmdlet anahtarın belirtilen *ada* sahip geçerli sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="23131-145">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, ByInputObjectKeyVersions, ByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23131-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23131-146">-InputObject</span></span>
<span data-ttu-id="23131-147">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="23131-147">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23131-148">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="23131-148">-InRemovedState</span></span>
<span data-ttu-id="23131-149">Çıktıda önceden silinen anahtarların gösterilip gösterilmeyeceğini belirtir</span><span class="sxs-lookup"><span data-stu-id="23131-149">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23131-150">-Ad</span><span class="sxs-lookup"><span data-stu-id="23131-150">-Name</span></span>
<span data-ttu-id="23131-151">Alınacak anahtar paketi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23131-151">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23131-152">-Çıkışdosyası</span><span class="sxs-lookup"><span data-stu-id="23131-152">-OutFile</span></span>
<span data-ttu-id="23131-153">Bu cmdlet 'in anahtarı kaydettiği çıkış dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23131-153">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="23131-154">Genel anahtar varsayılan olarak PEM biçiminde kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="23131-154">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="23131-155">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="23131-155">-ResourceId</span></span>
<span data-ttu-id="23131-156">Tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="23131-156">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23131-157">-VaultName</span><span class="sxs-lookup"><span data-stu-id="23131-157">-VaultName</span></span>
<span data-ttu-id="23131-158">Bu cmdlet 'in anahtarları aldığı Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23131-158">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="23131-159">Bu cmdlet, bu parametrenin belirttiği adı ve seçtiğiniz ortamı belirten bir Anahtar Kasası tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23131-159">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23131-160">-Version</span><span class="sxs-lookup"><span data-stu-id="23131-160">-Version</span></span>
<span data-ttu-id="23131-161">Anahtar sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="23131-161">Specifies the key version.</span></span>
<span data-ttu-id="23131-162">Bu cmdlet, Anahtar Kasası adına, şu anda seçtiğiniz ortama, anahtar adına ve anahtar sürümüne bağlı olarak bir anahtarın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23131-162">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByInputObjectKeyName, ByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23131-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23131-163">CommonParameters</span></span>
<span data-ttu-id="23131-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23131-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23131-165">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="23131-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23131-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23131-166">INPUTS</span></span>

### <span data-ttu-id="23131-167">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="23131-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="23131-168">System. String</span><span class="sxs-lookup"><span data-stu-id="23131-168">System.String</span></span>

## <span data-ttu-id="23131-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23131-169">OUTPUTS</span></span>

### <span data-ttu-id="23131-170">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultkeyıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="23131-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="23131-171">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="23131-171">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="23131-172">Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultkeyıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="23131-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="23131-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="23131-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="23131-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23131-174">NOTES</span></span>

## <span data-ttu-id="23131-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23131-175">RELATED LINKS</span></span>

[<span data-ttu-id="23131-176">Add-Azanahtarvaultkey</span><span class="sxs-lookup"><span data-stu-id="23131-176">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="23131-177">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="23131-177">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="23131-178">Geri al-Aztuş Vaultkeykaldırması</span><span class="sxs-lookup"><span data-stu-id="23131-178">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="23131-179">Set-Azanahtarvaultkeyattribute</span><span class="sxs-lookup"><span data-stu-id="23131-179">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

