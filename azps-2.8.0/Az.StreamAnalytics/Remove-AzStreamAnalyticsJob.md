---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 2b15c1a3b4b69b1a1db3eb25dd953cf62644c8a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933504"
---
# <span data-ttu-id="be706-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="be706-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="be706-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be706-102">SYNOPSIS</span></span>
<span data-ttu-id="be706-103">Akış Analizi işini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="be706-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="be706-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be706-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be706-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="be706-105">DESCRIPTION</span></span>
<span data-ttu-id="be706-106">**Remove-AzStreamAnalyticsJob** cmdlet 'i Azure 'da belirli bir Stream Analytics işini eşzamansız olarak siler.</span><span class="sxs-lookup"><span data-stu-id="be706-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="be706-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be706-107">EXAMPLES</span></span>

### <span data-ttu-id="be706-108">Örnek 1: işi kaldırma</span><span class="sxs-lookup"><span data-stu-id="be706-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="be706-109">Bu komut, StreamingJob öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="be706-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="be706-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be706-110">PARAMETERS</span></span>

### <span data-ttu-id="be706-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be706-111">-DefaultProfile</span></span>
<span data-ttu-id="be706-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be706-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be706-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="be706-113">-Name</span></span>
<span data-ttu-id="be706-114">Kaldırılacak Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be706-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="be706-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be706-115">-ResourceGroupName</span></span>
<span data-ttu-id="be706-116">Azure Stream Analytics işinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be706-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="be706-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="be706-117">-Confirm</span></span>
<span data-ttu-id="be706-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="be706-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be706-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be706-119">-WhatIf</span></span>
<span data-ttu-id="be706-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="be706-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be706-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="be706-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be706-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be706-122">CommonParameters</span></span>
<span data-ttu-id="be706-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be706-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be706-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be706-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be706-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be706-125">INPUTS</span></span>

### <span data-ttu-id="be706-126">System. String</span><span class="sxs-lookup"><span data-stu-id="be706-126">System.String</span></span>

## <span data-ttu-id="be706-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be706-127">OUTPUTS</span></span>

### <span data-ttu-id="be706-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="be706-128">System.Boolean</span></span>

## <span data-ttu-id="be706-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be706-129">NOTES</span></span>

## <span data-ttu-id="be706-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be706-130">RELATED LINKS</span></span>

[<span data-ttu-id="be706-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="be706-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="be706-132">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="be706-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="be706-133">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="be706-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="be706-134">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="be706-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


