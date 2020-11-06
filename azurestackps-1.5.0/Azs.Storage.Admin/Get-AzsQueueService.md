---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62c174a3aec5034b230954922f6aab5078fe4bac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572009"
---
# <span data-ttu-id="01892-101">Get-AzsQueueService</span><span class="sxs-lookup"><span data-stu-id="01892-101">Get-AzsQueueService</span></span>

## <span data-ttu-id="01892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01892-102">SYNOPSIS</span></span>
<span data-ttu-id="01892-103">Sıra hizmetini döndürür.</span><span class="sxs-lookup"><span data-stu-id="01892-103">Returns the queue service.</span></span>

## <span data-ttu-id="01892-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01892-104">SYNTAX</span></span>

```
Get-AzsQueueService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="01892-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="01892-105">DESCRIPTION</span></span>
<span data-ttu-id="01892-106">Sıra hizmetini döndürür.</span><span class="sxs-lookup"><span data-stu-id="01892-106">Returns the queue service.</span></span>

## <span data-ttu-id="01892-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01892-107">EXAMPLES</span></span>

### <span data-ttu-id="01892-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="01892-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsQueueService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="01892-109">Sıra hizmetini edinin.</span><span class="sxs-lookup"><span data-stu-id="01892-109">Get the queue service.</span></span>

## <span data-ttu-id="01892-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01892-110">PARAMETERS</span></span>

### <span data-ttu-id="01892-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="01892-111">-FarmName</span></span>
<span data-ttu-id="01892-112">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="01892-112">Farm Id.</span></span>

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

### <span data-ttu-id="01892-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01892-113">-ResourceGroupName</span></span>
<span data-ttu-id="01892-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="01892-114">Resource group name.</span></span>

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

### <span data-ttu-id="01892-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01892-115">CommonParameters</span></span>
<span data-ttu-id="01892-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01892-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01892-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01892-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01892-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01892-118">INPUTS</span></span>

## <span data-ttu-id="01892-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01892-119">OUTPUTS</span></span>

### <span data-ttu-id="01892-120">Microsoft. AzureStack. Management. Storage. admin. modeller. QueueService</span><span class="sxs-lookup"><span data-stu-id="01892-120">Microsoft.AzureStack.Management.Storage.Admin.Models.QueueService</span></span>

## <span data-ttu-id="01892-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01892-121">NOTES</span></span>

## <span data-ttu-id="01892-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01892-122">RELATED LINKS</span></span>

