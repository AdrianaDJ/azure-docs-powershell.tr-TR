---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: b4e85f85d0e7b7724b2a09f3c78af03dfd489014
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753153"
---
# <span data-ttu-id="cd845-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="cd845-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="cd845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd845-102">SYNOPSIS</span></span>
<span data-ttu-id="cd845-103">Aboneliğin fatura dönemlerini alın.</span><span class="sxs-lookup"><span data-stu-id="cd845-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="cd845-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd845-104">SYNTAX</span></span>

### <span data-ttu-id="cd845-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cd845-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd845-106">Başına</span><span class="sxs-lookup"><span data-stu-id="cd845-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd845-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd845-107">DESCRIPTION</span></span>
<span data-ttu-id="cd845-108">**Get-Azbillingdönem** cmdlet 'i aboneliğin fatura dönemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="cd845-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="cd845-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd845-109">EXAMPLES</span></span>

### <span data-ttu-id="cd845-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cd845-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="cd845-111">Aboneliğin tüm kullanılabilir fatura dönemlerini edinin.</span><span class="sxs-lookup"><span data-stu-id="cd845-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="cd845-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="cd845-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="cd845-113">Belirtilen ada sahip aboneliğin fatura dönemini alın.</span><span class="sxs-lookup"><span data-stu-id="cd845-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="cd845-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="cd845-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="cd845-115">Aboneliğin en fazla 2 fatura dönemini alın.</span><span class="sxs-lookup"><span data-stu-id="cd845-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="cd845-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd845-116">PARAMETERS</span></span>

### <span data-ttu-id="cd845-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd845-117">-DefaultProfile</span></span>
<span data-ttu-id="cd845-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cd845-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd845-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="cd845-119">-MaxCount</span></span>
<span data-ttu-id="cd845-120">Döndürülecek en fazla kayıt sayısını belirleme.</span><span class="sxs-lookup"><span data-stu-id="cd845-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="cd845-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="cd845-121">-Name</span></span>
<span data-ttu-id="cd845-122">Alınacak belirli bir fatura döneminin adı.</span><span class="sxs-lookup"><span data-stu-id="cd845-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="cd845-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd845-123">CommonParameters</span></span>
<span data-ttu-id="cd845-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd845-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd845-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd845-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd845-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd845-126">INPUTS</span></span>

### <span data-ttu-id="cd845-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cd845-127">None</span></span>

## <span data-ttu-id="cd845-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd845-128">OUTPUTS</span></span>

### <span data-ttu-id="cd845-129">Microsoft. Azure. Commands. faturalandırma. modeller. Psbillingdönem</span><span class="sxs-lookup"><span data-stu-id="cd845-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="cd845-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd845-130">NOTES</span></span>

## <span data-ttu-id="cd845-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd845-131">RELATED LINKS</span></span>
