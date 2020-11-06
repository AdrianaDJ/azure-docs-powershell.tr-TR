---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 5a6ccf36f8e7aecdca4d6560614e9185a5ca26b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587669"
---
# <span data-ttu-id="e7195-101">Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="e7195-101">Get-AzureRmBillingInvoice</span></span>

## <span data-ttu-id="e7195-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7195-102">SYNOPSIS</span></span>
<span data-ttu-id="e7195-103">Aboneliğin fatura faturalarını alma.</span><span class="sxs-lookup"><span data-stu-id="e7195-103">Get billing invoices of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7195-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7195-104">SYNTAX</span></span>

### <span data-ttu-id="e7195-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e7195-105">List (Default)</span></span>
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7195-106">Sürümü</span><span class="sxs-lookup"><span data-stu-id="e7195-106">Latest</span></span>
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7195-107">Başına</span><span class="sxs-lookup"><span data-stu-id="e7195-107">Single</span></span>
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7195-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7195-108">DESCRIPTION</span></span>
<span data-ttu-id="e7195-109">**Get-Azurermbillingınvoice** cmdlet 'inin fatura faturalarını alır.</span><span class="sxs-lookup"><span data-stu-id="e7195-109">The **Get-AzureRmBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="e7195-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7195-110">EXAMPLES</span></span>

### <span data-ttu-id="e7195-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e7195-111">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

<span data-ttu-id="e7195-112">Aboneliğin en son faturasını edinin.</span><span class="sxs-lookup"><span data-stu-id="e7195-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="e7195-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e7195-113">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="e7195-114">Belirtilen ada sahip aboneliğin faturasını alın.</span><span class="sxs-lookup"><span data-stu-id="e7195-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="e7195-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="e7195-115">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingInvoice
```

<span data-ttu-id="e7195-116">Aboneliğin tüm kullanılabilir faturalarını, indirme URL 'Si olmadan en son faturayla başlayan ters kronolojik sırada alın.</span><span class="sxs-lookup"><span data-stu-id="e7195-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="e7195-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="e7195-117">Example 4</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="e7195-118">Aboneliğin en son 10 faturalarını alın ve indirme URL 'sini sonuç olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e7195-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="e7195-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7195-119">PARAMETERS</span></span>

### <span data-ttu-id="e7195-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7195-120">-DefaultProfile</span></span>
<span data-ttu-id="e7195-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e7195-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7195-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="e7195-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="e7195-123">Faturaların indirme URL 'sini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e7195-123">Generate the download url of the invoices.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7195-124">-En son</span><span class="sxs-lookup"><span data-stu-id="e7195-124">-Latest</span></span>
<span data-ttu-id="e7195-125">En son faturayı edinin.</span><span class="sxs-lookup"><span data-stu-id="e7195-125">Get the latest invoice.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Latest
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7195-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e7195-126">-MaxCount</span></span>
<span data-ttu-id="e7195-127">Döndürülecek en fazla kayıt sayısını belirler.</span><span class="sxs-lookup"><span data-stu-id="e7195-127">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="e7195-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7195-128">-Name</span></span>
<span data-ttu-id="e7195-129">Bir veya en son belirtilmemişse, belirli bir faturanın adı.</span><span class="sxs-lookup"><span data-stu-id="e7195-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="e7195-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7195-130">CommonParameters</span></span>
<span data-ttu-id="e7195-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7195-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7195-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7195-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7195-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7195-133">INPUTS</span></span>

### <span data-ttu-id="e7195-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e7195-134">None</span></span>

## <span data-ttu-id="e7195-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7195-135">OUTPUTS</span></span>

### <span data-ttu-id="e7195-136">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. faturalandırma. modeller. Invoice, Microsoft. Azure. Commands. Faturalandırma, Version = 0.14.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e7195-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Billing.Models.Invoice, Microsoft.Azure.Commands.Billing, Version=0.14.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="e7195-137">Microsoft. Azure. Management. faturalandırma. modeller. fatura</span><span class="sxs-lookup"><span data-stu-id="e7195-137">Microsoft.Azure.Management.Billing.Models.Invoice</span></span>

## <span data-ttu-id="e7195-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7195-138">NOTES</span></span>

## <span data-ttu-id="e7195-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7195-139">RELATED LINKS</span></span>

