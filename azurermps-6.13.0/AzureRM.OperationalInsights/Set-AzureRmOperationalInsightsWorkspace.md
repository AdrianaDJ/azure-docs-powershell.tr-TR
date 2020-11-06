---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 8c884e69dd13b96925940f467633baf515d88eda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589398"
---
# <span data-ttu-id="8f088-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="8f088-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="8f088-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f088-102">SYNOPSIS</span></span>
<span data-ttu-id="8f088-103">Çalışma alanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8f088-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f088-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f088-104">SYNTAX</span></span>

### <span data-ttu-id="8f088-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8f088-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f088-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="8f088-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f088-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f088-107">DESCRIPTION</span></span>
<span data-ttu-id="8f088-108">**Set-Azurermoperationalınsightsworkspace** cmdlet 'i bir çalışma alanının yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8f088-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="8f088-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f088-109">EXAMPLES</span></span>

### <span data-ttu-id="8f088-110">Örnek 1: çalışma alanını adla değiştirme</span><span class="sxs-lookup"><span data-stu-id="8f088-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="8f088-111">Bu komut, ContosoResourceGroup adlı kaynak grubundaki MyWorkspace adındaki çalışma alanının SKU ve etiketlerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8f088-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="8f088-112">Örnek 2: ardışık düzeni kullanarak çalışma alanını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="8f088-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="8f088-113">Bu komut MyWorkSpace adlı çalışma alanını almak için Get-AzureRmOperationalInsightsWorkspace cmdlet 'ini kullanır ve ardından STB 'yi Premium olarak ayarlamak için ardışık düzen işlecini kullanarak bunu **set-Azurermoperationalınsightsworkspace** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="8f088-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="8f088-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f088-114">PARAMETERS</span></span>

### <span data-ttu-id="8f088-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f088-115">-DefaultProfile</span></span>
<span data-ttu-id="8f088-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8f088-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f088-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="8f088-117">-Name</span></span>
<span data-ttu-id="8f088-118">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f088-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="8f088-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f088-119">-ResourceGroupName</span></span>
<span data-ttu-id="8f088-120">Azure Resource grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f088-120">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="8f088-121">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8f088-121">-RetentionInDays</span></span>
<span data-ttu-id="8f088-122">Gün içinde çalışma alanı verileri tutma.</span><span class="sxs-lookup"><span data-stu-id="8f088-122">The workspace data retention in days.</span></span> <span data-ttu-id="8f088-123">730 gün, diğer tüm STB 'ler için izin verilen maksimum değer</span><span class="sxs-lookup"><span data-stu-id="8f088-123">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="8f088-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="8f088-124">-Sku</span></span>
<span data-ttu-id="8f088-125">Çalışma alanının hizmet katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f088-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="8f088-126">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="8f088-126">Valid values are:</span></span> 
- <span data-ttu-id="8f088-127">bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="8f088-127">free</span></span>
- <span data-ttu-id="8f088-128">ardından</span><span class="sxs-lookup"><span data-stu-id="8f088-128">standard</span></span>
- <span data-ttu-id="8f088-129">Min</span><span class="sxs-lookup"><span data-stu-id="8f088-129">premium</span></span>

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

### <span data-ttu-id="8f088-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="8f088-130">-Tag</span></span>
<span data-ttu-id="8f088-131">Çalışma alanının kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="8f088-131">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="8f088-132">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="8f088-132">-Workspace</span></span>
<span data-ttu-id="8f088-133">Güncelleştirilecek çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f088-133">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="8f088-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f088-134">CommonParameters</span></span>
<span data-ttu-id="8f088-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f088-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f088-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f088-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f088-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f088-137">INPUTS</span></span>

### <span data-ttu-id="8f088-138">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8f088-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="8f088-139">Parametreler: çalışma alanı (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8f088-139">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="8f088-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8f088-140">System.String</span></span>

### <span data-ttu-id="8f088-141">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8f088-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8f088-142">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8f088-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="8f088-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f088-143">OUTPUTS</span></span>

### <span data-ttu-id="8f088-144">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8f088-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="8f088-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f088-145">NOTES</span></span>

## <span data-ttu-id="8f088-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f088-146">RELATED LINKS</span></span>

[<span data-ttu-id="8f088-147">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="8f088-147">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="8f088-148">Get-Azurermoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="8f088-148">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


