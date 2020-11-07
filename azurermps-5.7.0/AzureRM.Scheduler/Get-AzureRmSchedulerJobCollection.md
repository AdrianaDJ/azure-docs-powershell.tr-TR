---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: da1133895d062e3f49fae0bf6571c3bfeb72992c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763995"
---
# <span data-ttu-id="54fa2-101">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="54fa2-101">Get-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="54fa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="54fa2-103">İş koleksiyonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="54fa2-103">Gets job collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54fa2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54fa2-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54fa2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="54fa2-105">DESCRIPTION</span></span>
<span data-ttu-id="54fa2-106">**Get-AzureRmSchedulerJobCollection** cmdlet 'ı Azure Scheduler 'daki iş koleksiyonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="54fa2-106">The **Get-AzureRmSchedulerJobCollection** cmdlet gets job collections in Azure Scheduler.</span></span>

## <span data-ttu-id="54fa2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54fa2-107">EXAMPLES</span></span>

## <span data-ttu-id="54fa2-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54fa2-108">PARAMETERS</span></span>

### <span data-ttu-id="54fa2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54fa2-109">-DefaultProfile</span></span>
<span data-ttu-id="54fa2-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54fa2-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54fa2-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="54fa2-111">-JobCollectionName</span></span>
<span data-ttu-id="54fa2-112">İş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fa2-112">Specifies the name of a job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fa2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54fa2-113">-ResourceGroupName</span></span>
<span data-ttu-id="54fa2-114">Bu cmdlet 'in iş koleksiyonlarını aldığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fa2-114">Specifies resource group from which this cmdlet gets job collections.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fa2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54fa2-115">CommonParameters</span></span>
<span data-ttu-id="54fa2-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54fa2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54fa2-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54fa2-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54fa2-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54fa2-118">INPUTS</span></span>

### <span data-ttu-id="54fa2-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="54fa2-119">None</span></span>
<span data-ttu-id="54fa2-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="54fa2-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="54fa2-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54fa2-121">OUTPUTS</span></span>

### <span data-ttu-id="54fa2-122">System. Object</span><span class="sxs-lookup"><span data-stu-id="54fa2-122">System.Object</span></span>

## <span data-ttu-id="54fa2-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54fa2-123">NOTES</span></span>

## <span data-ttu-id="54fa2-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54fa2-124">RELATED LINKS</span></span>

[<span data-ttu-id="54fa2-125">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="54fa2-125">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="54fa2-126">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="54fa2-126">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="54fa2-127">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="54fa2-127">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="54fa2-128">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="54fa2-128">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="54fa2-129">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="54fa2-129">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


