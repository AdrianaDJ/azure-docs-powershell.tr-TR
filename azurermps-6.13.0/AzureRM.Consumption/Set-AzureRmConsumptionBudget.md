---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/set-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Set-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Set-AzureRmConsumptionBudget.md
ms.openlocfilehash: f416a6cef4888e51dfabbc9f34b4afad9dbd7370
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593706"
---
# <span data-ttu-id="502b4-101">Set-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="502b4-101">Set-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="502b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="502b4-102">SYNOPSIS</span></span>
<span data-ttu-id="502b4-103">Bir abonelikteki veya bir kaynak grubundaki bütçeyi güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="502b4-103">Update a budget in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="502b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="502b4-104">SYNTAX</span></span>

### <span data-ttu-id="502b4-105">Abonelik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="502b4-105">Subscription (Default)</span></span>
```
Set-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="502b4-106">Bilgilendirme</span><span class="sxs-lookup"><span data-stu-id="502b4-106">Notification</span></span>
```
Set-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="502b4-107">Yöneltil</span><span class="sxs-lookup"><span data-stu-id="502b4-107">Piping</span></span>
```
Set-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget>
 [-Amount <Decimal>] [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="502b4-108">Boru ve bildirim</span><span class="sxs-lookup"><span data-stu-id="502b4-108">Piping and Notification</span></span>
```
Set-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget>
 [-Amount <Decimal>] [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="502b4-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="502b4-109">DESCRIPTION</span></span>
<span data-ttu-id="502b4-110">Set-AzureRmConsumptionBudget cmdlet 'i, bir abonelikte veya kaynak grubunda bir bütçeyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="502b4-110">The Set-AzureRmConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="502b4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="502b4-111">EXAMPLES</span></span>

### <span data-ttu-id="502b4-112">Örnek 1: abonelik düzeyinde bütçe adı içeren bir bütçeyi yeni bir miktara göre güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="502b4-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
```powershell
PS C:\> Set-AzureRmConsumptionBudget -Name PSBudget -Amount 75
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

### <span data-ttu-id="502b4-113">Örnek 2: maliyet veya kullanım, abonelik düzeyindeki tutarın yüzde 90 eşiğine ulaştığında bir bütçeyi bildirim ile güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="502b4-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
```powershell
PS C:\> Set-AzureRmConsumptionBudget -Name PSBudget -NotificationKey notificationKey-ps1234 -NotificationEnabled -NotificationThreshold 90 -ContactEmail johndoe@contoso.com,janesmith@contoso.com -ContactRole Owner,Reader,Contributor
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

### <span data-ttu-id="502b4-114">Örnek 3: kaynak grup düzeyinde bütçe adı içeren bir bütçeyi yeni bir miktara göre güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="502b4-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
```powershell
PS C:\> Set-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -Amount 75
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

## <span data-ttu-id="502b4-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="502b4-115">PARAMETERS</span></span>

### <span data-ttu-id="502b4-116">-Tutar</span><span class="sxs-lookup"><span data-stu-id="502b4-116">-Amount</span></span>
<span data-ttu-id="502b4-117">Bütçe miktarı.</span><span class="sxs-lookup"><span data-stu-id="502b4-117">Amount of a budget.</span></span>

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

### <span data-ttu-id="502b4-118">-Kategori</span><span class="sxs-lookup"><span data-stu-id="502b4-118">-Category</span></span>
<span data-ttu-id="502b4-119">Bütçenin kategorisi maliyet veya kullanım olabilir.</span><span class="sxs-lookup"><span data-stu-id="502b4-119">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="502b4-120">-Posta</span><span class="sxs-lookup"><span data-stu-id="502b4-120">-ContactEmail</span></span>
<span data-ttu-id="502b4-121">Eşik aşıldığında bütçe bildirimini göndermek için e-posta adresleri.</span><span class="sxs-lookup"><span data-stu-id="502b4-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="502b4-122">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="502b4-122">-ContactGroup</span></span>
<span data-ttu-id="502b4-123">Eşik aşıldığında, bütçe bildirimini gönderecek eylem grupları.</span><span class="sxs-lookup"><span data-stu-id="502b4-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="502b4-124">-İlgili kişi</span><span class="sxs-lookup"><span data-stu-id="502b4-124">-ContactRole</span></span>
<span data-ttu-id="502b4-125">Eşik aşıldığında bütçe bildirimini göndermek için ilgili roller.</span><span class="sxs-lookup"><span data-stu-id="502b4-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="502b4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="502b4-126">-DefaultProfile</span></span>
<span data-ttu-id="502b4-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="502b4-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="502b4-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="502b4-128">-EndDate</span></span>
<span data-ttu-id="502b4-129">Bütçenin bitiş tarihi (UTC olarak YYYY-AA-GG).</span><span class="sxs-lookup"><span data-stu-id="502b4-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="502b4-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="502b4-130">-InputObject</span></span>
<span data-ttu-id="502b4-131">Bütçe nesnesi.</span><span class="sxs-lookup"><span data-stu-id="502b4-131">Budget object.</span></span>

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

### <span data-ttu-id="502b4-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="502b4-132">-MeterFilter</span></span>
<span data-ttu-id="502b4-133">Filtrelemek için virgülle ayrılmış metre listesi.</span><span class="sxs-lookup"><span data-stu-id="502b4-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="502b4-134">Kategori kullanım ise gereklidir.</span><span class="sxs-lookup"><span data-stu-id="502b4-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="502b4-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="502b4-135">-Name</span></span>
<span data-ttu-id="502b4-136">Bütçenin adı.</span><span class="sxs-lookup"><span data-stu-id="502b4-136">Name of a budget.</span></span>

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

### <span data-ttu-id="502b4-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="502b4-137">-NotificationEnabled</span></span>
<span data-ttu-id="502b4-138">Bildirim etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="502b4-138">The notification is enabled.</span></span>
<span data-ttu-id="502b4-139">Belirtilmezse, bildirim varsayılan olarak devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="502b4-139">If not specified, the notification is disabled by default.</span></span>

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

### <span data-ttu-id="502b4-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="502b4-140">-NotificationKey</span></span>
<span data-ttu-id="502b4-141">Bir bütçeyle ilişkili bildirimin anahtarı, bildirim etkin anahtar, bildirim eşiği, kişi e-postalarına, kişi gruplarıyla veya kişi rolleriyle bildirim oluşturmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="502b4-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="502b4-142">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="502b4-142">-NotificationThreshold</span></span>
<span data-ttu-id="502b4-143">Bildirimle ilişkilendirilmiş eşik değeri.</span><span class="sxs-lookup"><span data-stu-id="502b4-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="502b4-144">Maliyet veya kullanım eşiği aştığı zaman bildirim gönderilir.</span><span class="sxs-lookup"><span data-stu-id="502b4-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="502b4-145">Her zaman yüzde ve 0 ile 1000 arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="502b4-145">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="502b4-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="502b4-146">-ResourceFilter</span></span>
<span data-ttu-id="502b4-147">Filtre uygulanacak kaynak örneklerinin virgülle ayrılmış listesi.</span><span class="sxs-lookup"><span data-stu-id="502b4-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="502b4-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="502b4-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="502b4-149">Filtre uygulanacak kaynak gruplarının virgülle ayrılmış listesi.</span><span class="sxs-lookup"><span data-stu-id="502b4-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="502b4-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="502b4-150">-ResourceGroupName</span></span>
<span data-ttu-id="502b4-151">Bütçenin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="502b4-151">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="502b4-152">-StartDate</span><span class="sxs-lookup"><span data-stu-id="502b4-152">-StartDate</span></span>
<span data-ttu-id="502b4-153">Bütçenin dönem başlangıç tarihi (UTC olarak).</span><span class="sxs-lookup"><span data-stu-id="502b4-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="502b4-154">Aylık zaman çizgisi için geçerli aydan önce değil.</span><span class="sxs-lookup"><span data-stu-id="502b4-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="502b4-155">Üç aydan önceki üç ay içinde değil.</span><span class="sxs-lookup"><span data-stu-id="502b4-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="502b4-156">Yıllık zaman çizgisi için on iki aydan önce değil.</span><span class="sxs-lookup"><span data-stu-id="502b4-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="502b4-157">Gelecekteki başlangıç tarihi üç aydan uzun olamaz.</span><span class="sxs-lookup"><span data-stu-id="502b4-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="502b4-158">-Zaman çizgisi</span><span class="sxs-lookup"><span data-stu-id="502b4-158">-TimeGrain</span></span>
<span data-ttu-id="502b4-159">Bütçenin zaman çizgisi aylık, üç aylık veya yıllık olabilir.</span><span class="sxs-lookup"><span data-stu-id="502b4-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="502b4-160">-Onay</span><span class="sxs-lookup"><span data-stu-id="502b4-160">-Confirm</span></span>
<span data-ttu-id="502b4-161">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="502b4-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="502b4-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="502b4-162">-WhatIf</span></span>
<span data-ttu-id="502b4-163">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="502b4-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="502b4-164">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="502b4-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="502b4-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="502b4-165">CommonParameters</span></span>
<span data-ttu-id="502b4-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="502b4-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="502b4-167">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="502b4-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="502b4-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="502b4-168">INPUTS</span></span>

### <span data-ttu-id="502b4-169">Microsoft. Azure. Commands. tüketim. modeller. Psbütçe</span><span class="sxs-lookup"><span data-stu-id="502b4-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>
<span data-ttu-id="502b4-170">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="502b4-170">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="502b4-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="502b4-171">OUTPUTS</span></span>

### <span data-ttu-id="502b4-172">Microsoft. Azure. Commands. tüketim. modeller. Psbütçe</span><span class="sxs-lookup"><span data-stu-id="502b4-172">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="502b4-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="502b4-173">NOTES</span></span>

## <span data-ttu-id="502b4-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="502b4-174">RELATED LINKS</span></span>
