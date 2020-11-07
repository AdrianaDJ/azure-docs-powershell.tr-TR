---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/new-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
ms.openlocfilehash: 45e41da30d90041c1e8670ebe8e356688785e355
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753131"
---
# <span data-ttu-id="3651e-101">New-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="3651e-101">New-AzConsumptionBudget</span></span>

## <span data-ttu-id="3651e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3651e-102">SYNOPSIS</span></span>
<span data-ttu-id="3651e-103">Bir abonelikte veya bir kaynak grubunda bütçe oluşturma.</span><span class="sxs-lookup"><span data-stu-id="3651e-103">Create a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="3651e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3651e-104">SYNTAX</span></span>

### <span data-ttu-id="3651e-105">Abonelik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3651e-105">Subscription (Default)</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3651e-106">Bilgilendirme</span><span class="sxs-lookup"><span data-stu-id="3651e-106">Notification</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3651e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3651e-107">DESCRIPTION</span></span>
<span data-ttu-id="3651e-108">New-AzConsumptionBudget cmdlet 'i bir abonelikte veya kaynak grubunda bütçe oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3651e-108">The New-AzConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="3651e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3651e-109">EXAMPLES</span></span>

### <span data-ttu-id="3651e-110">Örnek 1: abonelik düzeyinde bütçe adıyla bir maliyet bütçesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="3651e-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -Amount 60 -Name PSBudget -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="3651e-111">Örnek 2: kaynak grup düzeyinde bütçe adıyla bir maliyet bütçesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="3651e-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -ResourceGroupName RGBudgets -Amount 60 -Name PSBudgetRG -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="3651e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3651e-112">PARAMETERS</span></span>

### <span data-ttu-id="3651e-113">-Tutar</span><span class="sxs-lookup"><span data-stu-id="3651e-113">-Amount</span></span>
<span data-ttu-id="3651e-114">Bütçe miktarı.</span><span class="sxs-lookup"><span data-stu-id="3651e-114">Amount of a budget.</span></span>

