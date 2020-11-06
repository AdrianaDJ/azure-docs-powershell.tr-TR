---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 345e7c6365a66abde5f350f20f614d4d6c94b1b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594817"
---
# <span data-ttu-id="ae5ed-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="ae5ed-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="ae5ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae5ed-102">SYNOPSIS</span></span>
<span data-ttu-id="ae5ed-103">Hesap anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ae5ed-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae5ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae5ed-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae5ed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae5ed-105">DESCRIPTION</span></span>
<span data-ttu-id="ae5ed-106">**Yeni-Azurermöğretici ınitialveservicesaccountkey** cmdlet 'ı, öğretici bir hizmetler hesabı IÇIN bir API anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ae5ed-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="ae5ed-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae5ed-107">EXAMPLES</span></span>

## <span data-ttu-id="ae5ed-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae5ed-108">PARAMETERS</span></span>

### <span data-ttu-id="ae5ed-109">-Force</span><span class="sxs-lookup"><span data-stu-id="ae5ed-109">-Force</span></span>
<span data-ttu-id="ae5ed-110">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ae5ed-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ae5ed-111">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="ae5ed-111">-KeyName</span></span>
<span data-ttu-id="ae5ed-112">Yeniden üretmek için anahtarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae5ed-112">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="ae5ed-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ae5ed-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae5ed-114">Anahtar</span><span class="sxs-lookup"><span data-stu-id="ae5ed-114">Key1</span></span>
- <span data-ttu-id="ae5ed-115">Anahtar2</span><span class="sxs-lookup"><span data-stu-id="ae5ed-115">Key2</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.KeyName
Parameter Sets: (All)
Aliases: 
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5ed-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="ae5ed-116">-Name</span></span>
<span data-ttu-id="ae5ed-117">Hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae5ed-117">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="ae5ed-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae5ed-118">-ResourceGroupName</span></span>
<span data-ttu-id="ae5ed-119">Hesabın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae5ed-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="ae5ed-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="ae5ed-120">-Confirm</span></span>
<span data-ttu-id="ae5ed-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ae5ed-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae5ed-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae5ed-122">-WhatIf</span></span>
<span data-ttu-id="ae5ed-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ae5ed-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae5ed-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ae5ed-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae5ed-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae5ed-125">-DefaultProfile</span></span>
<span data-ttu-id="ae5ed-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ae5ed-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae5ed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae5ed-127">CommonParameters</span></span>
<span data-ttu-id="ae5ed-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae5ed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae5ed-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae5ed-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae5ed-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae5ed-130">INPUTS</span></span>

## <span data-ttu-id="ae5ed-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae5ed-131">OUTPUTS</span></span>

### <span data-ttu-id="ae5ed-132">Microsoft. Azure. Management. öğretici Bveservices. modeller.</span><span class="sxs-lookup"><span data-stu-id="ae5ed-132">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="ae5ed-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae5ed-133">NOTES</span></span>

## <span data-ttu-id="ae5ed-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae5ed-134">RELATED LINKS</span></span>

[<span data-ttu-id="ae5ed-135">Get-Azurermöğretici Iveservicesaccountkey</span><span class="sxs-lookup"><span data-stu-id="ae5ed-135">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


