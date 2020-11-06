---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 97f8cba0641ed576cb187f3b995d400bc7f521a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591313"
---
# <span data-ttu-id="e2524-101">New-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="e2524-101">New-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="e2524-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2524-102">SYNOPSIS</span></span>
<span data-ttu-id="e2524-103">Çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2524-103">Creates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2524-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2524-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2524-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2524-105">DESCRIPTION</span></span>
<span data-ttu-id="e2524-106">**Yeni-Azurermoperationalınsightsworkspace** cmdlet 'i belirtilen kaynak grubunda ve konumda bir çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2524-106">The **New-AzureRmOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="e2524-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2524-107">EXAMPLES</span></span>

### <span data-ttu-id="e2524-108">Örnek 1: ada göre çalışma alanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="e2524-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="e2524-109">Bu komut, ContosoResourceGroup adlı kaynak grubunda MyWorkspace adlı standart bir SKU çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2524-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="e2524-110">Örnek 2: çalışma alanı oluşturma ve varolan bir hesaba bağlama</span><span class="sxs-lookup"><span data-stu-id="e2524-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzureRmOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="e2524-111">İlk komut, Operational Insights hesap bağlantısı hedeflerini almak için Get-AzureRmOperationalInsightsLinkTargets cmdlet 'ini kullanır ve ardından $OILinkTargets değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e2524-111">The first command uses the Get-AzureRmOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="e2524-112">İkinci komut $OILinkTargets ilk hesap bağlantı hedefini ardışık düzen işlecini kullanarak **Yeni-Azurermoperationalınsightsworkspace** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="e2524-112">The second command passes the first account link target in $OILinkTargets to the **New-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e2524-113">Bu komut, $OILinkTargets 'de ilk Operational Insights hesabına bağlı MyWorkspace adlı standart bir SKU çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2524-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="e2524-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2524-114">PARAMETERS</span></span>

### <span data-ttu-id="e2524-115">-CustomerID</span><span class="sxs-lookup"><span data-stu-id="e2524-115">-CustomerId</span></span>
<span data-ttu-id="e2524-116">Bu çalışma alanının bağlanacağı hesabı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2524-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="e2524-117">Get-AzureRmOperationalInsightsLinkTargets cmdlet 'i, olası hesapları listelemek için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e2524-117">The Get-AzureRmOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

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

### <span data-ttu-id="e2524-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2524-118">-DefaultProfile</span></span>
<span data-ttu-id="e2524-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e2524-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2524-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e2524-120">-Force</span></span>
<span data-ttu-id="e2524-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e2524-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e2524-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="e2524-122">-Location</span></span>
<span data-ttu-id="e2524-123">Çalışma alanının oluşturulacağı konumu (örneğin, Doğu ABD veya Batı Avrupa) belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2524-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="e2524-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="e2524-124">-Name</span></span>
<span data-ttu-id="e2524-125">Çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2524-125">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="e2524-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2524-126">-ResourceGroupName</span></span>
<span data-ttu-id="e2524-127">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2524-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e2524-128">Çalışma alanı bu kaynak grubunda oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e2524-128">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="e2524-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e2524-129">-RetentionInDays</span></span>
<span data-ttu-id="e2524-130">Gün içinde çalışma alanı verileri tutma.</span><span class="sxs-lookup"><span data-stu-id="e2524-130">The workspace data retention in days.</span></span> <span data-ttu-id="e2524-131">730 gün, diğer tüm STB 'ler için izin verilen maksimum değer</span><span class="sxs-lookup"><span data-stu-id="e2524-131">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="e2524-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="e2524-132">-Sku</span></span>
<span data-ttu-id="e2524-133">Çalışma alanının hizmet katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2524-133">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="e2524-134">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="e2524-134">Valid values are:</span></span> 
- <span data-ttu-id="e2524-135">bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="e2524-135">free</span></span>
- <span data-ttu-id="e2524-136">ardından</span><span class="sxs-lookup"><span data-stu-id="e2524-136">standard</span></span>
- <span data-ttu-id="e2524-137">Min</span><span class="sxs-lookup"><span data-stu-id="e2524-137">premium</span></span>

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

### <span data-ttu-id="e2524-138">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e2524-138">-Tag</span></span>
<span data-ttu-id="e2524-139">Çalışma alanının kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="e2524-139">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="e2524-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="e2524-140">-Confirm</span></span>
<span data-ttu-id="e2524-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e2524-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2524-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2524-142">-WhatIf</span></span>
<span data-ttu-id="e2524-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2524-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2524-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e2524-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2524-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2524-145">CommonParameters</span></span>
<span data-ttu-id="e2524-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2524-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2524-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2524-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2524-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2524-148">INPUTS</span></span>

### <span data-ttu-id="e2524-149">System. String</span><span class="sxs-lookup"><span data-stu-id="e2524-149">System.String</span></span>

### <span data-ttu-id="e2524-150">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e2524-150">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e2524-151">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e2524-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e2524-152">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e2524-152">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e2524-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2524-153">OUTPUTS</span></span>

### <span data-ttu-id="e2524-154">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e2524-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="e2524-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2524-155">NOTES</span></span>

## <span data-ttu-id="e2524-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2524-156">RELATED LINKS</span></span>

[<span data-ttu-id="e2524-157">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="e2524-157">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="e2524-158">Get-Azurermoperationalınsightslinktargets</span><span class="sxs-lookup"><span data-stu-id="e2524-158">Get-AzureRmOperationalInsightsLinkTargets</span></span>](./Get-AzureRmOperationalInsightsLinkTargets.md)


