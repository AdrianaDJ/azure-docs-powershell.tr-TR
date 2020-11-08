---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: fc510ebede11168dd8d8b090cd2069ce3e6de52c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095778"
---
# <span data-ttu-id="fd47a-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fd47a-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="fd47a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd47a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd47a-103">Bir hesabı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="fd47a-103">Modifies an account.</span></span>

## <span data-ttu-id="fd47a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd47a-104">SYNTAX</span></span>

### <span data-ttu-id="fd47a-105">Öğretici (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fd47a-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd47a-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="fd47a-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd47a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd47a-107">DESCRIPTION</span></span>
<span data-ttu-id="fd47a-108">**Set-Azsitiveservicesaccount** cmdlet 'i, belirtilen öğretici Sien HIZMETLER hesabının SKU veya etiketlerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="fd47a-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="fd47a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd47a-109">EXAMPLES</span></span>

### <span data-ttu-id="fd47a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fd47a-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="fd47a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd47a-111">PARAMETERS</span></span>

### <span data-ttu-id="fd47a-112">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="fd47a-112">-AssignIdentity</span></span>
<span data-ttu-id="fd47a-113">Azure Keykasa gibi temel yönetim hizmetleri ile kullanmak için bu depolama hesabı için yeni bir öğretici hizmetler hesap kimliği oluşturup atayın.</span><span class="sxs-lookup"><span data-stu-id="fd47a-113">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="fd47a-114">-Öğretici Bveservicesencryption</span><span class="sxs-lookup"><span data-stu-id="fd47a-114">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="fd47a-115">Öğretici hizmetler hesap şifrelemesi KeySource 'ı Microsoft. öğretici.</span><span class="sxs-lookup"><span data-stu-id="fd47a-115">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CognitiveServicesEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd47a-116">-Customsubetkialanıadı</span><span class="sxs-lookup"><span data-stu-id="fd47a-116">-CustomSubdomainName</span></span>
<span data-ttu-id="fd47a-117">Öğretici hizmetler hesap alt etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="fd47a-117">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="fd47a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd47a-118">-DefaultProfile</span></span>
<span data-ttu-id="fd47a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fd47a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd47a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fd47a-120">-Force</span></span>
<span data-ttu-id="fd47a-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="fd47a-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fd47a-122">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="fd47a-122">-IdentityType</span></span>
<span data-ttu-id="fd47a-123">Yönetilen hizmet kimliği türü.</span><span class="sxs-lookup"><span data-stu-id="fd47a-123">Type of managed service identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.CognitiveServices.Models.IdentityType]
Parameter Sets: (All)
Aliases:
Accepted values: None, SystemAssigned, UserAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd47a-124">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="fd47a-124">-KeyName</span></span>
<span data-ttu-id="fd47a-125">Öğretici hizmetler hesap şifrelemesi keySource tuş Kasası anahtar</span><span class="sxs-lookup"><span data-stu-id="fd47a-125">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd47a-126">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="fd47a-126">-KeyVaultEncryption</span></span>
<span data-ttu-id="fd47a-127">Öğretici hizmetler hesap şifrelemesi keySource 'ı Microsoft. Keykasa 'ya ayarlamak.</span><span class="sxs-lookup"><span data-stu-id="fd47a-127">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="fd47a-128">KeyName, KeyVersion ve KeyVaultUri belirtirseniz, öğretici hizmet hesabı şifrelemesi tuş kaynağı da Microsoft 'a ayarlanır. tuş Kasası Hava durumu bu parametre ayarlandı veya yok.</span><span class="sxs-lookup"><span data-stu-id="fd47a-128">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyVaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd47a-129">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="fd47a-129">-KeyVaultUri</span></span>
<span data-ttu-id="fd47a-130">Öğretici hizmetler hesap şifrelemesi tuş kaynağı tuş Kasası tuş tipi</span><span class="sxs-lookup"><span data-stu-id="fd47a-130">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd47a-131">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="fd47a-131">-KeyVersion</span></span>
<span data-ttu-id="fd47a-132">Öğretici hizmetler hesap şifrelemesi keySource tuş Kasası tuş sürümü</span><span class="sxs-lookup"><span data-stu-id="fd47a-132">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd47a-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="fd47a-133">-Name</span></span>
<span data-ttu-id="fd47a-134">Değiştirilecek hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd47a-134">Specifies the name of the account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd47a-135">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="fd47a-135">-NetworkRuleSet</span></span>
<span data-ttu-id="fd47a-136">NetworkRuleSet, güvenlik duvarları ve sanal ağlar için yapılandırma kuralları kümesi tanımlamak ve ayrıca tanımlı kuralların hiçbiriyle eşleşmeyen isteklerin nasıl işleneceği gibi ağ özelliklerini belirlemek için kullanılır</span><span class="sxs-lookup"><span data-stu-id="fd47a-136">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd47a-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd47a-137">-ResourceGroupName</span></span>
<span data-ttu-id="fd47a-138">Hesabın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd47a-138">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="fd47a-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fd47a-139">-SkuName</span></span>
<span data-ttu-id="fd47a-140">Hesabın STB 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd47a-140">Specifies the SKU for the account.</span></span>
<span data-ttu-id="fd47a-141">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fd47a-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fd47a-142">F0 (serbest katman)</span><span class="sxs-lookup"><span data-stu-id="fd47a-142">F0 (free tier)</span></span>
- <span data-ttu-id="fd47a-143">S0</span><span class="sxs-lookup"><span data-stu-id="fd47a-143">S0</span></span>
- <span data-ttu-id="fd47a-144">S1</span><span class="sxs-lookup"><span data-stu-id="fd47a-144">S1</span></span>
- <span data-ttu-id="fd47a-145">S2</span><span class="sxs-lookup"><span data-stu-id="fd47a-145">S2</span></span>
- <span data-ttu-id="fd47a-146">S3</span><span class="sxs-lookup"><span data-stu-id="fd47a-146">S3</span></span>
- <span data-ttu-id="fd47a-147">Modundan</span><span class="sxs-lookup"><span data-stu-id="fd47a-147">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd47a-148">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="fd47a-148">-StorageAccountId</span></span>
<span data-ttu-id="fd47a-149">Kullanıcının sahip olduğu depolama hesaplarının listesi.</span><span class="sxs-lookup"><span data-stu-id="fd47a-149">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="fd47a-150">Etiketli</span><span class="sxs-lookup"><span data-stu-id="fd47a-150">-Tag</span></span>
<span data-ttu-id="fd47a-151">Ad/değer çifti olarak bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd47a-151">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd47a-152">-Onay</span><span class="sxs-lookup"><span data-stu-id="fd47a-152">-Confirm</span></span>
<span data-ttu-id="fd47a-153">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fd47a-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd47a-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd47a-154">-WhatIf</span></span>
<span data-ttu-id="fd47a-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd47a-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd47a-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fd47a-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd47a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd47a-157">CommonParameters</span></span>
<span data-ttu-id="fd47a-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd47a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd47a-159">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fd47a-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd47a-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd47a-160">INPUTS</span></span>

### <span data-ttu-id="fd47a-161">System. String</span><span class="sxs-lookup"><span data-stu-id="fd47a-161">System.String</span></span>

### <span data-ttu-id="fd47a-162">System. topluluklar. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="fd47a-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="fd47a-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd47a-163">OUTPUTS</span></span>

### <span data-ttu-id="fd47a-164">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="fd47a-164">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="fd47a-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd47a-165">NOTES</span></span>

## <span data-ttu-id="fd47a-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd47a-166">RELATED LINKS</span></span>

[<span data-ttu-id="fd47a-167">Get-Azsitiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="fd47a-167">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="fd47a-168">Yeni-Azsitiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="fd47a-168">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="fd47a-169">Remove-Azsiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="fd47a-169">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
