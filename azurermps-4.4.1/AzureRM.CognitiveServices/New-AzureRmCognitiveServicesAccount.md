---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 449b10f851dbd4e2f2e804bab0772543d512c0c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594818"
---
# <span data-ttu-id="25d06-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="25d06-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="25d06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25d06-102">SYNOPSIS</span></span>
<span data-ttu-id="25d06-103">Bir öğretici Hizmetler hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="25d06-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25d06-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25d06-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25d06-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="25d06-105">DESCRIPTION</span></span>
<span data-ttu-id="25d06-106">**New-Azurermöğretici ınitialveservicesaccount** cmdlet 'i belirtilen tür ve SKU 'ya sahip bir öğretici Hizmetler hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="25d06-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="25d06-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25d06-107">EXAMPLES</span></span>

### <span data-ttu-id="25d06-108">2</span><span class="sxs-lookup"><span data-stu-id="25d06-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="25d06-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25d06-109">PARAMETERS</span></span>

### <span data-ttu-id="25d06-110">-Force</span><span class="sxs-lookup"><span data-stu-id="25d06-110">-Force</span></span>
<span data-ttu-id="25d06-111">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="25d06-111">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="25d06-112">-Konum</span><span class="sxs-lookup"><span data-stu-id="25d06-112">-Location</span></span>
<span data-ttu-id="25d06-113">Hesabın oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="25d06-113">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="25d06-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="25d06-114">-Name</span></span>
<span data-ttu-id="25d06-115">Hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="25d06-115">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="25d06-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d06-116">-ResourceGroupName</span></span>
<span data-ttu-id="25d06-117">Hesabın atanacağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="25d06-117">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="25d06-118">Kaynak grubu zaten var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="25d06-118">The resource group must already exist.</span></span>

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

### <span data-ttu-id="25d06-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="25d06-119">-SkuName</span></span>
<span data-ttu-id="25d06-120">Hesabın STB 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="25d06-120">Specifies the SKU for the account.</span></span>
<span data-ttu-id="25d06-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="25d06-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="25d06-122">F0 (serbest katman)</span><span class="sxs-lookup"><span data-stu-id="25d06-122">F0 (free tier)</span></span>
- <span data-ttu-id="25d06-123">S0</span><span class="sxs-lookup"><span data-stu-id="25d06-123">S0</span></span>
- <span data-ttu-id="25d06-124">S1</span><span class="sxs-lookup"><span data-stu-id="25d06-124">S1</span></span>
- <span data-ttu-id="25d06-125">S2</span><span class="sxs-lookup"><span data-stu-id="25d06-125">S2</span></span>
- <span data-ttu-id="25d06-126">S3</span><span class="sxs-lookup"><span data-stu-id="25d06-126">S3</span></span>
- <span data-ttu-id="25d06-127">Modundan</span><span class="sxs-lookup"><span data-stu-id="25d06-127">S4</span></span>

<span data-ttu-id="25d06-128">Daha fazla bilgi için bkz [.](https://www.microsoft.com/cognitive-services/en-us/apis)</span><span class="sxs-lookup"><span data-stu-id="25d06-128">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="25d06-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="25d06-129">-Tag</span></span>
<span data-ttu-id="25d06-130">Ad/değer çifti olarak bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="25d06-130">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="25d06-131">-Tür</span><span class="sxs-lookup"><span data-stu-id="25d06-131">-Type</span></span>
<span data-ttu-id="25d06-132">Oluşturulacak hesap türünü belirtir. Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="25d06-132">Specifies the type of account to create.The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="25d06-133">ComputerVision</span><span class="sxs-lookup"><span data-stu-id="25d06-133">ComputerVision</span></span>
- <span data-ttu-id="25d06-134">Emotion</span><span class="sxs-lookup"><span data-stu-id="25d06-134">Emotion</span></span>
- <span data-ttu-id="25d06-135">Dil</span><span class="sxs-lookup"><span data-stu-id="25d06-135">Face</span></span>
- <span data-ttu-id="25d06-136">LUIS</span><span class="sxs-lookup"><span data-stu-id="25d06-136">LUIS</span></span>
- <span data-ttu-id="25d06-137">Önerilerinin</span><span class="sxs-lookup"><span data-stu-id="25d06-137">Recommendations</span></span>
- <span data-ttu-id="25d06-138">İşlevi</span><span class="sxs-lookup"><span data-stu-id="25d06-138">Speech</span></span>
- <span data-ttu-id="25d06-139">TextAnalytics</span><span class="sxs-lookup"><span data-stu-id="25d06-139">TextAnalytics</span></span>
- <span data-ttu-id="25d06-140">Web lm</span><span class="sxs-lookup"><span data-stu-id="25d06-140">WebLM</span></span>

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

### <span data-ttu-id="25d06-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="25d06-141">-Confirm</span></span>
<span data-ttu-id="25d06-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="25d06-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25d06-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25d06-143">-WhatIf</span></span>
<span data-ttu-id="25d06-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="25d06-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25d06-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="25d06-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25d06-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d06-146">-DefaultProfile</span></span>
<span data-ttu-id="25d06-147">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="25d06-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25d06-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d06-148">CommonParameters</span></span>
<span data-ttu-id="25d06-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25d06-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d06-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25d06-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d06-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25d06-151">INPUTS</span></span>

## <span data-ttu-id="25d06-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25d06-152">OUTPUTS</span></span>

### <span data-ttu-id="25d06-153">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="25d06-153">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="25d06-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25d06-154">NOTES</span></span>

## <span data-ttu-id="25d06-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25d06-155">RELATED LINKS</span></span>

[<span data-ttu-id="25d06-156">Get-Azurermöğretici Itiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="25d06-156">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="25d06-157">Remove-Azurermöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="25d06-157">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="25d06-158">Set-Azurermöğretici Itiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="25d06-158">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
