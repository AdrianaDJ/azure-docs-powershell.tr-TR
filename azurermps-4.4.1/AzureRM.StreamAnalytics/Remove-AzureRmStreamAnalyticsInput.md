---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: f801a7c8dd83927e8aceebdc98138aa6ad39d31c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593773"
---
# <span data-ttu-id="01c61-101">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="01c61-101">Remove-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="01c61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01c61-102">SYNOPSIS</span></span>
<span data-ttu-id="01c61-103">Akış Analizi işinden bir girişi siler.</span><span class="sxs-lookup"><span data-stu-id="01c61-103">Deletes an input from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01c61-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01c61-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01c61-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="01c61-105">DESCRIPTION</span></span>
<span data-ttu-id="01c61-106">**Remove-AzureRmStreamAnalyticsInput** cmdlet 'i Azure 'Daki bir Stream Analytics işinden gelen bir girişi zaman uyumsuz olarak siler.</span><span class="sxs-lookup"><span data-stu-id="01c61-106">The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="01c61-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01c61-107">EXAMPLES</span></span>

### <span data-ttu-id="01c61-108">Örnek 1: bir işten giriş akışını kaldırma</span><span class="sxs-lookup"><span data-stu-id="01c61-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="01c61-109">Bu komut, StreamingJob 'dan giriş Olayakışını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="01c61-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="01c61-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01c61-110">PARAMETERS</span></span>

### <span data-ttu-id="01c61-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="01c61-111">-JobName</span></span>
<span data-ttu-id="01c61-112">Azure Stream Analytics girişinin ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01c61-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="01c61-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="01c61-113">-Name</span></span>
<span data-ttu-id="01c61-114">Kaldırılacak Azure Stream Analytics girişinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01c61-114">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="01c61-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01c61-115">-ResourceGroupName</span></span>
<span data-ttu-id="01c61-116">Azure Akış Analizi girişinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01c61-116">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="01c61-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="01c61-117">-Confirm</span></span>
<span data-ttu-id="01c61-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="01c61-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01c61-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01c61-119">-WhatIf</span></span>
<span data-ttu-id="01c61-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="01c61-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01c61-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="01c61-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01c61-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c61-122">-DefaultProfile</span></span>
<span data-ttu-id="01c61-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="01c61-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01c61-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c61-124">CommonParameters</span></span>
<span data-ttu-id="01c61-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01c61-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c61-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01c61-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c61-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01c61-127">INPUTS</span></span>

## <span data-ttu-id="01c61-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01c61-128">OUTPUTS</span></span>

### <span data-ttu-id="01c61-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="01c61-129">System.Object</span></span>

## <span data-ttu-id="01c61-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01c61-130">NOTES</span></span>

## <span data-ttu-id="01c61-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01c61-131">RELATED LINKS</span></span>

[<span data-ttu-id="01c61-132">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="01c61-132">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="01c61-133">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="01c61-133">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="01c61-134">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="01c61-134">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


