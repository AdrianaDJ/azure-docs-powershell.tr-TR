---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
ms.openlocfilehash: 5ca65c09746f6bb9a050c14fe10987702465b484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590595"
---
# <span data-ttu-id="c9e73-101">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c9e73-101">Set-AzureRmStorageAccount</span></span>

## <span data-ttu-id="c9e73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9e73-102">SYNOPSIS</span></span>
<span data-ttu-id="c9e73-103">Depolama hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-103">Modifies a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9e73-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9e73-104">SYNTAX</span></span>

### <span data-ttu-id="c9e73-105">StorageEncryption (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c9e73-105">StorageEncryption (Default)</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9e73-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="c9e73-106">KeyvaultEncryption</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9e73-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9e73-107">DESCRIPTION</span></span>
<span data-ttu-id="c9e73-108">**Set-AzureRmStorageAccount** cmdlet 'ı Azure Depolama hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-108">The **Set-AzureRmStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="c9e73-109">Bu cmdlet 'i hesap türünü değiştirmek, müşteri etki alanını güncelleştirmek veya depolama hesabında etiketleri ayarlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c9e73-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="c9e73-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9e73-110">EXAMPLES</span></span>

### <span data-ttu-id="c9e73-111">Örnek 1: depolama hesabı türünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="c9e73-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="c9e73-112">Bu komut depolama hesabı türünü Standard_RAGRS olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c9e73-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="c9e73-113">Örnek 2: depolama hesabı için özel etki alanı ayarlama</span><span class="sxs-lookup"><span data-stu-id="c9e73-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="c9e73-114">Bu komut, bir depolama hesabı için özel bir etki alanı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c9e73-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="c9e73-115">Örnek 3: blob ve dosya hizmetlerinde şifrelemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="c9e73-115">Example 3: Enable encryption on Blob and File Services</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob,File"
```

<span data-ttu-id="c9e73-116">Bu komut, depolama hesabı için blob ve dosyada depolama hizmeti şifrelemesini etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-116">This command enables Storage Service encryption on Blob and File for a Storage account.</span></span>

### <span data-ttu-id="c9e73-117">Örnek 4: erişim katmanı değerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="c9e73-117">Example 4: Set the access tier value</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AccessTier Cool
```

<span data-ttu-id="c9e73-118">Komut, erişim katmanı değerini Cool olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c9e73-118">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="c9e73-119">Örnek 4: özel etki alanı ve etiketleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="c9e73-119">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="c9e73-120">Komut, erişim katmanı değerini Cool olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c9e73-120">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="c9e73-121">Örnek 5: Anahtar Kasası ile blob hizmetlerinde şifrelemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="c9e73-121">Example 5: Enable encryption on Blob Services with Keyvault</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="c9e73-122">Bu komut, blob 'taki yeni oluşturulmuş bir Keykasası ile depolama hizmeti şifrelemesini etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-122">This command enables Storage Service encryption on Blob with a new created Keyvault.</span></span>

