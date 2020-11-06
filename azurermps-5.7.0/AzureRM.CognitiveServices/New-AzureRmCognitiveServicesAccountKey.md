---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 1c3ebaf3e95c1094b02b73505e471d13015721d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587638"
---
# <span data-ttu-id="16cc0-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="16cc0-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="16cc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="16cc0-103">Hesap anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16cc0-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16cc0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16cc0-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16cc0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="16cc0-105">DESCRIPTION</span></span>
<span data-ttu-id="16cc0-106">**Yeni-Azurermöğretici ınitialveservicesaccountkey** cmdlet 'ı, öğretici bir hizmetler hesabı IÇIN bir API anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16cc0-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="16cc0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16cc0-107">EXAMPLES</span></span>

## <span data-ttu-id="16cc0-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16cc0-108">PARAMETERS</span></span>

### <span data-ttu-id="16cc0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16cc0-109">-DefaultProfile</span></span>
<span data-ttu-id="16cc0-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="16cc0-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16cc0-111">-Force</span><span class="sxs-lookup"><span data-stu-id="16cc0-111">-Force</span></span>
<span data-ttu-id="16cc0-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="16cc0-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="16cc0-113">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="16cc0-113">-KeyName</span></span>
<span data-ttu-id="16cc0-114">Yeniden üretmek için anahtarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16cc0-114">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="16cc0-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="16cc0-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="16cc0-116">Anahtar</span><span class="sxs-lookup"><span data-stu-id="16cc0-116">Key1</span></span>
- <span data-ttu-id="16cc0-117">Anahtar2</span><span class="sxs-lookup"><span data-stu-id="16cc0-117">Key2</span></span>

```yaml
Type: KeyName
Parameter Sets: (All)
Aliases: 
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16cc0-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="16cc0-118">-Name</span></span>
<span data-ttu-id="16cc0-119">Hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16cc0-119">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="16cc0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16cc0-120">-ResourceGroupName</span></span>
<span data-ttu-id="16cc0-121">Hesabın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16cc0-121">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="16cc0-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="16cc0-122">-Confirm</span></span>
<span data-ttu-id="16cc0-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="16cc0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16cc0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16cc0-124">-WhatIf</span></span>
<span data-ttu-id="16cc0-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="16cc0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16cc0-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="16cc0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16cc0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16cc0-127">CommonParameters</span></span>
<span data-ttu-id="16cc0-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16cc0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16cc0-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16cc0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16cc0-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16cc0-130">INPUTS</span></span>

### <span data-ttu-id="16cc0-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="16cc0-131">None</span></span>
<span data-ttu-id="16cc0-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="16cc0-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="16cc0-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16cc0-133">OUTPUTS</span></span>

### <span data-ttu-id="16cc0-134">Microsoft. Azure. Management. öğretici Bveservices. modeller.</span><span class="sxs-lookup"><span data-stu-id="16cc0-134">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="16cc0-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16cc0-135">NOTES</span></span>

## <span data-ttu-id="16cc0-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16cc0-136">RELATED LINKS</span></span>

[<span data-ttu-id="16cc0-137">Get-Azurermöğretici Iveservicesaccountkey</span><span class="sxs-lookup"><span data-stu-id="16cc0-137">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


