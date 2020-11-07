---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/set-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
ms.openlocfilehash: c159ab71befb52e8131ade0b90e69c4ba8158885
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753133"
---
# <span data-ttu-id="fa063-101">Set-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="fa063-101">Set-AzConsumptionBudget</span></span>

## <span data-ttu-id="fa063-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa063-102">SYNOPSIS</span></span>
<span data-ttu-id="fa063-103">Bir abonelikteki veya bir kaynak grubundaki bütçeyi güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="fa063-103">Update a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="fa063-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa063-104">SYNTAX</span></span>

### <span data-ttu-id="fa063-105">Abonelik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fa063-105">Subscription (Default)</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa063-106">Bilgilendirme</span><span class="sxs-lookup"><span data-stu-id="fa063-106">Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa063-107">Yöneltil</span><span class="sxs-lookup"><span data-stu-id="fa063-107">Piping</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa063-108">Boru ve bildirim</span><span class="sxs-lookup"><span data-stu-id="fa063-108">Piping and Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa063-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa063-109">DESCRIPTION</span></span>
<span data-ttu-id="fa063-110">Set-AzConsumptionBudget cmdlet 'i, bir abonelikte veya kaynak grubunda bir bütçeyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fa063-110">The Set-AzConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="fa063-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa063-111">EXAMPLES</span></span>

### <span data-ttu-id="fa063-112">Örnek 1: abonelik düzeyinde bütçe adı içeren bir bütçeyi yeni bir miktara göre güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="fa063-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="fa063-113">Örnek 2: maliyet veya kullanım, abonelik düzeyindeki tutarın yüzde 90 eşiğine ulaştığında bir bütçeyi bildirim ile güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="fa063-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -NotificationKey notificationKey-ps1234 -NotificationEnabled -NotificationThreshold 90 -ContactEmail johndoe@contoso.com,janesmith@contoso.com -ContactRole Owner,Reader,Contributor
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
Notification:  NotificationKey:  notificationKey-ps1234
               Threshold:  90
               Enabled:  true
               ContactEmail:  johndoe@contoso.com,janesmith@contoso.com
               ContactRole:  Owner,Reader,Contributor
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="fa063-114">Örnek 3: kaynak grup düzeyinde bütçe adı içeren bir bütçeyi yeni bir miktara göre güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="fa063-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="fa063-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa063-115">PARAMETERS</span></span>

