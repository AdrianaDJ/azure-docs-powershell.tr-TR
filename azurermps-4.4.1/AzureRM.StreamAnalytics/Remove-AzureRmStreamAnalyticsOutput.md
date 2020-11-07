---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 9904699d95429e029f330e5c3ca3e5957eb4c35e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762183"
---
# <span data-ttu-id="f3174-101">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f3174-101">Remove-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="f3174-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3174-102">SYNOPSIS</span></span>
<span data-ttu-id="f3174-103">Bir Stream Analytics işinden çıktı siler.</span><span class="sxs-lookup"><span data-stu-id="f3174-103">Deletes an output from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3174-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3174-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3174-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3174-105">DESCRIPTION</span></span>
<span data-ttu-id="f3174-106">**Remove-AzureRmStreamAnalyticsOutput** cmdlet 'i Azure 'Daki bir Stream Analytics işinin çıktısını zaman uyumsuz olarak siler.</span><span class="sxs-lookup"><span data-stu-id="f3174-106">The **Remove-AzureRmStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="f3174-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3174-107">EXAMPLES</span></span>

### <span data-ttu-id="f3174-108">Örnek 1: bir işten çıktı kaldırma</span><span class="sxs-lookup"><span data-stu-id="f3174-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="f3174-109">Bu komut, iş StreamingJob 'daki çıkış çıkışını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f3174-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="f3174-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3174-110">PARAMETERS</span></span>

### <span data-ttu-id="f3174-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="f3174-111">-JobName</span></span>
<span data-ttu-id="f3174-112">Azure Stream Analytics çıkışının ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3174-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="f3174-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="f3174-113">-Name</span></span>
<span data-ttu-id="f3174-114">Kaldırılacak Azure Stream Analytics çıktısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3174-114">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="f3174-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3174-115">-ResourceGroupName</span></span>
<span data-ttu-id="f3174-116">Azure Stream Analytics çıktısının ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3174-116">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="f3174-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="f3174-117">-Confirm</span></span>
<span data-ttu-id="f3174-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f3174-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3174-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3174-119">-WhatIf</span></span>
<span data-ttu-id="f3174-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3174-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3174-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f3174-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3174-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3174-122">-DefaultProfile</span></span>
<span data-ttu-id="f3174-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f3174-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3174-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3174-124">CommonParameters</span></span>
<span data-ttu-id="f3174-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3174-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3174-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3174-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3174-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3174-127">INPUTS</span></span>

## <span data-ttu-id="f3174-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3174-128">OUTPUTS</span></span>

### <span data-ttu-id="f3174-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="f3174-129">System.Object</span></span>

## <span data-ttu-id="f3174-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3174-130">NOTES</span></span>

## <span data-ttu-id="f3174-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3174-131">RELATED LINKS</span></span>

[<span data-ttu-id="f3174-132">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f3174-132">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="f3174-133">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f3174-133">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="f3174-134">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f3174-134">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


