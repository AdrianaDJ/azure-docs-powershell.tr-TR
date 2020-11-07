---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 7e5253951ec3c74850584aaac9818a6a7c8f2737
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761389"
---
# <span data-ttu-id="3a9ac-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3a9ac-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="3a9ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a9ac-102">SYNOPSIS</span></span>
<span data-ttu-id="3a9ac-103">Bir öğretici Hizmetler hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3a9ac-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="3a9ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a9ac-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a9ac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a9ac-105">DESCRIPTION</span></span>
<span data-ttu-id="3a9ac-106">**New-Azsitiveservicesaccount** cmdlet 'i belirtilen tür ve SKU 'ya sahip bir öğretici Hizmetler hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3a9ac-106">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="3a9ac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a9ac-107">EXAMPLES</span></span>

### <span data-ttu-id="3a9ac-108">2</span><span class="sxs-lookup"><span data-stu-id="3a9ac-108">1:</span></span>
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

## <span data-ttu-id="3a9ac-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a9ac-109">PARAMETERS</span></span>

### <span data-ttu-id="3a9ac-110">-Customsubetkialanıadı</span><span class="sxs-lookup"><span data-stu-id="3a9ac-110">-CustomSubdomainName</span></span>
<span data-ttu-id="3a9ac-111">Öğretici hizmetler hesap alt etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="3a9ac-111">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="3a9ac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a9ac-112">-DefaultProfile</span></span>
<span data-ttu-id="3a9ac-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3a9ac-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a9ac-114">-Force</span><span class="sxs-lookup"><span data-stu-id="3a9ac-114">-Force</span></span>
<span data-ttu-id="3a9ac-115">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3a9ac-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a9ac-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="3a9ac-116">-Location</span></span>
<span data-ttu-id="3a9ac-117">Hesabın oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a9ac-117">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="3a9ac-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a9ac-118">-Name</span></span>
<span data-ttu-id="3a9ac-119">Hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a9ac-119">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="3a9ac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a9ac-120">-ResourceGroupName</span></span>
<span data-ttu-id="3a9ac-121">Hesabın atanacağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a9ac-121">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="3a9ac-122">Kaynak grubu zaten var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3a9ac-122">The resource group must already exist.</span></span>

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

### <span data-ttu-id="3a9ac-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3a9ac-123">-SkuName</span></span>
<span data-ttu-id="3a9ac-124">Hesabın STB 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a9ac-124">Specifies the SKU for the account.</span></span>
<span data-ttu-id="3a9ac-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3a9ac-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3a9ac-126">F0 (serbest katman)</span><span class="sxs-lookup"><span data-stu-id="3a9ac-126">F0 (free tier)</span></span>
- <span data-ttu-id="3a9ac-127">S0</span><span class="sxs-lookup"><span data-stu-id="3a9ac-127">S0</span></span>
- <span data-ttu-id="3a9ac-128">S1</span><span class="sxs-lookup"><span data-stu-id="3a9ac-128">S1</span></span>
- <span data-ttu-id="3a9ac-129">S2</span><span class="sxs-lookup"><span data-stu-id="3a9ac-129">S2</span></span>
- <span data-ttu-id="3a9ac-130">S3</span><span class="sxs-lookup"><span data-stu-id="3a9ac-130">S3</span></span>
- <span data-ttu-id="3a9ac-131">S4 daha fazla bilgi [için bkz.](https://www.microsoft.com/cognitive-services/en-us/apis)</span><span class="sxs-lookup"><span data-stu-id="3a9ac-131">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="3a9ac-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3a9ac-132">-Tag</span></span>
<span data-ttu-id="3a9ac-133">Ad/değer çifti olarak bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a9ac-133">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="3a9ac-134">-Tür</span><span class="sxs-lookup"><span data-stu-id="3a9ac-134">-Type</span></span>
<span data-ttu-id="3a9ac-135">Oluşturulacak hesap türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a9ac-135">Specifies the type of account to create.</span></span> <span data-ttu-id="3a9ac-136">`Get-AzCognitiveServicesAccountType`Geçerli kabul edilebilir değerleri almak için cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="3a9ac-136">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="3a9ac-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="3a9ac-137">-Confirm</span></span>
<span data-ttu-id="3a9ac-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a9ac-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a9ac-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a9ac-139">-WhatIf</span></span>
<span data-ttu-id="3a9ac-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a9ac-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a9ac-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3a9ac-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a9ac-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a9ac-142">CommonParameters</span></span>
<span data-ttu-id="3a9ac-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a9ac-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a9ac-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a9ac-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a9ac-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a9ac-145">INPUTS</span></span>

### <span data-ttu-id="3a9ac-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3a9ac-146">System.String</span></span>

## <span data-ttu-id="3a9ac-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a9ac-147">OUTPUTS</span></span>

### <span data-ttu-id="3a9ac-148">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="3a9ac-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="3a9ac-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a9ac-149">NOTES</span></span>

## <span data-ttu-id="3a9ac-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a9ac-150">RELATED LINKS</span></span>

[<span data-ttu-id="3a9ac-151">Get-Azsitiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="3a9ac-151">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="3a9ac-152">Remove-Azsiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="3a9ac-152">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="3a9ac-153">Set-Azsiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="3a9ac-153">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
