---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 402bb79dbd3b767cbc285600b9c81e27f244141e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593884"
---
# <span data-ttu-id="8295e-101">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8295e-101">Get-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="8295e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8295e-102">SYNOPSIS</span></span>
<span data-ttu-id="8295e-103">İş koleksiyonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="8295e-103">Gets job collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8295e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8295e-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8295e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8295e-105">DESCRIPTION</span></span>
<span data-ttu-id="8295e-106">**Get-AzureRmSchedulerJobCollection** cmdlet 'ı Azure Scheduler 'daki iş koleksiyonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="8295e-106">The **Get-AzureRmSchedulerJobCollection** cmdlet gets job collections in Azure Scheduler.</span></span>

## <span data-ttu-id="8295e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8295e-107">EXAMPLES</span></span>

## <span data-ttu-id="8295e-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8295e-108">PARAMETERS</span></span>

### <span data-ttu-id="8295e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8295e-109">-DefaultProfile</span></span>
<span data-ttu-id="8295e-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8295e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8295e-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="8295e-111">-JobCollectionName</span></span>
<span data-ttu-id="8295e-112">İş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8295e-112">Specifies the name of a job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8295e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8295e-113">-ResourceGroupName</span></span>
<span data-ttu-id="8295e-114">Bu cmdlet 'in iş koleksiyonlarını aldığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8295e-114">Specifies resource group from which this cmdlet gets job collections.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8295e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8295e-115">CommonParameters</span></span>
<span data-ttu-id="8295e-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8295e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8295e-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8295e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8295e-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8295e-118">INPUTS</span></span>

### <span data-ttu-id="8295e-119">System. String</span><span class="sxs-lookup"><span data-stu-id="8295e-119">System.String</span></span>

## <span data-ttu-id="8295e-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8295e-120">OUTPUTS</span></span>

### <span data-ttu-id="8295e-121">Microsoft. Azure. Commands. Scheduler. modeller. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="8295e-121">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="8295e-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8295e-122">NOTES</span></span>

## <span data-ttu-id="8295e-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8295e-123">RELATED LINKS</span></span>

[<span data-ttu-id="8295e-124">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8295e-124">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8295e-125">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8295e-125">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8295e-126">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8295e-126">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8295e-127">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8295e-127">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8295e-128">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8295e-128">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


