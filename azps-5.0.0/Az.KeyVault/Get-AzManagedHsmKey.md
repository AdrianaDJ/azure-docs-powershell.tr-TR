---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
ms.openlocfilehash: 34bc2f074ee37dcf670e3e43ad647781b4d59e56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275308"
---
# <span data-ttu-id="0760f-101">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0760f-101">Get-AzManagedHsmKey</span></span>

## <span data-ttu-id="0760f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0760f-102">SYNOPSIS</span></span>
<span data-ttu-id="0760f-103">Yönetilen HSM tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="0760f-103">Gets Managed Hsm keys.</span></span>

## <span data-ttu-id="0760f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0760f-104">SYNTAX</span></span>

### <span data-ttu-id="0760f-105">Yhsmbyhsmnamegetkeywithoutconstraint 'i (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0760f-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (Default)</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0760f-106">Yhsmbyhsmnamegetkeywithbelirtildiedversion</span><span class="sxs-lookup"><span data-stu-id="0760f-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0760f-107">Yhsmbyhsmnamegetkeyıncludeallversions 'i kullanma</span><span class="sxs-lookup"><span data-stu-id="0760f-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0760f-108">Yhsmbyinputobjectgetkeywithoutconstraint 'i</span><span class="sxs-lookup"><span data-stu-id="0760f-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0760f-109">Yhsmbyinputobjectgetkeywithbelirtiledversion</span><span class="sxs-lookup"><span data-stu-id="0760f-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0760f-110">Yhsmbyinputobjectgetkeyıncludeallversions 'ı</span><span class="sxs-lookup"><span data-stu-id="0760f-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0760f-111">Yhsmbyresourceıdgetkeywithoutconstraint 'i</span><span class="sxs-lookup"><span data-stu-id="0760f-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0760f-112">Yhsmbyresourceıdgetkeywithbelirtiledversion</span><span class="sxs-lookup"><span data-stu-id="0760f-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0760f-113">Yhsmbyresourceıdgetkeyıncludeallversions 'i kullanma</span><span class="sxs-lookup"><span data-stu-id="0760f-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0760f-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="0760f-114">DESCRIPTION</span></span>
<span data-ttu-id="0760f-115">**Get-AzManagedHsmKey** cmdlet 'ı Azure yönetilebilir HSM anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="0760f-115">The **Get-AzManagedHsmKey** cmdlet gets Azure Managed Hsm keys.</span></span>
<span data-ttu-id="0760f-116">Bu cmdlet, yönetilen bir HSM veya sürüme göre belirli bir **Microsoft. Azure. Commands. Keykasa. model. keydemeti** veya tüm **anahtar paketi** nesnelerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="0760f-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a managed Hsm or by version.</span></span>

## <span data-ttu-id="0760f-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0760f-117">EXAMPLES</span></span>

