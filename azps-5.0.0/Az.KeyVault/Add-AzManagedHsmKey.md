---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
ms.openlocfilehash: 89238992b99d86cdd56337a3002167be9c0d78d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280233"
---
# <span data-ttu-id="03c19-101">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="03c19-101">Add-AzManagedHsmKey</span></span>

## <span data-ttu-id="03c19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03c19-102">SYNOPSIS</span></span>
<span data-ttu-id="03c19-103">Yönetilen bir HSM 'de anahtar oluşturur veya bir anahtarı yönetilen bir HSM 'ye aktarır.</span><span class="sxs-lookup"><span data-stu-id="03c19-103">Creates a key in a managed HSM or imports a key into a managed HSM.</span></span>

## <span data-ttu-id="03c19-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03c19-104">SYNTAX</span></span>

### <span data-ttu-id="03c19-105">Interactivecoluştur (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="03c19-105">InteractiveCreate (Default)</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c19-106">Interactiveımport</span><span class="sxs-lookup"><span data-stu-id="03c19-106">InteractiveImport</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03c19-107">Inputobjectcreate</span><span class="sxs-lookup"><span data-stu-id="03c19-107">InputObjectCreate</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyType <String> [-CurveName <String>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-Size <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c19-108">Inputobjectimport</span><span class="sxs-lookup"><span data-stu-id="03c19-108">InputObjectImport</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03c19-109">Resourceıdcreate</span><span class="sxs-lookup"><span data-stu-id="03c19-109">ResourceIdCreate</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c19-110">Resourceidmport</span><span class="sxs-lookup"><span data-stu-id="03c19-110">ResourceIdImport</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03c19-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="03c19-111">DESCRIPTION</span></span>
<span data-ttu-id="03c19-112">**Add-AzManagedHsmKey** cmdlet 'i, yönetilen HSM 'de yönetilen bir HSM 'de anahtar oluşturur veya bir anahtarı YÖNETILEN bir HSM 'ye aktarır.</span><span class="sxs-lookup"><span data-stu-id="03c19-112">The **Add-AzManagedHsmKey** cmdlet creates a key in a managed HSM in Azure Managed Hsm or imports a key into a managed HSM.</span></span>
<span data-ttu-id="03c19-113">Aşağıdaki yöntemlerden herhangi birini kullanarak anahtar eklemek için bu cmdlet 'i kullanın:</span><span class="sxs-lookup"><span data-stu-id="03c19-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="03c19-114">Varsayılan anahtar öznitelikleriyle anahtar oluşturma</span><span class="sxs-lookup"><span data-stu-id="03c19-114">Create a key with default key attributes</span></span>
- <span data-ttu-id="03c19-115">Verilen anahtar öznitelikleri ile anahtar oluşturma</span><span class="sxs-lookup"><span data-stu-id="03c19-115">Create a key with given key attributes</span></span>
- <span data-ttu-id="03c19-116">Bilgisayarınızdaki. pfx dosyasından bir anahtar içeri aktarın.</span><span class="sxs-lookup"><span data-stu-id="03c19-116">Import a key from a .pfx file on your computer.</span></span>
<span data-ttu-id="03c19-117">Bu işlemlerden herhangi biri için, anahtar öznitelikleri sağlayabilir veya varsayılan ayarları kabul edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03c19-117">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="03c19-118">Yönetilen HSM 'unuzda varolan bir anahtarla aynı ada sahip bir anahtar oluşturabilir veya içeri aktarırsanız, özgün anahtar yeni anahtar için belirttiğiniz değerlerle güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="03c19-118">If you create or import a key that has the same name as an existing key in your managed HSM, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="03c19-119">Anahtarın söz konusu sürümü için sürüme özgü URI 'yi kullanarak önceki değerlere erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03c19-119">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="03c19-120">Anahtar sürümleri ve URI yapısı hakkında bilgi edinmek için, yönetilen HSM REST API belgelerindeki [anahtarlar ve gizlilikler hakkında](http://go.microsoft.com/fwlink/?linkid=518560) bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="03c19-120">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Managed HSM REST API documentation.</span></span>

## <span data-ttu-id="03c19-121">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03c19-121">EXAMPLES</span></span>

### <span data-ttu-id="03c19-122">Örnek 1: RSA-HSM anahtarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="03c19-122">Example 1: Create a RSA-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType RSA

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 7:55:43 AM
Updated        : 10/14/2020 7:55:43 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="03c19-123">Bu komut testmhsm adlı yönetilen HSM testanahtarındaki TestKey adında bir RSA-HSM anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03c19-123">This command creates a RSA-HSM key named testkey in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="03c19-124">Örnek 2: EC-HSM anahtarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="03c19-124">Example 2: Create a EC-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType EC -CurveName P-256

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="03c19-125">Bu komut testmhsm adlı yönetilen HSM testanahtarındaki P-256 eğrisini kullanarak test anahtarı adında bir EC HSM anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03c19-125">This command creates a EC-HSM key named testkey using P-256 curve in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="03c19-126">Örnek 3: varsayılan olmayan değerler içeren bir eki HSM anahtarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="03c19-126">Example 3: Create a oct-HSM key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType oct -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
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

<span data-ttu-id="03c19-127">İlk komut, değerleri çözme ve $KeyOperations değişkeninde doğrulama değerlerini depolar.</span><span class="sxs-lookup"><span data-stu-id="03c19-127">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="03c19-128">İkinci komut, **Get-Date** cmdlet 'INI kullanarak UTC 'de tanımlanmış bir **DateTime** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03c19-128">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="03c19-129">Bu nesne gelecek yıl iki yıl belirtir.</span><span class="sxs-lookup"><span data-stu-id="03c19-129">That object specifies a time two years in the future.</span></span> <span data-ttu-id="03c19-130">Komut bu tarihi $Expires değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="03c19-130">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="03c19-131">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="03c19-131">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="03c19-132">Üçüncü komut **Get-Date** cmdlet 'ini kullanarak bir **DateTime** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03c19-132">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="03c19-133">Bu nesne geçerli UTC zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03c19-133">That object specifies current UTC time.</span></span> <span data-ttu-id="03c19-134">Komut bu tarihi $NotBefore değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="03c19-134">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="03c19-135">Son komutu, Eki HSM anahtarı olan TestKey adında bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03c19-135">The final command creates a key named testkey that is an oct-HSM key.</span></span> <span data-ttu-id="03c19-136">Komut $KeyOperations depolanan izin verilen anahtar işlemlerinin değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="03c19-136">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="03c19-137">Komut, önceki komutlarda oluşturulan *son* ve *notöncesi* parametrelerinin zamanlarını ve yüksek önem düzeyi ve etiket etiketlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="03c19-137">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="03c19-138">Yeni anahtar devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="03c19-138">The new key is disabled.</span></span> <span data-ttu-id="03c19-139">**Update-AzManagedHsmKey** cmdlet 'ini kullanarak etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03c19-139">You can enable it by using the **Update-AzManagedHsmKey** cmdlet.</span></span>

## <span data-ttu-id="03c19-140">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03c19-140">PARAMETERS</span></span>

### <span data-ttu-id="03c19-141">-CurveName</span><span class="sxs-lookup"><span data-stu-id="03c19-141">-CurveName</span></span>
<span data-ttu-id="03c19-142">Eliptik Eğri şifrelemesi 'nin eğri adını belirtir; KeyType EC olduğunda bu değer geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="03c19-142">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

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

### <span data-ttu-id="03c19-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c19-143">-DefaultProfile</span></span>
<span data-ttu-id="03c19-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="03c19-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03c19-145">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="03c19-145">-Disable</span></span>
<span data-ttu-id="03c19-146">Eklediğiniz anahtarın başlangıçtaki durumuna ayarlı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="03c19-146">Indicates that the key you are adding is set to an initial state of disabled.</span></span>
<span data-ttu-id="03c19-147">Anahtarı kullanma girişimleri başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="03c19-147">Any attempt to use the key will fail.</span></span>
<span data-ttu-id="03c19-148">Daha sonra etkinleştirmeyi düşündüğünüz anahtarları önceden yüklüyorsanız, bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="03c19-148">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="03c19-149">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="03c19-149">-Expires</span></span>
<span data-ttu-id="03c19-150">UTC 'de anahtarın son kullanma zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03c19-150">Specifies the expiration time of the key in UTC.</span></span>
<span data-ttu-id="03c19-151">Belirtilmezse, anahtarın süresi dolmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="03c19-151">If not specified, key will not expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c19-152">-HsmName</span><span class="sxs-lookup"><span data-stu-id="03c19-152">-HsmName</span></span>
<span data-ttu-id="03c19-153">HSM adı.</span><span class="sxs-lookup"><span data-stu-id="03c19-153">HSM name.</span></span> <span data-ttu-id="03c19-154">Cmdlet, yönetilen bir HSM 'in FQDN 'sini ad ve şu anda seçili olan ortama göre oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03c19-154">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c19-155">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03c19-155">-InputObject</span></span>
<span data-ttu-id="03c19-156">HSM nesnesi.</span><span class="sxs-lookup"><span data-stu-id="03c19-156">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03c19-157">-Anahtardosyasıparolası</span><span class="sxs-lookup"><span data-stu-id="03c19-157">-KeyFilePassword</span></span>
<span data-ttu-id="03c19-158">İçeri aktarılacak anahtar malzemesini içeren yerel dosyanın parolası.</span><span class="sxs-lookup"><span data-stu-id="03c19-158">Password of the local file containing the key material to be imported.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c19-159">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="03c19-159">-KeyFilePath</span></span>
<span data-ttu-id="03c19-160">İçeri aktarılacak anahtar malzemesini içeren yerel dosyanın yolu.</span><span class="sxs-lookup"><span data-stu-id="03c19-160">Path to the local file containing the key material to be imported.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c19-161">-Keyolar</span><span class="sxs-lookup"><span data-stu-id="03c19-161">-KeyOps</span></span>
<span data-ttu-id="03c19-162">Anahtarla gerçekleştirilebileceği işlemler.</span><span class="sxs-lookup"><span data-stu-id="03c19-162">The operations that can be performed with the key.</span></span>
<span data-ttu-id="03c19-163">Yoksa tüm işlemler gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="03c19-163">If not present, all operations can be performed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c19-164">-KeyType</span><span class="sxs-lookup"><span data-stu-id="03c19-164">-KeyType</span></span>
<span data-ttu-id="03c19-165">Bu anahtarın anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="03c19-165">Specifies the key type of this key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c19-166">-Ad</span><span class="sxs-lookup"><span data-stu-id="03c19-166">-Name</span></span>
<span data-ttu-id="03c19-167">Anahtar adı.</span><span class="sxs-lookup"><span data-stu-id="03c19-167">Key name.</span></span>
<span data-ttu-id="03c19-168">Cmdlet yönetilen HSM adından, şu anda seçili olan ortamdan ve anahtar adından bir anahtarın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03c19-168">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c19-169">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="03c19-169">-NotBefore</span></span>
<span data-ttu-id="03c19-170">Anahtarın kullanılmadığı UTC saati.</span><span class="sxs-lookup"><span data-stu-id="03c19-170">The UTC time before which the key can't be used.</span></span>
<span data-ttu-id="03c19-171">Belirtilmezse, hiçbir sınırlama yoktur.</span><span class="sxs-lookup"><span data-stu-id="03c19-171">If not specified, there is no limitation.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c19-172">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="03c19-172">-ResourceId</span></span>
<span data-ttu-id="03c19-173">HSM kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="03c19-173">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03c19-174">-Boyut</span><span class="sxs-lookup"><span data-stu-id="03c19-174">-Size</span></span>
<span data-ttu-id="03c19-175">RSA anahtar boyutu, bit cinsinden.</span><span class="sxs-lookup"><span data-stu-id="03c19-175">RSA key size, in bits.</span></span>
<span data-ttu-id="03c19-176">Belirtilmezse, hizmet güvenli bir varsayılan olacaktır.</span><span class="sxs-lookup"><span data-stu-id="03c19-176">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c19-177">Etiketli</span><span class="sxs-lookup"><span data-stu-id="03c19-177">-Tag</span></span>
<span data-ttu-id="03c19-178">Anahtar etiketleri temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="03c19-178">A hashtable representing key tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c19-179">-Onay</span><span class="sxs-lookup"><span data-stu-id="03c19-179">-Confirm</span></span>
<span data-ttu-id="03c19-180">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="03c19-180">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c19-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03c19-181">-WhatIf</span></span>
<span data-ttu-id="03c19-182">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="03c19-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03c19-183">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="03c19-183">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c19-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c19-184">CommonParameters</span></span>
<span data-ttu-id="03c19-185">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03c19-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c19-186">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="03c19-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c19-187">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03c19-187">INPUTS</span></span>

### <span data-ttu-id="03c19-188">Microsoft. Azure. Commands. Keykasa. modeller. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="03c19-188">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="03c19-189">System. String</span><span class="sxs-lookup"><span data-stu-id="03c19-189">System.String</span></span>

## <span data-ttu-id="03c19-190">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03c19-190">OUTPUTS</span></span>

### <span data-ttu-id="03c19-191">Microsoft. Azure. Commands. Keykasa. modeller. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="03c19-191">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="03c19-192">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03c19-192">NOTES</span></span>

## <span data-ttu-id="03c19-193">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03c19-193">RELATED LINKS</span></span>

[<span data-ttu-id="03c19-194">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="03c19-194">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="03c19-195">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="03c19-195">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="03c19-196">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="03c19-196">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="03c19-197">Geri al-Azmanagedhsmanahtarkaldırma</span><span class="sxs-lookup"><span data-stu-id="03c19-197">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="03c19-198">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="03c19-198">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="03c19-199">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="03c19-199">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)
