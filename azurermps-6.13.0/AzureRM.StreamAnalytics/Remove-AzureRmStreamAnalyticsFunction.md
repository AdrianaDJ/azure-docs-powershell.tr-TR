---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 4429142b19e64939b9fcc90d56c80f67c5296c15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762712"
---
# <span data-ttu-id="ed2c3-101">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="ed2c3-101">Remove-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="ed2c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed2c3-102">SYNOPSIS</span></span>
<span data-ttu-id="ed2c3-103">Stream Analytics işinden bir işlevi siler.</span><span class="sxs-lookup"><span data-stu-id="ed2c3-103">Deletes a function from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed2c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed2c3-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed2c3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed2c3-105">DESCRIPTION</span></span>
<span data-ttu-id="ed2c3-106">**Remove-AzureRmStreamAnalyticsFunction** cmdlet 'ı bir Azure Stream Analytics işinden zaman uyumsuz bir işlevi siler.</span><span class="sxs-lookup"><span data-stu-id="ed2c3-106">The **Remove-AzureRmStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="ed2c3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed2c3-107">EXAMPLES</span></span>

### <span data-ttu-id="ed2c3-108">Örnek 1: Stream Analytics işlevini kaldırma</span><span class="sxs-lookup"><span data-stu-id="ed2c3-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="ed2c3-109">Bu komut, StreamJob22 adındaki işten ScoreTweet adındaki işlevi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ed2c3-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="ed2c3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed2c3-110">PARAMETERS</span></span>

### <span data-ttu-id="ed2c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed2c3-111">-DefaultProfile</span></span>
<span data-ttu-id="ed2c3-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed2c3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed2c3-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="ed2c3-113">-JobName</span></span>
<span data-ttu-id="ed2c3-114">İşlevin ait olduğu akış analizi işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed2c3-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="ed2c3-115">Bu cmdlet, bu parametrenin belirttiği işten bir işlevi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ed2c3-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed2c3-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed2c3-116">-Name</span></span>
<span data-ttu-id="ed2c3-117">Bu cmdlet 'in kaldırdığı Stream Analytics işlevinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed2c3-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed2c3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed2c3-118">-ResourceGroupName</span></span>
<span data-ttu-id="ed2c3-119">Bir Stream Analytics işlevinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed2c3-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="ed2c3-120">Bu cmdlet, bu parametrenin belirttiği kaynak grubundaki bir işlevi siler.</span><span class="sxs-lookup"><span data-stu-id="ed2c3-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed2c3-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="ed2c3-121">-Confirm</span></span>
<span data-ttu-id="ed2c3-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ed2c3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed2c3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed2c3-123">-WhatIf</span></span>
<span data-ttu-id="ed2c3-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed2c3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed2c3-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ed2c3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed2c3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed2c3-126">CommonParameters</span></span>
<span data-ttu-id="ed2c3-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed2c3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed2c3-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed2c3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed2c3-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed2c3-129">INPUTS</span></span>

### <span data-ttu-id="ed2c3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ed2c3-130">System.String</span></span>

## <span data-ttu-id="ed2c3-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed2c3-131">OUTPUTS</span></span>

### <span data-ttu-id="ed2c3-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed2c3-132">System.Boolean</span></span>

## <span data-ttu-id="ed2c3-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed2c3-133">NOTES</span></span>

## <span data-ttu-id="ed2c3-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed2c3-134">RELATED LINKS</span></span>

[<span data-ttu-id="ed2c3-135">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="ed2c3-135">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="ed2c3-136">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="ed2c3-136">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="ed2c3-137">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="ed2c3-137">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


