---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 1c1d4ad776ed3db2cb3b5adfb490902a7de12f42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762168"
---
# <span data-ttu-id="3c19d-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3c19d-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="3c19d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c19d-102">SYNOPSIS</span></span>
<span data-ttu-id="3c19d-103">Bir öğretici Hizmetler hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3c19d-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c19d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c19d-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c19d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c19d-105">DESCRIPTION</span></span>
<span data-ttu-id="3c19d-106">**New-Azurermöğretici ınitialveservicesaccount** cmdlet 'i belirtilen tür ve SKU 'ya sahip bir öğretici Hizmetler hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3c19d-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="3c19d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c19d-107">EXAMPLES</span></span>

### <span data-ttu-id="3c19d-108">2</span><span class="sxs-lookup"><span data-stu-id="3c19d-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="3c19d-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c19d-109">PARAMETERS</span></span>

### <span data-ttu-id="3c19d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c19d-110">-DefaultProfile</span></span>
<span data-ttu-id="3c19d-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3c19d-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c19d-112">-Force</span><span class="sxs-lookup"><span data-stu-id="3c19d-112">-Force</span></span>
<span data-ttu-id="3c19d-113">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3c19d-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3c19d-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="3c19d-114">-Location</span></span>
<span data-ttu-id="3c19d-115">Hesabın oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c19d-115">Specifies the location in which to create the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c19d-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="3c19d-116">-Name</span></span>
<span data-ttu-id="3c19d-117">Hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c19d-117">Specifies the name for the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c19d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c19d-118">-ResourceGroupName</span></span>
<span data-ttu-id="3c19d-119">Hesabın atanacağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c19d-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="3c19d-120">Kaynak grubu zaten var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3c19d-120">The resource group must already exist.</span></span>

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

### <span data-ttu-id="3c19d-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3c19d-121">-SkuName</span></span>
<span data-ttu-id="3c19d-122">Hesabın STB 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c19d-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="3c19d-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3c19d-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3c19d-124">F0 (serbest katman)</span><span class="sxs-lookup"><span data-stu-id="3c19d-124">F0 (free tier)</span></span>
- <span data-ttu-id="3c19d-125">S0</span><span class="sxs-lookup"><span data-stu-id="3c19d-125">S0</span></span>
- <span data-ttu-id="3c19d-126">S1</span><span class="sxs-lookup"><span data-stu-id="3c19d-126">S1</span></span>
- <span data-ttu-id="3c19d-127">S2</span><span class="sxs-lookup"><span data-stu-id="3c19d-127">S2</span></span>
- <span data-ttu-id="3c19d-128">S3</span><span class="sxs-lookup"><span data-stu-id="3c19d-128">S3</span></span>
- <span data-ttu-id="3c19d-129">Modundan</span><span class="sxs-lookup"><span data-stu-id="3c19d-129">S4</span></span>

