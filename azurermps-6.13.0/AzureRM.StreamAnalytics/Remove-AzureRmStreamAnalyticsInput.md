---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 8e80162d5efa6aa274617941df218812ae6901a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590804"
---
# <span data-ttu-id="7e4bb-101">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7e4bb-101">Remove-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="7e4bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e4bb-102">SYNOPSIS</span></span>
<span data-ttu-id="7e4bb-103">Akış Analizi işinden bir girişi siler.</span><span class="sxs-lookup"><span data-stu-id="7e4bb-103">Deletes an input from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e4bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e4bb-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e4bb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e4bb-105">DESCRIPTION</span></span>
<span data-ttu-id="7e4bb-106">**Remove-AzureRmStreamAnalyticsInput** cmdlet 'i Azure 'Daki bir Stream Analytics işinden gelen bir girişi zaman uyumsuz olarak siler.</span><span class="sxs-lookup"><span data-stu-id="7e4bb-106">The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="7e4bb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e4bb-107">EXAMPLES</span></span>

### <span data-ttu-id="7e4bb-108">Örnek 1: bir işten giriş akışını kaldırma</span><span class="sxs-lookup"><span data-stu-id="7e4bb-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="7e4bb-109">Bu komut, StreamingJob 'dan giriş Olayakışını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7e4bb-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="7e4bb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e4bb-110">PARAMETERS</span></span>

### <span data-ttu-id="7e4bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e4bb-111">-DefaultProfile</span></span>
<span data-ttu-id="7e4bb-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e4bb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e4bb-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="7e4bb-113">-JobName</span></span>
<span data-ttu-id="7e4bb-114">Azure Stream Analytics girişinin ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e4bb-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="7e4bb-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="7e4bb-115">-Name</span></span>
<span data-ttu-id="7e4bb-116">Kaldırılacak Azure Stream Analytics girişinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e4bb-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="7e4bb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e4bb-117">-ResourceGroupName</span></span>
<span data-ttu-id="7e4bb-118">Azure Akış Analizi girişinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e4bb-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="7e4bb-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="7e4bb-119">-Confirm</span></span>
<span data-ttu-id="7e4bb-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7e4bb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e4bb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e4bb-121">-WhatIf</span></span>
<span data-ttu-id="7e4bb-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e4bb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e4bb-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7e4bb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e4bb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e4bb-124">CommonParameters</span></span>
<span data-ttu-id="7e4bb-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e4bb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e4bb-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e4bb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e4bb-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e4bb-127">INPUTS</span></span>

### <span data-ttu-id="7e4bb-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7e4bb-128">System.String</span></span>

## <span data-ttu-id="7e4bb-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e4bb-129">OUTPUTS</span></span>

### <span data-ttu-id="7e4bb-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e4bb-130">System.Boolean</span></span>

## <span data-ttu-id="7e4bb-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e4bb-131">NOTES</span></span>

## <span data-ttu-id="7e4bb-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e4bb-132">RELATED LINKS</span></span>

[<span data-ttu-id="7e4bb-133">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7e4bb-133">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="7e4bb-134">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7e4bb-134">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="7e4bb-135">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7e4bb-135">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


