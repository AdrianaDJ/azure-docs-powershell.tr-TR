---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: ccb686ab0aeb373a542e958aab7b90489fc36f63
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278417"
---
# <span data-ttu-id="6f6ce-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="6f6ce-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="6f6ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f6ce-102">SYNOPSIS</span></span>
<span data-ttu-id="6f6ce-103">Fatura bölümlerini al.</span><span class="sxs-lookup"><span data-stu-id="6f6ce-103">Get invoice sections.</span></span>

## <span data-ttu-id="6f6ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f6ce-104">SYNTAX</span></span>

### <span data-ttu-id="6f6ce-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6f6ce-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f6ce-106">Başına</span><span class="sxs-lookup"><span data-stu-id="6f6ce-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f6ce-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f6ce-107">DESCRIPTION</span></span>
<span data-ttu-id="6f6ce-108">**Get-Azfaturasection** cmdlet 'i, fatura bölümlerini belirtilen faturalandırma profilinin altında alır.</span><span class="sxs-lookup"><span data-stu-id="6f6ce-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="6f6ce-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f6ce-109">EXAMPLES</span></span>

### <span data-ttu-id="6f6ce-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6f6ce-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="6f6ce-111">Belirtilen fatura profilinin altındaki tüm fatura bölümlerini alın.</span><span class="sxs-lookup"><span data-stu-id="6f6ce-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="6f6ce-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6f6ce-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="6f6ce-113">Belirtilen ada sahip fatura bölümünü alın.</span><span class="sxs-lookup"><span data-stu-id="6f6ce-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="6f6ce-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f6ce-114">PARAMETERS</span></span>

### <span data-ttu-id="6f6ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f6ce-115">-DefaultProfile</span></span>
<span data-ttu-id="6f6ce-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6f6ce-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f6ce-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="6f6ce-117">-BillingAccountName</span></span>
<span data-ttu-id="6f6ce-118">Belirli bir faturalandırma hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="6f6ce-118">Name of the specific billing account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6ce-119">-Billingprodosyaadı</span><span class="sxs-lookup"><span data-stu-id="6f6ce-119">-BillingProfileName</span></span>
<span data-ttu-id="6f6ce-120">Belirli bir faturalandırma profilinin adı.</span><span class="sxs-lookup"><span data-stu-id="6f6ce-120">Name of the specific billing profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6ce-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="6f6ce-121">-Name</span></span>
<span data-ttu-id="6f6ce-122">Belirli bir fatura bölümünün adı.</span><span class="sxs-lookup"><span data-stu-id="6f6ce-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="6f6ce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f6ce-123">CommonParameters</span></span>
<span data-ttu-id="6f6ce-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f6ce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f6ce-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f6ce-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f6ce-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f6ce-126">INPUTS</span></span>

### <span data-ttu-id="6f6ce-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6f6ce-127">None</span></span>

## <span data-ttu-id="6f6ce-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f6ce-128">OUTPUTS</span></span>

### <span data-ttu-id="6f6ce-129">Microsoft. Azure. Commands. faturalandırma. modeller. Psınvoicesection</span><span class="sxs-lookup"><span data-stu-id="6f6ce-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="6f6ce-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f6ce-130">NOTES</span></span>

## <span data-ttu-id="6f6ce-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f6ce-131">RELATED LINKS</span></span>
