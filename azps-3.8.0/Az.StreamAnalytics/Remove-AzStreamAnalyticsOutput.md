---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 23f7c8270f3d5c0073be9705e43086aae3a3e903
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937493"
---
# <span data-ttu-id="7e4a2-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="7e4a2-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="7e4a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e4a2-102">SYNOPSIS</span></span>
<span data-ttu-id="7e4a2-103">Bir Stream Analytics işinden çıktı siler.</span><span class="sxs-lookup"><span data-stu-id="7e4a2-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="7e4a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e4a2-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e4a2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e4a2-105">DESCRIPTION</span></span>
<span data-ttu-id="7e4a2-106">**Remove-AzStreamAnalyticsOutput** cmdlet 'i Azure 'Daki bir Stream Analytics işinin çıktısını zaman uyumsuz olarak siler.</span><span class="sxs-lookup"><span data-stu-id="7e4a2-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="7e4a2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e4a2-107">EXAMPLES</span></span>

### <span data-ttu-id="7e4a2-108">Örnek 1: bir işten çıktı kaldırma</span><span class="sxs-lookup"><span data-stu-id="7e4a2-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="7e4a2-109">Bu komut, iş StreamingJob 'daki çıkış çıkışını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7e4a2-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="7e4a2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e4a2-110">PARAMETERS</span></span>

### <span data-ttu-id="7e4a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e4a2-111">-DefaultProfile</span></span>
<span data-ttu-id="7e4a2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e4a2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e4a2-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="7e4a2-113">-JobName</span></span>
<span data-ttu-id="7e4a2-114">Azure Stream Analytics çıkışının ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e4a2-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="7e4a2-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="7e4a2-115">-Name</span></span>
<span data-ttu-id="7e4a2-116">Kaldırılacak Azure Stream Analytics çıktısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e4a2-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="7e4a2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e4a2-117">-ResourceGroupName</span></span>
<span data-ttu-id="7e4a2-118">Azure Stream Analytics çıktısının ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e4a2-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="7e4a2-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="7e4a2-119">-Confirm</span></span>
<span data-ttu-id="7e4a2-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7e4a2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e4a2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e4a2-121">-WhatIf</span></span>
<span data-ttu-id="7e4a2-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e4a2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e4a2-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7e4a2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e4a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e4a2-124">CommonParameters</span></span>
<span data-ttu-id="7e4a2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e4a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e4a2-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e4a2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e4a2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e4a2-127">INPUTS</span></span>

### <span data-ttu-id="7e4a2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7e4a2-128">System.String</span></span>

## <span data-ttu-id="7e4a2-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e4a2-129">OUTPUTS</span></span>

### <span data-ttu-id="7e4a2-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e4a2-130">System.Boolean</span></span>

## <span data-ttu-id="7e4a2-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e4a2-131">NOTES</span></span>

## <span data-ttu-id="7e4a2-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e4a2-132">RELATED LINKS</span></span>

[<span data-ttu-id="7e4a2-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="7e4a2-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="7e4a2-134">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="7e4a2-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="7e4a2-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="7e4a2-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)

