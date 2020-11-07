---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: e339becd21be14d3587252b88dd8069b266b2408
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938630"
---
# <span data-ttu-id="66340-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="66340-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="66340-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66340-102">SYNOPSIS</span></span>
<span data-ttu-id="66340-103">Çalışma alanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="66340-103">Updates a workspace.</span></span>

## <span data-ttu-id="66340-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66340-104">SYNTAX</span></span>

### <span data-ttu-id="66340-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="66340-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="66340-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="66340-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66340-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="66340-107">DESCRIPTION</span></span>
<span data-ttu-id="66340-108">**Set-Azoperationalınsightsworkspace** cmdlet 'i, çalışma alanının yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="66340-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="66340-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66340-109">EXAMPLES</span></span>

### <span data-ttu-id="66340-110">Örnek 1: çalışma alanını adla değiştirme</span><span class="sxs-lookup"><span data-stu-id="66340-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="66340-111">Bu komut, ContosoResourceGroup adlı kaynak grubundaki MyWorkspace adındaki çalışma alanının SKU ve etiketlerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="66340-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="66340-112">Örnek 2: ardışık düzeni kullanarak çalışma alanını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="66340-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="66340-113">Bu komut MyWorkSpace adlı çalışma alanını almak için Get-AzOperationalInsightsWorkspace cmdlet 'ini kullanır ve ardından STB 'yi Premium olarak ayarlamak için ardışık düzen işlecini kullanarak bunu **set-Azoperationalınsightsworkspace** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="66340-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="66340-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66340-114">PARAMETERS</span></span>

### <span data-ttu-id="66340-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66340-115">-DefaultProfile</span></span>
<span data-ttu-id="66340-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="66340-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66340-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="66340-117">-Name</span></span>
<span data-ttu-id="66340-118">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="66340-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66340-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66340-119">-ResourceGroupName</span></span>
<span data-ttu-id="66340-120">Azure Resource grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="66340-120">Specifies the Azure resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66340-121">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="66340-121">-RetentionInDays</span></span>
<span data-ttu-id="66340-122">Gün içinde çalışma alanı verileri tutma.</span><span class="sxs-lookup"><span data-stu-id="66340-122">The workspace data retention in days.</span></span> <span data-ttu-id="66340-123">730 gün, diğer tüm STB 'ler için izin verilen maksimum değer</span><span class="sxs-lookup"><span data-stu-id="66340-123">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66340-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="66340-124">-Sku</span></span>
<span data-ttu-id="66340-125">Çalışma alanının hizmet katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="66340-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="66340-126">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="66340-126">Valid values are:</span></span> 
- <span data-ttu-id="66340-127">bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="66340-127">free</span></span>
- <span data-ttu-id="66340-128">ardından</span><span class="sxs-lookup"><span data-stu-id="66340-128">standard</span></span>
- <span data-ttu-id="66340-129">Min</span><span class="sxs-lookup"><span data-stu-id="66340-129">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66340-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="66340-130">-Tag</span></span>
<span data-ttu-id="66340-131">Çalışma alanının kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="66340-131">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66340-132">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="66340-132">-Workspace</span></span>
<span data-ttu-id="66340-133">Güncelleştirilecek çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="66340-133">Specifies the workspace to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66340-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66340-134">CommonParameters</span></span>
<span data-ttu-id="66340-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66340-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66340-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66340-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66340-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66340-137">INPUTS</span></span>

### <span data-ttu-id="66340-138">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="66340-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="66340-139">System. String</span><span class="sxs-lookup"><span data-stu-id="66340-139">System.String</span></span>

### <span data-ttu-id="66340-140">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="66340-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="66340-141">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="66340-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="66340-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66340-142">OUTPUTS</span></span>

### <span data-ttu-id="66340-143">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="66340-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="66340-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66340-144">NOTES</span></span>

## <span data-ttu-id="66340-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66340-145">RELATED LINKS</span></span>

[<span data-ttu-id="66340-146">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="66340-146">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="66340-147">Get-Azoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="66340-147">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


