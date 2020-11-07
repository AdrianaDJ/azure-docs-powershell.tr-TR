---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 48b5182efd368b0950313ac4d2c7b2e23f2948fd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936647"
---
# <span data-ttu-id="476eb-101">Set-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="476eb-101">Set-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="476eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="476eb-102">SYNOPSIS</span></span>
<span data-ttu-id="476eb-103">Belirli bir Anahtar Kasası yönetilen Azure depolama hesabı için anahtar kasası ile paylaşılan erişim Imzası (SAS) tanımı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="476eb-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="476eb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="476eb-104">SYNTAX</span></span>

### <span data-ttu-id="476eb-105">RawSas (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="476eb-105">RawSas (Default)</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Parameter] <Hashtable> [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="476eb-106">AdhocAccountSas</span><span class="sxs-lookup"><span data-stu-id="476eb-106">AdhocAccountSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition -Service <String[]> -ResourceType <String[]>
 [-ApiVersion <String>] [-VaultName] <String> [-AccountName] <String> [-Name] <String> [-Disable]
 [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>] [-IPAddressOrRange <String>]
 -ValidityPeriod <TimeSpan> -Permission <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="476eb-107">AdhocServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="476eb-107">AdhocServiceBlobSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Blob <String>
 -Container <String> [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="476eb-108">AdhocServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="476eb-108">AdhocServiceContainerSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Container <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="476eb-109">AdhocServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="476eb-109">AdhocServiceFileSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="476eb-110">AdhocServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="476eb-110">AdhocServiceShareSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="476eb-111">AdhocServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="476eb-111">AdhocServiceQueueSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Queue <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="476eb-112">AdhocServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="476eb-112">AdhocServiceTableSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Table <String>
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="476eb-113">StoredPolicyServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="476eb-113">StoredPolicyServiceBlobSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Blob <String> -Container <String> -Policy <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="476eb-114">StoredPolicyServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="476eb-114">StoredPolicyServiceContainerSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Container <String> -Policy <String> [-SharedAccessHeader <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="476eb-115">StoredPolicyServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="476eb-115">StoredPolicyServiceFileSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String> -Path <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="476eb-116">StoredPolicyServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="476eb-116">StoredPolicyServiceShareSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="476eb-117">StoredPolicyServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="476eb-117">StoredPolicyServiceQueueSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Queue <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="476eb-118">StoredPolicyServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="476eb-118">StoredPolicyServiceTableSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Table <String> [-StartPartitionKey <String>]
 [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="476eb-119">Tanım</span><span class="sxs-lookup"><span data-stu-id="476eb-119">DESCRIPTION</span></span>
<span data-ttu-id="476eb-120">Belirli bir Anahtar Kasası yönetilen Azure depolama hesabıyla paylaşılan erişim Imzası (SAS) tanımı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="476eb-120">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="476eb-121">Bu, SAS belirtecini bu SAS tanımına almak için kullanılabilecek bir gizli ayarlar da yapar.</span><span class="sxs-lookup"><span data-stu-id="476eb-121">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="476eb-122">SAS belirteci, bu parametreler ve Anahtar Kasası yönetilen Azure depolama hesabının etkin anahtarı kullanılarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="476eb-122">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="476eb-123">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="476eb-123">EXAMPLES</span></span>

### <span data-ttu-id="476eb-124">Örnek 1: geçici hizmet blob SAS tanımını ayarlama</span><span class="sxs-lookup"><span data-stu-id="476eb-124">Example 1 : Set an ad hoc service Blob sas definition</span></span>
```
PS C:\> Set-AzKeyVaultManagedStorageSasDefinition -Blob 'blob1' -Container 'container1' -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add -SharedAccessHeader CacheControl,ContentDisposition -Protocol HttpsOnly -IPAddressOrRange '168.1.5.60-168.1.5.70'
```

<span data-ttu-id="476eb-125">' Vault1 ' kasasındaki ' hesabı1 ' Anahtar Kasası yönetilen depolama hesabı ile geçici hizmet blob SAS tanımı ' sas1 ' ayarlar.</span><span class="sxs-lookup"><span data-stu-id="476eb-125">Sets an ad hoc service blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="476eb-126">Örnek 2: geçici hesap SAS tanımını ayarlama</span><span class="sxs-lookup"><span data-stu-id="476eb-126">Example 2 : Set an ad hoc account sas definition</span></span>
```
PS C:\> Set-AzKeyVaultManagedStorageSasDefinition -Service Blob,File -ResourceType Container,Service -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -Protocol HttpsOrHttp -IPAddressOrRange '168.1.5.60' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add
```

<span data-ttu-id="476eb-127">' Vault1 ' kasasındaki ' hesabı1 ' Anahtar Kasası yönetilen depolama hesabı olan bir geçici blob SAS tanımı ' sas1 ' ayarlar.</span><span class="sxs-lookup"><span data-stu-id="476eb-127">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="476eb-128">Örnek 3: Hashtable kullanarak SAS tanımını ayarlama</span><span class="sxs-lookup"><span data-stu-id="476eb-128">Example 3 : Set a sas definition using a hashtable</span></span>
```
PS C:\> $parameters = @{"sasType"="blob";"signedVersion"="2016-05-31";"signedProtocols"="https";"signedIp"="168.1.5.60-168.1.5.70";"validityPeriod"="P30D";"signedPermissions"="ra";"blobName"="blob1";"containerName"="container1";"rscd"="";"rscc"=""}
PS C:\> Set-AzKeyVaultManagedStorageSasDefinition -VaultName vault1 -AccountName account1 -Name sas1 -Parameter $parameters
```

<span data-ttu-id="476eb-129">Karma anahtar kullanarak ' vault1 ' kasasındaki ' ' Anahtar Kasası yönetilen depolama hesabı ' sas1 ' ad hoc blob SAS tanımını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="476eb-129">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1' using a hashtable.</span></span>

## <span data-ttu-id="476eb-130">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="476eb-130">PARAMETERS</span></span>

### <span data-ttu-id="476eb-131">-AccountName</span><span class="sxs-lookup"><span data-stu-id="476eb-131">-AccountName</span></span>
<span data-ttu-id="476eb-132">Anahtar Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="476eb-132">Key Vault managed storage account name.</span></span> <span data-ttu-id="476eb-133">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve yönetim depolama hesap adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="476eb-133">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-134">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="476eb-134">-ApiVersion</span></span>
<span data-ttu-id="476eb-135">Hesap SAS URI 'SI kullanılarak yapılan isteği yürütmek için kullanılacak depolama hizmeti sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="476eb-135">Specifies the storage service version to use to execute the request made using the account SAS URI.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-136">-Blob</span><span class="sxs-lookup"><span data-stu-id="476eb-136">-Blob</span></span>
<span data-ttu-id="476eb-137">Blob adı</span><span class="sxs-lookup"><span data-stu-id="476eb-137">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceBlobSas, StoredPolicyServiceBlobSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-138">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="476eb-138">-Container</span></span>
<span data-ttu-id="476eb-139">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="476eb-139">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="476eb-140">-DefaultProfile</span></span>
<span data-ttu-id="476eb-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="476eb-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-142">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="476eb-142">-Disable</span></span>
<span data-ttu-id="476eb-143">SAS belirtecinin oluşturulması için SAS tanımı kullanımını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="476eb-143">Disables the use of sas definition for generation of sas token.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-144">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="476eb-144">-EndPartitionKey</span></span>
<span data-ttu-id="476eb-145">Bölüm anahtarını Sonlandır</span><span class="sxs-lookup"><span data-stu-id="476eb-145">End Partition Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-146">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="476eb-146">-EndRowKey</span></span>
<span data-ttu-id="476eb-147">Satır anahtarını bitir</span><span class="sxs-lookup"><span data-stu-id="476eb-147">End Row Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-148">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="476eb-148">-IPAddressOrRange</span></span>
<span data-ttu-id="476eb-149">Azure depolama tarafından kabul edilecek isteğin IP veya IP aralığı ACL 'SI (erişim denetim listesi).</span><span class="sxs-lookup"><span data-stu-id="476eb-149">IP, or IP range ACL (access control list) of the request that would be accepted by Azure Storage.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-150">-Ad</span><span class="sxs-lookup"><span data-stu-id="476eb-150">-Name</span></span>
<span data-ttu-id="476eb-151">Depolama SAS tanım adı.</span><span class="sxs-lookup"><span data-stu-id="476eb-151">Storage sas definition name.</span></span> <span data-ttu-id="476eb-152">Cmdlet, kasa adından depolama SAS tanımının FQDN 'sini, şu anda seçili olan ortamı, depolama hesabı adını ve SAS tanım adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="476eb-152">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-153">-Parametre</span><span class="sxs-lookup"><span data-stu-id="476eb-153">-Parameter</span></span>
<span data-ttu-id="476eb-154">SAS belirtecini oluşturmak için kullanılacak SAS tanım parametreleri.</span><span class="sxs-lookup"><span data-stu-id="476eb-154">Sas definition parameters that will be used to create the sas token.</span></span>

```yaml
Type: Hashtable
Parameter Sets: RawSas
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-155">-Yol</span><span class="sxs-lookup"><span data-stu-id="476eb-155">-Path</span></span>
<span data-ttu-id="476eb-156">SAS belirteci oluşturmak için bulut dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="476eb-156">Path to the cloud file to generate sas token against.</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceFileSas, StoredPolicyServiceFileSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-157">-İzin</span><span class="sxs-lookup"><span data-stu-id="476eb-157">-Permission</span></span>
<span data-ttu-id="476eb-158">İzinlerinin.</span><span class="sxs-lookup"><span data-stu-id="476eb-158">Permission.</span></span> <span data-ttu-id="476eb-159">Değerler ' sorgu ', ' Ekle ', ' Güncelleştir ', ' Process ' değerleridir</span><span class="sxs-lookup"><span data-stu-id="476eb-159">Values include 'Query','Add','Update','Process'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases: 
Accepted values: Add, Create, Delete, List, Process, Read, Query, Update, Write

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-160">-İlke</span><span class="sxs-lookup"><span data-stu-id="476eb-160">-Policy</span></span>
<span data-ttu-id="476eb-161">İlke tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="476eb-161">Policy Identifier</span></span>

```yaml
Type: String
Parameter Sets: StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-162">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="476eb-162">-Protocol</span></span>
<span data-ttu-id="476eb-163">Protokolü istekte SAS belirteciyle kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="476eb-163">Protocol can be used in the request with the SAS token.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-164">-Sıra</span><span class="sxs-lookup"><span data-stu-id="476eb-164">-Queue</span></span>
<span data-ttu-id="476eb-165">Sıra adı</span><span class="sxs-lookup"><span data-stu-id="476eb-165">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceQueueSas, StoredPolicyServiceQueueSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-166">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="476eb-166">-ResourceType</span></span>
<span data-ttu-id="476eb-167">Bu SAS belirtecinin uygulandığı kaynak türleri.</span><span class="sxs-lookup"><span data-stu-id="476eb-167">Resource types that this SAS token applies to.</span></span> <span data-ttu-id="476eb-168">Değerler ' servis ', ' Container ', ' nesne ' içerir</span><span class="sxs-lookup"><span data-stu-id="476eb-168">Values include 'Service','Container','Object'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas
Aliases: 
Accepted values: Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-169">-Hizmet</span><span class="sxs-lookup"><span data-stu-id="476eb-169">-Service</span></span>
<span data-ttu-id="476eb-170">Bu SAS belirtecinin uygulandığı hizmet türleri.</span><span class="sxs-lookup"><span data-stu-id="476eb-170">Service types that this SAS token applies to.</span></span> <span data-ttu-id="476eb-171">Değerler ' blob ', ' dosya ', ' sıra ', ' tablo ' içerir</span><span class="sxs-lookup"><span data-stu-id="476eb-171">Values include 'Blob','File','Queue','Table'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas
Aliases: 
Accepted values: Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-172">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="476eb-172">-Share</span></span>
<span data-ttu-id="476eb-173">Paylaşım adı</span><span class="sxs-lookup"><span data-stu-id="476eb-173">Share Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-174">-SharedAccessHeader</span><span class="sxs-lookup"><span data-stu-id="476eb-174">-SharedAccessHeader</span></span>
<span data-ttu-id="476eb-175">Yanıt üstbilgilerini geçersiz kılan sorgu parametrelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="476eb-175">Specifies the query parameters to override response headers.</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases: 
Accepted values: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-176">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="476eb-176">-StartPartitionKey</span></span>
<span data-ttu-id="476eb-177">Başlangıç bölümü anahtarı</span><span class="sxs-lookup"><span data-stu-id="476eb-177">Start Partition Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-178">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="476eb-178">-StartRowKey</span></span>
<span data-ttu-id="476eb-179">Başlangıç satırı tuşu</span><span class="sxs-lookup"><span data-stu-id="476eb-179">Start Row Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-180">-Tablo</span><span class="sxs-lookup"><span data-stu-id="476eb-180">-Table</span></span>
<span data-ttu-id="476eb-181">Tablo adı</span><span class="sxs-lookup"><span data-stu-id="476eb-181">Table Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-182">Etiketli</span><span class="sxs-lookup"><span data-stu-id="476eb-182">-Tag</span></span>
<span data-ttu-id="476eb-183">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="476eb-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="476eb-184">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="476eb-184">For example:</span></span>

<span data-ttu-id="476eb-185">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="476eb-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-186">-TargetStorageVersion</span><span class="sxs-lookup"><span data-stu-id="476eb-186">-TargetStorageVersion</span></span>
<span data-ttu-id="476eb-187">SAS belirteciyle yapılan isteklerin kimlik doğrulaması için kullanılacak, imzaladığınız depolama hizmeti sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="476eb-187">Specifies the signed storage service version to use to authenticate requests made with the SAS token.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-188">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="476eb-188">-ValidityPeriod</span></span>
<span data-ttu-id="476eb-189">SAS belirtecinin geçerlilik süresini oluşturulduğu saatten ayarlamak için kullanılacak geçerlilik süresi</span><span class="sxs-lookup"><span data-stu-id="476eb-189">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: TimeSpan
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-190">-VaultName</span><span class="sxs-lookup"><span data-stu-id="476eb-190">-VaultName</span></span>
<span data-ttu-id="476eb-191">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="476eb-191">Vault name.</span></span>
<span data-ttu-id="476eb-192">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="476eb-192">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-193">-Onay</span><span class="sxs-lookup"><span data-stu-id="476eb-193">-Confirm</span></span>
<span data-ttu-id="476eb-194">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="476eb-194">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="476eb-195">-WhatIf</span></span>
<span data-ttu-id="476eb-196">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="476eb-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="476eb-197">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="476eb-197">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476eb-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="476eb-198">CommonParameters</span></span>
<span data-ttu-id="476eb-199">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="476eb-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="476eb-200">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="476eb-200">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="476eb-201">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="476eb-201">INPUTS</span></span>

### <span data-ttu-id="476eb-202">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="476eb-202">None</span></span>
<span data-ttu-id="476eb-203">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="476eb-203">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="476eb-204">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="476eb-204">OUTPUTS</span></span>

### <span data-ttu-id="476eb-205">Microsoft. Azure. Commands. Keykasa. model. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="476eb-205">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="476eb-206">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="476eb-206">NOTES</span></span>

## <span data-ttu-id="476eb-207">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="476eb-207">RELATED LINKS</span></span>

[<span data-ttu-id="476eb-208">Azureâ € ‹ RM. â € ‹ Keyâ € ‹ kasa</span><span class="sxs-lookup"><span data-stu-id="476eb-208">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/Az.keyvault/)
