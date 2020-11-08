---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62c174a3aec5034b230954922f6aab5078fe4bac
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934861"
---
# <span data-ttu-id="cb59b-101">Get-AzsQueueService</span><span class="sxs-lookup"><span data-stu-id="cb59b-101">Get-AzsQueueService</span></span>

## <span data-ttu-id="cb59b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb59b-102">SYNOPSIS</span></span>
<span data-ttu-id="cb59b-103">Sıra hizmetini döndürür.</span><span class="sxs-lookup"><span data-stu-id="cb59b-103">Returns the queue service.</span></span>

## <span data-ttu-id="cb59b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb59b-104">SYNTAX</span></span>

```
Get-AzsQueueService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="cb59b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb59b-105">DESCRIPTION</span></span>
<span data-ttu-id="cb59b-106">Sıra hizmetini döndürür.</span><span class="sxs-lookup"><span data-stu-id="cb59b-106">Returns the queue service.</span></span>

## <span data-ttu-id="cb59b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb59b-107">EXAMPLES</span></span>

### <span data-ttu-id="cb59b-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cb59b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsQueueService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="cb59b-109">Sıra hizmetini edinin.</span><span class="sxs-lookup"><span data-stu-id="cb59b-109">Get the queue service.</span></span>

## <span data-ttu-id="cb59b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb59b-110">PARAMETERS</span></span>

### <span data-ttu-id="cb59b-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="cb59b-111">-FarmName</span></span>
<span data-ttu-id="cb59b-112">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="cb59b-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb59b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb59b-113">-ResourceGroupName</span></span>
<span data-ttu-id="cb59b-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cb59b-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb59b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb59b-115">CommonParameters</span></span>
<span data-ttu-id="cb59b-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb59b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb59b-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb59b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb59b-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb59b-118">INPUTS</span></span>

## <span data-ttu-id="cb59b-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb59b-119">OUTPUTS</span></span>

### <span data-ttu-id="cb59b-120">Microsoft. AzureStack. Management. Storage. admin. modeller. QueueService</span><span class="sxs-lookup"><span data-stu-id="cb59b-120">Microsoft.AzureStack.Management.Storage.Admin.Models.QueueService</span></span>

## <span data-ttu-id="cb59b-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb59b-121">NOTES</span></span>

## <span data-ttu-id="cb59b-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb59b-122">RELATED LINKS</span></span>