<span data-ttu-id="3c19d-130">Daha fazla bilgi için bkz [.](https://www.microsoft.com/cognitive-services/en-us/apis)</span><span class="sxs-lookup"><span data-stu-id="3c19d-130">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c19d-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3c19d-131">-Tag</span></span>
<span data-ttu-id="3c19d-132">Ad/değer çifti olarak bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c19d-132">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c19d-133">-Tür</span><span class="sxs-lookup"><span data-stu-id="3c19d-133">-Type</span></span>
<span data-ttu-id="3c19d-134">Oluşturulacak hesap türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c19d-134">Specifies the type of account to create.</span></span> <span data-ttu-id="3c19d-135">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3c19d-135">Current acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3c19d-136">Bing. Autoöner. v7</span><span class="sxs-lookup"><span data-stu-id="3c19d-136">Bing.Autosuggest.v7</span></span>
- <span data-ttu-id="3c19d-137">Bing. CustomSearch</span><span class="sxs-lookup"><span data-stu-id="3c19d-137">Bing.CustomSearch</span></span>
- <span data-ttu-id="3c19d-138">Bing. Search. v7</span><span class="sxs-lookup"><span data-stu-id="3c19d-138">Bing.Search.v7</span></span>
- <span data-ttu-id="3c19d-139">Bing. Speech</span><span class="sxs-lookup"><span data-stu-id="3c19d-139">Bing.Speech</span></span>
- <span data-ttu-id="3c19d-140">Bing. yazım denetimi. v7</span><span class="sxs-lookup"><span data-stu-id="3c19d-140">Bing.SpellCheck.v7</span></span>
- <span data-ttu-id="3c19d-141">ComputerVision</span><span class="sxs-lookup"><span data-stu-id="3c19d-141">ComputerVision</span></span>
- <span data-ttu-id="3c19d-142">Içerik Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="3c19d-142">ContentModerator</span></span>
- <span data-ttu-id="3c19d-143">CustomSpeech</span><span class="sxs-lookup"><span data-stu-id="3c19d-143">CustomSpeech</span></span>
- <span data-ttu-id="3c19d-144">CustomVision. öngörü</span><span class="sxs-lookup"><span data-stu-id="3c19d-144">CustomVision.Prediction</span></span>
- <span data-ttu-id="3c19d-145">CustomVision. eğitim</span><span class="sxs-lookup"><span data-stu-id="3c19d-145">CustomVision.Training</span></span>
- <span data-ttu-id="3c19d-146">Emotion</span><span class="sxs-lookup"><span data-stu-id="3c19d-146">Emotion</span></span>
- <span data-ttu-id="3c19d-147">Dil</span><span class="sxs-lookup"><span data-stu-id="3c19d-147">Face</span></span>
- <span data-ttu-id="3c19d-148">LUIS</span><span class="sxs-lookup"><span data-stu-id="3c19d-148">LUIS</span></span>
- <span data-ttu-id="3c19d-149">QnAMaker</span><span class="sxs-lookup"><span data-stu-id="3c19d-149">QnAMaker</span></span>
- <span data-ttu-id="3c19d-150">Hoparlör</span><span class="sxs-lookup"><span data-stu-id="3c19d-150">SpeakerRecognition</span></span>
- <span data-ttu-id="3c19d-151">SpeechTranslation</span><span class="sxs-lookup"><span data-stu-id="3c19d-151">SpeechTranslation</span></span>
- <span data-ttu-id="3c19d-152">TextAnalytics</span><span class="sxs-lookup"><span data-stu-id="3c19d-152">TextAnalytics</span></span>
- <span data-ttu-id="3c19d-153">Metin çevirisi</span><span class="sxs-lookup"><span data-stu-id="3c19d-153">TextTranslation</span></span>
- <span data-ttu-id="3c19d-154">Web lm</span><span class="sxs-lookup"><span data-stu-id="3c19d-154">WebLM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c19d-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="3c19d-155">-Confirm</span></span>
<span data-ttu-id="3c19d-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3c19d-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c19d-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c19d-157">-WhatIf</span></span>
<span data-ttu-id="3c19d-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c19d-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c19d-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3c19d-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c19d-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c19d-160">CommonParameters</span></span>
<span data-ttu-id="3c19d-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c19d-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c19d-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c19d-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c19d-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c19d-163">INPUTS</span></span>

### <span data-ttu-id="3c19d-164">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3c19d-164">None</span></span>
<span data-ttu-id="3c19d-165">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="3c19d-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3c19d-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c19d-166">OUTPUTS</span></span>

### <span data-ttu-id="3c19d-167">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="3c19d-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="3c19d-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c19d-168">NOTES</span></span>

## <span data-ttu-id="3c19d-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c19d-169">RELATED LINKS</span></span>

[<span data-ttu-id="3c19d-170">Get-Azurermöğretici Itiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="3c19d-170">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="3c19d-171">Remove-Azurermöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="3c19d-171">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="3c19d-172">Set-Azurermöğretici Itiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="3c19d-172">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
