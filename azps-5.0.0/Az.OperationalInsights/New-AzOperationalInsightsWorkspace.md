---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: feac2aa9c5dd92c0d76090c6fc28353d56f9647c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325102"
---
# <span data-ttu-id="1b9f8-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1b9f8-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="1b9f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b9f8-102">SYNOPSIS</span></span>
<span data-ttu-id="1b9f8-103">Çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-103">Creates a workspace.</span></span>

## <span data-ttu-id="1b9f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b9f8-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b9f8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b9f8-105">DESCRIPTION</span></span>
<span data-ttu-id="1b9f8-106">**New-Azoperationalınsightsworkspace** cmdlet 'i belirtilen kaynak grubunda ve konumda bir çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="1b9f8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b9f8-107">EXAMPLES</span></span>

### <span data-ttu-id="1b9f8-108">Örnek 1: ada göre çalışma alanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="1b9f8-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="1b9f8-109">Bu komut, ContosoResourceGroup adlı kaynak grubunda MyWorkspace adlı standart bir SKU çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="1b9f8-110">Örnek 2: çalışma alanı oluşturma ve varolan bir hesaba bağlama</span><span class="sxs-lookup"><span data-stu-id="1b9f8-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="1b9f8-111">İlk komut, Operational Insights hesap bağlantısı hedeflerini almak için Get-AzOperationalInsightsLinkTargets cmdlet 'ini kullanır ve ardından $OILinkTargets değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="1b9f8-112">İkinci komut $OILinkTargets ilk hesap bağlantı hedefini ardışık düzen işlecini kullanarak **Yeni-Azoperationalınsightsworkspace** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1b9f8-113">Bu komut, $OILinkTargets 'de ilk Operational Insights hesabına bağlı MyWorkspace adlı standart bir SKU çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="1b9f8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b9f8-114">PARAMETERS</span></span>

### <span data-ttu-id="1b9f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b9f8-115">-DefaultProfile</span></span>
<span data-ttu-id="1b9f8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1b9f8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b9f8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1b9f8-117">-Force</span></span>
<span data-ttu-id="1b9f8-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1b9f8-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="1b9f8-119">-Location</span></span>
<span data-ttu-id="1b9f8-120">Çalışma alanının oluşturulacağı konumu (örneğin, Doğu ABD veya Batı Avrupa) belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-120">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b9f8-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b9f8-121">-Name</span></span>
<span data-ttu-id="1b9f8-122">Çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-122">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b9f8-123">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="1b9f8-123">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="1b9f8-124">Çalışma alanına erişmek için ağ erişim türü.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-124">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="1b9f8-125">Değer ' Enabled ' veya ' Disabled ' olmalıdır</span><span class="sxs-lookup"><span data-stu-id="1b9f8-125">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b9f8-126">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="1b9f8-126">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="1b9f8-127">Çalışma alanı sorgusuna erişmek için ağ erişim türü.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-127">The network access type for accessing workspace query.</span></span> <span data-ttu-id="1b9f8-128">Değer ' Enabled ' veya ' Disabled ' olmalıdır</span><span class="sxs-lookup"><span data-stu-id="1b9f8-128">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b9f8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b9f8-129">-ResourceGroupName</span></span>
<span data-ttu-id="1b9f8-130">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-130">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1b9f8-131">Çalışma alanı bu kaynak grubunda oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-131">The workspace is created in this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b9f8-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1b9f8-132">-RetentionInDays</span></span>
<span data-ttu-id="1b9f8-133">Gün içinde çalışma alanı verileri tutma.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-133">The workspace data retention in days.</span></span> <span data-ttu-id="1b9f8-134">730 gün, diğer tüm STB 'ler için izin verilen maksimum değer</span><span class="sxs-lookup"><span data-stu-id="1b9f8-134">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b9f8-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="1b9f8-135">-Sku</span></span>
<span data-ttu-id="1b9f8-136">Çalışma alanının hizmet katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-136">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="1b9f8-137">Hangi değerin kullanılacağı hakkında daha fazla bilgi için lütfen denetleyin https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers .</span><span class="sxs-lookup"><span data-stu-id="1b9f8-137">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="1b9f8-138">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="1b9f8-138">Valid values are:</span></span>
- <span data-ttu-id="1b9f8-139">bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="1b9f8-139">free</span></span>
- <span data-ttu-id="1b9f8-140">pergb2018</span><span class="sxs-lookup"><span data-stu-id="1b9f8-140">pergb2018</span></span>
- <span data-ttu-id="1b9f8-141">PerNode</span><span class="sxs-lookup"><span data-stu-id="1b9f8-141">pernode</span></span>
- <span data-ttu-id="1b9f8-142">Min</span><span class="sxs-lookup"><span data-stu-id="1b9f8-142">premium</span></span>
- <span data-ttu-id="1b9f8-143">tek başına</span><span class="sxs-lookup"><span data-stu-id="1b9f8-143">standalone</span></span>
- <span data-ttu-id="1b9f8-144">ardından</span><span class="sxs-lookup"><span data-stu-id="1b9f8-144">standard</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b9f8-145">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1b9f8-145">-Tag</span></span>
<span data-ttu-id="1b9f8-146">Çalışma alanının kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-146">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b9f8-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b9f8-147">-Confirm</span></span>
<span data-ttu-id="1b9f8-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b9f8-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b9f8-149">-WhatIf</span></span>
<span data-ttu-id="1b9f8-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b9f8-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b9f8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b9f8-152">CommonParameters</span></span>
<span data-ttu-id="1b9f8-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b9f8-154">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b9f8-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b9f8-155">INPUTS</span></span>

### <span data-ttu-id="1b9f8-156">System. String</span><span class="sxs-lookup"><span data-stu-id="1b9f8-156">System.String</span></span>

### <span data-ttu-id="1b9f8-157">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="1b9f8-157">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1b9f8-158">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1b9f8-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1b9f8-159">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="1b9f8-159">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1b9f8-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b9f8-160">OUTPUTS</span></span>

### <span data-ttu-id="1b9f8-161">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1b9f8-161">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="1b9f8-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b9f8-162">NOTES</span></span>

<span data-ttu-id="1b9f8-163">Yeni bir fiyatlandırma modeli yayımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-163">A new pricing model has been released.</span></span> <span data-ttu-id="1b9f8-164">Bir CSP kullanıyorsanız, SKU için "tek başına" yı kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-164">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="1b9f8-165">Arka planda, STB pergb2018 olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="1b9f8-165">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="1b9f8-166">Daha fazla bilgi için lütfen aşağıdakilere bakın: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="1b9f8-166">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="1b9f8-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b9f8-167">RELATED LINKS</span></span>

[<span data-ttu-id="1b9f8-168">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="1b9f8-168">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="1b9f8-169">Get-Azoperationalınsightslinktargets</span><span class="sxs-lookup"><span data-stu-id="1b9f8-169">Get-AzOperationalInsightsLinkTargets</span></span>](./Get-AzOperationalInsightsLinkTargets.md)


