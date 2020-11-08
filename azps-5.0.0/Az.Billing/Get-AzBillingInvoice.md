---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 2392b3275feeb6fa23f8f76dd3e76b6d97c33d46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278429"
---
# <span data-ttu-id="e0f18-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="e0f18-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="e0f18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0f18-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f18-103">Aboneliğin fatura faturalarını alma.</span><span class="sxs-lookup"><span data-stu-id="e0f18-103">Get billing invoices of the subscription.</span></span>
<span data-ttu-id="e0f18-104">Faturalandırma hesabı ve faturalandırma profilinin fatura faturalarını alma</span><span class="sxs-lookup"><span data-stu-id="e0f18-104">Get billing invoices of a billing account and billing profile</span></span>

## <span data-ttu-id="e0f18-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0f18-105">SYNTAX</span></span>

### <span data-ttu-id="e0f18-106">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e0f18-106">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### <span data-ttu-id="e0f18-107">Sürümü</span><span class="sxs-lookup"><span data-stu-id="e0f18-107">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### <span data-ttu-id="e0f18-108">Başına</span><span class="sxs-lookup"><span data-stu-id="e0f18-108">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0f18-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0f18-109">DESCRIPTION</span></span>
<span data-ttu-id="e0f18-110">**Get-Azbillingınvoice** cmdlet 'inin fatura faturalarını alır.</span><span class="sxs-lookup"><span data-stu-id="e0f18-110">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="e0f18-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0f18-111">EXAMPLES</span></span>

### <span data-ttu-id="e0f18-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e0f18-112">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="e0f18-113">Aboneliğin en son faturasını edinin.</span><span class="sxs-lookup"><span data-stu-id="e0f18-113">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="e0f18-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e0f18-114">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="e0f18-115">Belirtilen ada sahip aboneliğin faturasını alın.</span><span class="sxs-lookup"><span data-stu-id="e0f18-115">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="e0f18-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="e0f18-116">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="e0f18-117">Aboneliğin tüm kullanılabilir faturalarını, indirme URL 'Si olmadan en son faturayla başlayan ters kronolojik sırada alın.</span><span class="sxs-lookup"><span data-stu-id="e0f18-117">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="e0f18-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="e0f18-118">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="e0f18-119">Aboneliğin en son 10 faturalarını alın ve indirme URL 'sini sonuç olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e0f18-119">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

### <span data-ttu-id="e0f18-120">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="e0f18-120">Example 5</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

<span data-ttu-id="e0f18-121">Belirli faturayı ada göre alın ve sonucu indirme URL 'sini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e0f18-121">Get the specific invoice by name and include download url in the result.</span></span>

