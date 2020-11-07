---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: 21d2f6efa039dbd9b229562fcefd53c715f400fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916324"
---
# <span data-ttu-id="9ccff-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9ccff-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="9ccff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ccff-102">SYNOPSIS</span></span>
<span data-ttu-id="9ccff-103">Önemli kasa anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="9ccff-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="9ccff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ccff-104">SYNTAX</span></span>

### <span data-ttu-id="9ccff-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9ccff-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ccff-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="9ccff-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ccff-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="9ccff-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ccff-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="9ccff-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ccff-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="9ccff-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ccff-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="9ccff-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ccff-111">Byresourceıdvaultname</span><span class="sxs-lookup"><span data-stu-id="9ccff-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ccff-112">Byresourceıdkeyname</span><span class="sxs-lookup"><span data-stu-id="9ccff-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ccff-113">Byresourceıdkeyversions</span><span class="sxs-lookup"><span data-stu-id="9ccff-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ccff-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ccff-114">DESCRIPTION</span></span>
<span data-ttu-id="9ccff-115">**Get-Azanahtarvaultkey** cmdlet 'ı Azure Anahtar Kasası anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="9ccff-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="9ccff-116">Bu cmdlet, belirli bir **Microsoft. Azure. Commands. Keykasa. model. Keydemeti** veya Anahtar Kasası veya sürüme göre tüm **anahtar paketi** nesnelerinin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="9ccff-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="9ccff-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ccff-117">EXAMPLES</span></span>

### <span data-ttu-id="9ccff-118">Örnek 1: anahtar kasasındaki tüm anahtarları alma</span><span class="sxs-lookup"><span data-stu-id="9ccff-118">Example 1: Get all the keys in a key vault</span></span>
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

<span data-ttu-id="9ccff-119">Bu komut, contoso adlı anahtar kasasındaki tüm anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="9ccff-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="9ccff-120">Örnek 2: anahtarın geçerli sürümünü alma</span><span class="sxs-lookup"><span data-stu-id="9ccff-120">Example 2: Get the current version of a key</span></span>
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

<span data-ttu-id="9ccff-121">Bu komut, contoso adlı anahtar kasasına test1 adlı anahtarın geçerli sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="9ccff-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="9ccff-122">Örnek 3: anahtarın tüm sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="9ccff-122">Example 3: Get all versions of a key</span></span>
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

<span data-ttu-id="9ccff-123">Bu komut, contoso adındaki anahtar vaultile ıpfx adındaki anahtarın tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="9ccff-123">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="9ccff-124">Örnek 4: anahtarın belirli bir sürümünü alma</span><span class="sxs-lookup"><span data-stu-id="9ccff-124">Example 4: Get a specific version of a key</span></span>
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

<span data-ttu-id="9ccff-125">Bu komut, contoso adlı anahtar kasasına test1 adlı anahtarın belirli bir sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="9ccff-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="9ccff-126">Bu komutu çalıştırdıktan sonra, $Key nesnesinde gezinerek anahtarın çeşitli özelliklerini inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9ccff-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="9ccff-127">Örnek 5: silinmiş ancak bu Anahtar Kasası için temizlenmiş tüm anahtarları edinin.</span><span class="sxs-lookup"><span data-stu-id="9ccff-127">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="9ccff-128">Bu komut, contoso adlı tuş kasasına önceden silinen ancak temizlenmemayan tüm anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="9ccff-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="9ccff-129">Örnek 6: silinen, ancak bu Anahtar Kasası için temizlenmiş olan anahtar ıpfx 'i alır.</span><span class="sxs-lookup"><span data-stu-id="9ccff-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="9ccff-130">Bu komut, contoso adlı Anahtar Kasası 'nda daha önce silinen ancak temizlenmediğim anahtar test3.</span><span class="sxs-lookup"><span data-stu-id="9ccff-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="9ccff-131">Bu komut, silme tarihi gibi meta verileri ve bu silinmiş anahtarın zamanlanan Temizleme tarihini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9ccff-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="9ccff-132">Örnek 7: filtreleme kullanarak anahtar kasasındaki tüm anahtarları alma</span><span class="sxs-lookup"><span data-stu-id="9ccff-132">Example 7: Get all the keys in a key vault using filtering</span></span>
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