### <span data-ttu-id="fa063-116">-Tutar</span><span class="sxs-lookup"><span data-stu-id="fa063-116">-Amount</span></span>
<span data-ttu-id="fa063-117">Bütçe miktarı.</span><span class="sxs-lookup"><span data-stu-id="fa063-117">Amount of a budget.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa063-118">-Kategori</span><span class="sxs-lookup"><span data-stu-id="fa063-118">-Category</span></span>
<span data-ttu-id="fa063-119">Bütçenin kategorisi maliyet veya kullanım olabilir.</span><span class="sxs-lookup"><span data-stu-id="fa063-119">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa063-120">-Posta</span><span class="sxs-lookup"><span data-stu-id="fa063-120">-ContactEmail</span></span>
<span data-ttu-id="fa063-121">Eşik aşıldığında bütçe bildirimini göndermek için e-posta adresleri.</span><span class="sxs-lookup"><span data-stu-id="fa063-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa063-122">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="fa063-122">-ContactGroup</span></span>
<span data-ttu-id="fa063-123">Eşik aşıldığında, bütçe bildirimini gönderecek eylem grupları.</span><span class="sxs-lookup"><span data-stu-id="fa063-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa063-124">-İlgili kişi</span><span class="sxs-lookup"><span data-stu-id="fa063-124">-ContactRole</span></span>
<span data-ttu-id="fa063-125">Eşik aşıldığında bütçe bildirimini göndermek için ilgili roller.</span><span class="sxs-lookup"><span data-stu-id="fa063-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa063-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa063-126">-DefaultProfile</span></span>
<span data-ttu-id="fa063-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fa063-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa063-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="fa063-128">-EndDate</span></span>
<span data-ttu-id="fa063-129">Bütçenin bitiş tarihi (UTC olarak YYYY-AA-GG).</span><span class="sxs-lookup"><span data-stu-id="fa063-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="fa063-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa063-130">-InputObject</span></span>
<span data-ttu-id="fa063-131">Bütçe nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fa063-131">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa063-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="fa063-132">-MeterFilter</span></span>
<span data-ttu-id="fa063-133">Filtrelemek için virgülle ayrılmış metre listesi.</span><span class="sxs-lookup"><span data-stu-id="fa063-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="fa063-134">Kategori kullanım ise gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fa063-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="fa063-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa063-135">-Name</span></span>
<span data-ttu-id="fa063-136">Bütçenin adı.</span><span class="sxs-lookup"><span data-stu-id="fa063-136">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa063-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="fa063-137">-NotificationEnabled</span></span>
<span data-ttu-id="fa063-138">Bildirim etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="fa063-138">The notification is enabled.</span></span>
<span data-ttu-id="fa063-139">Belirtilmezse, bildirim varsayılan olarak devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="fa063-139">If not specified, the notification is disabled by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa063-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="fa063-140">-NotificationKey</span></span>
<span data-ttu-id="fa063-141">Bir bütçeyle ilişkili bildirimin anahtarı, bildirim etkin anahtar, bildirim eşiği, kişi e-postalarına, kişi gruplarıyla veya kişi rolleriyle bildirim oluşturmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fa063-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa063-142">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="fa063-142">-NotificationThreshold</span></span>
<span data-ttu-id="fa063-143">Bildirimle ilişkilendirilmiş eşik değeri.</span><span class="sxs-lookup"><span data-stu-id="fa063-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="fa063-144">Maliyet veya kullanım eşiği aştığı zaman bildirim gönderilir.</span><span class="sxs-lookup"><span data-stu-id="fa063-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="fa063-145">Her zaman yüzde ve 0 ile 1000 arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fa063-145">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa063-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="fa063-146">-ResourceFilter</span></span>
<span data-ttu-id="fa063-147">Filtre uygulanacak kaynak örneklerinin virgülle ayrılmış listesi.</span><span class="sxs-lookup"><span data-stu-id="fa063-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="fa063-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="fa063-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="fa063-149">Filtre uygulanacak kaynak gruplarının virgülle ayrılmış listesi.</span><span class="sxs-lookup"><span data-stu-id="fa063-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="fa063-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa063-150">-ResourceGroupName</span></span>
<span data-ttu-id="fa063-151">Bütçenin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="fa063-151">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa063-152">-StartDate</span><span class="sxs-lookup"><span data-stu-id="fa063-152">-StartDate</span></span>
<span data-ttu-id="fa063-153">Bütçenin dönem başlangıç tarihi (UTC olarak).</span><span class="sxs-lookup"><span data-stu-id="fa063-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="fa063-154">Aylık zaman çizgisi için geçerli aydan önce değil.</span><span class="sxs-lookup"><span data-stu-id="fa063-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="fa063-155">Üç aydan önceki üç ay içinde değil.</span><span class="sxs-lookup"><span data-stu-id="fa063-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="fa063-156">Yıllık zaman çizgisi için on iki aydan önce değil.</span><span class="sxs-lookup"><span data-stu-id="fa063-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="fa063-157">Gelecekteki başlangıç tarihi üç aydan uzun olamaz.</span><span class="sxs-lookup"><span data-stu-id="fa063-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="fa063-158">-Zaman çizgisi</span><span class="sxs-lookup"><span data-stu-id="fa063-158">-TimeGrain</span></span>
<span data-ttu-id="fa063-159">Bütçenin zaman çizgisi aylık, üç aylık veya yıllık olabilir.</span><span class="sxs-lookup"><span data-stu-id="fa063-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa063-160">-Onay</span><span class="sxs-lookup"><span data-stu-id="fa063-160">-Confirm</span></span>
<span data-ttu-id="fa063-161">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fa063-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa063-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa063-162">-WhatIf</span></span>
<span data-ttu-id="fa063-163">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa063-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa063-164">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fa063-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa063-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa063-165">CommonParameters</span></span>
<span data-ttu-id="fa063-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa063-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa063-167">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa063-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa063-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa063-168">INPUTS</span></span>

### <span data-ttu-id="fa063-169">Microsoft. Azure. Commands. tüketim. modeller. Psbütçe</span><span class="sxs-lookup"><span data-stu-id="fa063-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="fa063-170">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa063-170">OUTPUTS</span></span>

### <span data-ttu-id="fa063-171">Microsoft. Azure. Commands. tüketim. modeller. Psbütçe</span><span class="sxs-lookup"><span data-stu-id="fa063-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="fa063-172">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa063-172">NOTES</span></span>

## <span data-ttu-id="fa063-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa063-173">RELATED LINKS</span></span>
