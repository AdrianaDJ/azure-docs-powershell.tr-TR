---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: e24597d25fffdc1b516c5a18cf011f7222d288c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587817"
---
# <span data-ttu-id="2b59e-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="2b59e-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="2b59e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b59e-102">SYNOPSIS</span></span>
<span data-ttu-id="2b59e-103">Çalışma alanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2b59e-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b59e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b59e-104">SYNTAX</span></span>

### <span data-ttu-id="2b59e-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2b59e-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tags] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b59e-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="2b59e-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tags] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b59e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b59e-107">DESCRIPTION</span></span>
<span data-ttu-id="2b59e-108">**Set-Azurermoperationalınsightsworkspace** cmdlet 'i bir çalışma alanının yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2b59e-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="2b59e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b59e-109">EXAMPLES</span></span>

### <span data-ttu-id="2b59e-110">Örnek 1: çalışma alanını adla değiştirme</span><span class="sxs-lookup"><span data-stu-id="2b59e-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="2b59e-111">Bu komut, ContosoResourceGroup adlı kaynak grubundaki MyWorkspace adındaki çalışma alanının SKU ve etiketlerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2b59e-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="2b59e-112">Örnek 2: ardışık düzeni kullanarak çalışma alanını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2b59e-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="2b59e-113">Bu komut MyWorkSpace adlı çalışma alanını almak için Get-AzureRmOperationalInsightsWorkspace cmdlet 'ini kullanır ve ardından STB 'yi Premium olarak ayarlamak için ardışık düzen işlecini kullanarak bunu **set-Azurermoperationalınsightsworkspace** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="2b59e-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="2b59e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b59e-114">PARAMETERS</span></span>

### <span data-ttu-id="2b59e-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="2b59e-115">-Name</span></span>
<span data-ttu-id="2b59e-116">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b59e-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="2b59e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b59e-117">-ResourceGroupName</span></span>
<span data-ttu-id="2b59e-118">Azure Resource grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b59e-118">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="2b59e-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="2b59e-119">-Sku</span></span>
<span data-ttu-id="2b59e-120">Çalışma alanının hizmet katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b59e-120">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="2b59e-121">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="2b59e-121">Valid values are:</span></span> 

- <span data-ttu-id="2b59e-122">bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="2b59e-122">free</span></span>
- <span data-ttu-id="2b59e-123">ardından</span><span class="sxs-lookup"><span data-stu-id="2b59e-123">standard</span></span>
- <span data-ttu-id="2b59e-124">Min</span><span class="sxs-lookup"><span data-stu-id="2b59e-124">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: free, standard, premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b59e-125">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="2b59e-125">-Tags</span></span>
<span data-ttu-id="2b59e-126">Çalışma alanının kaynak etiketlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b59e-126">Specifies the resource tags for the workspace.</span></span>

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

### <span data-ttu-id="2b59e-127">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="2b59e-127">-Workspace</span></span>
<span data-ttu-id="2b59e-128">Güncelleştirilecek çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b59e-128">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="2b59e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b59e-129">-DefaultProfile</span></span>
<span data-ttu-id="2b59e-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b59e-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b59e-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="2b59e-131">-RetentionInDays</span></span>
<span data-ttu-id="2b59e-132">Gün içinde çalışma alanı verileri tutma.</span><span class="sxs-lookup"><span data-stu-id="2b59e-132">The workspace data retention in days.</span></span> <span data-ttu-id="2b59e-133">730 gün, diğer tüm STB 'ler için izin verilen en yüksek değer.</span><span class="sxs-lookup"><span data-stu-id="2b59e-133">730 days is the maximum allowed for all other Skus.</span></span>

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

### <span data-ttu-id="2b59e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b59e-134">CommonParameters</span></span>
<span data-ttu-id="2b59e-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b59e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b59e-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b59e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b59e-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b59e-137">INPUTS</span></span>

### <span data-ttu-id="2b59e-138">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2b59e-138">PSWorkspace</span></span>
<span data-ttu-id="2b59e-139">Parametre ' çalışma alanı ', ardışık düzenin ' PSWorkspace ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="2b59e-139">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="2b59e-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b59e-140">OUTPUTS</span></span>

### <span data-ttu-id="2b59e-141">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2b59e-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="2b59e-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b59e-142">NOTES</span></span>

## <span data-ttu-id="2b59e-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b59e-143">RELATED LINKS</span></span>

[<span data-ttu-id="2b59e-144">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="2b59e-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="2b59e-145">Get-Azurermoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="2b59e-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


