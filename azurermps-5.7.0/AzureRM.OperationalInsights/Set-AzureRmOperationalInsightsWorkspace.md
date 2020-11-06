---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: a4584e4c0fc64920fbffb7e3d685a9be3ac04ad1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589743"
---
# <span data-ttu-id="bf3d2-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="bf3d2-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="bf3d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf3d2-102">SYNOPSIS</span></span>
<span data-ttu-id="bf3d2-103">Çalışma alanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf3d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf3d2-104">SYNTAX</span></span>

### <span data-ttu-id="bf3d2-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bf3d2-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf3d2-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="bf3d2-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf3d2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf3d2-107">DESCRIPTION</span></span>
<span data-ttu-id="bf3d2-108">**Set-Azurermoperationalınsightsworkspace** cmdlet 'i bir çalışma alanının yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="bf3d2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf3d2-109">EXAMPLES</span></span>

### <span data-ttu-id="bf3d2-110">Örnek 1: çalışma alanını adla değiştirme</span><span class="sxs-lookup"><span data-stu-id="bf3d2-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="bf3d2-111">Bu komut, ContosoResourceGroup adlı kaynak grubundaki MyWorkspace adındaki çalışma alanının SKU ve etiketlerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="bf3d2-112">Örnek 2: ardışık düzeni kullanarak çalışma alanını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="bf3d2-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="bf3d2-113">Bu komut MyWorkSpace adlı çalışma alanını almak için Get-AzureRmOperationalInsightsWorkspace cmdlet 'ini kullanır ve ardından STB 'yi Premium olarak ayarlamak için ardışık düzen işlecini kullanarak bunu **set-Azurermoperationalınsightsworkspace** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="bf3d2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf3d2-114">PARAMETERS</span></span>

### <span data-ttu-id="bf3d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf3d2-115">-DefaultProfile</span></span>
<span data-ttu-id="bf3d2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bf3d2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf3d2-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf3d2-117">-Name</span></span>
<span data-ttu-id="bf3d2-118">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-118">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3d2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf3d2-119">-ResourceGroupName</span></span>
<span data-ttu-id="bf3d2-120">Azure Resource grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-120">Specifies the Azure resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3d2-121">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="bf3d2-121">-RetentionInDays</span></span>
<span data-ttu-id="bf3d2-122">Gün içinde çalışma alanı verileri tutma.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-122">The workspace data retention in days.</span></span> <span data-ttu-id="bf3d2-123">730 gün, diğer tüm STB 'ler için izin verilen maksimum değer</span><span class="sxs-lookup"><span data-stu-id="bf3d2-123">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3d2-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="bf3d2-124">-Sku</span></span>
<span data-ttu-id="bf3d2-125">Çalışma alanının hizmet katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="bf3d2-126">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="bf3d2-126">Valid values are:</span></span> 

- <span data-ttu-id="bf3d2-127">bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="bf3d2-127">free</span></span>
- <span data-ttu-id="bf3d2-128">ardından</span><span class="sxs-lookup"><span data-stu-id="bf3d2-128">standard</span></span>
- <span data-ttu-id="bf3d2-129">Min</span><span class="sxs-lookup"><span data-stu-id="bf3d2-129">premium</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3d2-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="bf3d2-130">-Tag</span></span>
<span data-ttu-id="bf3d2-131">Çalışma alanının kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-131">The resource tags for the workspace.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3d2-132">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="bf3d2-132">-Workspace</span></span>
<span data-ttu-id="bf3d2-133">Güncelleştirilecek çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-133">Specifies the workspace to be updated.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3d2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf3d2-134">CommonParameters</span></span>
<span data-ttu-id="bf3d2-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf3d2-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf3d2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf3d2-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf3d2-137">INPUTS</span></span>

### <span data-ttu-id="bf3d2-138">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bf3d2-138">PSWorkspace</span></span>
<span data-ttu-id="bf3d2-139">Parametre ' çalışma alanı ', ardışık düzenin ' PSWorkspace ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="bf3d2-139">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="bf3d2-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf3d2-140">OUTPUTS</span></span>

### <span data-ttu-id="bf3d2-141">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bf3d2-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="bf3d2-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf3d2-142">NOTES</span></span>

## <span data-ttu-id="bf3d2-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf3d2-143">RELATED LINKS</span></span>

[<span data-ttu-id="bf3d2-144">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="bf3d2-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="bf3d2-145">Get-Azurermoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="bf3d2-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