### <span data-ttu-id="e0f18-122">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="e0f18-122">Example 6</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="e0f18-123">Fatura hesap adına göre faturaları alın ve sonuca her faturada indirme URL 'sini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e0f18-123">Get invoices by billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="e0f18-124">Örnek 7</span><span class="sxs-lookup"><span data-stu-id="e0f18-124">Example 7</span></span>
```
PS C:\> Get-AzBillingInvoice Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="e0f18-125">Fatura adına ve fatura hesap adına göre belirli faturaları alın ve sonuca her faturada indirme URL 'sini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e0f18-125">Get specific invoice by invoice name and billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="e0f18-126">Örnek 8</span><span class="sxs-lookup"><span data-stu-id="e0f18-126">Example 8</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="e0f18-127">Fatura hesap adına göre en son faturalamayı alın ve sonuca fatura için indirme URL 'sini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e0f18-127">Get latest invoice by billing account name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="e0f18-128">Örnek 9</span><span class="sxs-lookup"><span data-stu-id="e0f18-128">Example 9</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

<span data-ttu-id="e0f18-129">Belirli bir faturalandırma hesabının ve belirli bir faturalandırma profilinin en son 10 faturalarını alın ve yükleme URL 'sini de ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e0f18-129">Get most recent 10 invoices of the specific billing account and specific billing profile and include the download Url in the result.</span></span>

### <span data-ttu-id="e0f18-130">Örnek 10</span><span class="sxs-lookup"><span data-stu-id="e0f18-130">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

<span data-ttu-id="e0f18-131">Fatura hesap adına ve fatura profili adına göre en son faturalamayı alın ve faturaya yükleme URL 'sini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e0f18-131">Get latest invoice by billing account name and billing profile name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="e0f18-132">Örnek 10</span><span class="sxs-lookup"><span data-stu-id="e0f18-132">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

<span data-ttu-id="e0f18-133">PerioStart Date ve periodEnd Date ile belirtilen bir faturalandırma dönemi için fatura hesap adına ve fatura profili adına göre faturaları alın.</span><span class="sxs-lookup"><span data-stu-id="e0f18-133">Get invoices by billing account name and billing profile name for a billing period specified by perioStart date and periodEnd date.</span></span>


## <span data-ttu-id="e0f18-134">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0f18-134">PARAMETERS</span></span>

### <span data-ttu-id="e0f18-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f18-135">-DefaultProfile</span></span>
<span data-ttu-id="e0f18-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e0f18-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0f18-137">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="e0f18-137">-GenerateDownloadUrl</span></span>
<span data-ttu-id="e0f18-138">Faturaların indirme URL 'sini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e0f18-138">Generate the download url of the invoices.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f18-139">-En son</span><span class="sxs-lookup"><span data-stu-id="e0f18-139">-Latest</span></span>
<span data-ttu-id="e0f18-140">En son faturayı edinin.</span><span class="sxs-lookup"><span data-stu-id="e0f18-140">Get the latest invoice.</span></span>

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

### <span data-ttu-id="e0f18-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e0f18-141">-MaxCount</span></span>
<span data-ttu-id="e0f18-142">Döndürülecek en fazla kayıt sayısını belirler.</span><span class="sxs-lookup"><span data-stu-id="e0f18-142">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="e0f18-143">-Ad</span><span class="sxs-lookup"><span data-stu-id="e0f18-143">-Name</span></span>
<span data-ttu-id="e0f18-144">Bir veya en son belirtilmemişse, belirli bir faturanın adı.</span><span class="sxs-lookup"><span data-stu-id="e0f18-144">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="e0f18-145">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="e0f18-145">-BillingAccountName</span></span>
<span data-ttu-id="e0f18-146">Faturaların alınacağı belirli bir faturalandırma hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="e0f18-146">Name of a specific billing account to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f18-147">-Billingprodosyaadı</span><span class="sxs-lookup"><span data-stu-id="e0f18-147">-BillingProfileName</span></span>
<span data-ttu-id="e0f18-148">Faturaların alınacağı belirli bir faturalandırma profilinin adı.</span><span class="sxs-lookup"><span data-stu-id="e0f18-148">Name of a specific billing profile to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f18-149">-PeriodStartDate</span><span class="sxs-lookup"><span data-stu-id="e0f18-149">-PeriodStartDate</span></span>
<span data-ttu-id="e0f18-150">Fatura için başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="e0f18-150">Start date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f18-151">-PeriodEndDate</span><span class="sxs-lookup"><span data-stu-id="e0f18-151">-PeriodEndDate</span></span>
<span data-ttu-id="e0f18-152">Fatura için bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="e0f18-152">End date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```



### <span data-ttu-id="e0f18-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f18-153">CommonParameters</span></span>
<span data-ttu-id="e0f18-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0f18-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f18-155">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0f18-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f18-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0f18-156">INPUTS</span></span>

### <span data-ttu-id="e0f18-157">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e0f18-157">None</span></span>

## <span data-ttu-id="e0f18-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0f18-158">OUTPUTS</span></span>

### <span data-ttu-id="e0f18-159">Microsoft. Azure. Commands. faturalandırma. modeller. Psınvoice</span><span class="sxs-lookup"><span data-stu-id="e0f18-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="e0f18-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0f18-160">NOTES</span></span>

## <span data-ttu-id="e0f18-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0f18-161">RELATED LINKS</span></span>
