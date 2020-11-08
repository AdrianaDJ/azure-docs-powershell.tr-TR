---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 713c5cb34133a233bace576ea80035b8e004eb7f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095791"
---
# <span data-ttu-id="2d31f-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2d31f-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="2d31f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d31f-102">SYNOPSIS</span></span>
<span data-ttu-id="2d31f-103">Bir öğretici Hizmetler hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2d31f-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="2d31f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d31f-104">SYNTAX</span></span>

### <span data-ttu-id="2d31f-105">Öğretici</span><span class="sxs-lookup"><span data-stu-id="2d31f-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d31f-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="2d31f-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d31f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d31f-107">DESCRIPTION</span></span>
<span data-ttu-id="2d31f-108">**New-Azsitiveservicesaccount** cmdlet 'i belirtilen tür ve SKU 'ya sahip bir öğretici Hizmetler hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2d31f-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="2d31f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d31f-109">EXAMPLES</span></span>

### <span data-ttu-id="2d31f-110">2</span><span class="sxs-lookup"><span data-stu-id="2d31f-110">1:</span></span>
```
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
n 'WestUS'


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WestUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="2d31f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d31f-111">PARAMETERS</span></span>

### <span data-ttu-id="2d31f-112">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="2d31f-112">-AssignIdentity</span></span>
<span data-ttu-id="2d31f-113">Azure Keykasa gibi temel yönetim hizmetleri ile kullanmak için bu depolama hesabı için yeni bir öğretici hizmetler hesap kimliği oluşturup atayın.</span><span class="sxs-lookup"><span data-stu-id="2d31f-113">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="2d31f-114">-Öğretici Bveservicesencryption</span><span class="sxs-lookup"><span data-stu-id="2d31f-114">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="2d31f-115">Öğretici hizmetler hesap şifrelemesi KeySource 'ı Microsoft. öğretici.</span><span class="sxs-lookup"><span data-stu-id="2d31f-115">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="2d31f-116">-Customsubetkialanıadı</span><span class="sxs-lookup"><span data-stu-id="2d31f-116">-CustomSubdomainName</span></span>
<span data-ttu-id="2d31f-117">Öğretici hizmetler hesap alt etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="2d31f-117">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="2d31f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d31f-118">-DefaultProfile</span></span>
<span data-ttu-id="2d31f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2d31f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d31f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2d31f-120">-Force</span></span>
<span data-ttu-id="2d31f-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="2d31f-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2d31f-122">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="2d31f-122">-KeyName</span></span>
<span data-ttu-id="2d31f-123">Öğretici hizmetler hesap şifrelemesi keySource tuş Kasası anahtar</span><span class="sxs-lookup"><span data-stu-id="2d31f-123">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="2d31f-124">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="2d31f-124">-KeyVaultEncryption</span></span>
<span data-ttu-id="2d31f-125">Öğretici hizmetler hesap şifrelemesi keySource 'ı Microsoft. Keykasa 'ya ayarlamak.</span><span class="sxs-lookup"><span data-stu-id="2d31f-125">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="2d31f-126">KeyName, KeyVersion ve KeyVaultUri belirtirseniz, öğretici hizmet hesabı şifrelemesi tuş kaynağı da Microsoft 'a ayarlanır. tuş Kasası Hava durumu bu parametre ayarlandı veya yok.</span><span class="sxs-lookup"><span data-stu-id="2d31f-126">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="2d31f-127">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="2d31f-127">-KeyVaultUri</span></span>
<span data-ttu-id="2d31f-128">Öğretici hizmetler hesap şifrelemesi tuş kaynağı tuş Kasası tuş tipi</span><span class="sxs-lookup"><span data-stu-id="2d31f-128">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="2d31f-129">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="2d31f-129">-KeyVersion</span></span>
<span data-ttu-id="2d31f-130">Öğretici hizmetler hesap şifrelemesi keySource tuş Kasası tuş sürümü</span><span class="sxs-lookup"><span data-stu-id="2d31f-130">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="2d31f-131">-Konum</span><span class="sxs-lookup"><span data-stu-id="2d31f-131">-Location</span></span>
<span data-ttu-id="2d31f-132">Hesabın oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d31f-132">Specifies the location in which to create the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d31f-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="2d31f-133">-Name</span></span>
<span data-ttu-id="2d31f-134">Hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d31f-134">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="2d31f-135">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d31f-135">-NetworkRuleSet</span></span>
<span data-ttu-id="2d31f-136">NetworkRuleSet, güvenlik duvarları ve sanal ağlar için yapılandırma kuralları kümesi tanımlamak ve ayrıca tanımlı kuralların hiçbiriyle eşleşmeyen isteklerin nasıl işleneceği gibi ağ özelliklerini belirlemek için kullanılır</span><span class="sxs-lookup"><span data-stu-id="2d31f-136">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="2d31f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d31f-137">-ResourceGroupName</span></span>
<span data-ttu-id="2d31f-138">Hesabın atanacağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d31f-138">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="2d31f-139">Kaynak grubu zaten var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2d31f-139">The resource group must already exist.</span></span>

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

### <span data-ttu-id="2d31f-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2d31f-140">-SkuName</span></span>
<span data-ttu-id="2d31f-141">Hesabın STB 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d31f-141">Specifies the SKU for the account.</span></span>
<span data-ttu-id="2d31f-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2d31f-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2d31f-143">F0 (serbest katman)</span><span class="sxs-lookup"><span data-stu-id="2d31f-143">F0 (free tier)</span></span>
- <span data-ttu-id="2d31f-144">S0</span><span class="sxs-lookup"><span data-stu-id="2d31f-144">S0</span></span>
- <span data-ttu-id="2d31f-145">S1</span><span class="sxs-lookup"><span data-stu-id="2d31f-145">S1</span></span>
- <span data-ttu-id="2d31f-146">S2</span><span class="sxs-lookup"><span data-stu-id="2d31f-146">S2</span></span>
- <span data-ttu-id="2d31f-147">S3</span><span class="sxs-lookup"><span data-stu-id="2d31f-147">S3</span></span>
- <span data-ttu-id="2d31f-148">S4 daha fazla bilgi [için bkz.](https://www.microsoft.com/cognitive-services/en-us/apis)</span><span class="sxs-lookup"><span data-stu-id="2d31f-148">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d31f-149">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="2d31f-149">-StorageAccountId</span></span>
<span data-ttu-id="2d31f-150">Kullanıcının sahip olduğu depolama hesaplarının listesi.</span><span class="sxs-lookup"><span data-stu-id="2d31f-150">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="2d31f-151">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2d31f-151">-Tag</span></span>
<span data-ttu-id="2d31f-152">Ad/değer çifti olarak bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d31f-152">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d31f-153">-Tür</span><span class="sxs-lookup"><span data-stu-id="2d31f-153">-Type</span></span>
<span data-ttu-id="2d31f-154">Oluşturulacak hesap türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d31f-154">Specifies the type of account to create.</span></span> <span data-ttu-id="2d31f-155">`Get-AzCognitiveServicesAccountType`Geçerli kabul edilebilir değerleri almak için cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="2d31f-155">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d31f-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="2d31f-156">-Confirm</span></span>
<span data-ttu-id="2d31f-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2d31f-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d31f-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d31f-158">-WhatIf</span></span>
<span data-ttu-id="2d31f-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2d31f-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d31f-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2d31f-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d31f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d31f-161">CommonParameters</span></span>
<span data-ttu-id="2d31f-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d31f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d31f-163">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2d31f-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d31f-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d31f-164">INPUTS</span></span>

### <span data-ttu-id="2d31f-165">System. String</span><span class="sxs-lookup"><span data-stu-id="2d31f-165">System.String</span></span>

## <span data-ttu-id="2d31f-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d31f-166">OUTPUTS</span></span>

### <span data-ttu-id="2d31f-167">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="2d31f-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="2d31f-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d31f-168">NOTES</span></span>

## <span data-ttu-id="2d31f-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d31f-169">RELATED LINKS</span></span>

[<span data-ttu-id="2d31f-170">Get-Azsitiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="2d31f-170">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="2d31f-171">Remove-Azsiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="2d31f-171">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="2d31f-172">Set-Azsiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="2d31f-172">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
