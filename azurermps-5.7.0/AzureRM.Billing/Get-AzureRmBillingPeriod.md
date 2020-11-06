---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: 7d3c09385c76fef525535384459d03b0cc65dd9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594139"
---
# <span data-ttu-id="76067-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="76067-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="76067-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76067-102">SYNOPSIS</span></span>
<span data-ttu-id="76067-103">Aboneliğin fatura dönemlerini alın.</span><span class="sxs-lookup"><span data-stu-id="76067-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76067-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76067-104">SYNTAX</span></span>

### <span data-ttu-id="76067-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="76067-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76067-106">Başına</span><span class="sxs-lookup"><span data-stu-id="76067-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76067-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="76067-107">DESCRIPTION</span></span>
<span data-ttu-id="76067-108">**Get-Azurermbillingdönem** cmdlet 'i aboneliğin fatura dönemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="76067-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="76067-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76067-109">EXAMPLES</span></span>

### <span data-ttu-id="76067-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="76067-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="76067-111">Aboneliğin tüm kullanılabilir fatura dönemlerini edinin.</span><span class="sxs-lookup"><span data-stu-id="76067-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="76067-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="76067-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="76067-113">Belirtilen ada sahip aboneliğin fatura dönemini alın.</span><span class="sxs-lookup"><span data-stu-id="76067-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="76067-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="76067-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="76067-115">Aboneliğin en fazla 2 fatura dönemini alın.</span><span class="sxs-lookup"><span data-stu-id="76067-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="76067-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76067-116">PARAMETERS</span></span>

### <span data-ttu-id="76067-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76067-117">-DefaultProfile</span></span>
<span data-ttu-id="76067-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="76067-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76067-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="76067-119">-MaxCount</span></span>
<span data-ttu-id="76067-120">Döndürülecek en fazla kayıt sayısını belirleme.</span><span class="sxs-lookup"><span data-stu-id="76067-120">Determine the maximum number of records to return.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76067-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="76067-121">-Name</span></span>
<span data-ttu-id="76067-122">Alınacak belirli bir fatura döneminin adı.</span><span class="sxs-lookup"><span data-stu-id="76067-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="76067-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76067-123">CommonParameters</span></span>
<span data-ttu-id="76067-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76067-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76067-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76067-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76067-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76067-126">INPUTS</span></span>

### <span data-ttu-id="76067-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="76067-127">None</span></span>

## <span data-ttu-id="76067-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76067-128">OUTPUTS</span></span>

### <span data-ttu-id="76067-129">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. faturalandırma. modeller. Psbillingdönem, Microsoft. Azure. Commands. Faturalandırma, Version = 0.14.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="76067-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod, Microsoft.Azure.Commands.Billing, Version=0.14.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="76067-130">Microsoft. Azure. Commands. faturalandırma. modeller. Psbillingdönem</span><span class="sxs-lookup"><span data-stu-id="76067-130">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="76067-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76067-131">NOTES</span></span>

## <span data-ttu-id="76067-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76067-132">RELATED LINKS</span></span>

