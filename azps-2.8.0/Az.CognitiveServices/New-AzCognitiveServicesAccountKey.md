---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: ac8bc0e8fd65a82f05108351a5b3140da8c1fb3c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753016"
---
# <span data-ttu-id="c99e2-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="c99e2-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="c99e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c99e2-102">SYNOPSIS</span></span>
<span data-ttu-id="c99e2-103">Hesap anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c99e2-103">Regenerates an account key.</span></span>

## <span data-ttu-id="c99e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c99e2-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c99e2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c99e2-105">DESCRIPTION</span></span>
<span data-ttu-id="c99e2-106">**New-Azöğretici ınitialveservicesaccountkey** cmdlet 'ı, öğretici bir hizmetler hesabı IÇIN bir API anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c99e2-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="c99e2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c99e2-107">EXAMPLES</span></span>

### <span data-ttu-id="c99e2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c99e2-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="c99e2-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c99e2-109">PARAMETERS</span></span>

### <span data-ttu-id="c99e2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c99e2-110">-DefaultProfile</span></span>
<span data-ttu-id="c99e2-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c99e2-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c99e2-112">-Force</span><span class="sxs-lookup"><span data-stu-id="c99e2-112">-Force</span></span>
<span data-ttu-id="c99e2-113">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c99e2-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c99e2-114">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="c99e2-114">-KeyName</span></span>
<span data-ttu-id="c99e2-115">Yeniden üretmek için anahtarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c99e2-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="c99e2-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c99e2-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c99e2-117">Anahtar</span><span class="sxs-lookup"><span data-stu-id="c99e2-117">Key1</span></span>
- <span data-ttu-id="c99e2-118">Anahtar2</span><span class="sxs-lookup"><span data-stu-id="c99e2-118">Key2</span></span>

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

### <span data-ttu-id="c99e2-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="c99e2-119">-Name</span></span>
<span data-ttu-id="c99e2-120">Hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c99e2-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="c99e2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c99e2-121">-ResourceGroupName</span></span>
<span data-ttu-id="c99e2-122">Hesabın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c99e2-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="c99e2-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="c99e2-123">-Confirm</span></span>
<span data-ttu-id="c99e2-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c99e2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c99e2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c99e2-125">-WhatIf</span></span>
<span data-ttu-id="c99e2-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c99e2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c99e2-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c99e2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c99e2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c99e2-128">CommonParameters</span></span>
<span data-ttu-id="c99e2-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c99e2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c99e2-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c99e2-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c99e2-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c99e2-131">INPUTS</span></span>

### <span data-ttu-id="c99e2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c99e2-132">System.String</span></span>

### <span data-ttu-id="c99e2-133">Microsoft. Azure. Management. öğretici Bveservices. modeller. AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="c99e2-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="c99e2-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c99e2-134">OUTPUTS</span></span>

### <span data-ttu-id="c99e2-135">Microsoft. Azure. Management. öğretici Bveservices. modeller.</span><span class="sxs-lookup"><span data-stu-id="c99e2-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="c99e2-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c99e2-136">NOTES</span></span>

## <span data-ttu-id="c99e2-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c99e2-137">RELATED LINKS</span></span>

[<span data-ttu-id="c99e2-138">Get-az</span><span class="sxs-lookup"><span data-stu-id="c99e2-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