<span data-ttu-id="9ccff-133">Bu komut, "test" ile başlayan contoso adlı tuş kasasındaki tüm anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="9ccff-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

## <span data-ttu-id="9ccff-134">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ccff-134">PARAMETERS</span></span>

### <span data-ttu-id="9ccff-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ccff-135">-DefaultProfile</span></span>
<span data-ttu-id="9ccff-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9ccff-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ccff-137">-Includeversions</span><span class="sxs-lookup"><span data-stu-id="9ccff-137">-IncludeVersions</span></span>
<span data-ttu-id="9ccff-138">Bu cmdlet 'in bir anahtarın tüm sürümlerini aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9ccff-138">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="9ccff-139">Anahtarın geçerli sürümü listedeki ilk sürümdür.</span><span class="sxs-lookup"><span data-stu-id="9ccff-139">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="9ccff-140">Bu parametreyi belirtirseniz, *Name* ve *vaultname* parametrelerini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9ccff-140">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="9ccff-141">*Includeversions* parametresini belirtmezseniz, bu cmdlet anahtarın belirtilen *ada* sahip geçerli sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="9ccff-141">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

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

### <span data-ttu-id="9ccff-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ccff-142">-InputObject</span></span>
<span data-ttu-id="9ccff-143">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9ccff-143">KeyVault object.</span></span>

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

### <span data-ttu-id="9ccff-144">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="9ccff-144">-InRemovedState</span></span>
<span data-ttu-id="9ccff-145">Çıktıda önceden silinen anahtarların gösterilip gösterilmeyeceğini belirtir</span><span class="sxs-lookup"><span data-stu-id="9ccff-145">Specifies whether to show the previously deleted keys in the output</span></span>

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

### <span data-ttu-id="9ccff-146">-Ad</span><span class="sxs-lookup"><span data-stu-id="9ccff-146">-Name</span></span>
<span data-ttu-id="9ccff-147">Alınacak anahtar paketi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ccff-147">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="9ccff-148">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9ccff-148">-ResourceId</span></span>
<span data-ttu-id="9ccff-149">Tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="9ccff-149">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="9ccff-150">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9ccff-150">-VaultName</span></span>
<span data-ttu-id="9ccff-151">Bu cmdlet 'in anahtarları aldığı Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ccff-151">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="9ccff-152">Bu cmdlet, bu parametrenin belirttiği adı ve seçtiğiniz ortamı belirten bir Anahtar Kasası tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ccff-152">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="9ccff-153">-Version</span><span class="sxs-lookup"><span data-stu-id="9ccff-153">-Version</span></span>
<span data-ttu-id="9ccff-154">Anahtar sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ccff-154">Specifies the key version.</span></span>
<span data-ttu-id="9ccff-155">Bu cmdlet, Anahtar Kasası adına, şu anda seçtiğiniz ortama, anahtar adına ve anahtar sürümüne bağlı olarak bir anahtarın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ccff-155">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="9ccff-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ccff-156">CommonParameters</span></span>
<span data-ttu-id="9ccff-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ccff-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ccff-158">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9ccff-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ccff-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ccff-159">INPUTS</span></span>

### <span data-ttu-id="9ccff-160">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="9ccff-160">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="9ccff-161">System. String</span><span class="sxs-lookup"><span data-stu-id="9ccff-161">System.String</span></span>

## <span data-ttu-id="9ccff-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ccff-162">OUTPUTS</span></span>

### <span data-ttu-id="9ccff-163">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultkeyıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="9ccff-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="9ccff-164">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9ccff-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="9ccff-165">Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultkeyıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="9ccff-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="9ccff-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9ccff-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="9ccff-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ccff-167">NOTES</span></span>

## <span data-ttu-id="9ccff-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ccff-168">RELATED LINKS</span></span>

[<span data-ttu-id="9ccff-169">Add-Azanahtarvaultkey</span><span class="sxs-lookup"><span data-stu-id="9ccff-169">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="9ccff-170">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9ccff-170">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="9ccff-171">Geri al-Aztuş Vaultkeykaldırması</span><span class="sxs-lookup"><span data-stu-id="9ccff-171">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="9ccff-172">Set-Azanahtarvaultkeyattribute</span><span class="sxs-lookup"><span data-stu-id="9ccff-172">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

