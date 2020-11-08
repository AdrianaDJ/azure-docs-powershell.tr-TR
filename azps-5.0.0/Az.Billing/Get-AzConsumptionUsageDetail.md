---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionUsageDetail.md
ms.openlocfilehash: 8eeee753fda32f40dfabf156b352724b0bd87b92
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278421"
---
# <span data-ttu-id="fb735-101">Get-AzConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="fb735-101">Get-AzConsumptionUsageDetail</span></span>

## <span data-ttu-id="fb735-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb735-102">SYNOPSIS</span></span>
<span data-ttu-id="fb735-103">Aboneliğin kullanım ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="fb735-103">Get usage details of the subscription.</span></span>

## <span data-ttu-id="fb735-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb735-104">SYNTAX</span></span>

```
Get-AzConsumptionUsageDetail [-BillingPeriodName <String>] [-Expand <String>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>] [-ResourceGroup <String>]
 [-InstanceName <String>] [-InstanceId <String>] [-Tag <String>] [-MaxCount <Int32>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb735-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb735-105">DESCRIPTION</span></span>
<span data-ttu-id="fb735-106">**Get-Aztüketimptionusagedetail** cmdlet 'inin kullanım ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="fb735-106">The **Get-AzConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="fb735-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb735-107">EXAMPLES</span></span>

### <span data-ttu-id="fb735-108">Örnek 1: MeterDetails ile kullanım ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="fb735-108">Example 1: Get usage details with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -Expand MeterDetails -Top 10
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

### <span data-ttu-id="fb735-109">Örnek 2: tarih aralığıyla kullanım ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="fb735-109">Example 2: Get usage details with date range</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -StartDate 2017-10-02 -EndDate 2017-10-05 -Top 10
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

### <span data-ttu-id="fb735-110">Örnek 3: BillingPeriodName ile</span><span class="sxs-lookup"><span data-stu-id="fb735-110">Example 3: Get usage details of BillingPeriodName with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -BillingPeriodName 201710 -InstanceName 1c2052westus -Top 10
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

## <span data-ttu-id="fb735-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb735-111">PARAMETERS</span></span>

### <span data-ttu-id="fb735-112">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="fb735-112">-BillingPeriodName</span></span>
<span data-ttu-id="fb735-113">İlgili kullanım ayrıntılarının alınacağı belirli bir fatura döneminin adı.</span><span class="sxs-lookup"><span data-stu-id="fb735-113">Name of a specific billing period to get the usage details that associate with.</span></span>

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

### <span data-ttu-id="fb735-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb735-114">-DefaultProfile</span></span>
<span data-ttu-id="fb735-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb735-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb735-116">-EndDate</span><span class="sxs-lookup"><span data-stu-id="fb735-116">-EndDate</span></span>
<span data-ttu-id="fb735-117">Filtre uygulanacak kullanımlarının bitiş tarihi (UTC).</span><span class="sxs-lookup"><span data-stu-id="fb735-117">The end date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="fb735-118">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="fb735-118">-Expand</span></span>
<span data-ttu-id="fb735-119">MeterDetails veya AdditionalInfo tabanlı kullanımları genişletin.</span><span class="sxs-lookup"><span data-stu-id="fb735-119">Expand the usages based on MeterDetails, or AdditionalInfo.</span></span>

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

### <span data-ttu-id="fb735-120">-Includeadditionalproperties</span><span class="sxs-lookup"><span data-stu-id="fb735-120">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="fb735-121">Özelliklere ek özellikler ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fb735-121">Include additional properties in the usages.</span></span>

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

### <span data-ttu-id="fb735-122">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="fb735-122">-IncludeMeterDetails</span></span>
<span data-ttu-id="fb735-123">Kullanım için ölçüm ayrıntılarını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fb735-123">Include meter details in the usages.</span></span>

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

### <span data-ttu-id="fb735-124">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="fb735-124">-InstanceId</span></span>
<span data-ttu-id="fb735-125">Filtre uygulanacak kullanımlarının örnek kimliği.</span><span class="sxs-lookup"><span data-stu-id="fb735-125">The instance id of the usages to filter.</span></span>

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

### <span data-ttu-id="fb735-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="fb735-126">-InstanceName</span></span>
<span data-ttu-id="fb735-127">Filtre uygulanacak kullanımlarının örnek adı.</span><span class="sxs-lookup"><span data-stu-id="fb735-127">The instance name of the usages to filter.</span></span>

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

### <span data-ttu-id="fb735-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fb735-128">-MaxCount</span></span>
<span data-ttu-id="fb735-129">Döndürülecek en fazla kayıt sayısını belirleme.</span><span class="sxs-lookup"><span data-stu-id="fb735-129">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="fb735-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fb735-130">-ResourceGroup</span></span>
<span data-ttu-id="fb735-131">Filtre uygulanacak kullanımlarının kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="fb735-131">The resource group of the usages to filter.</span></span>

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

### <span data-ttu-id="fb735-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="fb735-132">-StartDate</span></span>
<span data-ttu-id="fb735-133">Filtre uygulanacak kullanımlarının başlangıç tarihi (UTC).</span><span class="sxs-lookup"><span data-stu-id="fb735-133">The start date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="fb735-134">Etiketli</span><span class="sxs-lookup"><span data-stu-id="fb735-134">-Tag</span></span>
<span data-ttu-id="fb735-135">Filtre uygulama kullanımlarının etiketi.</span><span class="sxs-lookup"><span data-stu-id="fb735-135">The tag of the usages to filter.</span></span>

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

### <span data-ttu-id="fb735-136">-Üst</span><span class="sxs-lookup"><span data-stu-id="fb735-136">-Top</span></span>
<span data-ttu-id="fb735-137">Döndürülecek en fazla kayıt sayısını belirleme.</span><span class="sxs-lookup"><span data-stu-id="fb735-137">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="fb735-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb735-138">CommonParameters</span></span>
<span data-ttu-id="fb735-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb735-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb735-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb735-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb735-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb735-141">INPUTS</span></span>

### <span data-ttu-id="fb735-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fb735-142">None</span></span>

## <span data-ttu-id="fb735-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb735-143">OUTPUTS</span></span>

### <span data-ttu-id="fb735-144">Microsoft. Azure. Commands. tüketim. modeller. PSUsageDetail</span><span class="sxs-lookup"><span data-stu-id="fb735-144">Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail</span></span>

## <span data-ttu-id="fb735-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb735-145">NOTES</span></span>

## <span data-ttu-id="fb735-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb735-146">RELATED LINKS</span></span>
