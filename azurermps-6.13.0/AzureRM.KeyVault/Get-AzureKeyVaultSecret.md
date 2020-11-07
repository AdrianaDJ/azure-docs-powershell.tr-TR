---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
ms.openlocfilehash: aa8306070eb560deb465cbaa9ddae2bce24c5600
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593245"
---
# <span data-ttu-id="e1a33-101">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e1a33-101">Get-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="e1a33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1a33-102">SYNOPSIS</span></span>
<span data-ttu-id="e1a33-103">Anahtar kasasındaki gizlilikleri alır.</span><span class="sxs-lookup"><span data-stu-id="e1a33-103">Gets the secrets in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1a33-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e1a33-104">SYNTAX</span></span>

### <span data-ttu-id="e1a33-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e1a33-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1a33-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="e1a33-106">BySecretName</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1a33-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="e1a33-107">BySecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1a33-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="e1a33-108">ByInputObjectVaultName</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1a33-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="e1a33-109">ByInputObjectSecretName</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1a33-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="e1a33-110">ByInputObjectSecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1a33-111">Byresourceıdvaultname</span><span class="sxs-lookup"><span data-stu-id="e1a33-111">ByResourceIdVaultName</span></span>
```
Get-AzureKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1a33-112">Byresourceıdsecretname</span><span class="sxs-lookup"><span data-stu-id="e1a33-112">ByResourceIdSecretName</span></span>
```
Get-AzureKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1a33-113">Byresourceıdsecretversions</span><span class="sxs-lookup"><span data-stu-id="e1a33-113">ByResourceIdSecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1a33-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="e1a33-114">DESCRIPTION</span></span>
<span data-ttu-id="e1a33-115">**Get-AzureKeyVaultSecret** cmdlet 'i anahtar kasasındaki gizlilikleri alır.</span><span class="sxs-lookup"><span data-stu-id="e1a33-115">The **Get-AzureKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="e1a33-116">Bu cmdlet, bir anahtar kasasındaki belirli bir gizliliği veya tüm gizlilikleri alır.</span><span class="sxs-lookup"><span data-stu-id="e1a33-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="e1a33-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e1a33-117">EXAMPLES</span></span>

### <span data-ttu-id="e1a33-118">Örnek 1: anahtar kasasındaki tüm gizliliklerin tüm geçerli sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="e1a33-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso'

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="e1a33-119">Bu komut, contoso adlı anahtar kasasındaki tüm gizliliklerin geçerli sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="e1a33-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="e1a33-120">Örnek 2: belirli bir gizliliğin tüm sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="e1a33-120">Example 2: Get all versions of a specific secret</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -IncludeVersions

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="e1a33-121">Bu komut, contoso adlı anahtar kasasındaki parola adındaki tüm secret1.</span><span class="sxs-lookup"><span data-stu-id="e1a33-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="e1a33-122">Örnek 3: belirli bir parolanın geçerli sürümünü alma</span><span class="sxs-lookup"><span data-stu-id="e1a33-122">Example 3: Get the current version of a specific secret</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'secret1'

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="e1a33-123">Bu komut, contoso adlı anahtar kasasındaki parola adlı secret1 'in geçerli sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="e1a33-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="e1a33-124">Örnek 4: belirli bir gizli sürümü alma</span><span class="sxs-lookup"><span data-stu-id="e1a33-124">Example 4: Get a specific version of a specific secret</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -Version '5d1a74ba2c454439886fb8509b6cab3c'

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="e1a33-125">Bu komut, contoso adlı anahtar kasasındaki gizli adlı secret1 'in belirli bir sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="e1a33-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="e1a33-126">Örnek 5: belirli bir parolanın geçerli sürümünün düz metin değerini alma</span><span class="sxs-lookup"><span data-stu-id="e1a33-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is:" $secret.SecretValueText

Secret Value is: P@ssw0rd
```

<span data-ttu-id="e1a33-127">Bu komutlar, gizli adlı gizli adı olan geçerli sürümü alır ve bu gizliliğin düz metin değerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="e1a33-127">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="e1a33-128">Örnek 6: silinmiş ancak bu Anahtar Kasası için temizlenmiş tüm gizlilikleri alın.</span><span class="sxs-lookup"><span data-stu-id="e1a33-128">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Id                   : https://contoso.vault.azure.net:443/secrets/secret1
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :

Vault Name           : contoso
Name                 : secret2
Id                   : https://contoso.vault.azure.net:443/secrets/secret2
Deleted Date         : 5/7/2018 7:56:34 PM
Scheduled Purge Date : 8/5/2018 7:56:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/6/2018 8:39:15 PM
Updated              : 4/6/2018 10:11:24 PM
Content Type         : 
Tags                 :
```