### <span data-ttu-id="0760f-118">Örnek 1: yönetilen bir HSM 'deki tüm anahtarları alma</span><span class="sxs-lookup"><span data-stu-id="0760f-118">Example 1: Get all the keys in a managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm
```

<span data-ttu-id="0760f-119">Kasa/HSM adı: testmhsm adı: testkey001 Version: ID: https://testmhsm.managedhsm.azure.net:443/keys/testkey001 Enabled: true süre sonu: Şu tarihten önce değil:: 10/14/2020 3:39:16 10/14/2020 3:39:16.</span><span class="sxs-lookup"><span data-stu-id="0760f-119">Vault/HSM Name : testmhsm Name           : testkey001 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001 Enabled        : True Expires        : Not Before     : Created        : 10/14/2020 3:39:16 AM Updated        : 10/14/2020 3:39:16 AM Recovery Level : Recoverable+Purgeable Tags           :</span></span>

<span data-ttu-id="0760f-120">Kasa/HSM adı: testmhsm adı: testkey002 Version: ID: https://testmhsm.managedhsm.azure.net:443/keys/testkey002 Enabled: yanlış süre sonu: 10/14/2022 8:13:29 şu tarihten 10/14/2020 8:14:01 10/14/2020 8:14:01 10/14/2020 8:13:33 önce değil::</span><span class="sxs-lookup"><span data-stu-id="0760f-120">Vault/HSM Name : testmhsm Name           : testkey002 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey002 Enabled        : False Expires        : 10/14/2022 8:13:29 AM Not Before     : 10/14/2020 8:13:33 AM Created        : 10/14/2020 8:14:01 AM Updated        : 10/14/2020 8:14:01 AM Recovery Level : Recoverable+Purgeable Tags           : Name        Value Severity    high Accounting  true</span></span>

<span data-ttu-id="0760f-121">Bu komut testmhsm adındaki yönetilen HSM 'deki tüm anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="0760f-121">This command gets all the keys in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="0760f-122">Örnek 2: anahtarın geçerli sürümünü alma</span><span class="sxs-lookup"><span data-stu-id="0760f-122">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\>$hsm = Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001
PS C:\>$hsm

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="0760f-123">Bu komut, testmhsm adındaki yönetilen HSM 'deki testkey001 adındaki geçerli sürümü alır.</span><span class="sxs-lookup"><span data-stu-id="0760f-123">This command gets the current version of the key named testkey001 in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="0760f-124">Not: HSM adı $hsm tarafından alınabilir. VaultName</span><span class="sxs-lookup"><span data-stu-id="0760f-124">Note: Hsm Name can be obtained by $hsm.VaultName</span></span>

### <span data-ttu-id="0760f-125">Örnek 3: anahtarın tüm sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="0760f-125">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001 -IncludeVersions

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/9a9de2bcec540c3b160cd54cbae71339
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="0760f-126">Bu komut, testmhsm adındaki yönetilen HSM 'deki testkey001 adındaki anahtarın tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="0760f-126">This command gets all versions the key named testkey001 in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="0760f-127">Örnek 4: anahtarın belirli bir sürümünü alma</span><span class="sxs-lookup"><span data-stu-id="0760f-127">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey -Version 80fd43e31e8649873520053c91148418

Vault/HSM Name : testmhsm
Name           : testkey
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="0760f-128">Bu komut testmhsm adlı yönetilen HSM 'deki TestKey adındaki belirli bir sürümü alır.</span><span class="sxs-lookup"><span data-stu-id="0760f-128">This command gets a specific version of the key named testkey in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="0760f-129">Bu komutu çalıştırdıktan sonra, $Key nesnesinde gezinerek anahtarın çeşitli özelliklerini inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0760f-129">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="0760f-130">Örnek 5: silinen ancak bu yönetilen HSM için temizlenmediği tüm anahtarları edinin</span><span class="sxs-lookup"><span data-stu-id="0760f-130">Example 5: Get all the keys that have been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -InRemovedState

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 : Name        Value
                       Severity    high
                       Accounting  true                :
```

<span data-ttu-id="0760f-131">Bu komut, testmhsm adlı yönetilen HSM 'de önceden silinen ancak temizlenmediği tüm anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="0760f-131">This command gets all the keys that have been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="0760f-132">Örnek 6: silinen, ancak bu yönetilen HSM için temizlenmediği anahtar TestKey değerini alır</span><span class="sxs-lookup"><span data-stu-id="0760f-132">Example 6: Gets the key testkey that has been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\>  Get-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState 

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="0760f-133">Bu komut, testmhsm adlı yönetilen HSM 'de önceden silinen ancak temizlenmediği anahtar TestKey değerini alır.</span><span class="sxs-lookup"><span data-stu-id="0760f-133">This command gets the key testkey that has been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="0760f-134">Bu komut, silme tarihi gibi meta verileri ve bu silinmiş anahtarın zamanlanan Temizleme tarihini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0760f-134">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="0760f-135">Örnek 7: filtreleme kullanarak yönetilen bir HSM 'deki tüm anahtarları alma</span><span class="sxs-lookup"><span data-stu-id="0760f-135">Example 7: Get all the keys in a managed HSM using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName "test*"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="0760f-136">Bu komut, yönetilen HSM 'deki "test" ile başlayan testmhsm adındaki tüm anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="0760f-136">This command gets all the keys in the managed HSM named testmhsm that start with "test".</span></span>

### <span data-ttu-id="0760f-137">Örnek 8: ortak anahtarı. pem dosyası olarak Indirme</span><span class="sxs-lookup"><span data-stu-id="0760f-137">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> Get-AzManagedHsmKey -HsmName bezmhsm -Name testkey -OutFile  "C:\public.pem"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="0760f-138">Parametre belirterek RSA anahtarının ortak anahtarını indirebilirsiniz `-OutFile` .</span><span class="sxs-lookup"><span data-stu-id="0760f-138">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>

