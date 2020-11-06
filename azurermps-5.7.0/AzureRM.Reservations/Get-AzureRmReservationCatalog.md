---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
ms.openlocfilehash: 4714b97773583197807d6ca54152ee25ab520909
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589702"
---
# <span data-ttu-id="bad07-101">Get-AzureRmReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="bad07-101">Get-AzureRmReservationCatalog</span></span>

## <span data-ttu-id="bad07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bad07-102">SYNOPSIS</span></span>
<span data-ttu-id="bad07-103">Kullanılabilir ayırma kataloğunu alma</span><span class="sxs-lookup"><span data-stu-id="bad07-103">Get the catalog of available reservation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bad07-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bad07-104">SYNTAX</span></span>

```
Get-AzureRmReservationCatalog [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="bad07-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bad07-105">DESCRIPTION</span></span>
<span data-ttu-id="bad07-106">Belirtilen Azure aboneliği için ayrılan örnek satın alma için sağlanan bölgeleri ve STB 'leri edinin.</span><span class="sxs-lookup"><span data-stu-id="bad07-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="bad07-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bad07-107">EXAMPLES</span></span>

### <span data-ttu-id="bad07-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bad07-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationCatalog
```

<span data-ttu-id="bad07-109">Varsayılan aboneliğin kataloğunu alma</span><span class="sxs-lookup"><span data-stu-id="bad07-109">Get the catalog for the default subscription</span></span>

### <span data-ttu-id="bad07-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bad07-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="bad07-111">Belirtilen abonelik için kataloğu edinin</span><span class="sxs-lookup"><span data-stu-id="bad07-111">Get the catalog for the specified subscription</span></span>

## <span data-ttu-id="bad07-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bad07-112">PARAMETERS</span></span>

### <span data-ttu-id="bad07-113">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="bad07-113">-SubscriptionId</span></span>
<span data-ttu-id="bad07-114">Aboneliğin kimliği</span><span class="sxs-lookup"><span data-stu-id="bad07-114">Id of the subscription</span></span>

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

### <span data-ttu-id="bad07-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bad07-115">CommonParameters</span></span>
<span data-ttu-id="bad07-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bad07-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bad07-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bad07-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bad07-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bad07-118">INPUTS</span></span>

### <span data-ttu-id="bad07-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bad07-119">None</span></span>

## <span data-ttu-id="bad07-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bad07-120">OUTPUTS</span></span>

### <span data-ttu-id="bad07-121">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. rezervasyonlar. modeller. PSCatalog, Microsoft. Azure. Commands. rezervasyonlar, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bad07-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSCatalog, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bad07-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bad07-122">NOTES</span></span>

## <span data-ttu-id="bad07-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bad07-123">RELATED LINKS</span></span>

