---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: b6c703b1c3373e4e0f1347d9bb2a9819ac1e5de6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590802"
---
# <span data-ttu-id="a957f-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a957f-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="a957f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a957f-102">SYNOPSIS</span></span>
<span data-ttu-id="a957f-103">Akış Analizi işini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a957f-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a957f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a957f-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a957f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a957f-105">DESCRIPTION</span></span>
<span data-ttu-id="a957f-106">**Remove-AzureRmStreamAnalyticsJob** cmdlet 'i Azure 'da belirli bir Stream Analytics işini eşzamansız olarak siler.</span><span class="sxs-lookup"><span data-stu-id="a957f-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="a957f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a957f-107">EXAMPLES</span></span>

### <span data-ttu-id="a957f-108">Örnek 1: işi kaldırma</span><span class="sxs-lookup"><span data-stu-id="a957f-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="a957f-109">Bu komut, StreamingJob öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a957f-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="a957f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a957f-110">PARAMETERS</span></span>

### <span data-ttu-id="a957f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a957f-111">-DefaultProfile</span></span>
<span data-ttu-id="a957f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a957f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a957f-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="a957f-113">-Name</span></span>
<span data-ttu-id="a957f-114">Kaldırılacak Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a957f-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="a957f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a957f-115">-ResourceGroupName</span></span>
<span data-ttu-id="a957f-116">Azure Stream Analytics işinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a957f-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="a957f-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="a957f-117">-Confirm</span></span>
<span data-ttu-id="a957f-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a957f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a957f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a957f-119">-WhatIf</span></span>
<span data-ttu-id="a957f-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a957f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a957f-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a957f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a957f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a957f-122">CommonParameters</span></span>
<span data-ttu-id="a957f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a957f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a957f-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a957f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a957f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a957f-125">INPUTS</span></span>

### <span data-ttu-id="a957f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a957f-126">System.String</span></span>

## <span data-ttu-id="a957f-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a957f-127">OUTPUTS</span></span>

### <span data-ttu-id="a957f-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a957f-128">System.Boolean</span></span>

## <span data-ttu-id="a957f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a957f-129">NOTES</span></span>

## <span data-ttu-id="a957f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a957f-130">RELATED LINKS</span></span>

[<span data-ttu-id="a957f-131">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a957f-131">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="a957f-132">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a957f-132">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="a957f-133">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a957f-133">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="a957f-134">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a957f-134">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


