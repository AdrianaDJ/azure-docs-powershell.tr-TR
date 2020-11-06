---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 41defe467244647f707bae16c653dfcbe99eaec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589585"
---
# <span data-ttu-id="4fb93-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4fb93-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="4fb93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fb93-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb93-103">Bir öğretici Hizmetler hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4fb93-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fb93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4fb93-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fb93-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4fb93-105">DESCRIPTION</span></span>
<span data-ttu-id="4fb93-106">**New-Azurermöğretici ınitialveservicesaccount** cmdlet 'i belirtilen tür ve SKU 'ya sahip bir öğretici Hizmetler hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4fb93-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="4fb93-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4fb93-107">EXAMPLES</span></span>

### <span data-ttu-id="4fb93-108">2</span><span class="sxs-lookup"><span data-stu-id="4fb93-108">1:</span></span>
```
PS C:\> New-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
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

## <span data-ttu-id="4fb93-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4fb93-109">PARAMETERS</span></span>

### <span data-ttu-id="4fb93-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb93-110">-DefaultProfile</span></span>
<span data-ttu-id="4fb93-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4fb93-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fb93-112">-Force</span><span class="sxs-lookup"><span data-stu-id="4fb93-112">-Force</span></span>
<span data-ttu-id="4fb93-113">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4fb93-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4fb93-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="4fb93-114">-Location</span></span>
<span data-ttu-id="4fb93-115">Hesabın oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fb93-115">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="4fb93-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="4fb93-116">-Name</span></span>
<span data-ttu-id="4fb93-117">Hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fb93-117">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="4fb93-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fb93-118">-ResourceGroupName</span></span>
<span data-ttu-id="4fb93-119">Hesabın atanacağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fb93-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="4fb93-120">Kaynak grubu zaten var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4fb93-120">The resource group must already exist.</span></span>

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

### <span data-ttu-id="4fb93-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4fb93-121">-SkuName</span></span>
<span data-ttu-id="4fb93-122">Hesabın STB 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fb93-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="4fb93-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4fb93-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4fb93-124">F0 (serbest katman)</span><span class="sxs-lookup"><span data-stu-id="4fb93-124">F0 (free tier)</span></span>
- <span data-ttu-id="4fb93-125">S0</span><span class="sxs-lookup"><span data-stu-id="4fb93-125">S0</span></span>
- <span data-ttu-id="4fb93-126">S1</span><span class="sxs-lookup"><span data-stu-id="4fb93-126">S1</span></span>
- <span data-ttu-id="4fb93-127">S2</span><span class="sxs-lookup"><span data-stu-id="4fb93-127">S2</span></span>
- <span data-ttu-id="4fb93-128">S3</span><span class="sxs-lookup"><span data-stu-id="4fb93-128">S3</span></span>
- <span data-ttu-id="4fb93-129">S4 daha fazla bilgi [için bkz.](https://www.microsoft.com/cognitive-services/en-us/apis)</span><span class="sxs-lookup"><span data-stu-id="4fb93-129">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="4fb93-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4fb93-130">-Tag</span></span>
<span data-ttu-id="4fb93-131">Ad/değer çifti olarak bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fb93-131">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="4fb93-132">-Tür</span><span class="sxs-lookup"><span data-stu-id="4fb93-132">-Type</span></span>
<span data-ttu-id="4fb93-133">Oluşturulacak hesap türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fb93-133">Specifies the type of account to create.</span></span> <span data-ttu-id="4fb93-134">`Get-AzureRmCognitiveServicesAccountType`Geçerli kabul edilebilir değerleri almak için cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="4fb93-134">Use `Get-AzureRmCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="4fb93-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="4fb93-135">-Confirm</span></span>
<span data-ttu-id="4fb93-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4fb93-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fb93-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fb93-137">-WhatIf</span></span>
<span data-ttu-id="4fb93-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4fb93-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fb93-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4fb93-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fb93-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb93-140">CommonParameters</span></span>
<span data-ttu-id="4fb93-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4fb93-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb93-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fb93-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb93-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4fb93-143">INPUTS</span></span>

### <span data-ttu-id="4fb93-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4fb93-144">System.String</span></span>

## <span data-ttu-id="4fb93-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4fb93-145">OUTPUTS</span></span>

### <span data-ttu-id="4fb93-146">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="4fb93-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="4fb93-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4fb93-147">NOTES</span></span>

## <span data-ttu-id="4fb93-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4fb93-148">RELATED LINKS</span></span>

[<span data-ttu-id="4fb93-149">Get-Azurermöğretici Itiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="4fb93-149">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="4fb93-150">Remove-Azurermöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="4fb93-150">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="4fb93-151">Set-Azurermöğretici Itiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="4fb93-151">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
