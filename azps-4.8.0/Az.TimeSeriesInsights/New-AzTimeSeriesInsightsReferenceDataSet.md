---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 39bbdf61a5068ea32f1febf66249213264235dfc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268629"
---
# <span data-ttu-id="972b2-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="972b2-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="972b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="972b2-102">SYNOPSIS</span></span>
<span data-ttu-id="972b2-103">Belirtilen ortamda bir başvuru verileri kümesi oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="972b2-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="972b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="972b2-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="972b2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="972b2-105">DESCRIPTION</span></span>
<span data-ttu-id="972b2-106">Belirtilen ortamda bir başvuru verileri kümesi oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="972b2-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="972b2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="972b2-107">EXAMPLES</span></span>

### <span data-ttu-id="972b2-108">Örnek 1: belirli bir ortam için başvuru veri kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="972b2-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="972b2-109">Bu komut, belirli bir ortam için bir başvuru verileri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="972b2-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="972b2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="972b2-110">PARAMETERS</span></span>

### <span data-ttu-id="972b2-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="972b2-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="972b2-112">Başvuru veri kümesi anahtar karşılaştırma davranışı bu özellik kullanılarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="972b2-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="972b2-113">Varsayılan olarak, değer ' sıra ' değeridir; bu, büyük küçük harf duyarlı anahtar karşılaştırması, olaylarla başvuru verilerine katılırken veya yeni başvuru verileri eklenirken gerçekleştirilecektir.</span><span class="sxs-lookup"><span data-stu-id="972b2-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="972b2-114">' OrdinalIgnoreCase ' ayarlandığında büyük/küçük harfe duyarsız karşılaştırma kullanılır.</span><span class="sxs-lookup"><span data-stu-id="972b2-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.DataStringComparisonBehavior
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="972b2-115">-DefaultProfile</span></span>
<span data-ttu-id="972b2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="972b2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972b2-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="972b2-117">-EnvironmentName</span></span>
<span data-ttu-id="972b2-118">Belirtilen kaynak grubuyla ilişkili saat serisi öngörüleri ortamının adı.</span><span class="sxs-lookup"><span data-stu-id="972b2-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="972b2-119">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="972b2-119">-KeyProperty</span></span>
<span data-ttu-id="972b2-120">Başvuru verileri kümesi için anahtar özellikler listesi.</span><span class="sxs-lookup"><span data-stu-id="972b2-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="972b2-121">Oluşturmak için, KEYPROPERTY özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="972b2-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetKeyProperty[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972b2-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="972b2-122">-Location</span></span>
<span data-ttu-id="972b2-123">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="972b2-123">The location of the resource.</span></span>

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

### <span data-ttu-id="972b2-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="972b2-124">-Name</span></span>
<span data-ttu-id="972b2-125">Başvuru veri kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="972b2-125">Name of the reference data set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972b2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="972b2-126">-ResourceGroupName</span></span>
<span data-ttu-id="972b2-127">Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="972b2-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="972b2-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="972b2-128">-SubscriptionId</span></span>
<span data-ttu-id="972b2-129">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="972b2-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972b2-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="972b2-130">-Tag</span></span>
<span data-ttu-id="972b2-131">Kaynak için ek özelliklerin anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="972b2-131">Key-value pairs of additional properties for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972b2-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="972b2-132">-Confirm</span></span>
<span data-ttu-id="972b2-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="972b2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="972b2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="972b2-134">-WhatIf</span></span>
<span data-ttu-id="972b2-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="972b2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="972b2-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="972b2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="972b2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="972b2-137">CommonParameters</span></span>
<span data-ttu-id="972b2-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="972b2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="972b2-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="972b2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="972b2-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="972b2-140">INPUTS</span></span>

## <span data-ttu-id="972b2-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="972b2-141">OUTPUTS</span></span>

### <span data-ttu-id="972b2-142">Microsoft. Azure. PowerShell. cmdlet. zaman</span><span class="sxs-lookup"><span data-stu-id="972b2-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="972b2-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="972b2-143">NOTES</span></span>

<span data-ttu-id="972b2-144">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="972b2-144">ALIASES</span></span>

<span data-ttu-id="972b2-145">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="972b2-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="972b2-146">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="972b2-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="972b2-147">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="972b2-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="972b2-148">KEYPROPERTY <ıreferencedatasetkeyproperty [] >: başvuru veri kümesinin anahtar özelliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="972b2-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="972b2-149">`[Name <String>]`: Anahtar özelliğinin adı.</span><span class="sxs-lookup"><span data-stu-id="972b2-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="972b2-150">`[Type <ReferenceDataKeyPropertyType?>]`: Anahtar özelliğinin türü.</span><span class="sxs-lookup"><span data-stu-id="972b2-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="972b2-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="972b2-151">RELATED LINKS</span></span>