```yaml
Type: System.Decimal
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3651e-115">-Kategori</span><span class="sxs-lookup"><span data-stu-id="3651e-115">-Category</span></span>
<span data-ttu-id="3651e-116">Bütçenin kategorisi maliyet veya kullanım olabilir.</span><span class="sxs-lookup"><span data-stu-id="3651e-116">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3651e-117">-Posta</span><span class="sxs-lookup"><span data-stu-id="3651e-117">-ContactEmail</span></span>
<span data-ttu-id="3651e-118">Eşik aşıldığında bütçe bildirimini göndermek için e-posta adresleri.</span><span class="sxs-lookup"><span data-stu-id="3651e-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3651e-119">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="3651e-119">-ContactGroup</span></span>
<span data-ttu-id="3651e-120">Eşik aşıldığında, bütçe bildirimini gönderecek eylem grupları.</span><span class="sxs-lookup"><span data-stu-id="3651e-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3651e-121">-İlgili kişi</span><span class="sxs-lookup"><span data-stu-id="3651e-121">-ContactRole</span></span>
<span data-ttu-id="3651e-122">Eşik aşıldığında bütçe bildirimini göndermek için ilgili roller.</span><span class="sxs-lookup"><span data-stu-id="3651e-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3651e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3651e-123">-DefaultProfile</span></span>
<span data-ttu-id="3651e-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3651e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3651e-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="3651e-125">-EndDate</span></span>
<span data-ttu-id="3651e-126">Bütçenin bitiş tarihi (UTC olarak YYYY-AA-GG).</span><span class="sxs-lookup"><span data-stu-id="3651e-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="3651e-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="3651e-127">-MeterFilter</span></span>
<span data-ttu-id="3651e-128">Filtrelemek için virgülle ayrılmış metre listesi.</span><span class="sxs-lookup"><span data-stu-id="3651e-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="3651e-129">Kategori kullanım ise gereklidir.</span><span class="sxs-lookup"><span data-stu-id="3651e-129">Required if category is usage.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3651e-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="3651e-130">-Name</span></span>
<span data-ttu-id="3651e-131">Bütçenin adı.</span><span class="sxs-lookup"><span data-stu-id="3651e-131">Name of a budget.</span></span>

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

### <span data-ttu-id="3651e-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="3651e-132">-NotificationEnabled</span></span>
<span data-ttu-id="3651e-133">Bildirim etkin veya değil.</span><span class="sxs-lookup"><span data-stu-id="3651e-133">The notification is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3651e-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="3651e-134">-NotificationKey</span></span>
<span data-ttu-id="3651e-135">Bir bütçeyle ilişkili bildirimin anahtarı, bildirim etkin anahtar, bildirim eşiği, kişi e-postalarına, kişi gruplarıyla veya kişi rolleriyle bildirim oluşturmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="3651e-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3651e-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="3651e-136">-NotificationThreshold</span></span>
<span data-ttu-id="3651e-137">Bildirimle ilişkilendirilmiş eşik değeri.</span><span class="sxs-lookup"><span data-stu-id="3651e-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="3651e-138">Maliyet veya kullanım eşiği aştığı zaman bildirim gönderilir.</span><span class="sxs-lookup"><span data-stu-id="3651e-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="3651e-139">Her zaman yüzde ve 0 ile 1000 arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3651e-139">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3651e-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="3651e-140">-ResourceFilter</span></span>
<span data-ttu-id="3651e-141">Filtre uygulanacak kaynak örneklerinin virgülle ayrılmış listesi.</span><span class="sxs-lookup"><span data-stu-id="3651e-141">Comma-separated list of resource instances to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3651e-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="3651e-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="3651e-143">Filtre uygulanacak kaynak gruplarının virgülle ayrılmış listesi.</span><span class="sxs-lookup"><span data-stu-id="3651e-143">Comma-separated list of resource groups to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3651e-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3651e-144">-ResourceGroupName</span></span>
<span data-ttu-id="3651e-145">Bütçenin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="3651e-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="3651e-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="3651e-146">-StartDate</span></span>
<span data-ttu-id="3651e-147">Bütçenin dönem başlangıç tarihi (UTC olarak).</span><span class="sxs-lookup"><span data-stu-id="3651e-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="3651e-148">Aylık zaman çizgisi için geçerli aydan önce değil.</span><span class="sxs-lookup"><span data-stu-id="3651e-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="3651e-149">Üç aydan önceki üç ay içinde değil.</span><span class="sxs-lookup"><span data-stu-id="3651e-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="3651e-150">Yıllık zaman çizgisi için on iki aydan önce değil.</span><span class="sxs-lookup"><span data-stu-id="3651e-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="3651e-151">Gelecekteki başlangıç tarihi üç aydan uzun olamaz.</span><span class="sxs-lookup"><span data-stu-id="3651e-151">Future start date not more than three months.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3651e-152">-Zaman çizgisi</span><span class="sxs-lookup"><span data-stu-id="3651e-152">-TimeGrain</span></span>
<span data-ttu-id="3651e-153">Bütçenin zaman çizgisi aylık, üç aylık veya yıllık olabilir.</span><span class="sxs-lookup"><span data-stu-id="3651e-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3651e-154">-Onay</span><span class="sxs-lookup"><span data-stu-id="3651e-154">-Confirm</span></span>
<span data-ttu-id="3651e-155">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3651e-155">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3651e-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3651e-156">-WhatIf</span></span>
<span data-ttu-id="3651e-157">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3651e-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3651e-158">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3651e-158">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3651e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3651e-159">CommonParameters</span></span>
<span data-ttu-id="3651e-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3651e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3651e-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3651e-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3651e-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3651e-162">INPUTS</span></span>

### <span data-ttu-id="3651e-163">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3651e-163">None</span></span>

## <span data-ttu-id="3651e-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3651e-164">OUTPUTS</span></span>

### <span data-ttu-id="3651e-165">Microsoft. Azure. Commands. tüketim. modeller. Psbütçe</span><span class="sxs-lookup"><span data-stu-id="3651e-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="3651e-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3651e-166">NOTES</span></span>

## <span data-ttu-id="3651e-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3651e-167">RELATED LINKS</span></span>