<span data-ttu-id="e1a33-129">Bu komut, contoso adlı tuş kasasına daha önce silinen ancak temizlenmediğim tüm gizlilikleri alır.</span><span class="sxs-lookup"><span data-stu-id="e1a33-129">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="e1a33-130">Örnek 7: silinen, ancak bu Anahtar Kasası için temizlenmedi gizli gizli kaldırmaları alır.</span><span class="sxs-lookup"><span data-stu-id="e1a33-130">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'secret1' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Version              : 689d23346e9c42a2a64f4e3d75094dcc
Id                   : https://contoso.vault.azure.net:443/secrets/secret1/689d23346e9c42a2a64f4e3d75094dcc
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="e1a33-131">Bu komut, contoso adlı Anahtar Kasası 'nda, önceden silinmiş ancak temizlenmeden önce ' secret1 ' parolasını alır.</span><span class="sxs-lookup"><span data-stu-id="e1a33-131">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="e1a33-132">Bu komut, silme tarihi gibi meta verileri ve bu silinmiş gizliliğin zamanlanmış temizleme tarihini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e1a33-132">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="e1a33-133">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e1a33-133">PARAMETERS</span></span>

### <span data-ttu-id="e1a33-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1a33-134">-DefaultProfile</span></span>
<span data-ttu-id="e1a33-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e1a33-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1a33-136">-Includeversions</span><span class="sxs-lookup"><span data-stu-id="e1a33-136">-IncludeVersions</span></span>
<span data-ttu-id="e1a33-137">Bu cmdlet 'in tüm gizli sürümleri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e1a33-137">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="e1a33-138">Bir parolanın geçerli sürümü listedeki ilk sürümdür.</span><span class="sxs-lookup"><span data-stu-id="e1a33-138">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="e1a33-139">Bu parametreyi belirtirseniz, *Name* ve *vaultname* parametrelerini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e1a33-139">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="e1a33-140">*Includeversions* parametresini belirtmezseniz, bu cmdlet parolanın belirtilen *adla* geçerli gizliliğini alır.</span><span class="sxs-lookup"><span data-stu-id="e1a33-140">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySecretVersions, ByInputObjectSecretVersions, ByResourceIdSecretVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a33-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1a33-141">-InputObject</span></span>
<span data-ttu-id="e1a33-142">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e1a33-142">KeyVault Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1a33-143">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="e1a33-143">-InRemovedState</span></span>
<span data-ttu-id="e1a33-144">Çıktıda önceden silinen gizliliklerin gösterilip gösterilmeyeceğini belirtir</span><span class="sxs-lookup"><span data-stu-id="e1a33-144">Specifies whether to show the previously deleted secrets in the output</span></span>

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

### <span data-ttu-id="e1a33-145">-Ad</span><span class="sxs-lookup"><span data-stu-id="e1a33-145">-Name</span></span>
<span data-ttu-id="e1a33-146">Alınacak parolanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1a33-146">Specifies the name of the secret to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a33-147">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e1a33-147">-ResourceId</span></span>
<span data-ttu-id="e1a33-148">Tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="e1a33-148">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1a33-149">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e1a33-149">-VaultName</span></span>
<span data-ttu-id="e1a33-150">Gizliliğin ait olduğu Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1a33-150">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="e1a33-151">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e1a33-151">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, BySecretName, BySecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a33-152">-Version</span><span class="sxs-lookup"><span data-stu-id="e1a33-152">-Version</span></span>
<span data-ttu-id="e1a33-153">Gizli sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1a33-153">Specifies the secret version.</span></span>
<span data-ttu-id="e1a33-154">Bu cmdlet, Anahtar Kasası adına, şu anda seçili ortama, gizli adına ve gizli sürüme göre gizli bir FQDN oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e1a33-154">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName, ByInputObjectSecretName, ByResourceIdSecretName
Aliases: SecretVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a33-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1a33-155">CommonParameters</span></span>
<span data-ttu-id="e1a33-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e1a33-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1a33-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1a33-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1a33-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e1a33-158">INPUTS</span></span>

### <span data-ttu-id="e1a33-159">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="e1a33-159">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="e1a33-160">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e1a33-160">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e1a33-161">System. String</span><span class="sxs-lookup"><span data-stu-id="e1a33-161">System.String</span></span>

## <span data-ttu-id="e1a33-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e1a33-162">OUTPUTS</span></span>

### <span data-ttu-id="e1a33-163">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultsecretidentityıtem</span><span class="sxs-lookup"><span data-stu-id="e1a33-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="e1a33-164">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e1a33-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="e1a33-165">Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultsecretidentityıtem</span><span class="sxs-lookup"><span data-stu-id="e1a33-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="e1a33-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e1a33-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="e1a33-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e1a33-167">NOTES</span></span>

## <span data-ttu-id="e1a33-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e1a33-168">RELATED LINKS</span></span>

[<span data-ttu-id="e1a33-169">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e1a33-169">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="e1a33-170">Geri al-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="e1a33-170">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

[<span data-ttu-id="e1a33-171">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e1a33-171">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)
