---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 5abfd1a02687eb2715ad924510176748e04e56cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324565"
---
# <span data-ttu-id="e54b4-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="e54b4-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="e54b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e54b4-102">SYNOPSIS</span></span>
<span data-ttu-id="e54b4-103">Çalışma alanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e54b4-103">Updates a workspace.</span></span>

## <span data-ttu-id="e54b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e54b4-104">SYNTAX</span></span>

### <span data-ttu-id="e54b4-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e54b4-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

### <span data-ttu-id="e54b4-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="e54b4-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

## <span data-ttu-id="e54b4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e54b4-107">DESCRIPTION</span></span>
<span data-ttu-id="e54b4-108">**Set-Azoperationalınsightsworkspace** cmdlet 'i, çalışma alanının yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e54b4-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="e54b4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e54b4-109">EXAMPLES</span></span>

### <span data-ttu-id="e54b4-110">Örnek 1: çalışma alanını adla değiştirme</span><span class="sxs-lookup"><span data-stu-id="e54b4-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="e54b4-111">Bu komut, ContosoResourceGroup adlı kaynak grubundaki MyWorkspace adındaki çalışma alanının SKU ve etiketlerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e54b4-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="e54b4-112">Örnek 2: ardışık düzeni kullanarak çalışma alanını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e54b4-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="e54b4-113">Bu komut MyWorkSpace adlı çalışma alanını almak için Get-AzOperationalInsightsWorkspace cmdlet 'ini kullanır ve ardından STB 'yi Premium olarak ayarlamak için ardışık düzen işlecini kullanarak bunu **set-Azoperationalınsightsworkspace** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="e54b4-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="e54b4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e54b4-114">PARAMETERS</span></span>

### <span data-ttu-id="e54b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e54b4-115">-DefaultProfile</span></span>
<span data-ttu-id="e54b4-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e54b4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e54b4-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="e54b4-117">-Name</span></span>
<span data-ttu-id="e54b4-118">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e54b4-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="e54b4-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="e54b4-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="e54b4-120">Çalışma alanına erişmek için ağ erişim türü.</span><span class="sxs-lookup"><span data-stu-id="e54b4-120">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="e54b4-121">Değer ' Enabled ' veya ' Disabled ' olmalıdır</span><span class="sxs-lookup"><span data-stu-id="e54b4-121">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="e54b4-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="e54b4-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="e54b4-123">Çalışma alanı sorgusuna erişmek için ağ erişim türü.</span><span class="sxs-lookup"><span data-stu-id="e54b4-123">The network access type for accessing workspace query.</span></span> <span data-ttu-id="e54b4-124">Değer ' Enabled ' veya ' Disabled ' olmalıdır</span><span class="sxs-lookup"><span data-stu-id="e54b4-124">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="e54b4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e54b4-125">-ResourceGroupName</span></span>
<span data-ttu-id="e54b4-126">Azure Resource grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e54b4-126">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="e54b4-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e54b4-127">-RetentionInDays</span></span>
<span data-ttu-id="e54b4-128">Gün içinde çalışma alanı verileri tutma.</span><span class="sxs-lookup"><span data-stu-id="e54b4-128">The workspace data retention in days.</span></span> <span data-ttu-id="e54b4-129">730 gün, diğer tüm STB 'ler için izin verilen maksimum değer</span><span class="sxs-lookup"><span data-stu-id="e54b4-129">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="e54b4-130">-SKU</span><span class="sxs-lookup"><span data-stu-id="e54b4-130">-Sku</span></span>
<span data-ttu-id="e54b4-131">Çalışma alanının hizmet katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e54b4-131">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="e54b4-132">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="e54b4-132">Valid values are:</span></span> 
- <span data-ttu-id="e54b4-133">bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="e54b4-133">free</span></span>
- <span data-ttu-id="e54b4-134">ardından</span><span class="sxs-lookup"><span data-stu-id="e54b4-134">standard</span></span>
- <span data-ttu-id="e54b4-135">Min</span><span class="sxs-lookup"><span data-stu-id="e54b4-135">premium</span></span>
- <span data-ttu-id="e54b4-136">PerNode</span><span class="sxs-lookup"><span data-stu-id="e54b4-136">pernode</span></span>
- <span data-ttu-id="e54b4-137">tek başına</span><span class="sxs-lookup"><span data-stu-id="e54b4-137">standalone</span></span>
- <span data-ttu-id="e54b4-138">pergb2018</span><span class="sxs-lookup"><span data-stu-id="e54b4-138">pergb2018</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone, pergb2018

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e54b4-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e54b4-139">-Tag</span></span>
<span data-ttu-id="e54b4-140">Çalışma alanının kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="e54b4-140">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="e54b4-141">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="e54b4-141">-Workspace</span></span>
<span data-ttu-id="e54b4-142">Güncelleştirilecek çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e54b4-142">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="e54b4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e54b4-143">CommonParameters</span></span>
<span data-ttu-id="e54b4-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e54b4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e54b4-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e54b4-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e54b4-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e54b4-146">INPUTS</span></span>

### <span data-ttu-id="e54b4-147">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e54b4-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="e54b4-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e54b4-148">System.String</span></span>

### <span data-ttu-id="e54b4-149">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e54b4-149">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e54b4-150">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="e54b4-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e54b4-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e54b4-151">OUTPUTS</span></span>

### <span data-ttu-id="e54b4-152">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e54b4-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="e54b4-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e54b4-153">NOTES</span></span>

## <span data-ttu-id="e54b4-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e54b4-154">RELATED LINKS</span></span>

[<span data-ttu-id="e54b4-155">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="e54b4-155">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="e54b4-156">Get-Azoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="e54b4-156">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


