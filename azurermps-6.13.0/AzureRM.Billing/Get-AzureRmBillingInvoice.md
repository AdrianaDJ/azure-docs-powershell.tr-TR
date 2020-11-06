---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 1f21022294b1bcf5c75a7cf49dcc009600dc4cc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592797"
---
# <span data-ttu-id="c4b0a-101">Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="c4b0a-101">Get-AzureRmBillingInvoice</span></span>

## <span data-ttu-id="c4b0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4b0a-102">SYNOPSIS</span></span>
<span data-ttu-id="c4b0a-103">Aboneliğin fatura faturalarını alma.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-103">Get billing invoices of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4b0a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4b0a-104">SYNTAX</span></span>

### <span data-ttu-id="c4b0a-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c4b0a-105">List (Default)</span></span>
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4b0a-106">Sürümü</span><span class="sxs-lookup"><span data-stu-id="c4b0a-106">Latest</span></span>
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4b0a-107">Başına</span><span class="sxs-lookup"><span data-stu-id="c4b0a-107">Single</span></span>
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4b0a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4b0a-108">DESCRIPTION</span></span>
<span data-ttu-id="c4b0a-109">**Get-Azurermbillingınvoice** cmdlet 'inin fatura faturalarını alır.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-109">The **Get-AzureRmBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="c4b0a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4b0a-110">EXAMPLES</span></span>

### <span data-ttu-id="c4b0a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c4b0a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

<span data-ttu-id="c4b0a-112">Aboneliğin en son faturasını edinin.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="c4b0a-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c4b0a-113">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="c4b0a-114">Belirtilen ada sahip aboneliğin faturasını alın.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="c4b0a-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c4b0a-115">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingInvoice
```

<span data-ttu-id="c4b0a-116">Aboneliğin tüm kullanılabilir faturalarını, indirme URL 'Si olmadan en son faturayla başlayan ters kronolojik sırada alın.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="c4b0a-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="c4b0a-117">Example 4</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="c4b0a-118">Aboneliğin en son 10 faturalarını alın ve indirme URL 'sini sonuç olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="c4b0a-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4b0a-119">PARAMETERS</span></span>

### <span data-ttu-id="c4b0a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4b0a-120">-DefaultProfile</span></span>
<span data-ttu-id="c4b0a-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c4b0a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4b0a-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="c4b0a-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="c4b0a-123">Faturaların indirme URL 'sini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-123">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="c4b0a-124">-En son</span><span class="sxs-lookup"><span data-stu-id="c4b0a-124">-Latest</span></span>
<span data-ttu-id="c4b0a-125">En son faturayı edinin.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-125">Get the latest invoice.</span></span>

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

### <span data-ttu-id="c4b0a-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c4b0a-126">-MaxCount</span></span>
<span data-ttu-id="c4b0a-127">Döndürülecek en fazla kayıt sayısını belirler.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-127">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="c4b0a-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="c4b0a-128">-Name</span></span>
<span data-ttu-id="c4b0a-129">Bir veya en son belirtilmemişse, belirli bir faturanın adı.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="c4b0a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4b0a-130">CommonParameters</span></span>
<span data-ttu-id="c4b0a-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4b0a-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4b0a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4b0a-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4b0a-133">INPUTS</span></span>

### <span data-ttu-id="c4b0a-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c4b0a-134">None</span></span>

## <span data-ttu-id="c4b0a-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4b0a-135">OUTPUTS</span></span>

### <span data-ttu-id="c4b0a-136">Microsoft. Azure. Commands. faturalandırma. modeller. Psınvoice</span><span class="sxs-lookup"><span data-stu-id="c4b0a-136">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="c4b0a-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4b0a-137">NOTES</span></span>

## <span data-ttu-id="c4b0a-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4b0a-138">RELATED LINKS</span></span>
