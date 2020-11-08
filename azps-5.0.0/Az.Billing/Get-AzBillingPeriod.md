---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: 6a7f7d47976608b521e69e7aaf926a9600b35382
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278427"
---
# <span data-ttu-id="c4c94-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="c4c94-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="c4c94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4c94-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c94-103">Aboneliğin fatura dönemlerini alın.</span><span class="sxs-lookup"><span data-stu-id="c4c94-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="c4c94-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4c94-104">SYNTAX</span></span>

### <span data-ttu-id="c4c94-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c4c94-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4c94-106">Başına</span><span class="sxs-lookup"><span data-stu-id="c4c94-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4c94-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4c94-107">DESCRIPTION</span></span>
<span data-ttu-id="c4c94-108">**Get-Azbillingdönem** cmdlet 'i aboneliğin fatura dönemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c4c94-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="c4c94-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4c94-109">EXAMPLES</span></span>

### <span data-ttu-id="c4c94-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c4c94-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="c4c94-111">Aboneliğin tüm kullanılabilir fatura dönemlerini edinin.</span><span class="sxs-lookup"><span data-stu-id="c4c94-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="c4c94-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c4c94-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="c4c94-113">Belirtilen ada sahip aboneliğin fatura dönemini alın.</span><span class="sxs-lookup"><span data-stu-id="c4c94-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="c4c94-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c4c94-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="c4c94-115">Aboneliğin en fazla 2 fatura dönemini alın.</span><span class="sxs-lookup"><span data-stu-id="c4c94-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="c4c94-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4c94-116">PARAMETERS</span></span>

### <span data-ttu-id="c4c94-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4c94-117">-DefaultProfile</span></span>
<span data-ttu-id="c4c94-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c4c94-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4c94-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c4c94-119">-MaxCount</span></span>
<span data-ttu-id="c4c94-120">Döndürülecek en fazla kayıt sayısını belirleme.</span><span class="sxs-lookup"><span data-stu-id="c4c94-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="c4c94-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="c4c94-121">-Name</span></span>
<span data-ttu-id="c4c94-122">Alınacak belirli bir fatura döneminin adı.</span><span class="sxs-lookup"><span data-stu-id="c4c94-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="c4c94-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c94-123">CommonParameters</span></span>
<span data-ttu-id="c4c94-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4c94-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c94-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4c94-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c94-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4c94-126">INPUTS</span></span>

### <span data-ttu-id="c4c94-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c4c94-127">None</span></span>

## <span data-ttu-id="c4c94-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4c94-128">OUTPUTS</span></span>

### <span data-ttu-id="c4c94-129">Microsoft. Azure. Commands. faturalandırma. modeller. Psbillingdönem</span><span class="sxs-lookup"><span data-stu-id="c4c94-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="c4c94-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4c94-130">NOTES</span></span>

## <span data-ttu-id="c4c94-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4c94-131">RELATED LINKS</span></span>
