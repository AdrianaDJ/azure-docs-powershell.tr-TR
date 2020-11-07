---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 03cca81794e190a97ce21b7e9ed8c82392db3e36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762001"
---
# <span data-ttu-id="421e2-101">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="421e2-101">Remove-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="421e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="421e2-102">SYNOPSIS</span></span>
<span data-ttu-id="421e2-103">Bir Stream Analytics işinden çıktı siler.</span><span class="sxs-lookup"><span data-stu-id="421e2-103">Deletes an output from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="421e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="421e2-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="421e2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="421e2-105">DESCRIPTION</span></span>
<span data-ttu-id="421e2-106">**Remove-AzureRmStreamAnalyticsOutput** cmdlet 'i Azure 'Daki bir Stream Analytics işinin çıktısını zaman uyumsuz olarak siler.</span><span class="sxs-lookup"><span data-stu-id="421e2-106">The **Remove-AzureRmStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="421e2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="421e2-107">EXAMPLES</span></span>

### <span data-ttu-id="421e2-108">Örnek 1: bir işten çıktı kaldırma</span><span class="sxs-lookup"><span data-stu-id="421e2-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="421e2-109">Bu komut, iş StreamingJob 'daki çıkış çıkışını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="421e2-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="421e2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="421e2-110">PARAMETERS</span></span>

### <span data-ttu-id="421e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="421e2-111">-DefaultProfile</span></span>
<span data-ttu-id="421e2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="421e2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="421e2-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="421e2-113">-JobName</span></span>
<span data-ttu-id="421e2-114">Azure Stream Analytics çıkışının ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="421e2-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="421e2-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="421e2-115">-Name</span></span>
<span data-ttu-id="421e2-116">Kaldırılacak Azure Stream Analytics çıktısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="421e2-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="421e2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="421e2-117">-ResourceGroupName</span></span>
<span data-ttu-id="421e2-118">Azure Stream Analytics çıktısının ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="421e2-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="421e2-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="421e2-119">-Confirm</span></span>
<span data-ttu-id="421e2-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="421e2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="421e2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="421e2-121">-WhatIf</span></span>
<span data-ttu-id="421e2-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="421e2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="421e2-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="421e2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="421e2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="421e2-124">CommonParameters</span></span>
<span data-ttu-id="421e2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="421e2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="421e2-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="421e2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="421e2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="421e2-127">INPUTS</span></span>

### <span data-ttu-id="421e2-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="421e2-128">None</span></span>
<span data-ttu-id="421e2-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="421e2-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="421e2-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="421e2-130">OUTPUTS</span></span>

### <span data-ttu-id="421e2-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="421e2-131">System.Object</span></span>

## <span data-ttu-id="421e2-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="421e2-132">NOTES</span></span>

## <span data-ttu-id="421e2-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="421e2-133">RELATED LINKS</span></span>

[<span data-ttu-id="421e2-134">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="421e2-134">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="421e2-135">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="421e2-135">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="421e2-136">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="421e2-136">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


