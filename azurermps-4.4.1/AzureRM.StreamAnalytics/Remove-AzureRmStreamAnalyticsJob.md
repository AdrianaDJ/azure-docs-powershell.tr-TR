---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 9ba839bbfc6740d9d62c9a036d233a8b5a1ce0e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593770"
---
# <span data-ttu-id="84954-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="84954-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="84954-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84954-102">SYNOPSIS</span></span>
<span data-ttu-id="84954-103">Akış Analizi işini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="84954-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84954-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84954-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84954-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="84954-105">DESCRIPTION</span></span>
<span data-ttu-id="84954-106">**Remove-AzureRmStreamAnalyticsJob** cmdlet 'i Azure 'da belirli bir Stream Analytics işini eşzamansız olarak siler.</span><span class="sxs-lookup"><span data-stu-id="84954-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="84954-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84954-107">EXAMPLES</span></span>

### <span data-ttu-id="84954-108">Örnek 1: işi kaldırma</span><span class="sxs-lookup"><span data-stu-id="84954-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="84954-109">Bu komut, StreamingJob öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="84954-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="84954-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84954-110">PARAMETERS</span></span>

### <span data-ttu-id="84954-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="84954-111">-Name</span></span>
<span data-ttu-id="84954-112">Kaldırılacak Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84954-112">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="84954-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84954-113">-ResourceGroupName</span></span>
<span data-ttu-id="84954-114">Azure Stream Analytics işinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84954-114">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="84954-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="84954-115">-Confirm</span></span>
<span data-ttu-id="84954-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="84954-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84954-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84954-117">-WhatIf</span></span>
<span data-ttu-id="84954-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="84954-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84954-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="84954-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84954-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84954-120">-DefaultProfile</span></span>
<span data-ttu-id="84954-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="84954-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84954-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84954-122">CommonParameters</span></span>
<span data-ttu-id="84954-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84954-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84954-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84954-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84954-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84954-125">INPUTS</span></span>

## <span data-ttu-id="84954-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84954-126">OUTPUTS</span></span>

### <span data-ttu-id="84954-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="84954-127">System.Object</span></span>

## <span data-ttu-id="84954-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84954-128">NOTES</span></span>

## <span data-ttu-id="84954-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84954-129">RELATED LINKS</span></span>

[<span data-ttu-id="84954-130">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="84954-130">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="84954-131">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="84954-131">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="84954-132">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="84954-132">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="84954-133">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="84954-133">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


