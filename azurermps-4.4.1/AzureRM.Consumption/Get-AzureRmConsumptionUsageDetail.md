---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
ms.openlocfilehash: f8347fca355080f11e69bae9793cc0367325ce98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764889"
---
# <span data-ttu-id="89fda-101">Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="89fda-101">Get-AzureRmConsumptionUsageDetail</span></span>

## <span data-ttu-id="89fda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89fda-102">SYNOPSIS</span></span>
<span data-ttu-id="89fda-103">Aboneliğin kullanım ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="89fda-103">Get usage details of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89fda-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89fda-104">SYNTAX</span></span>

### <span data-ttu-id="89fda-105">Abonelik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="89fda-105">Subscription (Default)</span></span>
```
Get-AzureRmConsumptionUsageDetail [-MaxCount <Int32>] [-IncludeMeterDetails] [-IncludeAdditionalProperties]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89fda-106">Faturasına</span><span class="sxs-lookup"><span data-stu-id="89fda-106">Invoice</span></span>
```
Get-AzureRmConsumptionUsageDetail -InvoiceName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89fda-107">Billingdönem</span><span class="sxs-lookup"><span data-stu-id="89fda-107">BillingPeriod</span></span>
```
Get-AzureRmConsumptionUsageDetail -BillingPeriodName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89fda-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="89fda-108">DESCRIPTION</span></span>
<span data-ttu-id="89fda-109">**Get-Azurermtüketimptionusagedetail** cmdlet 'inin kullanım ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="89fda-109">The **Get-AzureRmConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="89fda-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89fda-110">EXAMPLES</span></span>

### <span data-ttu-id="89fda-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="89fda-111">Example 1</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeMeterDetails -InvoiceName 201704-117283130069214
```

<span data-ttu-id="89fda-112">Belirtilen adla faturanın kullanım ayrıntılarını edinin ve MeterDetails özelliğini sonuca ekleyin.</span><span class="sxs-lookup"><span data-stu-id="89fda-112">Get usage details of the invoice with specified name, and include MeterDetails property in the result.</span></span>

### <span data-ttu-id="89fda-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="89fda-113">Example 2</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeAdditionalProperties -BillingPeriodName 201704-1
```

<span data-ttu-id="89fda-114">Belirtilen adla faturalandırma döneminin kullanım ayrıntılarını edinin ve sonuca AdditionalProperties özelliğini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="89fda-114">Get usage details of the billing period with specified name, and include AdditionalProperties property in the result.</span></span>

### <span data-ttu-id="89fda-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="89fda-115">Example 3</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -StartDate 2017-01-17 -EndDate 2017-01-19
```

<span data-ttu-id="89fda-116">2017-01-17 ile 2017-01-19 arasındaki aboneliğin kullanım ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="89fda-116">Get usage details of the subscription that is between 2017-01-17 to 2017-01-19.</span></span>

## <span data-ttu-id="89fda-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89fda-117">PARAMETERS</span></span>

### <span data-ttu-id="89fda-118">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="89fda-118">-BillingPeriodName</span></span>
<span data-ttu-id="89fda-119">İlgili kullanım ayrıntılarının alınacağı belirli bir fatura döneminin adı.</span><span class="sxs-lookup"><span data-stu-id="89fda-119">Name of a specific billing period to get the usage details that associate with.</span></span>

```yaml
Type: System.String
Parameter Sets: BillingPeriod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89fda-120">-EndDate</span><span class="sxs-lookup"><span data-stu-id="89fda-120">-EndDate</span></span>
<span data-ttu-id="89fda-121">Kullanımlarının bitiş tarihi (UTC).</span><span class="sxs-lookup"><span data-stu-id="89fda-121">The end date (in UTC) of the usages.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89fda-122">-Includeadditionalproperties</span><span class="sxs-lookup"><span data-stu-id="89fda-122">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="89fda-123">Özelliklere ek özellikler ekleyin.</span><span class="sxs-lookup"><span data-stu-id="89fda-123">Include additional properties in the usages.</span></span>

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

### <span data-ttu-id="89fda-124">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="89fda-124">-IncludeMeterDetails</span></span>
<span data-ttu-id="89fda-125">Kullanım için ölçüm ayrıntılarını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="89fda-125">Include meter details in the usages.</span></span>

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

### <span data-ttu-id="89fda-126">-Faturaadı</span><span class="sxs-lookup"><span data-stu-id="89fda-126">-InvoiceName</span></span>
<span data-ttu-id="89fda-127">İlgili kullanım ayrıntılarını almak için belirli bir faturanın adı.</span><span class="sxs-lookup"><span data-stu-id="89fda-127">Name of a specific invoice to get the usage details that associate with.</span></span>

```yaml
Type: System.String
Parameter Sets: Invoice
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89fda-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="89fda-128">-MaxCount</span></span>
<span data-ttu-id="89fda-129">Döndürülecek en fazla kayıt sayısını belirleme.</span><span class="sxs-lookup"><span data-stu-id="89fda-129">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89fda-130">-StartDate</span><span class="sxs-lookup"><span data-stu-id="89fda-130">-StartDate</span></span>
<span data-ttu-id="89fda-131">Kullanımlarının başlangıç tarihi (UTC).</span><span class="sxs-lookup"><span data-stu-id="89fda-131">The start date (in UTC) of the usages.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89fda-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89fda-132">-DefaultProfile</span></span>
<span data-ttu-id="89fda-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89fda-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89fda-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89fda-134">CommonParameters</span></span>
<span data-ttu-id="89fda-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89fda-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89fda-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89fda-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89fda-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89fda-137">INPUTS</span></span>

### <span data-ttu-id="89fda-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="89fda-138">None</span></span>

## <span data-ttu-id="89fda-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89fda-139">OUTPUTS</span></span>

### <span data-ttu-id="89fda-140">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. tüketim. modeller. PSUsageDetail, Microsoft. Azure. Commands. tüketim, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="89fda-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail, Microsoft.Azure.Commands.Consumption, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="89fda-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89fda-141">NOTES</span></span>

## <span data-ttu-id="89fda-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89fda-142">RELATED LINKS</span></span>

