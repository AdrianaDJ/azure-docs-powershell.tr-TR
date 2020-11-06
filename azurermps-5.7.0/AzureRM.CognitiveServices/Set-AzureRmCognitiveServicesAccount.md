---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: a31ee6979a73e4637e683a5b388f4265bf53d2a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594132"
---
# <span data-ttu-id="a480d-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a480d-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="a480d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a480d-102">SYNOPSIS</span></span>
<span data-ttu-id="a480d-103">Bir hesabı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a480d-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a480d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a480d-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a480d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a480d-105">DESCRIPTION</span></span>
<span data-ttu-id="a480d-106">**Set-Azurermöğretici Iveservicesaccount** cmdlet 'i, belirtilen öğretici sitif HIZMETLER hesabının SKU veya etiketlerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a480d-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="a480d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a480d-107">EXAMPLES</span></span>

## <span data-ttu-id="a480d-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a480d-108">PARAMETERS</span></span>

### <span data-ttu-id="a480d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a480d-109">-DefaultProfile</span></span>
<span data-ttu-id="a480d-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a480d-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a480d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a480d-111">-Force</span></span>
<span data-ttu-id="a480d-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="a480d-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a480d-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="a480d-113">-Name</span></span>
<span data-ttu-id="a480d-114">Değiştirilecek hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a480d-114">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="a480d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a480d-115">-ResourceGroupName</span></span>
<span data-ttu-id="a480d-116">Hesabın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a480d-116">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="a480d-117">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a480d-117">-SkuName</span></span>
<span data-ttu-id="a480d-118">Hesabın STB 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a480d-118">Specifies the SKU for the account.</span></span>
<span data-ttu-id="a480d-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a480d-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a480d-120">F0 (serbest katman)</span><span class="sxs-lookup"><span data-stu-id="a480d-120">F0 (free tier)</span></span>
- <span data-ttu-id="a480d-121">S0</span><span class="sxs-lookup"><span data-stu-id="a480d-121">S0</span></span>
- <span data-ttu-id="a480d-122">S1</span><span class="sxs-lookup"><span data-stu-id="a480d-122">S1</span></span>
- <span data-ttu-id="a480d-123">S2</span><span class="sxs-lookup"><span data-stu-id="a480d-123">S2</span></span>
- <span data-ttu-id="a480d-124">S3</span><span class="sxs-lookup"><span data-stu-id="a480d-124">S3</span></span>
- <span data-ttu-id="a480d-125">Modundan</span><span class="sxs-lookup"><span data-stu-id="a480d-125">S4</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a480d-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a480d-126">-Tag</span></span>
<span data-ttu-id="a480d-127">Ad/değer çifti olarak bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="a480d-127">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a480d-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="a480d-128">-Confirm</span></span>
<span data-ttu-id="a480d-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a480d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a480d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a480d-130">-WhatIf</span></span>
<span data-ttu-id="a480d-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a480d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a480d-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a480d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a480d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a480d-133">CommonParameters</span></span>
<span data-ttu-id="a480d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a480d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a480d-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a480d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a480d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a480d-136">INPUTS</span></span>

### <span data-ttu-id="a480d-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a480d-137">None</span></span>
<span data-ttu-id="a480d-138">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a480d-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a480d-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a480d-139">OUTPUTS</span></span>

### <span data-ttu-id="a480d-140">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="a480d-140">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="a480d-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a480d-141">NOTES</span></span>

## <span data-ttu-id="a480d-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a480d-142">RELATED LINKS</span></span>

[<span data-ttu-id="a480d-143">Get-Azurermöğretici Itiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="a480d-143">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="a480d-144">Yeni-Azurermöğretici</span><span class="sxs-lookup"><span data-stu-id="a480d-144">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="a480d-145">Remove-Azurermöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="a480d-145">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
