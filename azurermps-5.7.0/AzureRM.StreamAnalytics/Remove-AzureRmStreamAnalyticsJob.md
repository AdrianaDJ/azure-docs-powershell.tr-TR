---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 64ebe431333914a907c515744501f4624a7977ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588688"
---
# <span data-ttu-id="3f1c5-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3f1c5-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="3f1c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f1c5-102">SYNOPSIS</span></span>
<span data-ttu-id="3f1c5-103">Akış Analizi işini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3f1c5-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f1c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f1c5-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f1c5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f1c5-105">DESCRIPTION</span></span>
<span data-ttu-id="3f1c5-106">**Remove-AzureRmStreamAnalyticsJob** cmdlet 'i Azure 'da belirli bir Stream Analytics işini eşzamansız olarak siler.</span><span class="sxs-lookup"><span data-stu-id="3f1c5-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="3f1c5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f1c5-107">EXAMPLES</span></span>

### <span data-ttu-id="3f1c5-108">Örnek 1: işi kaldırma</span><span class="sxs-lookup"><span data-stu-id="3f1c5-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="3f1c5-109">Bu komut, StreamingJob öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3f1c5-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="3f1c5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f1c5-110">PARAMETERS</span></span>

### <span data-ttu-id="3f1c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f1c5-111">-DefaultProfile</span></span>
<span data-ttu-id="3f1c5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3f1c5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f1c5-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="3f1c5-113">-Name</span></span>
<span data-ttu-id="3f1c5-114">Kaldırılacak Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f1c5-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f1c5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f1c5-115">-ResourceGroupName</span></span>
<span data-ttu-id="3f1c5-116">Azure Stream Analytics işinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f1c5-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="3f1c5-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="3f1c5-117">-Confirm</span></span>
<span data-ttu-id="3f1c5-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3f1c5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f1c5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f1c5-119">-WhatIf</span></span>
<span data-ttu-id="3f1c5-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f1c5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f1c5-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3f1c5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f1c5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f1c5-122">CommonParameters</span></span>
<span data-ttu-id="3f1c5-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f1c5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f1c5-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f1c5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f1c5-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f1c5-125">INPUTS</span></span>

### <span data-ttu-id="3f1c5-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3f1c5-126">None</span></span>
<span data-ttu-id="3f1c5-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="3f1c5-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3f1c5-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f1c5-128">OUTPUTS</span></span>

### <span data-ttu-id="3f1c5-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="3f1c5-129">System.Object</span></span>

## <span data-ttu-id="3f1c5-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f1c5-130">NOTES</span></span>

## <span data-ttu-id="3f1c5-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f1c5-131">RELATED LINKS</span></span>

[<span data-ttu-id="3f1c5-132">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3f1c5-132">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="3f1c5-133">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3f1c5-133">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="3f1c5-134">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3f1c5-134">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="3f1c5-135">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3f1c5-135">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


