---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 22cc5c18e2c3cf21472426160d667c7890f04d4f
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94107295"
---
# <span data-ttu-id="427b8-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="427b8-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="427b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="427b8-102">SYNOPSIS</span></span>
<span data-ttu-id="427b8-103">Çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="427b8-103">Creates a workspace.</span></span>

## <span data-ttu-id="427b8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="427b8-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="427b8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="427b8-105">DESCRIPTION</span></span>
<span data-ttu-id="427b8-106">**New-Azoperationalınsightsworkspace** cmdlet 'i belirtilen kaynak grubunda ve konumda bir çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="427b8-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="427b8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="427b8-107">EXAMPLES</span></span>

### <span data-ttu-id="427b8-108">Örnek 1: ada göre çalışma alanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="427b8-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="427b8-109">Bu komut, ContosoResourceGroup adlı kaynak grubunda MyWorkspace adlı standart bir SKU çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="427b8-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="427b8-110">Örnek 2: çalışma alanı oluşturma ve varolan bir hesaba bağlama</span><span class="sxs-lookup"><span data-stu-id="427b8-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="427b8-111">İlk komut, Operational Insights hesap bağlantısı hedeflerini almak için Get-AzOperationalInsightsLinkTargets cmdlet 'ini kullanır ve ardından $OILinkTargets değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="427b8-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="427b8-112">İkinci komut $OILinkTargets ilk hesap bağlantı hedefini ardışık düzen işlecini kullanarak **Yeni-Azoperationalınsightsworkspace** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="427b8-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="427b8-113">Bu komut, $OILinkTargets 'de ilk Operational Insights hesabına bağlı MyWorkspace adlı standart bir SKU çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="427b8-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="427b8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="427b8-114">PARAMETERS</span></span>

### <span data-ttu-id="427b8-115">-CustomerID</span><span class="sxs-lookup"><span data-stu-id="427b8-115">-CustomerId</span></span>
<span data-ttu-id="427b8-116">Bu çalışma alanının bağlanacağı hesabı belirtir.</span><span class="sxs-lookup"><span data-stu-id="427b8-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="427b8-117">Get-AzOperationalInsightsLinkTargets cmdlet 'i, olası hesapları listelemek için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="427b8-117">The Get-AzOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="427b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="427b8-118">-DefaultProfile</span></span>
<span data-ttu-id="427b8-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="427b8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="427b8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="427b8-120">-Force</span></span>
<span data-ttu-id="427b8-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="427b8-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="427b8-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="427b8-122">-Location</span></span>
<span data-ttu-id="427b8-123">Çalışma alanının oluşturulacağı konumu (örneğin, Doğu ABD veya Batı Avrupa) belirtir.</span><span class="sxs-lookup"><span data-stu-id="427b8-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="427b8-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="427b8-124">-Name</span></span>
<span data-ttu-id="427b8-125">Çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="427b8-125">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="427b8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="427b8-126">-ResourceGroupName</span></span>
<span data-ttu-id="427b8-127">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="427b8-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="427b8-128">Çalışma alanı bu kaynak grubunda oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="427b8-128">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="427b8-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="427b8-129">-RetentionInDays</span></span>
<span data-ttu-id="427b8-130">Gün içinde çalışma alanı verileri tutma.</span><span class="sxs-lookup"><span data-stu-id="427b8-130">The workspace data retention in days.</span></span> <span data-ttu-id="427b8-131">730 gün, diğer tüm STB 'ler için izin verilen maksimum değer</span><span class="sxs-lookup"><span data-stu-id="427b8-131">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="427b8-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="427b8-132">-Sku</span></span>
<span data-ttu-id="427b8-133">Çalışma alanının hizmet katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="427b8-133">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="427b8-134">Hangi değerin kullanılacağı hakkında daha fazla bilgi için lütfen denetleyin https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers .</span><span class="sxs-lookup"><span data-stu-id="427b8-134">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="427b8-135">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="427b8-135">Valid values are:</span></span>
- <span data-ttu-id="427b8-136">bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="427b8-136">free</span></span>
- <span data-ttu-id="427b8-137">pergb2018</span><span class="sxs-lookup"><span data-stu-id="427b8-137">pergb2018</span></span>
- <span data-ttu-id="427b8-138">PerNode</span><span class="sxs-lookup"><span data-stu-id="427b8-138">pernode</span></span>
- <span data-ttu-id="427b8-139">Min</span><span class="sxs-lookup"><span data-stu-id="427b8-139">premium</span></span>
- <span data-ttu-id="427b8-140">tek başına</span><span class="sxs-lookup"><span data-stu-id="427b8-140">standalone</span></span>
- <span data-ttu-id="427b8-141">ardından</span><span class="sxs-lookup"><span data-stu-id="427b8-141">standard</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, pergb2018, pernode, premium, standalone, standard

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="427b8-142">Etiketli</span><span class="sxs-lookup"><span data-stu-id="427b8-142">-Tag</span></span>
<span data-ttu-id="427b8-143">Çalışma alanının kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="427b8-143">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="427b8-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="427b8-144">-Confirm</span></span>
<span data-ttu-id="427b8-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="427b8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="427b8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="427b8-146">-WhatIf</span></span>
<span data-ttu-id="427b8-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="427b8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="427b8-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="427b8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="427b8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="427b8-149">CommonParameters</span></span>
<span data-ttu-id="427b8-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="427b8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="427b8-151">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="427b8-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="427b8-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="427b8-152">INPUTS</span></span>

### <span data-ttu-id="427b8-153">System. String</span><span class="sxs-lookup"><span data-stu-id="427b8-153">System.String</span></span>

### <span data-ttu-id="427b8-154">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="427b8-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="427b8-155">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="427b8-155">System.Collections.Hashtable</span></span>

### <span data-ttu-id="427b8-156">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="427b8-156">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="427b8-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="427b8-157">OUTPUTS</span></span>

### <span data-ttu-id="427b8-158">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="427b8-158">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="427b8-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="427b8-159">NOTES</span></span>

<span data-ttu-id="427b8-160">Yeni bir fiyatlandırma modeli yayımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="427b8-160">A new pricing model has been released.</span></span> <span data-ttu-id="427b8-161">Bir CSP kullanıyorsanız, SKU için "tek başına" yı kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="427b8-161">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="427b8-162">Arka planda, STB pergb2018 olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="427b8-162">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="427b8-163">Daha fazla bilgi için lütfen aşağıdakilere bakın: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="427b8-163">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="427b8-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="427b8-164">RELATED LINKS</span></span>

[<span data-ttu-id="427b8-165">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="427b8-165">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)
