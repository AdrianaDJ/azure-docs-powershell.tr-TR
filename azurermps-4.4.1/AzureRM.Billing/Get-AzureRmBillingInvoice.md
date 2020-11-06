---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 38b1c4e29ed82ac3bddcff9565a216bd6db23411
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592247"
---
# <span data-ttu-id="fb8eb-101">Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="fb8eb-101">Get-AzureRmBillingInvoice</span></span>

## <span data-ttu-id="fb8eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb8eb-102">SYNOPSIS</span></span>
<span data-ttu-id="fb8eb-103">Aboneliğin fatura faturalarını alma.</span><span class="sxs-lookup"><span data-stu-id="fb8eb-103">Get billing invoices of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb8eb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb8eb-104">SYNTAX</span></span>

### <span data-ttu-id="fb8eb-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fb8eb-105">List (Default)</span></span>
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb8eb-106">Sürümü</span><span class="sxs-lookup"><span data-stu-id="fb8eb-106">Latest</span></span>
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb8eb-107">Başına</span><span class="sxs-lookup"><span data-stu-id="fb8eb-107">Single</span></span>
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb8eb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb8eb-108">DESCRIPTION</span></span>
<span data-ttu-id="fb8eb-109">**Get-Azurermbillingınvoice** cmdlet 'inin fatura faturalarını alır.</span><span class="sxs-lookup"><span data-stu-id="fb8eb-109">The **Get-AzureRmBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="fb8eb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb8eb-110">EXAMPLES</span></span>

### <span data-ttu-id="fb8eb-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fb8eb-111">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

<span data-ttu-id="fb8eb-112">Aboneliğin en son faturasını edinin.</span><span class="sxs-lookup"><span data-stu-id="fb8eb-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="fb8eb-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="fb8eb-113">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="fb8eb-114">Belirtilen ada sahip aboneliğin faturasını alın.</span><span class="sxs-lookup"><span data-stu-id="fb8eb-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="fb8eb-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="fb8eb-115">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingInvoice
```

<span data-ttu-id="fb8eb-116">Aboneliğin tüm kullanılabilir faturalarını, indirme URL 'Si olmadan en son faturayla başlayan ters kronolojik sırada alın.</span><span class="sxs-lookup"><span data-stu-id="fb8eb-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="fb8eb-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="fb8eb-117">Example 4</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="fb8eb-118">Aboneliğin en son 10 faturalarını alın ve indirme URL 'sini sonuç olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fb8eb-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="fb8eb-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb8eb-119">PARAMETERS</span></span>

### <span data-ttu-id="fb8eb-120">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="fb8eb-120">-GenerateDownloadUrl</span></span>
<span data-ttu-id="fb8eb-121">Faturaların indirme URL 'sini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fb8eb-121">Generate the download url of the invoices.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb8eb-122">-En son</span><span class="sxs-lookup"><span data-stu-id="fb8eb-122">-Latest</span></span>
<span data-ttu-id="fb8eb-123">En son faturayı edinin.</span><span class="sxs-lookup"><span data-stu-id="fb8eb-123">Get the latest invoice.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Latest
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb8eb-124">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fb8eb-124">-MaxCount</span></span>
<span data-ttu-id="fb8eb-125">Döndürülecek en fazla kayıt sayısını belirler.</span><span class="sxs-lookup"><span data-stu-id="fb8eb-125">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="fb8eb-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb8eb-126">-Name</span></span>
<span data-ttu-id="fb8eb-127">Bir veya en son belirtilmemişse, belirli bir faturanın adı.</span><span class="sxs-lookup"><span data-stu-id="fb8eb-127">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="fb8eb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb8eb-128">-DefaultProfile</span></span>
<span data-ttu-id="fb8eb-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb8eb-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb8eb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb8eb-130">CommonParameters</span></span>
<span data-ttu-id="fb8eb-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb8eb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb8eb-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb8eb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb8eb-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb8eb-133">INPUTS</span></span>

### <span data-ttu-id="fb8eb-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fb8eb-134">None</span></span>

## <span data-ttu-id="fb8eb-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb8eb-135">OUTPUTS</span></span>

### <span data-ttu-id="fb8eb-136">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. faturalandırma. modeller. Invoice, Microsoft. Azure. Commands. Faturalandırma, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fb8eb-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Billing.Models.Invoice, Microsoft.Azure.Commands.Billing, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="fb8eb-137">Microsoft. Azure. Management. faturalandırma. modeller. fatura</span><span class="sxs-lookup"><span data-stu-id="fb8eb-137">Microsoft.Azure.Management.Billing.Models.Invoice</span></span>

## <span data-ttu-id="fb8eb-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb8eb-138">NOTES</span></span>

## <span data-ttu-id="fb8eb-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb8eb-139">RELATED LINKS</span></span>

