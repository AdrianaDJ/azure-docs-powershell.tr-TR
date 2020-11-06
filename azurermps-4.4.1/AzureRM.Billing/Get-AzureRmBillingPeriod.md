---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: f6b75a1c161515ee45571ba3db6d2f84b95af967
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588276"
---
# <span data-ttu-id="3c74b-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="3c74b-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="3c74b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c74b-102">SYNOPSIS</span></span>
<span data-ttu-id="3c74b-103">Aboneliğin fatura dönemlerini alın.</span><span class="sxs-lookup"><span data-stu-id="3c74b-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c74b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c74b-104">SYNTAX</span></span>

### <span data-ttu-id="3c74b-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3c74b-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c74b-106">Başına</span><span class="sxs-lookup"><span data-stu-id="3c74b-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c74b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c74b-107">DESCRIPTION</span></span>
<span data-ttu-id="3c74b-108">**Get-Azurermbillingdönem** cmdlet 'i aboneliğin fatura dönemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="3c74b-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="3c74b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c74b-109">EXAMPLES</span></span>

### <span data-ttu-id="3c74b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3c74b-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="3c74b-111">Aboneliğin tüm kullanılabilir fatura dönemlerini edinin.</span><span class="sxs-lookup"><span data-stu-id="3c74b-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="3c74b-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3c74b-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="3c74b-113">Belirtilen ada sahip aboneliğin fatura dönemini alın.</span><span class="sxs-lookup"><span data-stu-id="3c74b-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="3c74b-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3c74b-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="3c74b-115">Aboneliğin en fazla 2 fatura dönemini alın.</span><span class="sxs-lookup"><span data-stu-id="3c74b-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="3c74b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c74b-116">PARAMETERS</span></span>

### <span data-ttu-id="3c74b-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3c74b-117">-MaxCount</span></span>
<span data-ttu-id="3c74b-118">Döndürülecek en fazla kayıt sayısını belirleme.</span><span class="sxs-lookup"><span data-stu-id="3c74b-118">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="3c74b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="3c74b-119">-Name</span></span>
<span data-ttu-id="3c74b-120">Alınacak belirli bir fatura döneminin adı.</span><span class="sxs-lookup"><span data-stu-id="3c74b-120">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="3c74b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c74b-121">-DefaultProfile</span></span>
<span data-ttu-id="3c74b-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3c74b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c74b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c74b-123">CommonParameters</span></span>
<span data-ttu-id="3c74b-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c74b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c74b-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c74b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c74b-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c74b-126">INPUTS</span></span>

### <span data-ttu-id="3c74b-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3c74b-127">None</span></span>

## <span data-ttu-id="3c74b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c74b-128">OUTPUTS</span></span>

### <span data-ttu-id="3c74b-129">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. faturalandırma. modeller. Psbillingdönem, Microsoft. Azure. Commands. Faturalandırma, Version = 0.12.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3c74b-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod, Microsoft.Azure.Commands.Billing, Version=0.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="3c74b-130">Microsoft. Azure. Commands. faturalandırma. modeller. Psbillingdönem</span><span class="sxs-lookup"><span data-stu-id="3c74b-130">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="3c74b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c74b-131">NOTES</span></span>

## <span data-ttu-id="3c74b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c74b-132">RELATED LINKS</span></span>

