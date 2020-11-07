---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: fe6c78c0a4d1f4fa3ae9f7f917bdcffa49431575
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753921"
---
# <span data-ttu-id="fde27-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="fde27-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="fde27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fde27-102">SYNOPSIS</span></span>
<span data-ttu-id="fde27-103">Akış Analizi işinden bir girişi siler.</span><span class="sxs-lookup"><span data-stu-id="fde27-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="fde27-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fde27-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fde27-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fde27-105">DESCRIPTION</span></span>
<span data-ttu-id="fde27-106">**Remove-AzStreamAnalyticsInput** cmdlet 'i Azure 'Daki bir Stream Analytics işinden gelen bir girişi zaman uyumsuz olarak siler.</span><span class="sxs-lookup"><span data-stu-id="fde27-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="fde27-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fde27-107">EXAMPLES</span></span>

### <span data-ttu-id="fde27-108">Örnek 1: bir işten giriş akışını kaldırma</span><span class="sxs-lookup"><span data-stu-id="fde27-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="fde27-109">Bu komut, StreamingJob 'dan giriş Olayakışını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fde27-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="fde27-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fde27-110">PARAMETERS</span></span>

### <span data-ttu-id="fde27-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde27-111">-DefaultProfile</span></span>
<span data-ttu-id="fde27-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fde27-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fde27-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="fde27-113">-JobName</span></span>
<span data-ttu-id="fde27-114">Azure Stream Analytics girişinin ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fde27-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="fde27-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="fde27-115">-Name</span></span>
<span data-ttu-id="fde27-116">Kaldırılacak Azure Stream Analytics girişinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fde27-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="fde27-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fde27-117">-ResourceGroupName</span></span>
<span data-ttu-id="fde27-118">Azure Akış Analizi girişinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fde27-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="fde27-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="fde27-119">-Confirm</span></span>
<span data-ttu-id="fde27-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fde27-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fde27-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fde27-121">-WhatIf</span></span>
<span data-ttu-id="fde27-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fde27-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fde27-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fde27-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fde27-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde27-124">CommonParameters</span></span>
<span data-ttu-id="fde27-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fde27-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde27-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fde27-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde27-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fde27-127">INPUTS</span></span>

### <span data-ttu-id="fde27-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fde27-128">System.String</span></span>

## <span data-ttu-id="fde27-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fde27-129">OUTPUTS</span></span>

### <span data-ttu-id="fde27-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fde27-130">System.Boolean</span></span>

## <span data-ttu-id="fde27-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fde27-131">NOTES</span></span>

## <span data-ttu-id="fde27-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fde27-132">RELATED LINKS</span></span>

[<span data-ttu-id="fde27-133">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="fde27-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="fde27-134">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="fde27-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="fde27-135">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="fde27-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