### <span data-ttu-id="c9e73-123">Örnek 6: anahtar kaynağı "Microsoft. Storage" olarak ayarlanmış dosya hizmetlerinde şifrelemeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="c9e73-123">Example 6: Disable encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -DisableEncryptionService File  -StorageEncryption
```

<span data-ttu-id="c9e73-124">Bu komut, anahtar kaynağı "Microsoft. Storage" olarak ayarlanmış dosya hizmetlerindeki şifrelemeyi devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="c9e73-124">This command disables encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>

## <span data-ttu-id="c9e73-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9e73-125">PARAMETERS</span></span>

### <span data-ttu-id="c9e73-126">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="c9e73-126">-AccessTier</span></span>
<span data-ttu-id="c9e73-127">Bu cmdlet 'in değiştirdiği depolama hesabının erişim katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-127">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="c9e73-128">Bu parametre için kabul edilebilir değerler: kolay ve serin.</span><span class="sxs-lookup"><span data-stu-id="c9e73-128">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="c9e73-129">Erişim katmanını değiştirirseniz, ek ücretler ortaya çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-129">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="c9e73-130">Daha fazla bilgi için, bkz https://go.microsoft.com/fwlink/?LinkId=786482 https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="c9e73-130">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="c9e73-131">Depolama hesabı türü depolama ise, bu parametreyi belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="c9e73-131">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-132">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="c9e73-132">-AssignIdentity</span></span>
<span data-ttu-id="c9e73-133">Azure Keykasa gibi temel yönetim hizmetleriyle kullanmak üzere bu depolama hesabı için yeni bir depolama hesabı kimliği oluşturup atayın.</span><span class="sxs-lookup"><span data-stu-id="c9e73-133">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c9e73-134">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="c9e73-134">-CustomDomainName</span></span>
<span data-ttu-id="c9e73-135">Özel etki alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-135">Specifies the name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-136">-DisableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="c9e73-136">-DisableEncryptionService</span></span>
<span data-ttu-id="c9e73-137">Bu cmdlet 'in depolama hizmeti için depolama hizmeti şifrelemesini devre dışı bırakıp bırakmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-137">Indicates whether this cmdlet disables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="c9e73-138">Azure Blob ve Azure dosya hizmetleri destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="c9e73-138">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-139">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="c9e73-139">-EnableEncryptionService</span></span>
<span data-ttu-id="c9e73-140">Bu cmdlet 'in depolama hizmeti için depolama hizmeti şifrelemesini etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-140">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="c9e73-141">Azure Blob ve Azure dosya hizmetleri destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="c9e73-141">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-142">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="c9e73-142">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="c9e73-143">Depolama hesabının https trafiğinin yalnızca etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-143">Indicates whether or not the Storage Account only enable https traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-144">-Force</span><span class="sxs-lookup"><span data-stu-id="c9e73-144">-Force</span></span>
<span data-ttu-id="c9e73-145">Erişim katmanını değiştirirseniz, ek ücretler ortaya çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-145">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="c9e73-146">Daha fazla bilgi için, bkz https://go.microsoft.com/fwlink/?LinkId=786482 https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="c9e73-146">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="c9e73-147">Depolama hesabı türü depolama ise, bu parametreyi belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="c9e73-147">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

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

### <span data-ttu-id="c9e73-148">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="c9e73-148">-InformationAction</span></span>
<span data-ttu-id="c9e73-149">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c9e73-150">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c9e73-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9e73-151">'A</span><span class="sxs-lookup"><span data-stu-id="c9e73-151">Continue</span></span>
- <span data-ttu-id="c9e73-152">Manıza</span><span class="sxs-lookup"><span data-stu-id="c9e73-152">Ignore</span></span>
- <span data-ttu-id="c9e73-153">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="c9e73-153">Inquire</span></span>
- <span data-ttu-id="c9e73-154">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="c9e73-154">SilentlyContinue</span></span>
- <span data-ttu-id="c9e73-155">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="c9e73-155">Stop</span></span>
- <span data-ttu-id="c9e73-156">Biliriz</span><span class="sxs-lookup"><span data-stu-id="c9e73-156">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-157">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="c9e73-157">-InformationVariable</span></span>
<span data-ttu-id="c9e73-158">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-158">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-159">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="c9e73-159">-KeyName</span></span>
<span data-ttu-id="c9e73-160">Depolama hesabı şifrelemesi tuş kaynağı tuş Kasası anahtar</span><span class="sxs-lookup"><span data-stu-id="c9e73-160">Storage Account encryption keySource KeyVault KeyName</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-161">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="c9e73-161">-KeyvaultEncryption</span></span>
<span data-ttu-id="c9e73-162">Depolama hesabı şifreleme KeySource 'un Microsoft. Keykasa olarak ayarlanması veya olmaması.</span><span class="sxs-lookup"><span data-stu-id="c9e73-162">Whether to set Storage Account Encryption KeySource to Microsoft.Keyvault or not.</span></span> <span data-ttu-id="c9e73-163">KeyName, KeyVersion ve KeyvaultUri belirtirseniz, depolama hesabı şifrelemesi tuş kaynağı da Microsoft 'a ayarlanır. tuş Kasası Hava durumu bu parametre ayarlandı veya yok.</span><span class="sxs-lookup"><span data-stu-id="c9e73-163">If you specify KeyName, KeyVersion and KeyvaultUri, Storage Account encryption keySource will also be set to Microsoft.Keyvault weather this parameter is set or not.</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-164">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="c9e73-164">-KeyVaultUri</span></span>
<span data-ttu-id="c9e73-165">Depolama hesabı şifrelemesi tuş kaynağı tuş Kasası tuş</span><span class="sxs-lookup"><span data-stu-id="c9e73-165">Storage Account encryption keySource KeyVault KeyVaultUri</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-166">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="c9e73-166">-KeyVersion</span></span>
<span data-ttu-id="c9e73-167">Depolama hesabı şifrelemesi tuş kaynağı tuş Kasası tuş sürümü</span><span class="sxs-lookup"><span data-stu-id="c9e73-167">Storage Account encryption keySource KeyVault KeyVersion</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-168">-Ad</span><span class="sxs-lookup"><span data-stu-id="c9e73-168">-Name</span></span>
<span data-ttu-id="c9e73-169">Değiştirilecek depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-169">Specifies the name of the Storage account to Modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-170">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c9e73-170">-NetworkRuleSet</span></span>
<span data-ttu-id="c9e73-171">Depolama hesabı ağ kuralı kümesi</span><span class="sxs-lookup"><span data-stu-id="c9e73-171">Storage Account NetworkRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9e73-172">-ResourceGroupName</span></span>
<span data-ttu-id="c9e73-173">Depolama hesabının değiştirileceği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-173">Specifies the name of the resource group in which to modify the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-174">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c9e73-174">-SkuName</span></span>
<span data-ttu-id="c9e73-175">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-175">Specifies the SKU name of the storage account.</span></span>
<span data-ttu-id="c9e73-176">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c9e73-176">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9e73-177">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="c9e73-177">Standard_LRS.</span></span>
<span data-ttu-id="c9e73-178">Yerel olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="c9e73-178">Locally-redundant storage.</span></span> 
- <span data-ttu-id="c9e73-179">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="c9e73-179">Standard_ZRS.</span></span>
<span data-ttu-id="c9e73-180">Bölge ile yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="c9e73-180">Zone-redundant storage.</span></span>
- <span data-ttu-id="c9e73-181">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="c9e73-181">Standard_GRS.</span></span>
<span data-ttu-id="c9e73-182">Coğrafi olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="c9e73-182">Geo-redundant storage.</span></span> 
- <span data-ttu-id="c9e73-183">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="c9e73-183">Standard_RAGRS.</span></span>
<span data-ttu-id="c9e73-184">Okuma erişimi coğrafi depolama.</span><span class="sxs-lookup"><span data-stu-id="c9e73-184">Read access geo-redundant storage.</span></span> 
- <span data-ttu-id="c9e73-185">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="c9e73-185">Premium_LRS.</span></span>
<span data-ttu-id="c9e73-186">Premium yerel olarak yedekli depolama.</span><span class="sxs-lookup"><span data-stu-id="c9e73-186">Premium locally-redundant storage.</span></span>

<span data-ttu-id="c9e73-187">Standard_ZRS ve Premium_LRS türlerini diğer hesap türleriyle değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="c9e73-187">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="c9e73-188">Diğer hesap türlerini Standard_ZRS veya Premium_LRS olarak değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="c9e73-188">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-189">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="c9e73-189">-StorageEncryption</span></span>
<span data-ttu-id="c9e73-190">Depolama hesabı şifrelemesi anahtar kaynağının Microsoft. Storage olarak ayarlanması gerekip gerekmediği.</span><span class="sxs-lookup"><span data-stu-id="c9e73-190">Whether to set Storage Account Encryption KeySource to Microsoft.Storage or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StorageEncryption
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-191">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c9e73-191">-Tag</span></span>
<span data-ttu-id="c9e73-192">New-AzureRmStorageAccount cmdlet 'inin *tür* parametresinde blobstorage değeri belirtirseniz, *accesstier* parametresi için bir değer belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-192">If you specify a value of BlobStorage for the *Kind* parameter of the New-AzureRmStorageAccount cmdlet, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="c9e73-193">Bu *tür* parametre Için bir depolama alanı değeri belirtirseniz, *accesstier* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="c9e73-193">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-194">-Usealt etki alanı</span><span class="sxs-lookup"><span data-stu-id="c9e73-194">-UseSubDomain</span></span>
<span data-ttu-id="c9e73-195">Dolaylı CName doğrulamasının etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-195">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-196">-Onay</span><span class="sxs-lookup"><span data-stu-id="c9e73-196">-Confirm</span></span>
<span data-ttu-id="c9e73-197">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c9e73-197">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9e73-198">-WhatIf</span></span>
<span data-ttu-id="c9e73-199">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9e73-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9e73-200">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c9e73-200">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e73-201">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9e73-201">-DefaultProfile</span></span>
<span data-ttu-id="c9e73-202">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c9e73-202">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9e73-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9e73-203">CommonParameters</span></span>
<span data-ttu-id="c9e73-204">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9e73-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9e73-205">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9e73-205">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9e73-206">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9e73-206">INPUTS</span></span>

## <span data-ttu-id="c9e73-207">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9e73-207">OUTPUTS</span></span>

## <span data-ttu-id="c9e73-208">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9e73-208">NOTES</span></span>

## <span data-ttu-id="c9e73-209">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9e73-209">RELATED LINKS</span></span>

[<span data-ttu-id="c9e73-210">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c9e73-210">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="c9e73-211">Yeni-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c9e73-211">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="c9e73-212">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c9e73-212">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)