## <span data-ttu-id="0760f-139">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0760f-139">PARAMETERS</span></span>

### <span data-ttu-id="0760f-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0760f-140">-DefaultProfile</span></span>
<span data-ttu-id="0760f-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0760f-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0760f-142">-HsmName</span><span class="sxs-lookup"><span data-stu-id="0760f-142">-HsmName</span></span>
<span data-ttu-id="0760f-143">HSM adı.</span><span class="sxs-lookup"><span data-stu-id="0760f-143">HSM name.</span></span> <span data-ttu-id="0760f-144">Cmdlet, yönetilen bir HSM 'in FQDN 'sini ad ve şu anda seçili olan ortama göre oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0760f-144">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0760f-145">-Includeversions</span><span class="sxs-lookup"><span data-stu-id="0760f-145">-IncludeVersions</span></span>
<span data-ttu-id="0760f-146">Çıktıda anahtarın sürümlerinin eklenip eklenmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0760f-146">Specifies whether to include the versions of the key in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0760f-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0760f-147">-InputObject</span></span>
<span data-ttu-id="0760f-148">HSM nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0760f-148">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0760f-149">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="0760f-149">-InRemovedState</span></span>
<span data-ttu-id="0760f-150">Çıktıda önceden silinen anahtarların gösterilip gösterilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0760f-150">Specifies whether to show the previously deleted keys in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0760f-151">-Ad</span><span class="sxs-lookup"><span data-stu-id="0760f-151">-Name</span></span>
<span data-ttu-id="0760f-152">Anahtar adı.</span><span class="sxs-lookup"><span data-stu-id="0760f-152">Key name.</span></span>
<span data-ttu-id="0760f-153">Cmdlet yönetilen HSM adından, şu anda seçili olan ortamdan ve anahtar adından bir anahtarın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0760f-153">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0760f-154">-Çıkışdosyası</span><span class="sxs-lookup"><span data-stu-id="0760f-154">-OutFile</span></span>
<span data-ttu-id="0760f-155">Bu cmdlet 'in anahtarı kaydettiği çıkış dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0760f-155">Specifies the output file for which this cmdlet saves the key.</span></span>
<span data-ttu-id="0760f-156">Genel anahtar varsayılan olarak PEM biçiminde kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="0760f-156">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="0760f-157">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0760f-157">-ResourceId</span></span>
<span data-ttu-id="0760f-158">HSM kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="0760f-158">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByResourceIdGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0760f-159">-Version</span><span class="sxs-lookup"><span data-stu-id="0760f-159">-Version</span></span>
<span data-ttu-id="0760f-160">Anahtar sürümü.</span><span class="sxs-lookup"><span data-stu-id="0760f-160">Key version.</span></span>
<span data-ttu-id="0760f-161">Cmdlet yönetilen HSM adından, şu anda seçili olan ortamdan, anahtar adıyla anahtar sürümünden bir anahtarın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0760f-161">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0760f-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0760f-162">CommonParameters</span></span>
<span data-ttu-id="0760f-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0760f-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0760f-164">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0760f-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0760f-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0760f-165">INPUTS</span></span>

### <span data-ttu-id="0760f-166">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultkeyıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="0760f-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="0760f-167">System. String</span><span class="sxs-lookup"><span data-stu-id="0760f-167">System.String</span></span>

## <span data-ttu-id="0760f-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0760f-168">OUTPUTS</span></span>

### <span data-ttu-id="0760f-169">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultkeyıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="0760f-169">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="0760f-170">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0760f-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="0760f-171">Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultkeyıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="0760f-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="0760f-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0760f-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="0760f-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0760f-173">NOTES</span></span>

## <span data-ttu-id="0760f-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0760f-174">RELATED LINKS</span></span>

[<span data-ttu-id="0760f-175">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0760f-175">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="0760f-176">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0760f-176">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="0760f-177">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0760f-177">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="0760f-178">Geri al-Azmanagedhsmanahtarkaldırma</span><span class="sxs-lookup"><span data-stu-id="0760f-178">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="0760f-179">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0760f-179">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="0760f-180">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0760f-180">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)