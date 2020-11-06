---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 98074a9893525882ce63ab86e31c677281f34ca3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587120"
---
# <span data-ttu-id="2d7ad-101">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="2d7ad-101">Remove-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="2d7ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d7ad-102">SYNOPSIS</span></span>
<span data-ttu-id="2d7ad-103">Bir Stream Analytics işinden çıktı siler.</span><span class="sxs-lookup"><span data-stu-id="2d7ad-103">Deletes an output from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d7ad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d7ad-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d7ad-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d7ad-105">DESCRIPTION</span></span>
<span data-ttu-id="2d7ad-106">**Remove-AzureRmStreamAnalyticsOutput** cmdlet 'i Azure 'Daki bir Stream Analytics işinin çıktısını zaman uyumsuz olarak siler.</span><span class="sxs-lookup"><span data-stu-id="2d7ad-106">The **Remove-AzureRmStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="2d7ad-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d7ad-107">EXAMPLES</span></span>

### <span data-ttu-id="2d7ad-108">Örnek 1: bir işten çıktı kaldırma</span><span class="sxs-lookup"><span data-stu-id="2d7ad-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="2d7ad-109">Bu komut, iş StreamingJob 'daki çıkış çıkışını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2d7ad-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="2d7ad-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d7ad-110">PARAMETERS</span></span>

### <span data-ttu-id="2d7ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d7ad-111">-DefaultProfile</span></span>
<span data-ttu-id="2d7ad-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2d7ad-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d7ad-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="2d7ad-113">-JobName</span></span>
<span data-ttu-id="2d7ad-114">Azure Stream Analytics çıkışının ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d7ad-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="2d7ad-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="2d7ad-115">-Name</span></span>
<span data-ttu-id="2d7ad-116">Kaldırılacak Azure Stream Analytics çıktısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d7ad-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="2d7ad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d7ad-117">-ResourceGroupName</span></span>
<span data-ttu-id="2d7ad-118">Azure Stream Analytics çıktısının ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d7ad-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="2d7ad-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="2d7ad-119">-Confirm</span></span>
<span data-ttu-id="2d7ad-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2d7ad-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d7ad-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d7ad-121">-WhatIf</span></span>
<span data-ttu-id="2d7ad-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2d7ad-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d7ad-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2d7ad-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d7ad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d7ad-124">CommonParameters</span></span>
<span data-ttu-id="2d7ad-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d7ad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d7ad-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d7ad-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d7ad-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d7ad-127">INPUTS</span></span>

### <span data-ttu-id="2d7ad-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2d7ad-128">System.String</span></span>

## <span data-ttu-id="2d7ad-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d7ad-129">OUTPUTS</span></span>

### <span data-ttu-id="2d7ad-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d7ad-130">System.Boolean</span></span>

## <span data-ttu-id="2d7ad-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d7ad-131">NOTES</span></span>

## <span data-ttu-id="2d7ad-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d7ad-132">RELATED LINKS</span></span>

[<span data-ttu-id="2d7ad-133">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="2d7ad-133">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="2d7ad-134">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="2d7ad-134">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="2d7ad-135">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="2d7ad-135">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


