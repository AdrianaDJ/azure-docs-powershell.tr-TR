---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
ms.openlocfilehash: 92e132d6ef35d4a085abc2d1bc80ec4ab433036a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593287"
---
# <span data-ttu-id="96efe-101">Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="96efe-101">Get-AzureRmConsumptionUsageDetail</span></span>

## <span data-ttu-id="96efe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96efe-102">SYNOPSIS</span></span>
<span data-ttu-id="96efe-103">Aboneliğin kullanım ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="96efe-103">Get usage details of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96efe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96efe-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionUsageDetail [-BillingPeriodName <String>] [-Expand <String>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>] [-ResourceGroup <String>]
 [-InstanceName <String>] [-InstanceId <String>] [-Tag <String>] [-MaxCount <Int32>] [-Top <Int32>]
 [-InvoiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96efe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="96efe-105">DESCRIPTION</span></span>
<span data-ttu-id="96efe-106">**Get-Azurermtüketimptionusagedetail** cmdlet 'inin kullanım ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="96efe-106">The **Get-AzureRmConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="96efe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96efe-107">EXAMPLES</span></span>

### <span data-ttu-id="96efe-108">Örnek 1: MeterDetails ile kullanım ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="96efe-108">Example 1: Get usage details with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionUsageDetail -Expand MeterDetails -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
ConsumedService:  Microsoft.Compute
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/usageDetails/24b9dff0-f022-55a1-886b-17b330000db3
InstanceId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/MAR-CCM/providers/Microsoft.Compute/disks/mar-ccm-vm01_OsDisk_1_d0beead4b6ff4b4088a687701d355d61
InstanceLocation:  usnorthcentral
InstanceName:  mar-ccm-vm01_OsDisk_1_d0beead4b6ff4b4088a687701d355d61
IsEstimated:  true
MeterDetails:  MeterCategory:  Data Management
               MeterLocation:  usnorthcentral
               MeterName:  Standard Managed Disk Operations (in 10,000s)
               MeterSubCategory:  Data Management
               Unit:  Operations
MeterId:  82cd70ab-1aee-4b30-bc04-8b71e1204dbc
Name:  24b9dff0-f022-55a1-886b-17b330000db3
PretaxCost:  0
Product:  Data Management Standard Managed Disk Operations
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  6/1/2018 11:59:59 PM
UsageQuantity:  3.8218
UsageStart:  6/1/2018 12:00:00 AM
```

### <span data-ttu-id="96efe-109">Örnek 2: tarih aralığıyla kullanım ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="96efe-109">Example 2: Get usage details with date range</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionUsageDetail -StartDate 2017-10-02 -EndDate 2017-10-05 -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001
ConsumedService:  Storage
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001/providers/Microsoft.Consumption/usageDetails/732582e5-40ad-bb23-7a69-ca1ff7c8b004
InstanceId:  storsimplezc9q6r2t7f
InstanceLocation:  US West Central
InstanceName:  storsimplezc9q6r2t7f
IsEstimated:  false
MeterId:  ad22fac8-9da5-4577-8683-56ae94d39e42
Name:  732582e5-40ad-bb23-7a69-ca1ff7c8b004
PretaxCost:  0
Product:  Data Management Geo Redundant Standard IO - Table Write
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  10/2/2017 11:59:59 PM
UsageQuantity:  0.0006
UsageStart:  10/2/2017 12:00:00 AM
```

### <span data-ttu-id="96efe-110">Örnek 3: BillingPeriodName ile</span><span class="sxs-lookup"><span data-stu-id="96efe-110">Example 3: Get usage details of BillingPeriodName with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionUsageDetail -BillingPeriodName 201710 -InstanceName 1c2052westus -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001
ConsumedService:  Microsoft.Storage
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001/providers/Microsoft.Consumption/usageDetails/8abc8b65-e8f1-31e1-f02b-058a7572363f
InstanceId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/securitydata/providers/Microsoft.Storage/storageAccounts/1c2052westus
InstanceLocation:  uswest
InstanceName:  1c2052westus
IsEstimated:  false
MeterId:  9995d93a-7d35-4d3f-9c69-7a7fea447ef4
Name:  8abc8b65-e8f1-31e1-f02b-058a7572363f
PretaxCost:  0.000000693016692
Product:  Data Transfer Out - Zone 1
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  10/1/2017 11:59:59 PM
UsageQuantity:  0.000009
UsageStart:  10/1/2017 12:00:00 AM
```

## <span data-ttu-id="96efe-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96efe-111">PARAMETERS</span></span>

### <span data-ttu-id="96efe-112">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="96efe-112">-BillingPeriodName</span></span>
<span data-ttu-id="96efe-113">İlgili kullanım ayrıntılarının alınacağı belirli bir fatura döneminin adı.</span><span class="sxs-lookup"><span data-stu-id="96efe-113">Name of a specific billing period to get the usage details that associate with.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96efe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96efe-114">-DefaultProfile</span></span>
<span data-ttu-id="96efe-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="96efe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96efe-116">-EndDate</span><span class="sxs-lookup"><span data-stu-id="96efe-116">-EndDate</span></span>
<span data-ttu-id="96efe-117">Filtre uygulanacak kullanımlarının bitiş tarihi (UTC).</span><span class="sxs-lookup"><span data-stu-id="96efe-117">The end date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="96efe-118">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="96efe-118">-Expand</span></span>
<span data-ttu-id="96efe-119">MeterDetails veya AdditionalInfo tabanlı kullanımları genişletin.</span><span class="sxs-lookup"><span data-stu-id="96efe-119">Expand the usages based on MeterDetails, or AdditionalInfo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96efe-120">-Includeadditionalproperties</span><span class="sxs-lookup"><span data-stu-id="96efe-120">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="96efe-121">Özelliklere ek özellikler ekleyin.</span><span class="sxs-lookup"><span data-stu-id="96efe-121">Include additional properties in the usages.</span></span>

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

### <span data-ttu-id="96efe-122">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="96efe-122">-IncludeMeterDetails</span></span>
<span data-ttu-id="96efe-123">Kullanım için ölçüm ayrıntılarını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="96efe-123">Include meter details in the usages.</span></span>

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

### <span data-ttu-id="96efe-124">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="96efe-124">-InstanceId</span></span>
<span data-ttu-id="96efe-125">Filtre uygulanacak kullanımlarının örnek kimliği.</span><span class="sxs-lookup"><span data-stu-id="96efe-125">The instance id of the usages to filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96efe-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="96efe-126">-InstanceName</span></span>
<span data-ttu-id="96efe-127">Filtre uygulanacak kullanımlarının örnek adı.</span><span class="sxs-lookup"><span data-stu-id="96efe-127">The instance name of the usages to filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96efe-128">-Faturaadı</span><span class="sxs-lookup"><span data-stu-id="96efe-128">-InvoiceName</span></span>
<span data-ttu-id="96efe-129">İlgili kullanım ayrıntılarını almak için belirli bir faturanın adı.</span><span class="sxs-lookup"><span data-stu-id="96efe-129">Name of a specific invoice to get the usage details that associate with.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96efe-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="96efe-130">-MaxCount</span></span>
<span data-ttu-id="96efe-131">Döndürülecek en fazla kayıt sayısını belirleme.</span><span class="sxs-lookup"><span data-stu-id="96efe-131">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="96efe-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="96efe-132">-ResourceGroup</span></span>
<span data-ttu-id="96efe-133">Filtre uygulanacak kullanımlarının kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="96efe-133">The resource group of the usages to filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96efe-134">-StartDate</span><span class="sxs-lookup"><span data-stu-id="96efe-134">-StartDate</span></span>
<span data-ttu-id="96efe-135">Filtre uygulanacak kullanımlarının başlangıç tarihi (UTC).</span><span class="sxs-lookup"><span data-stu-id="96efe-135">The start date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="96efe-136">Etiketli</span><span class="sxs-lookup"><span data-stu-id="96efe-136">-Tag</span></span>
<span data-ttu-id="96efe-137">Filtre uygulama kullanımlarının etiketi.</span><span class="sxs-lookup"><span data-stu-id="96efe-137">The tag of the usages to filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96efe-138">-Üst</span><span class="sxs-lookup"><span data-stu-id="96efe-138">-Top</span></span>
<span data-ttu-id="96efe-139">Döndürülecek en fazla kayıt sayısını belirleme.</span><span class="sxs-lookup"><span data-stu-id="96efe-139">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="96efe-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96efe-140">CommonParameters</span></span>
<span data-ttu-id="96efe-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96efe-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96efe-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96efe-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96efe-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96efe-143">INPUTS</span></span>

### <span data-ttu-id="96efe-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="96efe-144">None</span></span>

## <span data-ttu-id="96efe-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96efe-145">OUTPUTS</span></span>

### <span data-ttu-id="96efe-146">Microsoft. Azure. Commands. tüketim. modeller. PSUsageDetail</span><span class="sxs-lookup"><span data-stu-id="96efe-146">Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail</span></span>

## <span data-ttu-id="96efe-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96efe-147">NOTES</span></span>

## <span data-ttu-id="96efe-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96efe-148">RELATED LINKS</span></span>
