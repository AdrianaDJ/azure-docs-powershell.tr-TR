---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
ms.openlocfilehash: 2694ce516b1bb3202fc194e1c1eec55610f7b92a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586756"
---
# <span data-ttu-id="585ab-101">Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="585ab-101">Get-AzureRmConsumptionUsageDetail</span></span>

## <span data-ttu-id="585ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="585ab-102">SYNOPSIS</span></span>
<span data-ttu-id="585ab-103">Aboneliğin kullanım ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="585ab-103">Get usage details of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="585ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="585ab-104">SYNTAX</span></span>

### <span data-ttu-id="585ab-105">Abonelik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="585ab-105">Subscription (Default)</span></span>
```
Get-AzureRmConsumptionUsageDetail [-MaxCount <Int32>] [-IncludeMeterDetails] [-IncludeAdditionalProperties]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="585ab-106">Faturasına</span><span class="sxs-lookup"><span data-stu-id="585ab-106">Invoice</span></span>
```
Get-AzureRmConsumptionUsageDetail -InvoiceName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="585ab-107">Billingdönem</span><span class="sxs-lookup"><span data-stu-id="585ab-107">BillingPeriod</span></span>
```
Get-AzureRmConsumptionUsageDetail -BillingPeriodName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="585ab-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="585ab-108">DESCRIPTION</span></span>
<span data-ttu-id="585ab-109">**Get-Azurermtüketimptionusagedetail** cmdlet 'inin kullanım ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="585ab-109">The **Get-AzureRmConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="585ab-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="585ab-110">EXAMPLES</span></span>

### <span data-ttu-id="585ab-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="585ab-111">Example 1</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeMeterDetails -InvoiceName 201704-117283130069214
```

<span data-ttu-id="585ab-112">Belirtilen adla faturanın kullanım ayrıntılarını edinin ve MeterDetails özelliğini sonuca ekleyin.</span><span class="sxs-lookup"><span data-stu-id="585ab-112">Get usage details of the invoice with specified name, and include MeterDetails property in the result.</span></span>

### <span data-ttu-id="585ab-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="585ab-113">Example 2</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeAdditionalProperties -BillingPeriodName 201704-1
```

<span data-ttu-id="585ab-114">Belirtilen adla faturalandırma döneminin kullanım ayrıntılarını edinin ve sonuca AdditionalProperties özelliğini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="585ab-114">Get usage details of the billing period with specified name, and include AdditionalProperties property in the result.</span></span>

### <span data-ttu-id="585ab-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="585ab-115">Example 3</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -StartDate 2017-01-17 -EndDate 2017-01-19
```

<span data-ttu-id="585ab-116">2017-01-17 ile 2017-01-19 arasındaki aboneliğin kullanım ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="585ab-116">Get usage details of the subscription that is between 2017-01-17 to 2017-01-19.</span></span>

## <span data-ttu-id="585ab-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="585ab-117">PARAMETERS</span></span>

### <span data-ttu-id="585ab-118">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="585ab-118">-BillingPeriodName</span></span>
<span data-ttu-id="585ab-119">İlgili kullanım ayrıntılarının alınacağı belirli bir fatura döneminin adı.</span><span class="sxs-lookup"><span data-stu-id="585ab-119">Name of a specific billing period to get the usage details that associate with.</span></span>

```yaml
Type: String
Parameter Sets: BillingPeriod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585ab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="585ab-120">-DefaultProfile</span></span>
<span data-ttu-id="585ab-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="585ab-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="585ab-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="585ab-122">-EndDate</span></span>
<span data-ttu-id="585ab-123">Kullanımlarının bitiş tarihi (UTC).</span><span class="sxs-lookup"><span data-stu-id="585ab-123">The end date (in UTC) of the usages.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585ab-124">-Includeadditionalproperties</span><span class="sxs-lookup"><span data-stu-id="585ab-124">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="585ab-125">Özelliklere ek özellikler ekleyin.</span><span class="sxs-lookup"><span data-stu-id="585ab-125">Include additional properties in the usages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585ab-126">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="585ab-126">-IncludeMeterDetails</span></span>
<span data-ttu-id="585ab-127">Kullanım için ölçüm ayrıntılarını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="585ab-127">Include meter details in the usages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585ab-128">-Faturaadı</span><span class="sxs-lookup"><span data-stu-id="585ab-128">-InvoiceName</span></span>
<span data-ttu-id="585ab-129">İlgili kullanım ayrıntılarını almak için belirli bir faturanın adı.</span><span class="sxs-lookup"><span data-stu-id="585ab-129">Name of a specific invoice to get the usage details that associate with.</span></span>

```yaml
Type: String
Parameter Sets: Invoice
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585ab-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="585ab-130">-MaxCount</span></span>
<span data-ttu-id="585ab-131">Döndürülecek en fazla kayıt sayısını belirleme.</span><span class="sxs-lookup"><span data-stu-id="585ab-131">Determine the maximum number of records to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585ab-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="585ab-132">-StartDate</span></span>
<span data-ttu-id="585ab-133">Kullanımlarının başlangıç tarihi (UTC).</span><span class="sxs-lookup"><span data-stu-id="585ab-133">The start date (in UTC) of the usages.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585ab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="585ab-134">CommonParameters</span></span>
<span data-ttu-id="585ab-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="585ab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="585ab-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="585ab-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="585ab-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="585ab-137">INPUTS</span></span>

### <span data-ttu-id="585ab-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="585ab-138">None</span></span>

## <span data-ttu-id="585ab-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="585ab-139">OUTPUTS</span></span>

### <span data-ttu-id="585ab-140">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. tüketim. modeller. PSUsageDetail, Microsoft. Azure. Commands. tüketim, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="585ab-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail, Microsoft.Azure.Commands.Consumption, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="585ab-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="585ab-141">NOTES</span></span>

## <span data-ttu-id="585ab-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="585ab-142">RELATED LINKS</span></span>

