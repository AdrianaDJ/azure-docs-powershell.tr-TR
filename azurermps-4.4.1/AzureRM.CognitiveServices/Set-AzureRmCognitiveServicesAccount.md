---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 51338a2cae2aa8bde09ecdea18f0aa74f3727fef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594811"
---
# <span data-ttu-id="50439-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="50439-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="50439-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50439-102">SYNOPSIS</span></span>
<span data-ttu-id="50439-103">Bir hesabı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="50439-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50439-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50439-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50439-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="50439-105">DESCRIPTION</span></span>
<span data-ttu-id="50439-106">**Set-Azurermöğretici Iveservicesaccount** cmdlet 'i, belirtilen öğretici sitif HIZMETLER hesabının SKU veya etiketlerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="50439-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="50439-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50439-107">EXAMPLES</span></span>

## <span data-ttu-id="50439-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50439-108">PARAMETERS</span></span>

### <span data-ttu-id="50439-109">-Force</span><span class="sxs-lookup"><span data-stu-id="50439-109">-Force</span></span>
<span data-ttu-id="50439-110">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="50439-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="50439-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="50439-111">-Name</span></span>
<span data-ttu-id="50439-112">Değiştirilecek hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50439-112">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="50439-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50439-113">-ResourceGroupName</span></span>
<span data-ttu-id="50439-114">Hesabın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50439-114">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="50439-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="50439-115">-SkuName</span></span>
<span data-ttu-id="50439-116">Hesabın STB 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="50439-116">Specifies the SKU for the account.</span></span>
<span data-ttu-id="50439-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="50439-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="50439-118">F0 (serbest katman)</span><span class="sxs-lookup"><span data-stu-id="50439-118">F0 (free tier)</span></span>
- <span data-ttu-id="50439-119">S0</span><span class="sxs-lookup"><span data-stu-id="50439-119">S0</span></span>
- <span data-ttu-id="50439-120">S1</span><span class="sxs-lookup"><span data-stu-id="50439-120">S1</span></span>
- <span data-ttu-id="50439-121">S2</span><span class="sxs-lookup"><span data-stu-id="50439-121">S2</span></span>
- <span data-ttu-id="50439-122">S3</span><span class="sxs-lookup"><span data-stu-id="50439-122">S3</span></span>
- <span data-ttu-id="50439-123">Modundan</span><span class="sxs-lookup"><span data-stu-id="50439-123">S4</span></span>

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

### <span data-ttu-id="50439-124">Etiketli</span><span class="sxs-lookup"><span data-stu-id="50439-124">-Tag</span></span>
<span data-ttu-id="50439-125">Ad/değer çifti olarak bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="50439-125">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="50439-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="50439-126">-Confirm</span></span>
<span data-ttu-id="50439-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="50439-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50439-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50439-128">-WhatIf</span></span>
<span data-ttu-id="50439-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="50439-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50439-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="50439-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50439-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50439-131">-DefaultProfile</span></span>
<span data-ttu-id="50439-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="50439-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50439-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50439-133">CommonParameters</span></span>
<span data-ttu-id="50439-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50439-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50439-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50439-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50439-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50439-136">INPUTS</span></span>

## <span data-ttu-id="50439-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50439-137">OUTPUTS</span></span>

### <span data-ttu-id="50439-138">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="50439-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="50439-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50439-139">NOTES</span></span>

## <span data-ttu-id="50439-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50439-140">RELATED LINKS</span></span>

[<span data-ttu-id="50439-141">Get-Azurermöğretici Itiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="50439-141">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="50439-142">Yeni-Azurermöğretici</span><span class="sxs-lookup"><span data-stu-id="50439-142">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="50439-143">Remove-Azurermöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="50439-143">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
