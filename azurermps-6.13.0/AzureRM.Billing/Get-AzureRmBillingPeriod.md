---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: 66c9a0bb9ba4aa2f17c48ffb737f1c8d72034f1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592798"
---
# <span data-ttu-id="cd957-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="cd957-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="cd957-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd957-102">SYNOPSIS</span></span>
<span data-ttu-id="cd957-103">Aboneliğin fatura dönemlerini alın.</span><span class="sxs-lookup"><span data-stu-id="cd957-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd957-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd957-104">SYNTAX</span></span>

### <span data-ttu-id="cd957-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cd957-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd957-106">Başına</span><span class="sxs-lookup"><span data-stu-id="cd957-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd957-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd957-107">DESCRIPTION</span></span>
<span data-ttu-id="cd957-108">**Get-Azurermbillingdönem** cmdlet 'i aboneliğin fatura dönemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="cd957-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="cd957-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd957-109">EXAMPLES</span></span>

### <span data-ttu-id="cd957-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cd957-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="cd957-111">Aboneliğin tüm kullanılabilir fatura dönemlerini edinin.</span><span class="sxs-lookup"><span data-stu-id="cd957-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="cd957-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="cd957-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="cd957-113">Belirtilen ada sahip aboneliğin fatura dönemini alın.</span><span class="sxs-lookup"><span data-stu-id="cd957-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="cd957-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="cd957-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="cd957-115">Aboneliğin en fazla 2 fatura dönemini alın.</span><span class="sxs-lookup"><span data-stu-id="cd957-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="cd957-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd957-116">PARAMETERS</span></span>

### <span data-ttu-id="cd957-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd957-117">-DefaultProfile</span></span>
<span data-ttu-id="cd957-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cd957-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd957-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="cd957-119">-MaxCount</span></span>
<span data-ttu-id="cd957-120">Döndürülecek en fazla kayıt sayısını belirleme.</span><span class="sxs-lookup"><span data-stu-id="cd957-120">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd957-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="cd957-121">-Name</span></span>
<span data-ttu-id="cd957-122">Alınacak belirli bir fatura döneminin adı.</span><span class="sxs-lookup"><span data-stu-id="cd957-122">Name of a specific billing period to get.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd957-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd957-123">CommonParameters</span></span>
<span data-ttu-id="cd957-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd957-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd957-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd957-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd957-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd957-126">INPUTS</span></span>

### <span data-ttu-id="cd957-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cd957-127">None</span></span>

## <span data-ttu-id="cd957-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd957-128">OUTPUTS</span></span>

### <span data-ttu-id="cd957-129">Microsoft. Azure. Commands. faturalandırma. modeller. Psbillingdönem</span><span class="sxs-lookup"><span data-stu-id="cd957-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="cd957-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd957-130">NOTES</span></span>

## <span data-ttu-id="cd957-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd957-131">RELATED LINKS</span></span>
